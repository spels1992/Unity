# COMPATIBILITY_MATRIX — версии, зависимости, реальные тесты

Дата: 2026-10-08. Статусы: **DOC** документально заявлено; **TESTED** наш воспроизводимый тест; **UNKNOWN** не установлено; **CONFLICT** известный конфликт. **На текущий момент TESTED нет.**

| Решение | Официально указана версия | Тип | Статус с Unity 6.3 | Внутренние конфликты |
|---|---|---|---|---|
| Cinemachine | 3.1.7 для 6000.3 | Unity Package | DOC: 6000.3 | При миграции с 2.x есть breaking changes |
| AI Navigation | 2.0.15 для 6000.3 | Unity Package | DOC: 6000.3 | Система навигации, не behavior-tree и не combat AI |
| DOTS Samples | Unity 6.2 + Entities 1.4 и др. | демонстрационные проекты | UNKNOWN; не переносить без теста | ECS и обычный MonoBehaviour workflow требуют специальной интеграции |
| Mirror | Версию 6.3 в проверенном README не подтверждали | Сетевой фреймворк | UNKNOWN | Не устанавливать вместе с FishNet «для улучшения сети» без проектной архитектуры |
| FishNet | В проверенном README версия 6.3 не указана | Сетевой фреймворк | UNKNOWN | Custom licence, не смешивать с Mirror как один transport |
| UniTask | Точная ветка 6.3 требует проверки | Async библиотека | UNKNOWN | Проверять lifetime и отмену async |
| FPS Sample | Unity 2018.3.8f1 | учебная игра | UNKNOWN/legacy | HDRP старой версии; требуется портирование |
| Unity 2d-extras Git repo | upstream объявил прекращение развития | Tilemap scripts | Legacy | Предпочесть Unity Tilemap Extras через UPM |

## Правила записи результата теста
`stack ID | Unity editor exact | package versions | render pipeline | OS+GPU+target | сценарий | результат | crash log/PR/commit | дата | tester`.

**Никогда** не повышать «UNKNOWN» до «TESTED» по удачному ответу нейросети, Reddit-комментарию или README.

### Подозрительные сочетания
- Два разных сетевых стека как центральные транспорты без адаптера — технически конфликтующие концепции.
- Набор камер и контроллеров с собственными input/camera managers может дублировать управление.
- HDRP-only ассеты нельзя считать совместимыми с URP автоматически.
- Один giant framework и 5 отдельных manager-пакетов часто дублируют инвентарь, input, save и AI: проверить границы ответственности.

| Input System | com.unity.inputsystem 1.20.1 для 6000.3 | Unity Registry | DOC 6000.3 | Согласовать mappings со Starter Controller |
| Tilemap Extras | com.unity.2d.tilemap.extras 6.0.3 для 6000.3 | Unity Registry | DOC 6000.3 | Старый 2d-extras Git объявлен read-only |
| First Person + Third Person Controller | Asset Store 2.0.1 (17.09.2026) | Free Asset | DOC URP 6000.3.0f1; Built-in/HDRP нет | Non standard EULA |
| 2D Game Kit | Asset Store 5.0 (23.03.2026) | Free Asset | DOC URP 6000.3.0f1 | Standard EULA, Extension Asset |
| FPS Microgame | Asset Store DEPRECATED | Old Asset | Недоступен новым пользователям | НЕ рекомендовать как новый starter |

## Предлагаемые полностью бесплатные стеки — ПОКА не проверены
| Стек | Основные компоненты | Статус и основание |
|---|---|---|
| [2D-PLATFORMER-FREE](21_Compatible_Stacks/FREE_STACKS.md) | Kenney CC0 + Input System + Physics2D + Tilemap Extras | ASSUMED: официальные компоненты и бесплатная графика, live теста нет |
| [3D-RPG-EXPLORATION-FREE](21_Compatible_Stacks/FREE_STACKS.md) | Quaternius Standard Characters/Animations + Unity Input, Cinemachine, AI Navigation | ASSUMED: Quaternius заявляет совместимые rig, но retarget не тестировался |
| [3D-SCI-FI-CORRIDOR-FREE](21_Compatible_Stacks/FREE_STACKS.md) | Quaternius Standard Sci-Fi + Unity Camera/Input + URP | ASSUMED: FBX импорт и prefab/коллизии не проверены |
| [BOAT-RACING-REFERENCE](21_Compatible_Stacks/FREE_STACKS.md) | Boat Attack + Water | LEGACY: Unity 2019 demo, Unity 6 не подтверждена |

