# FREE_FRAMEWORK_FIRST_SCENARIOS — бесплатные системы как основа будущей игры

**Создано 2026-10-08. Все сочетания — `ASSUMED`; это инженерные гипотезы, а не проверенные сборки Unity Editor.** Цена обязательных компонентов 0 ₽ по выбранным upstream лицензиям; перед импортом проверять все зависимости и third-party art.

## RTS-2026: цельный игровой проект вместо переписывания RTS
**Базис:** [OpenEmpires](../Tool_Catalog/open-empires-rts.md) — MIT, Unity 6, управление армиями, бои, ресурсы, строительство, мультиплеер. Не добавлять одновременно Mirror/FishNet, поскольку OpenEmpires использует собственный deterministic lockstep и Rust relay.

**Установка:** открыть Unity project в отдельном каталоге, выбрать exact ProjectVersion **6000.5.9f1** (README 6000.3.9f1 устарел относительно конфигурации); собрать одиночную/локальную сцену. Для сетевого теста локально бесплатные Rust и PostgreSQL, при этом никаких платных VPS.

**Задачи теста:** проверить лицензии арт-ассетов, запуск Unity scene, экономику, prefab бойцов, сохранение карты, проигрыш/победу, локальную сеть. **Готовность:** нельзя давать статус VERIFIED, пока build/PlayMode не подтверждены на машине.

## RPG-TURN: готовое RPG-ядро + визуальное представление
**Базис:** [Moonforge Core](../Tool_Catalog/moonforge-rpg-engine.md) v1.2.0 (MIT). Он уже содержит combat, loot, quests, party, inventory, shop/economy и save/load. Unity только отображает игровые объекты и управление через тонкие адаптеры; не переписывать domain rules на MonoBehaviour.

**Опциональный нарратив:** [Ink 2.0](../Tool_Catalog/ink-unity-integration.md) (MIT) **только** если собственного dialogue Moonforge недостаточно. Возможна дубляция событий и состояния диалога, поэтому назначить Moonforge хозяином quest/inventory, Ink — сценарным UI и choices. Это `ASSUMED`, прямой мост требует кодирования/тестов.

**Бесплатные модели:** Kenney, Quaternius Standard, Poly Haven CC0 по нужному стилю. Никаких paid Source/All-in-1.

**Установка:** чистая Unity 6.3 сцена → Moonforge embedded UPM из upstream `unity-packages/com.moonforge.core` → один предмет/квест/диалог → тест повторного сохранения → только затем опциональный Ink.

**Готовность:** EditMode tests для deterministic quest/combat, PlayMode/UI, Player Build и нет двойного хранения состояния.

## RPG-DATA: готовый data-driven RPG + встроенный Unity playground
**Базис:** [Game Lattice](../Tool_Catalog/game-lattice-rpg.md) (Apache-2.0) **и его официальный Unity 6 Playground** [карточка](../Tool_Catalog/game-lattice-unity-playground.md). В демонстрации уже есть связь JSON RPG engine / quest / dialogue и Yarn, 9 уроков.

**Установка:** начать не с пустой сцены, а с **готового Unity 6000.4.11f1 playground**, открыть и пройти уроки без дополнительных сервисов. Нельзя предполагать, что в 6000.3 всё автоматически заработает. Проверить DLL конфликт Microsoft.CSharp CS1703 — README предупреждает об этом и отмечает обход в bundled package.

**AI-автоматизация:** агент может создавать JSON defs по [официальному guide](https://github.com/Toxic-Cookie/game-lattice/blob/main/docs/llm-guide.md) и проверять quest-лог без платного API.

**Готовность:** игра запускается, 9 уроков выполняются, JSON hot reload применим, сохранение state проходит тест.

## DUNGEON-3D: процедурный 3D labyrinth + управляемый FPS персонаж
**Базис:** [EZ Room Generator](../Tool_Catalog/ezroomgenerator.md) v0.1.0 + [Simple FPS Controller](../Tool_Catalog/simple-fps-controller-unity6-mit.md) (оба MIT), либо встроенный Unity CharacterController.

**Зависимости:** FBX Exporter `com.unity.formats.fbx` 5.1.5 в package.json генератора; надо проверить наличие бесплатной конкретной версии. FPS-контроллер использует **classic Input Manager**; если выбран новый Unity Input System, требуется адаптер, не считать автоматически совместимым.

**Установка:** пустой Unity 6 URP → UPM generator + demo generation → mesh/colliders → FPS camera/CharacterController → проверить перемещение, коллизии, застревания, освещение, runtime generation, build.

**Готовность:** из редактора генерируются комнаты и лабиринты без ошибок, персонаж достигает выхода; Blender FBX export — лишь опция.

## DUNGEON-2D: roguelike / сюжетное приключение
**Базис:** [Edgar Free Core](../Tool_Catalog/edgar-unity-free.md) (MIT) → генерируемый Tilemap из шаблонов комнат + [Kenney](../Tool_Catalog/kenney-new-platformer-pack.md) CC0.
**Для повествования:** отдельный [Ink](../Tool_Catalog/ink-unity-integration.md) или [Yarn](../Tool_Catalog/yarn-spinner-unity.md) (MIT), **не оба одновременно**.
**Запрещено:** Edgar PRO generator/platformer/isometric и другие платные additions.

**Установка:** Tilemap scene → Edgar git UPM `#upm` → два room templates, graph spawn→reward→exit → Kenney free sprites → для диалогов один narrative UPM → save state ownership тест.

**Готовность:** одинаковый seed reproducibly приводит к solvable generated level (если генератор гарантирует конкретное свойство — уточнить документацию), игровой персонаж может пройти коридоры без лишних collisions, опциональные диалоги запускаются.

## Матрица конфликтов и владельцев данных
| Игровая ответственность | Рекомендуемый главный владелец | Не ставить слепо поверх |
|---|---|---|
| RTS simulation/network | OpenEmpires | Mirror / FishNet / second network manager |
| RPG quests, stats, inventory | Moonforge **или** Game Lattice | Второе RPG-ядро и дублирующий inventory/save |
| Dialogue graph | Ink **или** Yarn | Второй dialogue engine, конфликт parser/saves |
| Input mapping | Unity Input System **или** классический Input Manager | Два независимых input pipelines в одном player |
| 3D dungeon generation | EZ Room | Edgar 2D (другое измерение и форматы данных) |
| 2D roguelike level graph | Edgar Free | Платные platformer/isometric PRO-only workflows |

**После проверки** перенести version, change log, Console logs и build artifacts **в инструкции GitHub**. Не загружать большие исходники или чужие игровые ассеты.
