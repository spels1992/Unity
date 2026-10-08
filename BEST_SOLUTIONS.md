# BEST_SOLUTIONS — выбор решений (осторожный старт)

**Дата:** 2026-10-08. **Важное обновление:** бывший FPS Microgame в Asset Store уже DEPRECATED, а вместо старого First-Person Controller представлен обновлённый объединённый First Person + Third Person контроллер. Список динамический. «Изучено по документации» **не равно** «проверено в Unity».

| Ситуация | Первым изучить | Причина | Статус |
|---|---|---|---|
| Учебный FPS | [Unity First Person + Third Person Controller](Tool_Catalog/official-starter-kits.md) | Новый бесплатный объединённый пакет Unity, версия 2.0.1 от 2026-09-17 | EULA нестандартная; требуется тест в Unity |
| TPS/движение персонажа | [Объединённые FPS+TPS Controllers](Tool_Catalog/official-starter-kits.md) | FREE, URP 6000.3, проверено по Asset Store | Non-standard EULA; не тестировалось |
| 2D платформер | [2D Game Kit](Tool_Catalog/2d-game-kit.md) | FREE, Asset Store v5.0 (2026-03-23), URP 6000.3 | Документально изучено, без Editor тестов |
| Камеры | [Cinemachine](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-cinemachine) | Официальный модуль; Unity 6.3: 3.1.7 | Изучено по документации |
| Навигация NPC | [AI Navigation](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-ai-navigation) | NavMesh и runtime/edit-time navigation; 6.3: 2.0.15 | Изучено по документации |
| Сетевой проект | [Mirror](Tool_Catalog/mirror-networking.md) | MIT, активный open source, комплексная сетевая система | Проверено по исходникам/лицензии, не тестировалось в Editor |
| Сложный async | [UniTask](Tool_Catalog/unitask.md) | MIT, поддерживаемый async toolkit | Изучено по исходникам; необходимость уточнить |
| Массовая ECS симуляция | [DOTS Samples](Tool_Catalog/unity-dots-samples.md) | Официальная подборка примеров ECS/Jobs/Physics/Netcode | Старые sample-версии: Unity 6.2, не заявлена совместимость с 6.3 |

**Не рекомендовать как новый production starter:** [FPSSample](Tool_Catalog/fps-sample-legacy.md) — сам README заявляет Unity 2018.3 и отсутствие поддержки. Важно различать красивую демонстрацию и поддерживаемую современную основу.

