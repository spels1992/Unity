# TOOL_CATALOG — канонические карточки

**Одна библиотека = одна основная карточка.** Из жанров/систем/стеков используются относительные ссылки. Поиск начинается с крупной готовой основы.

| Инструмент | Категория | Цена/лицензия | Проверка | Карточка |
|---|---|---|---|---|
| Unity FPS Sample | Готовая игра, FPS | Unity Companion License, legacy | README+license; не тестировалось | [FPSSample](fps-sample-legacy.md) |
| Unity DOTS Samples | ECS/физика/сеть | лицензия уточняется | README; не тестировалось | [DOTS Samples](unity-dots-samples.md) |
| Mirror | Multiplayer | MIT / бесплатный OSS | license+repo; не тестировалось | [Mirror](mirror-networking.md) |
| UniTask | Async/core | MIT / бесплатный OSS | license+repo; не тестировалось | [UniTask](unitask.md) |
| FishNet | Multiplayer | custom FishNet license, НЕ MIT; прочитана | README; не тестировалось | [FishNet](fishnet-networking.md) |
| Cinemachine | Camera | official Unity package, terms проверить | Unity 6.3 docs | [Cinemachine](cinemachine.md) |
| AI Navigation | Navigation | official Unity package, terms проверить | Unity 6.3 docs | [AI Navigation](ai-navigation.md) |
| Unity First Person + Third Person Controller | Starter kits | FREE, Non standard EULA | Asset Store: 2.0.1, URP 6000.3; не тестировалось | [Controllers](official-starter-kits.md) |
| Unity 2D Game Kit | 2D sample project | FREE, Asset Store standard EULA/Extension Asset | v5.0, URP 6000.3; не тестировалось | [2D Game Kit](2d-game-kit.md) |
| Input System | Ввод | Unity package | 1.20.1 Unity 6.3 docs | [Input System](input-system.md) |
| FPS Microgame (legacy) | FPS starter, недоступен новым пользователям | deprecated | Asset Store directly says deprecated | [FPS Microgame](fps-microgame-deprecated.md) |
| Unity Tilemap Extras | 2D level tools | условия проверить | подтверждён переход с 2d-extras | [Tilemap Extras](tilemap-extras.md) |

## Фильтры
- **Лицензия MIT:** Mirror, UniTask (подтверждено LICENSE upstream).
- **Бесплатные официальные образцы:** FPS Microgame / Starter Assets — условия скачивания/применения уточнить.
- **Сетевые альтернативы:** Mirror, FishNet (не смешивать без явной архитектуры).
- **Старое/legacy:** Unity FPS Sample (старое, огромный Git LFS проект), 2d-extras Git.
- **Требует live-теста:** **все** карточки первого прохода.

**Критично:** Unity FPS Microgame и старый FirstPerson пакет DEPRECATED. Не ориентироваться на старую страничку Unity 6 Resources как единственный источник доступности; открывать сам Asset Store.

| CoplayDev MCP for Unity | AI/Editor MCP | MIT | Unity Authorized Agentic Access НЕ подтверждён | [CoplayDev](coplaydev-unity-mcp.md) |
| CoderGamester MCP Unity | AI/Editor MCP | MIT | Unity Authorized Agentic Access НЕ подтверждён | [CoderGamester](codergamester-mcp-unity.md) |

[Важные условия подключения MCP](../19_AI_Automation/UNITY_MCP_AND_TERMS.md).

## Бесплатные библиотеки 2D/3D ассетов (проверено 2026-10-08)
| Решение | Назначение | Бесплатный объём | Карточка |
|---|---|---|---|
| Poly Haven | Библиотека 3D моделей, PBR-текстур, HDRI | Отдельные ассеты бесплатны без paywall и регистрации. Подписка/Vault, массовые скачивания и нек | [Открыть](poly-haven.md) |
| Kenney — бесплатные отдельные игровые наборы | 2D/3D UI, иконки, тайлы, анимации, музыка | Отдельные наборы бесплатно через «Continue without donating». **All-in-1 bundle на itch.io — пл | [Открыть](kenney-free-assets.md) |
| Kenney New Platformer Pack | Полный набор 2D спрайтов и тайлов для платформера | Бесплатно (donation optional); не переходить на платный All-in-1 bundle. | [Открыть](kenney-new-platformer-pack.md) |
| Kenney Platformer Kit (3D) | Комплексный 3D тематический набор моделей | Бесплатно отдельно, платный Kenney All-in-1 не нужен. | [Открыть](kenney-platformer-kit-3d.md) |
| Quaternius — бесплатные Standard ассеты | CC0 low-poly 3D персонажи, окружение, анимации | **Standard/Free часть обычно 60–70% моделей**; расширенная Source version, Blend и готовые Unit | [Открыть](quaternius-free-assets.md) |
| Quaternius Universal Base Characters | Набор humanoid 3D базовых персонажей | Free Standard лишь часть содержимого; Source с полными assets, готовым Unity проектом и .blend  | [Открыть](quaternius-universal-base-characters.md) |
| Quaternius Universal Animation Library | Библиотека анимаций humanoid | Free часть доступна; Source/.blend и готовые engine-проекты относятся к платной версии; полный  | [Открыть](quaternius-universal-animation-library.md) |
| Quaternius Modular Sci-Fi MegaKit | Модульное 3D окружение sci-fi | Только Standard бесплатен; Source со всеми Unity/Blender-сценами, collision и shaders требует о | [Открыть](quaternius-modular-sci-fi-megakit.md) |

