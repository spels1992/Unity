# Матрица жанров и игровых технологий

**Дата первого прохода: 2026-10-08.** Перечень жанров предназначен для покрытия поисковыми запросами; **это не утверждение, что для каждого уже найдены готовые инструменты**. Одна система описывается только в одной канонической карточке Tool_Catalog.

| Семейство | Жанры для поэтапного исследования | Типовые подсистемы | Куда идти |
|---|---|---|---|
| **Экшен** | FPS, TPS, Hack and Slash, Beat 'em up, Character Action, Stealth, Arena Combat, Extraction Shooter, Immersive Sim | character controller, camera, weapons/combat, AI, animation, hit detection, UI | [Индекс инструментов](../Tool_Catalog/INDEX.md) |
| **RPG** | RPG, Action RPG, JRPG, MMORPG, Dungeon Crawler, Roguelike, Roguelite, Soulslike, Tactical RPG, Creature Collector | inventory, stats, abilities, quests/dialogues, combat, save, AI | [Индекс инструментов](../Tool_Catalog/INDEX.md) |
| **Стратегии** | RTS, Пошаговая стратегия, 4X, Tower Defense, Тактическая стратегия, Auto Battler, Grand Strategy, Wargame | selection/order system, pathfinding, unit AI, production/economy, camera, UI | [Индекс инструментов](../Tool_Catalog/INDEX.md) |
| **Симуляторы** | Вождение, Авиационный, Железнодорожный, Фермерский, Строительный, Экономический, Симулятор жизни, Физический симулятор, Vehicle Combat | physics/model fidelity, input devices, camera, simulation clock, analytics, data | [Индекс инструментов](../Tool_Catalog/INDEX.md) |
| **Гонки** | Аркадные, Реалистичные, Картинг, Гонки на разных видах транспорта, Rally, Time Trial | vehicle physics, track tools, AI racing line, camera, lap timing, audio | [Индекс инструментов](../Tool_Catalog/INDEX.md) |
| **Приключения** | Adventure, Action Adventure, Survival, Survival Horror, Open World, Exploration, Narrative Adventure, Walking Simulator | world interactions, inventory, save, story, traversal, streaming | [Индекс инструментов](../Tool_Catalog/INDEX.md) |
| **Платформеры** | 2D, 2.5D, 3D, Precision Platformer, Metroidvania, Endless Runner | movement controller, collision, checkpoint, camera, 2D/3D animations | [Индекс инструментов](../Tool_Catalog/INDEX.md) |
| **Головоломки** | Физические, Логические, Пространственные, Puzzle Platformer, Match-3, Escape Room, Hidden Object | logic/rules, level editor, undo/reset, hints, progress saving | [Индекс инструментов](../Tool_Catalog/INDEX.md) |
| **Строительство/менеджмент** | City Builder, Colony Sim, Factory Automation, Management, Sandbox, Tycoon, Automation Puzzle | grid/build mode, UI, pathfinding, economy, simulation ticks, save | [Индекс инструментов](../Tool_Catalog/INDEX.md) |
| **Другие** | Fighting, Спорт, Ритм, Карточные, Настольные, Visual Novel, Idle/Incremental, Casual, Hypercasual, Mobile, Co-op, Social, VR/AR, Образовательные, Гибридные, Music Game, Party Game | genre-specific controls + common UI/audio/localization/save/build QA | [Индекс инструментов](../Tool_Catalog/INDEX.md) |

## Как заполнять карточку жанра
Для каждого из 87 названий необходимо определить: **core loop, уникальные и общие механики, полный фреймворк/starter kits, бесплатные контроллеры, анимацию, физику, AI, UI, мир/уровни, OSS игры, сочетаемые библиотеки, стоимость и лицензию, live-тест**. Добавить перекрёстные ссылки на канонические карточки. Не рекомендовать FPS kit для TPS лишь потому, что названия похожи.

## Системы сквозные
- Контроллер: платформер / action RPG / FPS; но оси, коллизии, камера и движение разные.
- Инвентарь: RPG / survival / sandbox / farming / factory automation.
- AI Navigation: TPS / RTS / city-builder / stealth; NavMesh не обеспечивает боевое поведение сам по себе.
- Сохранения: все жанры с прогрессом, нужна схема миграции данных.
- UI: локализация, accessibility, ввод и адаптивный layout почти для всех платформ.
- Networking: кооператив/competitive / MMOs / social, не обязательное условие жанра.
- Data-driven config: уровни, предметы, способности, экономика, параметры физики.

## Ограничения
Подобрать настоящий starter kit для каждого жанра и измерить интеграцию — дальнейшая работа. До получения таких данных нельзя помечать отдельную жанровую строку как «исследовано полностью».

## Бесплатные наборы по жанрам (первый проход)
| Жанр | Кандидатные полностью бесплатные части | Статус |
|---|---|---|
| 2D платформер | [Kenney](../Tool_Catalog/kenney-new-platformer-pack.md), Unity Input/Physics2D/Tilemap | [ASSUMED Stack](../21_Compatible_Stacks/FREE_STACKS.md#2d-platformer-free--2d-платформер) |
| TPS/3D RPG | [Quaternius Base Characters](../Tool_Catalog/quaternius-universal-base-characters.md) + [Animation Library](../Tool_Catalog/quaternius-universal-animation-library.md) + Input/Camera/NavMesh | [ASSUMED Stack](../21_Compatible_Stacks/FREE_STACKS.md#3d-rpg-exploration-free--3d-rpg--tps-exploration) |
| Sci-fi exploration | [Quaternius Standard](../Tool_Catalog/quaternius-modular-sci-fi-megakit.md) + Unity URP | [ASSUMED Stack](../21_Compatible_Stacks/FREE_STACKS.md#3d-sci-fi-corridor-free--sci-fi-fps--exploration) |
| Water racing | Boat Attack legacy | Требуется портирование; [reference](../Comparisons/COMPLETE_FREE_PROJECTS.md) |

Это **не завершённая жанровая матрица**: здесь несколько проверенных по источникам решений, ещё нет сборок на целевых платформах.
