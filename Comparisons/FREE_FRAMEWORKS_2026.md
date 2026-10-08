# Бесплатные готовые Unity системы — сравнение по назначению

**Проверено по публичным upstream источникам: 2026-10-08. В наших проектах в Unity Editor НЕ тестировалось.** Полный лицензионный/версионный аудит сторонних ассетов впереди.

| Инструмент | Уже реализовано | Бесплатность/лицензия | Фактические версии | Рекомендация |
|---|---|---|---|---|
| [OpenEmpires](../Tool_Catalog/open-empires-rts.md) | RTS целая игра | MIT; Editor версия README ≠ ProjectVersion | 6000.5.9f1 в ProjectVersion | Рекомендуется для пилота |
| [Moonforge RPG Engine](../Tool_Catalog/moonforge-rpg-engine.md) | RPG core: quest/combat/loot/save | MIT, бесплатный UPM | UPM Unity 2022.3+ | Рекомендуется для прототипа |
| [Yarn Spinner for Unity](../Tool_Catalog/yarn-spinner-unity.md) | Диалоги/визуальные новеллы | MIT Git бесплатно; Asset Store/Itch платные | 3.2.8, Unity 2022.3+ | Рекомендуется |
| [Ink Unity Integration](../Tool_Catalog/ink-unity-integration.md) | Нарратив и диалоги | MIT Git бесплатно | 2.0.0, Unity 2022.3+ | Рекомендуется |
| [OpenKCC](../Tool_Catalog/openkcc-controller.md) | Kinematic controller | MIT; upstream last push 2023 | package 1.5.0, Unity 2019.4+ (6 не тест) | Требует теста |
| [EZ Room Generator](../Tool_Catalog/ezroomgenerator.md) | 3D генератор лабиринтов | MIT | 0.1.0, Unity 6000+ | Рекомендуется для теста |
| [Edgar Free Core](../Tool_Catalog/edgar-unity-free.md) | 2D графовый dungeon generator | MIT free core; PRO платный | 2.1.0, минимальная Unity 2019.3 | Хорошая альтернатива |
| [Game Lattice](../Tool_Catalog/game-lattice-rpg.md) | Большой RPG+NPC AI framework | Apache-2.0; UPM 0.0.0-dev | Unity 2021.2+; пример 6000.4 | Пилот, высокий риск |
| [Game Lattice Playground](../Tool_Catalog/game-lattice-unity-playground.md) | Готовая учебная RPG песочница | Apache-2.0 | Unity 6000.4.11f1 | Первый шаг к Game Lattice |
| [Unity Modular Inventory](../Tool_Catalog/unity-modular-inventory.md) | Инвентарь drag/drop | MIT, assets Kenney separately | Unity 6000.0.50f1 | Кандидат, нет save |
| [Softlight](../Tool_Catalog/softlight-unity6-rpg.md) | 2D top-down RPG prototype | MIT, incomplete | Unity 6000.3.7f1 | Образец, не полный RPG |
| [Unity FPS Controller](../Tool_Catalog/simple-fps-controller-unity6-mit.md) | Базовый FPS контроллер | MIT, старый Input Manager | Unity 6, exact Editor неизвестна | Запасной |

## В каких случаях брать целую систему
### RTS
[OpenEmpires](../Tool_Catalog/open-empires-rts.md) — ядро целой игры с lockstep, units/resource/building. **Не** ставить поверх неё другой «глобальный сетевой фреймворк» как улучшение без системы интеграции. Для игры с одним игроком начать с локальной simulation. [Пример исходников](https://github.com/Chilly5/OpenEmpires).

**Критический расхождение первоисточников:** README = 6000.3.9f1, ProjectSettings/ProjectVersion.txt = 6000.5.9f1. При подготовке проекта сначала доверять ProjectVersion.txt и сверять его с релизом.

### RPG
- [Moonforge](../Tool_Catalog/moonforge-rpg-engine.md) — выбор при **пошаговом бою, party, inventory, quest tracking, save/load**, особенно с testable pure C#.
- [Game Lattice](../Tool_Catalog/game-lattice-rpg.md) — выбор при **data-driven JSON content, world simulation, 5 уровней NPC AI, quests и диалогах**, хорош для AI authored content, но пакет 0.0.0-dev и требует изучения архитектуры.
- **Не устанавливать оба RPG engines одновременно** без решения, кто хранит inventory/stats/quest/event/save truth. Иначе дублирование данных и сохранений.
- [Softlight](../Tool_Catalog/softlight-unity6-rpg.md) — содержит **движение, камеры, Tilemap и анимации**, но не реализованную полностью RPG систему. Это хороший base world prototype, не замена фреймворкам.
- [Unity Modular Inventory](../Tool_Catalog/unity-modular-inventory.md) — самостоятельный модуль drag/drop/stack, если полная RPG система не нужна; state/save adapter нужен.

### Диалоги
- [Yarn Spinner](../Tool_Catalog/yarn-spinner-unity.md): бесплатен **из GitHub**, платные Asset Store/Itch packages НЕ требуются.
- [Ink](../Tool_Catalog/ink-unity-integration.md): полностью бесплатен по MIT, подходит для branching narrative.
- **Обычно выбирать один** dialogue system; объединение двух усложнит UI, localization, save и event graph. Moonforge/Game Lattice также содержат narrative logic; проектировать single owner.

### Управление и генерация
- [OpenKCC](../Tool_Catalog/openkcc-controller.md) староват для Unity6 (UPM минимум 2019.4, GitHub last push 2023), поэтому не считать production-compatible без build.
- [Simple FPS Controller](../Tool_Catalog/simple-fps-controller-unity6-mit.md) лёгкий вариант, использует старый Input Manager, не готовый FPS gameplay kit.
- [EZ Room Generator](../Tool_Catalog/ezroomgenerator.md) 3D rooms / corridors/mazes, UPM 0.1.0 и FBX Exporter dependency.
- [Edgar Free](../Tool_Catalog/edgar-unity-free.md) 2D roguelike levels из графа и авторских комнат; **PRO не входит** и не требуется для обычных dungeons.

## Плата, которой НЕ должно быть
- Yarn Spinner платный store пакет — используем бесплатный Git UPM.
- Edgar PRO — не используем.
- Rust + PostgreSQL при локальном self-host OpenEmpires — бесплатные, но платные VPS/сервисы не запускаем.
- Unity cloud generation (fal/OpenRouter/Meshy/Tripo) — не включаем.
- Публичный репозиторий без LICENSE — **не разрешён к переиспользованию**.

## Нужно доказать тестом
1. Clone/install с точным tag/commit и отдельными LICENSE ассетов.
2. Совместимость Unity exact, build, demo, Console errors и platforms.
3. Story/inventory/AI/save системные конфликты и migrations.
4. Проверка CPU/GPU, памяти, управляемости и минимальный Windows Player Build.