**Критично:** отдельные пакеты Kenney бесплатны, но All-in-1 bundle платный. Quaternius Standard частично бесплатен, Source version с Unity/Blender projects — платная. Не приписывать бесплатной версии функции Source.

## Готовые полноценные проекты и крупные подсистемы
| Проект | Тип | Версия/лицензия | Карточка |
|---|---|---|---|
| Unity Open Project #1 — Chop Chop | Complete project / subsystem | Unity 2020.3 LTS из README, Unity 6 не проверена; Apache-2.0 root LICENSE | [chop-chop-open-project-1](chop-chop-open-project-1.md) |
| Unity Boat Attack | Complete project / subsystem | README указывает release/2019.3 и Unity 2019.3f5, другие branch проверять по ProjectVersion.txt; Unity Companion License (проверено LICENSE.md) | [boat-attack-urp-demo](boat-attack-urp-demo.md) |
| Unity Boat Attack Water | Complete project / subsystem | Unity 6 совместимость в README не подтверждена; версию пакета смотреть в package.json; Unity Companion License по LICENSE.md upstream | [boat-attack-water](boat-attack-water.md) |
[Сравнение](../Comparisons/COMPLETE_FREE_PROJECTS.md).


## Готовые бесплатные Unity 6 и кросс-версийные игровые системы (08.10.2026)
| Система | Назначение | Подтверждение бесплатности | Unity | Карточка |
|---|---|---|---|---|
| OpenEmpires | RTS целая игра | MIT; Editor версия README ≠ ProjectVersion | 6000.5.9f1 в ProjectVersion | [Основная](open-empires-rts.md) |
| Moonforge RPG Engine | RPG core: quest/combat/loot/save | MIT, бесплатный UPM | UPM Unity 2022.3+ | [Основная](moonforge-rpg-engine.md) |
| Yarn Spinner for Unity | Диалоги/визуальные новеллы | MIT Git бесплатно; Asset Store/Itch платные | 3.2.8, Unity 2022.3+ | [Основная](yarn-spinner-unity.md) |
| Ink Unity Integration | Нарратив и диалоги | MIT Git бесплатно | 2.0.0, Unity 2022.3+ | [Основная](ink-unity-integration.md) |
| OpenKCC | Kinematic controller | MIT; upstream last push 2023 | package 1.5.0, Unity 2019.4+ (6 не тест) | [Основная](openkcc-controller.md) |
| EZ Room Generator | 3D генератор лабиринтов | MIT | 0.1.0, Unity 6000+ | [Основная](ezroomgenerator.md) |
| Edgar Free Core | 2D графовый dungeon generator | MIT free core; PRO платный | 2.1.0, минимальная Unity 2019.3 | [Основная](edgar-unity-free.md) |
| Game Lattice | Большой RPG+NPC AI framework | Apache-2.0; UPM 0.0.0-dev | Unity 2021.2+; пример 6000.4 | [Основная](game-lattice-rpg.md) |
| Game Lattice Playground | Готовая учебная RPG песочница | Apache-2.0 | Unity 6000.4.11f1 | [Основная](game-lattice-unity-playground.md) |
| Unity Modular Inventory | Инвентарь drag/drop | MIT, assets Kenney separately | Unity 6000.0.50f1 | [Основная](unity-modular-inventory.md) |
| Softlight | 2D top-down RPG prototype | MIT, incomplete | Unity 6000.3.7f1 | [Основная](softlight-unity6-rpg.md) |
| Unity FPS Controller | Базовый FPS контроллер | MIT, старый Input Manager | Unity 6, exact Editor неизвестна | [Основная](simple-fps-controller-unity6-mit.md) |

[Сравнение комплексных бесплатных фреймворков](../Comparisons/FREE_FRAMEWORKS_2026.md) · [Отклонённые/неподтверждённые лицензии](../Research_Archive/REJECTED_OR_BLOCKED_LICENSE.md).


