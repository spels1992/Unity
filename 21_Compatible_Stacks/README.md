# Compatible Stacks

**Исследование:** начальный индекс от 2026-10-08. **Задачи:** Genre-specific verified/assumed bundles and conflicts; separate tested projects.

Искать **от крупного готового решения к маленькому компоненту**. Для каждого кандидата создавать карточку в [Tool_Catalog](../Tool_Catalog/INDEX.md), затем ссылаться сюда; не создавать дубликаты. Проверять лицензию, актуальность версий Unity, исходники и возможность интеграции с другими системами.

## Приоритетные вопросы
- Есть ли полноценный проект или поддерживаемый framework, выполняющий несколько задач сразу?
- Есть ли бесплатная официальная система Unity? Если нет — какой OSS вариант?
- Какие зависимости/версии, render pipeline и target platform обязательны?
- Может ли агент автоматизировать установку/проверку через Unity Editor API или CI?
- Какие альтернативы и известные риски, что тестировать перед производством?

**Статус:** каталог направления ещё не заполнен полностью; см. [ROADMAP](../ROADMAP.md).
## Готовые бесплатные сочетания
[FREE_STACKS.md](FREE_STACKS.md): 2D платформер, 3D-RPG exploration, Sci-fi FPS/exploration, Boat Racing reference. Все ASSUMED, без заявлений о практической проверке.


## Новые framework-first варианты (план тестирования)
- [OpenEmpires](../Tool_Catalog/open-empires-rts.md) использовать как **цельный RTS**. Rust/PostgreSQL бесплатно локально; не нужна дополнительная Mirror/FishNet network core.
- [Moonforge](../Tool_Catalog/moonforge-rpg-engine.md) или [Game Lattice](../Tool_Catalog/game-lattice-rpg.md) — выбирать **один** авторитетный RPG core, не два.
- [Yarn Spinner Git](../Tool_Catalog/yarn-spinner-unity.md) ИЛИ [Ink](../Tool_Catalog/ink-unity-integration.md) — выбирать одно решение для dialog, если RPG framework не предоставляет достаточное.
- [Unity Modular Inventory](../Tool_Catalog/unity-modular-inventory.md) добавлять отдельно лишь при отсутствии встроенного инвентаря.
- [EZ Room](../Tool_Catalog/ezroomgenerator.md) для 3D, [Edgar Free](../Tool_Catalog/edgar-unity-free.md) для 2D, в разных игровых стэках.

[Полное сравнение систем](../Comparisons/FREE_FRAMEWORKS_2026.md). **Совместимость предположительная**.
