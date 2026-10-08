# 05. Архитектура Unity: объекты, компоненты и сцены

**Первый проход:** 2026-10-08 · **Рабочая версия для примеров:** Unity 6.3 LTS (API нужно проверить в установленном Editor). **Выполнение на компьютере:** пока не тестировалось.

## Ментальная модель движка
```text
Project
  ├── Assets/Scenes/Main.unity
  │     ├── Player (GameObject)
  │     │     ├── Transform
  │     │     ├── SpriteRenderer
  │     │     ├── Rigidbody2D
  │     │     ├── Collider2D
  │     │     └── PlayerMovement : MonoBehaviour
  │     └── Camera
  ├── Assets/Prefabs/Target.prefab
  ├── Assets/Data/GameSettings.asset (ScriptableObject)
  └── Packages/manifest.json
```

**GameObject** — объект-контейнер. **Transform** — позиция/вращение/масштаб. **Component** определяет возможности; один объект может содержать несколько компонентов. **MonoBehaviour** — пользовательский компонент, который подключается к системам жизненного цикла Unity. **Scene** — сохраняемая композиция объектов. **Prefab** — сохранённая композиция компонентов/детей для многократного создания. **ScriptableObject** — данные-ассеты, полезные для настроек, но не автоматически пользовательские сохранения.

## Порядок событий жизненного цикла
- `Awake` — ранняя инициализация компонента/ссылок; `OnEnable` — реагировать на включение.
- `Start` — инициализация перед первым Update, если компонент включён.
- `Update` — каждый кадр; **не привязывать скорость перемещения к числу кадров**.
- `FixedUpdate` — цикл физики; применять для физических действий при соответствующей физической архитектуре.
- `LateUpdate` — часто используется для следящих камер после обновлений геймплея.
- `OnDisable`/`OnDestroy` — отписка от событий/очистка ресурсов.

Нюанс: **относительный порядок одинаковых вызовов на разных объектах не гарантируется** в общем случае. Поэтому не строить архитектуру, где `Enemy.Update` должен всегда произойти до `Player.Update`. Источник: [Event function execution order](https://docs.unity.com/en-us/engine/6000.3/manual/scripting/managing-update-order/execution-order).

## Практика 1: безопасная настройка компонента
1. Создать объект `Target` со SpriteRenderer/Collider2D.
2. Добавить простой скрипт `TargetHealth.cs`.
3. Показать поле `maxHealth` в Inspector через `[SerializeField]`.
4. Сделать Prefab перетаскиванием объекта из Hierarchy в папку Assets/Prefabs.
5. Создать два экземпляра в сцене, изменить maxHealth одного instance; посмотреть Inspector Overrides.
6. Изменить основной Prefab и убедиться, какие параметры наследуются, а какие остались overrides.

```csharp
using UnityEngine;

public sealed class TargetHealth : MonoBehaviour
{
    [SerializeField, Min(1)] private int maxHealth = 3;
    private int currentHealth;

    private void Awake()
    {
        currentHealth = maxHealth;
    }

    public void ApplyDamage(int amount)
    {
        if (amount <= 0 || currentHealth <= 0) return;
        currentHealth = Mathf.Max(0, currentHealth - amount);
        if (currentHealth == 0) Debug.Log("Target destroyed", this);
    }
}
```
Пример иллюстрирует модель компонента и сериализации. **Не является протестированным игровым пакетом.** На реальной игре следует добавить событие смерти и тесты, а не привязывать логику победы к Debug.Log.

## Префабы: полезно знать
Префаб хранит GameObject с компонентами/значениями и детьми, а инстансы наследуют его, кроме overrides. Существуют nested Prefabs и Prefab Variants. Не нажимать Apply/Overrides без проверки влияния на все экземпляры. Официальные материалы: [Prefabs](https://docs.unity.com/en-us/engine/6000.0/manual/working-with-gameobjects/prefabs), [Create prefabs](https://docs.unity.com/en-us/engine/6000.0/manual/working-with-gameobjects/prefabs/creating), [Override prefab instance data](https://docs.unity.com/en-us/engine/6000.3/manual/working-with-gameobjects/prefabs/override).

## Сериализация: ловушки
Unity имеет собственные правила сериализации, не идентичные обычному JSON/.NET serializer; данные должны соответствовать правилам для типов и полей. При reload изменённого кода Editor сериализует и восстанавливает часть состояния объектов. Отдельно разбирать `[Serializable]`, `[SerializeField]`, `[SerializeReference]`, свойства/поля, словари, циклические ссылки и asset GUID. Вопреки распространённой ошибке, `static` поля не становятся обычными сохраняемыми полями Inspector.
Источники: [Unity serialization rules](https://docs.unity.com/en-us/engine/6000.3/manual/programming-environment/code-reload-serialization/script-serialization/rules), [Code reload](https://docs.unity.com/en-us/engine/6000.3/manual/programming-environment/code-reload-serialization).

## Минимальный тест
- `Awake` устанавливает `currentHealth=maxHealth`, без нулевого здоровья при запуске.
- После 2 урона при `maxHealth=3` текущее значение 1.
- Отрицательный урон не лечит цель.
- Повторный урон после 0 не создаёт дополнительных событий.
- PlayMode/Build ведут себя одинаково.
- Смена значения на одном prefab instance не переписывает все Prefabs.

## Расширения для будущих глав
ScriptableObject architecture; dependency injection; scene loading/additive; Addressables; событие OnDeath без «бог-объекта»; event subscriptions; destroy/lifetime; prefab variants; scene/bootstrap patterns; memory leaks.