## CC0 графика для dungeon
| Набор | Категория | Лицензия | Статус | Карточка |
|---|---|---|---|---|
| 0x72 DungeonTileset II | 2D tilemap / sprites | Авторский CC0 | По первоисточнику; импорт не проверен | [Открыть](dungeontileset-ii-0x72.md) |

## Survival / Racing / Building / FPS — бесплатные исходники (2026-10-08)
| Название | Для чего | Правовые ограничения | Версия Unity | Карточка |
|---|---|---|---|---|
| Project Wanderer | Survival, gathering, crafting, save | MIT code + Unity Companion StarterAssets | 6000.3.13f1 | [Открыть](project-wanderer-survival.md) |
| Grid Building System | Construction, multi-floor A*, save | MIT code; assets отдельно | 6000.3.16f1 | [Открыть](grid-building-system.md) |
| GeoJSON City Builder | Генерация города из GeoJSON | MIT root; dependency BLOCKED | 0.4.3 / 2019.1+ | [Открыть](geojson-city-builder.md) |
| PolyRace | Sci-fi hover racing game | MIT root; third-party restrictions | 2020.3.25f1 | [Открыть](polyrace-legacy.md) |
| Street Racing | Тайм-триал / WebGL | MIT root; Asset Store EULA | 2020.3.25f1 | [Открыть](street-racing-free-demo.md) |
| ArcadeVehiclePhysics | Arcade car physics | MIT scripts; Sketchfab model отдельно | 2018.4.5f1 | [Открыть](arcade-vehicle-physics.md) |
| TLabVehiclePhysics | Pacejka/LUT vehicle physics | MIT root; git submodules BLOCKED | 2022.3.19f1 | [Открыть](tlab-vehicle-physics.md) |
| Grid-Based Crafting System | Рецепты, UI crafting | MIT source, store unknown | 2022.3.9f1 | [Открыть](grid-based-crafting-system.md) |
| Armour Multiplayer-FPS | Networked FPS reference | MIT root; Photon/Asset Store restrictions | 2022.3.55f1 | [Открыть](armour-multiplayer-fps.md) |

[Сравнение и выбор](../Comparisons/VEHICLES_SURVIVAL_BUILDING_FPS_2026.md) · [Как работать и искать правильно](../01_Game_Development_Pipeline/RESEARCH_METHOD_ZERO_COST.md).


## Blender ↔ Unity glTF, UV, Rigging, PBR — бесплатные инструменты
| Решение | Назначение | Лицензия | Примечание | Карточка |
|---|---|---|---|---|
| Rigify | Автоматизированный rig | GPL в Blender | Deform skeleton/animation bake для Unity | [Открыть](blender-rigify-free.md) |
| Khronos glTF Blender I/O | Импорт/экспорт GLB | Apache-2.0 | Blender bundled addon | [Открыть](khronos-blender-gltf-io.md) |
| Unity glTFast | Editor/runtime GLB import/export | Apache-2.0 | Не ставить preview в production без теста | [Открыть](unity-gltfast.md) |
| Ucupaint | Послойная текстурная живопись | GPLv3+ | Blender min 4.2; bake для Unity | [Открыть](ucupaint-blender-free.md) |
| TexTools | UV/texel density/texture baking | GPLv3+ | Blender 5.x не проверен | [Открыть](textools-blender-free.md) |
| ambientCG | PBR CC0 textures | CC0 assets | Не перепутать texture channel conventions | [Открыть](ambientcg-cc0.md) |

## Kenney — отдельные бесплатные CC0 аудионаборы
| Набор | Файлы | Готовая тематика | Карточка |
|---|---:|---|---|
| UI Audio | 50 | UI click/button/switch | [Открыть](kenney-ui-audio.md) |
| Impact Sounds | 130 | Столкновения/удары | [Открыть](kenney-impact-sounds.md) |
| RPG Audio | 50 | RPG шаги/экипировка/эффекты | [Открыть](kenney-rpg-audio.md) |
| Sci-fi Sounds | 70 | Космические двигатели/лазеры | [Открыть](kenney-sci-fi-sounds.md) |
| Music Jingles | 85 | Короткие победные музыкальные темы | [Открыть](kenney-music-jingles.md) |

**Всего: 385 аудиофайлов по официальным страницам, все пять наборов CC0.** Это не равно полной готовой аудиосистеме. [Аудиопайплайн](../14_Audio/FREE_SOUND_PIPELINE.md) и [3D-пайплайн](../18_Blender_Integration/FREE_GLTF_RIG_UV_PRODUCTION.md).