**В нашей базе значение VERIFIED = 0** до живых tests/build на целевой машине. Ссылки на package версии не заменяют результаты тестов.


## Фреймворки Unity 6: проверка README против исходной конфигурации
| Система | Upstream evidence | Статус интеграции у нас |
|---|---|---|
| [OpenEmpires](Tool_Catalog/open-empires-rts.md) | README 6000.3.9f1; фактический ProjectVersion.txt = **6000.5.9f1** | DOC-конфликт; build UNKNOWN |
| [Moonforge](Tool_Catalog/moonforge-rpg-engine.md) | UPM 1.2.0, Unity 2022.3+ | UNKNOWN на 6000.3 |
| [Yarn Spinner](Tool_Catalog/yarn-spinner-unity.md) | 3.2.8 UPM / 2022.3+ | UNKNOWN на 6000.3 |
| [Ink](Tool_Catalog/ink-unity-integration.md) | 2.0.0 UPM / 2022.3+ | UNKNOWN на 6000.3 |
| [Game Lattice](Tool_Catalog/game-lattice-rpg.md) | 0.0.0-dev UPM / 2021.2+; example ProjectVersion 6000.4.11f1 | DOC package, no Player test |
| [Softlight](Tool_Catalog/softlight-unity6-rpg.md) | ProjectVersion.txt 6000.3.7f1 | DOC only, early prototype |
| [Unity Modular Inventory](Tool_Catalog/unity-modular-inventory.md) | ProjectVersion.txt 6000.0.50f1 | DOC only, newer variants unknown |
| [EZ Room](Tool_Catalog/ezroomgenerator.md) | 0.1.0 UPM Unity 6000.0+, FBX Exporter 5.1.5 declared | DOC, integration dependency needs test |
| [Edgar Free](Tool_Catalog/edgar-unity-free.md) | 2.1.0 UPM Unity 2019.3+; PRO features paid | DOC only; newer Unity unknown |
| [OpenKCC](Tool_Catalog/openkcc-controller.md) | 1.5.0 UPM Unity 2019.4+, development last 2023 | Unity 6 unknown |

**VERIFIED still equals zero**: source code/README/manifest checks do not mean runtime compatibility.


## НОВЫЕ решения: гонки, survival, строительство, FPS (исключительно DOCUMENTED)
| Решение | ProjectVersion / metadata | Реальный результат |
|---|---|---|
| [Project Wanderer](Tool_Catalog/project-wanderer-survival.md) | 6000.3.13f1; Unity Input System | NOT_RUN |
| [Grid Building System](Tool_Catalog/grid-building-system.md) | 6000.3.16f1 | NOT_RUN |
| [GeoJSON City Builder](Tool_Catalog/geojson-city-builder.md) | 0.4.3, Unity 2019.1+, dependency com.virgis.geojson.net 1.2.17 | BLOCKED_DEPENDENCY / NOT_RUN |
| [PolyRace](Tool_Catalog/polyrace-legacy.md) | 2020.3.25f1, Blender 3.0 (README) | NOT_RUN, legacy |
| [Street Racing](Tool_Catalog/street-racing-free-demo.md) | 2020.3.25f1 | NOT_RUN, Asset Store packs не проверены |
| [ArcadeVehiclePhysics](Tool_Catalog/arcade-vehicle-physics.md) | 2018.4.5f1, legacy Input Manager | NOT_RUN |
| [TLabVehiclePhysics](Tool_Catalog/tlab-vehicle-physics.md) | 2022.3.19f1, 3 git submodules | BLOCKED_LICENSE / NOT_RUN |
| [Grid-Based Crafting](Tool_Catalog/grid-based-crafting-system.md) | 2022.3.9f1 | NOT_RUN |
| [Armour Multiplayer-FPS](Tool_Catalog/armour-multiplayer-fps.md) | 2022.3.55f1, Photon PUN2 | NOT_RUN, server cost unknown |

