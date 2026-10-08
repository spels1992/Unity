# 06. C#, архитектура кода и устойчивость игровых систем

**Дата:** 2026-10-08 · **Статус:** базовое инженерное исследование; примеры требуют компиляции и EditMode-тестов в Editor.

## Принцип: отдельно правила, отдельно Unity-обвязка
- **Доменная логика:** правила урона, очков, инвентаря, победы; обычные C# классы без наследования MonoBehaviour, когда это возможно.
- **Адаптер Unity:** считывает ввод, связывает сцену/компоненты с моделью, обновляет визуал.
- **Данные конфигурации:** ScriptableObject/JSON/управляемые asset data.
- **Инфраструктура:** сохранения, настройки, загрузка, аудио, телеметрия, сеть — через ограниченные интерфейсы и явные зависимости.

Так отделённую логику проще тестировать без сцены, многократно использовать и безопаснее менять. **Не нужно** вводить десятки интерфейсов ради 100 строк прототипа.

## Минимальный пример: правило здоровья как чистый C#
```csharp
using System;

public sealed class Health
{
    public int Maximum { get; }
    public int Current { get; private set; }
    public bool IsDead => Current == 0;
    public event Action Died;

    public Health(int maximum)
    {
        if (maximum < 1) throw new ArgumentOutOfRangeException(nameof(maximum));
        Maximum = maximum;
        Current = maximum;
    }

    public void Damage(int amount)
    {
        if (amount <= 0 || IsDead) return;
        Current = Math.Max(0, Current - amount);
        if (Current == 0) Died?.Invoke();
    }
}
```
Логика не зависит от Unity: можно тестировать `Health` в обычных unit tests. Событие смерти должно сработать не более одного раза при последовательном уроне после нуля. В Unity-приложении компонент-владелец подписывается на событие и **отписывается при уничтожении/повторном присоединении**, иначе возникает риск удержания ссылок.

## Три уровня асинхронности
| Механизм | Когда использовать | Основной риск |
|---|---|---|
| `Update` / `FixedUpdate` | Логика каждого кадра/физики | Связь поведения с FPS |
| Coroutines (`IEnumerator`) | Последовательности кадров/ожиданий | Неправильное завершение и lifetime |
| Unity `Awaitable` / `async-await` | Асинхронные операции и загрузки | Некорректный main-thread контекст, cancellation, повторное ожидание |
| C# Job System / Burst | Вычислительно тяжёлые независимые задачи | Нельзя использовать большинство Unity API из worker threads |

Официальная документация подчёркивает: большая часть `UnityEngine` и `UnityEditor` требует **главного потока**, поэтому запрещено изменять GameObject/Transform на фоне «как обычный .NET объект». Не блокировать главный поток через `Task.Result` или `Task.Wait`. Ориентиры: [Unity programming best practices](https://docs.unity.com/en-us/engine/6000.3/manual/scripting/get-started/programming-best-practices), [Awaitable](https://docs.unity.com/en-us/engine/6000.3/manual/scripting/programming-distribute-work-threads/async-await-support), [Distribute work](https://docs.unity.com/en-us/engine/6000.3/manual/scripting/programming-distribute-work-threads).

## Assembly Definitions (`.asmdef`)
Unity обычно компилирует множество собственных скриптов в `Assembly-CSharp.dll`. Можно отделить `Game.Core`, `Game.Gameplay`, `Game.UI`, `Game.Editor`, `Game.Tests`. Описывать ссылки снаружи внутрь (например Gameplay зависит от Core, но Core не зависит от UI).

```text
Game.UI ──────► Game.Gameplay ─────► Game.Core
    │                                   ▲
    └───────────────────────────────────┘
Game.Tests ────────────────────────► Core / Gameplay
```

**Важно:** `.asmdef` имеет явные ссылки, различает runtime/editor платформы, и использование GUID для references устойчивее к переименованию assembly. Не создавать круговые зависимости. Источники: [Organize assemblies](https://docs.unity.com/en-us/engine/6000.0/manual/programming-environment/script-compilation/assembly-definition-files), [Assembly Definition file format](https://docs.unity.com/en-us/engine/6000.3/manual/programming-environment/script-compilation/assembly-definition-files/file-format), [Assembly Inspector](https://docs.unity.com/en-us/engine/6000.3/manual/programming-environment/script-compilation/assembly-definition-files/class-assembly-definition-importer).

## Первое тестовое задание
Написать EditMode unit test: при `Health(3)` после `Damage(1)`, `Damage(2)`, `Damage(5)` Current = 0, событие Died = 1. Добавить тест на `Health(0)` (ожидаем exception). Затем протестировать сборку и PlayMode сцены с Unity-компонентом, который показывает здоровье через UI.

## Ошибки, которых избежать
- Каждая система ходит по всей сцене через `FindObjectOfType`/`FindObjectsByType` на каждом кадре.
- Жёсткие ссылки `UI→Enemy→Menu→UI` превращают исправление одной функции в каскад багов.
- Всё вычислять в `Update`, даже когда событие редкое.
- Игнорировать память/GC и производительность на целевом устройстве.
- Утверждать, что узконаправленный паттерн «обязателен для всех игр».

## Дальнейшие темы
Unity Test Framework, NUnit, event bus, DI/Zenject/Extenject/VContainer (проверка лицензий), state machines, pooling, object lifetime, частоты физики, инкапсуляция, ScriptableObject data, serialization migrations, Jobs/Burst, hot reload и профайлинг.
