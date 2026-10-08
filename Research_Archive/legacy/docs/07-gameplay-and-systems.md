# 07. Игровой процесс: механики, циклы и состояние

**Первая редакция:** 2026-10-08 · **Статус:** метод и воспроизводимый план реализации. Этап тестирования в Unity не проводился.

## От идеи к исполнимой системе
Любую механику описываем через `ввод → правило → изменение состояния → обратная связь → повтор`.

Пример 2D игры со стрельбой в пугало:
```text
Игрок удерживает управление → выбирает угол и силу → отпускает
  ↓
Лук отправляет снаряд с начальной скоростью
  ↓
Physics2D просчитывает полёт и взаимодействие с окружением
  ↓
Hit: пугало получает урон → очки/уровень; Miss: расходуется стрела
  ↓
Показ результата → продолжение или рестарт
```

**Сначала:** одна сцена, неподвижная мишень, одна физически движущаяся стрела, кнопка рестарта. **Потом:** препятствия, тайминг, звук, прогрессия, новые цели и уровни. Перед каждым усложнением проводить playtest.

## State machine вместо случайного набора bool-полей

```text
Boot → Menu → Playing → Paused → Playing
                       ↓
                    Victory / Defeat → Results → Menu / Replay
```

Пример чистой модели (не MonoBehaviour):
```csharp
public enum RunState { Menu, Playing, Paused, Results }

public sealed class RunStateMachine
{
    public RunState State { get; private set; } = RunState.Menu;

    public bool StartGame()
    {
        if (State != RunState.Menu && State != RunState.Results) return false;
        State = RunState.Playing;
        return true;
    }

    public bool Pause()
    {
        if (State != RunState.Playing) return false;
        State = RunState.Paused;
        return true;
    }

    public bool Resume()
    {
        if (State != RunState.Paused) return false;
        State = RunState.Playing;
        return true;
    }

    public void Finish() => State = RunState.Results;
}
```

Это **пример направления архитектуры**, а не окончательный manager для всех игр. В полноценной модели стоит заменить прямой доступ на операции/события и определить, разрешено ли завершать игру во время паузы.

## Схема систем с минимальной связностью
```text
Input Adapter → Player Controller → Shot Service → Projectile/Physics
                                    ↓
                            Target Health → Score/Level Rules
                                    ↓
                              RunStateMachine
                                    ↓
                             UI/Audio Feedback
```

- Input только сообщает о действии, не меняет напрямую Score/Level/UI.
- Projectile сообщает об обнаруженном попадании, не открывает меню победы.
- Score/Level решает, пройден ли уровень, без привязки к конкретному текстовому объекту на экране.
- UI обновляется после событий, не опрашивает каждый объект через Find* в Update.

## Требования к игровому балансу
| Система | Настройка | Измеримый критерий |
|---|---|---|
| Выстрел | угол, сила, число стрел | доля успешных попаданий |
| Пугало | размер хитбокса, положение | очевидность успешного попадания |
| Уровень | дистанция, препятствия, ветер (если есть) | попытки до прохождения |
| Обучение | визуальная подсказка управления | игрок смог сделать первый выстрел |
| Награда | очки, анимация, звук | игрок понял результат |

Не пытаться «сделать баланс объективно идеальным» без тестов на игроках. Дизайнерские параметры хранить в `ScriptableObject` или конфигурации по уровням после проверки правил сериализации.

## Time и физика
`Time.deltaTime` — интервал между кадрами, масштабированный временем игры; не путать со временем реального мира. При паузе `timeScale=0` интерфейсные таймеры могут требовать `Time.unscaledDeltaTime`. Физические действия обновлять согласованно с физическим шагом и выбором Rigidbody2D, а не напрямую перемещать Rigidbody `transform.position` в каждом кадре без понимания коллизий.
Документация: [Time.deltaTime](https://docs.unity.com/en-us/engine/6000.3/script-reference/unityengine/time/deltatime), [Unity 2D Physics](https://docs.unity.com/en-us/engine/6000.0/manual/unity2d/2d-physics).

## Дизайнерские проверки
1. При рестарте всё состояние (очки, патроны/стрелы, скорость, здоровье) возвращается к начальным значениям.
2. При двух пересекающихся коллайдерах мишень не получает урон дважды от одного попадания.
3. При паузе прекращается движение снаряда, но UI остаётся отзывчивым.
4. Прогрессия не требует знания Unity Editor у игрока.
5. Разные FPS не меняют существенно дальность выстрела и результат столкновений.
6. Механика воспроизводима в собранной игре без редактора.

## Источники и ближайшие задачи
- [Unity Learn — Prototyping](https://learn.unity.com/course/design-and-publish-your-original-game-unity-usc-games-unlocked/unit/prototyping) — проверка интересности.
- [Unity Learn — Set up your project](https://learn.unity.com/tutorial/66f53a14edbc2a0e75d4fe90) — от идеи к vertical slice.
- [Time.deltaTime](https://docs.unity.com/en-us/engine/6000.3/script-reference/unityengine/time/deltatime) — время.
- [2D Physics](https://docs.unity.com/en-us/engine/6000.0/manual/unity2d/2d-physics) — физические компоненты.
- **Осталось:** проект сохранения прогресса, конкретная реализация физического выстрела, статистика плейтестов, DI и UI bindings, инструментальный тест, game feel и аудио.