**VERIFIED здесь ноль**, подготовлен только анализ версий/конфликтов по исходникам.


## Blender/Unity import и бесплатный звук — документальная проверка
| Решение | Проверенная upstream metadata | Наш test status |
|---|---|---|
| [Rigify](Tool_Catalog/blender-rigify-free.md) | Blender built-in, docs 4.5/5.2, GPL | NOT_RUN |
| [glTF-Blender-IO](Tool_Catalog/khronos-blender-gltf-io.md) | Blender 2.80+ bundled, Apache-2.0 | NOT_RUN |
| [Unity glTFast](Tool_Catalog/unity-gltfast.md) | main package **6.20.1-pre.1**, minimum Unity 6000.0, Apache-2.0 | NOT_RUN; выбрать stable Registry |
| [Ucupaint](Tool_Catalog/ucupaint-blender-free.md) | manifest 3.0.0, min Blender 4.2.0, GPL-3.0-or-later | NOT_RUN |
| [TexTools](Tool_Catalog/textools-blender-free.md) | README Blender 3.2+, 5.x не гарантирована, GPLv3+ | NOT_RUN |
| [ambientCG](Tool_Catalog/ambientcg-cc0.md) | CC0 assets / PBR textures | NOT_IMPORTED |
| [Kenney CC0 audio](14_Audio/FREE_SOUND_PIPELINE.md) | 50 + 130 + 50 + 70 + 85 files | NOT_IMPORTED |

**Нельзя** считать glTFast runtime export/render совпадающим без проверки Player Build shader variants. См. [3D-гайд](18_Blender_Integration/FREE_GLTF_RIG_UV_PRODUCTION.md).


## Дополнительные Blender/audio кандидаты, 09.10.2026 — ТОЛЬКО ДОКУМЕНТАЦИЯ
| Решение | Заявленная upstream версия | Наш статус |
|---|---|---|
| [Geometry Nodes](Tool_Catalog/blender-geometry-nodes-free.md) | Built-in Blender 4.5, procedural scatter | NOT_RUN / export bake нужен |
| [Decimate LOD](Tool_Catalog/blender-decimate-lod-free.md) | Blender built-in | NOT_RUN / geometry QA |
| [Sapling Tree](Tool_Catalog/blender-sapling-tree.md) | v0.3.7, Blender 4.4+; 5.x animation complaints | NOT_RUN |
| [YGForge LowPolyTree](Tool_Catalog/blender-lowpoly-tree-generator.md) | 1.1.5, Blender 5.0.1+ | NOT_RUN |
| [Modular Tree](Tool_Catalog/blender-modular-tree.md) | 5.5.2, Blender 4.3.1+; 5.1 support | NOT_RUN |
| [Retarget KBS](Tool_Catalog/blender-retarget-kbs.md) | 5.2.0, Blender 5.0+ | NOT_RUN |
| [Rokoko Retarget](Tool_Catalog/blender-rokoko-retarget.md) | Blender 2.80+ claimed, live extra software optional | NOT_RUN, license LGPL |
| [Rhubarb NG](Tool_Catalog/rhubarb-lip-sync-ng-blender.md) | 1.8.1, Blender min 3.3, 4.2+ extension | NOT_RUN, Russian QA unknown |
| [Rhubarb CLI](Tool_Catalog/rhubarb-cli-open-source.md) | Offline CLI, cross-platform | NOT_RUN |
| [Music bundles](14_Audio/FREE_CC0_MUSIC_COLLECTION.md) | CC0 exact pages, 12+4+2 declared, 5 ZIP unknown | NOT_IMPORTED |

**TESTED/VERIFIED в нашем Blender/Unity по этому новому блоку: ноль.**