**Устарели/недоступны новым пользователям:** [FPS Microgame](Tool_Catalog/fps-microgame-deprecated.md) и отдельный старый [Starter Assets: FirstPerson](https://assetstore.unity.com/packages/essentials/starter-assets-firstperson-urp-196525). Первый официально deprecated; второй снят со страницы, использовать актуальный объединённый контроллер.

## Полностью бесплатные варианты для создания контента — первое предпочтение
| Что нужно | 0 ₽ вариант | Лицензия | Ограничения |
|---|---|---|---|
| HDRI, PBR материалы, 3D props | [Poly Haven](Tool_Catalog/poly-haven.md) | CC0 | Дополнительные Vault/Bulk удобства не обязательны и бывают платными |
| 2D платформер | [Kenney New Platformer Pack](Tool_Catalog/kenney-new-platformer-pack.md) | CC0 | Отдельный набор бесплатен, All-in-1 платный |
| 3D платформер | [Kenney Platformer Kit](Tool_Catalog/kenney-platformer-kit-3d.md) | CC0 | Контроллер и правила игры не входят |
| Бесплатные RPG/TPS базовые модели | [Quaternius Universal Base Characters](Tool_Catalog/quaternius-universal-base-characters.md) | CC0 Standard | Paid Source не покупать |
| Humanoid-анимации | [Quaternius Universal Animation Library](Tool_Catalog/quaternius-universal-animation-library.md) | CC0 Standard | Степень покрытия free части нужно сверять |
| Sci-fi окружение | [Quaternius Modular Sci-Fi MegaKit](Tool_Catalog/quaternius-modular-sci-fi-megakit.md) | CC0 Standard | Бесплатная часть ≠ готовая Unity сцена |

**Бесплатные совместимые стеки пока только на уровне кандидатов**: [FREE_STACKS.md](21_Compatible_Stacks/FREE_STACKS.md). Ни один не проходил live-тест в Unity Editor.


## Бесплатные решения, закрывающие сразу несколько задач (источники 08.10.2026)
| Для чего | Приоритетный кандидат | Цена | Статус |
|---|---|---|---|
| RTS целиком | [OpenEmpires](Tool_Catalog/open-empires-rts.md) | MIT, локально бесплатно | Версия Unity README/ProjectVersion различается, нужен тест |
| Turn-based RPG core | [Moonforge](Tool_Catalog/moonforge-rpg-engine.md) | MIT, бесплатно | Unity 2022.3+ package, Unity6 тест нужен |
| Data-driven RPG/NPC AI | [Game Lattice](Tool_Catalog/game-lattice-rpg.md) | Apache-2.0, бесплатно | Unity 6000.4 playground, dev package v0.0.0 |
| Диалоги / Visual novel | [Yarn Spinner Git](Tool_Catalog/yarn-spinner-unity.md) ИЛИ [Ink](Tool_Catalog/ink-unity-integration.md) | MIT, бесплатные Git UPM | Не устанавливать два без необходимости |
| Инвентарь без full RPG | [Unity Modular Inventory](Tool_Catalog/unity-modular-inventory.md) | MIT, бесплатно | PlayMode/Build теста нет, Save не готов |
| 3D процедурные комнаты | [EZ Room Generator](Tool_Catalog/ezroomgenerator.md) | MIT, бесплатно | 0.1.0 Unity 6000+; FBX Exporter dependency |
| 2D dungeon | [Edgar Free](Tool_Catalog/edgar-unity-free.md) | MIT core, бесплатно | PRO функции платные/исключены |

[Подробная сравнительная матрица](Comparisons/FREE_FRAMEWORKS_2026.md).


### Дополнение: Moonforge даёт готовую Unity roguelike sample
[Moonforge RPG](Tool_Catalog/moonforge-rpg-engine.md) не только Core: в UPM включена Unity sample с Town, Dungeon, HUD, боем, questing, save/load и процедурной генерацией. [Sample README](https://github.com/3583Bytes/moonforge-rpg-engine/blob/main/unity-packages/com.moonforge.core/Samples~/Roguelike/README.md). Для быстрого теста полноценной turn-based RPG он приоритетнее сборки отдельных подсистем. Однако **лицензионный файл тайлсета из README не найден в GitHub tree** — права на конкретный art подтвердить у правообладателя прежде чем переносить/распространять ассеты.


## Продолжение: стартовые бесплатные решения Survival/Building/Racing (08.10.2026)
| Запрос | В первую очередь | Почему | Неизвестное |
|---|---|---|---|
| Survival + craft + save | [Project Wanderer](Tool_Catalog/project-wanderer-survival.md) | Несколько рабочих систем связаны в один loop, Unity 6000.3.13f1, MIT code | Проверка StarterAssets Unity Companion и PlayMode |
| Построить здание по сетке | [Grid Building System](Tool_Catalog/grid-building-system.md) | Placement, многоэтажный A*, mesh chunks и save, Unity 6000.3.16f1 | Editor test, source assets |
| Аркадная физика авто | [ArcadeVehiclePhysics](Tool_Catalog/arcade-vehicle-physics.md) | MIT code, меньше масштаба чем full racing game | Устаревшая 2018 Unity, новый Input |
| Гонки sci-fi | [PolyRace](Tool_Catalog/polyrace-legacy.md) | Цельный проект с procedural track | Сторонние модели/музыка/ЛГПЛ, Unity 2020; **только изучение** |
| Реалистичные шины | [TLabVehiclePhysics](Tool_Catalog/tlab-vehicle-physics.md) | Pacejka + LUT | **BLOCKED**: лицензии git submodules неизвестны |
| Город из GeoJSON | [GeoJSON City Builder](Tool_Catalog/geojson-city-builder.md) | Готовое построение 3D объектов из геоданных | **BLOCKED**: лицензия com.virgis.geojson.net не выяснена |

При любой сборке система Input/Save/Network/Physics должна иметь **одного владельца**. [Сравнение](Comparisons/VEHICLES_SURVIVAL_BUILDING_FPS_2026.md).


## Бесплатные арт- и аудиопути от нуля до Unity
| Что нужно | Первое решение 0 ₽ | Если не подходит |
|---|---|---|
| Rig/анимация в Blender | [Встроенный Rigify](Tool_Catalog/blender-rigify-free.md) GPL | Ручной Armature/Quaternius готовые rigged models |
| UV острова, texel density | [TexTools](Tool_Catalog/textools-blender-free.md) GPL + Blender UV Editor | Штатный Blender UV Editor/Bake, без установки addon |
| Текстурные слои | [Ucupaint](Tool_Catalog/ucupaint-blender-free.md), GPL | Встроенный Blender Texture Paint |
| CC0 PBR | [ambientCG](Tool_Catalog/ambientcg-cc0.md), [Poly Haven](Tool_Catalog/poly-haven.md) | Blender procedural maps + bake |
| Unity GLB import | [Khronos exporter](Tool_Catalog/khronos-blender-gltf-io.md) + [Unity glTFast](Tool_Catalog/unity-gltfast.md), Apache-2.0 | FBX + Unity ModelImporter |
| UI/RPG/impact/sci-fi звуки | [Kenney отдельные CC0 наборы](14_Audio/FREE_SOUND_PIPELINE.md) | Собственные записи с лицензией |

**Unity glTFast main preview 6.20.1-pre.1 не считать production stable**; выбрать Registry stable package и проверить Shader Graph variants при Player Build. [Полное руководство](18_Blender_Integration/FREE_GLTF_RIG_UV_PRODUCTION.md).


## Бесплатные источники готовой анимации/леса/музыки (09.10.2026)
| Для чего | Выбрать сначала | Сильная сторона / caveat |
|---|---|---|
| Массовая трава и кустарники | [Geometry Nodes](Tool_Catalog/blender-geometry-nodes-free.md) | Бесплатно встроено; instances нужно перенести в Unity корректно |
| Генерировать лес | [YGForge](Tool_Catalog/blender-lowpoly-tree-generator.md) либо [Modular Tree](Tool_Catalog/blender-modular-tree.md) | Free GPL addons; v5+ и 4.3.1+ соответственно |
| Создать LOD mesh | [Decimate](Tool_Catalog/blender-decimate-lod-free.md) | Встроенный и бесплатный, но не автоматическая гарантия качества |
| Retarget Blender 5 | [Retarget KBS](Tool_Catalog/blender-retarget-kbs.md) | GPL; presets для разных rig |
| Ретаргет без платного Rokoko Studio | [Rokoko Blender](Tool_Catalog/blender-rokoko-retarget.md) | Бесплатный retarget по официальной справке, LGPL-код |
| Липсинк | [Rhubarb NG](Tool_Catalog/rhubarb-lip-sync-ng-blender.md) | MIT, не TTS; русскую речь отдельно тестировать |
| CC0 BGM для игр | [OpenGameArt 4 выбранные пакета](14_Audio/FREE_CC0_MUSIC_COLLECTION.md) | 18 заявленных треков + 5 архивов, конкретная CC0 license на каждой странице |

[Сравнение](Comparisons/FREE_FOLIAGE_ANIMATION_MUSIC.md). **Статус DOCUMENTED.**
