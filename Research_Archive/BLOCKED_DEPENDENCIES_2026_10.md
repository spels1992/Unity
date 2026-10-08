# Лицензии зависимостей: исключения для бесплатного пути

**Проверено 2026-10-08.** Корневой MIT не означает MIT для всех подпроектов и ассетов.

| Кандидат | Найденный риск | Статус |
|---|---|---|
| [TLabVehiclePhysics](../Tool_Catalog/tlab-vehicle-physics.md) | Root MIT, но .gitmodules подключает TLabCurveTool, TLab-Spline, Unity-SDF-UI-Toolkit. У TLab-Spline в Git tree не найден LICENSE, TLabCurveTool пока не проаудирован. Unity-SDF-UI-Toolkit имеет MIT. | BLOCKED_LICENSE для всего стека |
| [GeoJSON City Builder](../Tool_Catalog/geojson-city-builder.md) | Root MIT, но package.json требует com.virgis.geojson.net 1.2.17; источник/лицензия зависимости ещё не подтверждены. | BLOCKED_DEPENDENCY |
| [Armour Multiplayer-FPS](../Tool_Catalog/armour-multiplayer-fps.md) | Photon PUN2 с внешними тарифами/лимитами, Mixamo персонажи и Asset Store оружие под отдельными условиями. | REFERENCE_ONLY |
| [PolyRace](../Tool_Catalog/polyrace-legacy.md) | Buryat Sky модели, Gabe Castro музыка, LGPL LibNoise, DOTween, прочие сторонние материалы. | REFERENCE_ONLY |
| [Street Racing](../Tool_Catalog/street-racing-free-demo.md) | Cartoon Car Vehicle Pack и Low Poly Road Pack из Asset Store; точная текущая цена и EULA не подтверждены. | LEARNING_ONLY |
| [sromic1990/CityBuilder](https://github.com/sromic1990/CityBuilder) | Root MIT, но содержит Assets/Plugins/Demigiant/DOTweenPro и Assets/Plugins/Sirenix; лицензии премиальных плагинов не подтверждены. | RESEARCH_ONLY |

**Варианты без этой блокировки:** [Grid Building System](../Tool_Catalog/grid-building-system.md) (MIT-код, отдельно аудит ассетов), [Project Wanderer](../Tool_Catalog/project-wanderer-survival.md) (MIT + Unity Companion StarterAssets), [Kenney CC0](../Tool_Catalog/kenney-free-assets.md) для моделей. Установка и перепубликация блокированных модулей не выполняются до выяснения прав.

[Полное сравнение](../Comparisons/VEHICLES_SURVIVAL_BUILDING_FPS_2026.md).
