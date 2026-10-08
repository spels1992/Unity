# Гонки, выживание, строительство, FPS — сравнение бесплатных проектов

**Исследование 2026-10-08.** Проверены upstream README, LICENSE, ProjectVersion.txt, package.json и некоторые сторонние зависимости. **Editor-тестов ещё не было**. Корневая MIT-лицензия проекта не делает все встроенные модели, звуки и сетевые сервисы MIT.

| Жанр/задача | Основной кандидат | Реализованные функции | Unity по источнику | Юридическая граница | Решение |
|---|---|---|---|---|---|
| 3D survival | [Project Wanderer](../Tool_Catalog/project-wanderer-survival.md) | Gather, crafting, inventory, chests, durability, day/night, save, resource spawn | 6000.3.13f1 | MIT код; Unity Companion StarterAssets | PRIORITY_TEST |
| Строительство, colony | [Grid Building System](../Tool_Catalog/grid-building-system.md) | Walls/doors/stairs/multi-floor A*, chunk meshes, JSON save | 6000.3.16f1 | MIT код, third-party assets проверить | PRIORITY_TEST |
| Географические города | [GeoJSON City Builder](../Tool_Catalog/geojson-city-builder.md) | GeoJSON polygons→buildings, place prefabs | UPM 0.4.3 / 2019.1+ | com.virgis.geojson.net не подтверждён по лицензии | BLOCKED_DEPENDENCY |
| Гоночная игра | [PolyRace](../Tool_Catalog/polyrace-legacy.md) | 4 hovercraft, процедура генерации трасс | 2020.3.25f1 | LGPL LibNoise, сторонние музыка/модели/DOTween | LEARNING_ONLY |
| Тайм-триал | [Street Racing](../Tool_Catalog/street-racing-free-demo.md) | Race against clock, WebGL demo | 2020.3.25f1 | Unity Asset Store car/road EULA | LEARNING_ONLY |
| Аркадная физика авто | [ArcadeVehiclePhysics](../Tool_Catalog/arcade-vehicle-physics.md) | Driving/drift physics, legacy input | 2018.4.5f1 | MIT scripts, Sketchfab car separately | CODE_REFERENCE |
| Реалистичные шины | [TLabVehiclePhysics](../Tool_Catalog/tlab-vehicle-physics.md) | Pacejka, LUT, WheelCollider alternative | 2022.3.19f1 | MIT root; git submodules не все лицензированы | BLOCKED_LICENSE |
| Крафт по сетке | [Grid-Based Crafting](../Tool_Catalog/grid-based-crafting-system.md) | Recipe UI, CraftingManager, resource checks | 2022.3.9f1 | MIT GitHub source, Store listing price unknown | TEST_GITHUB_SOURCE |
| Многопользовательский FPS | [Armour FPS](../Tool_Catalog/armour-multiplayer-fps.md) | Lobby, shooting, HP, Photon PUN2 | 2022.3.55f1 | Photon тарифы, Mixamo и оружие отдельно | REFERENCE_ONLY |

## Практические выводы
- **Survival:** сначала [Project Wanderer](../Tool_Catalog/project-wanderer-survival.md); он уже объединяет Inventory/Crafting/Storage/Save. Не добавлять второй crafting core без необходимости.
- **City / base building:** [Grid Building System](../Tool_Catalog/grid-building-system.md) подходит для сооружений и навигации, но это НЕ готовая игра с жителями, экономикой и производством.
- **Racing:** PolyRace как полный учебный пример; ArcadeVehiclePhysics как изолированная физическая система, но устаревшая. TLab не внедрять до аудита submodules. Для современных проектов Unity 6 необходим smoke-test/портирование.
- **FPS:** Armour полезен как пример анимаций/лобби, но Photon — внешняя зависимость с тарифами. Беспроцентный локальный LAN-сценарий можно изучать с [Mirror MIT](../Tool_Catalog/mirror-networking.md), не объявляя его уже проверенным.
- **GeoJSON:** красивый город, созданный из координат, **не равен City Builder Game**. Нужны ещё zoning/road/traffic/economy, а источники геоданных лицензируются отдельно.

## Минимальная программа проверки
1. Проверить LICENSE именно того кода и ассетов, который намерены переносить в свою игру.
2. Зафиксировать tag/commit, ProjectVersion/UPM dependencies.
3. Открыть **копию в отдельном тестовом проекте**, Unity Console 0 compile errors.
4. Проверить основное действие в PlayMode: один круг, одно изделие, save/reload конструкции или 2 FPS-клиента.
5. Сделать Player Build, лог и FPS; только тогда отметить **TESTED**, иначе **DOCUMENTED**.
6. Записать выводы в [матрицу совместимости](../COMPATIBILITY_MATRIX.md) и журнал.

[Гайды по сборке](../21_Compatible_Stacks/FREE_SURVIVAL_RACING_BUILDING.md) · [правило 0 ₽](../FREE_ONLY_POLICY.md).
