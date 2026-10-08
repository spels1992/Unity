# Бесплатные сценарии для Survival, Racing, Building и FPS

**2026-10-08.** Статус всех архитектур = **ASSUMED**, реальный Unity Editor не проверялся. Никаких новых платных API/ассетов или облачного хостинга.

## SURVIVAL_BASE
**Основа:** [Project Wanderer](../Tool_Catalog/project-wanderer-survival.md), Unity 6000.3.13f1, MIT code + отдельные условия Unity Companion для StarterAssets.
**Порядок:** открыть изолированный upstream проект → собрать дерево/камень → создать инструмент → поместить предмет в сундук → сохранить → загрузить → проверить точное количество предметов и durability.
**Граница:** встроенные Inventory, Crafting, Save — единственные владельцы данных; не дублировать их отдельными ассетами. Для своего визуала использовать CC0 Kenney/Quaternius (бесплатный Standard), а не платную Source.

## BUILDING_GRID
**Основа:** [Grid Building System](../Tool_Catalog/grid-building-system.md), Unity 6000.3.16f1.
**Порядок:** SampleScene → построить полы/стены/дверь/лестницу → пройти путь A* по двум этажам → удалить дверь → проверить обновление пути → Save/Load → проверить точное восстановление построек/связей/mesh chunks.
**Граница:** один PlacementSystem, один NavGrid, один SaveLoadManager. Экономика, NPC, production zones не входят в перечень уже готовых функций.

## RACING_ARCADE
**Основа:** [ArcadeVehiclePhysics](../Tool_Catalog/arcade-vehicle-physics.md) как MIT reference; Unity 2018.4 → портировать с тестом в Unity6. **Не копировать чужую Sketchfab модель как MIT.**
**Порядок:** бесплатная CC0 машина или примитивный box vehicle → Rigidbody+один input owner → трасса с физическими стенами → steering/throttle/brake → 3 круга → performance и Windows build.
**Другие кандидаты:** [PolyRace](../Tool_Catalog/polyrace-legacy.md) — цельная legacy игра с отдельными правами на assets; [TLabVehiclePhysics](../Tool_Catalog/tlab-vehicle-physics.md) НЕ подключать пока не подтверждены лицензии сабмодулей.

## FPS_LOCAL
**Пример:** [Armour Multiplayer-FPS](../Tool_Catalog/armour-multiplayer-fps.md) как учебник. Photon PUN2 нельзя делать обязательным backend при требовании нулевых расходов.
**Гипотеза бесплатного локального стека:** [Mirror](../Tool_Catalog/mirror-networking.md) MIT + Unity встроенный CharacterController, Input System, простые CC0 модели. Два LAN клиента, стрельба/HP, серверное подтверждение урона, отключение и reconnect. ВЫПОЛНИТЬ совместимость/PlayMode/Player Build до статуса VERIFIED.

## Запрещённые или непроверенные привязки
- Обязательный Unity Asset Store PRO пакет, Quaternius Source, облачный оплачиваемый AI/BYOK.
- Вторая Inventory/Save/Pathfinding система без разграничения ownership.
- TLab submodules и GeoJSON geojson.net без подтверждённой лицензии/прав.
- Коммерческий сервер «бесплатен навсегда» — никогда не утверждать без проверки договора/лимитов.

**Все четыре стека — инструкции, а не завершённые сборки.** [Тестовый протокол](../22_Optimization_Testing/FREE_MODULE_SMOKE_TESTS.md).
