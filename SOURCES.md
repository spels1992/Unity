# SOURCES.md — реестр источников исследования Unity

**Исходный аудит:** 2026-10-08. Это **реестр проверенных страниц**, а не зеркальная копия документации. При изучении конкретного API версия пакета/движка важнее даты посещения. Перечень расширяется после каждого завершённого исследовательского блока.

## Легенда
- **A** — официальный первоисточник или оригинальная документация владельца продукта/пакета;
- **B** — оригинальный публичный код/образец от издателя или GitHub-репозиторий сторонней библиотеки;
- **C** — вторичный/зеркальный ресурс; ссылку использовать для ориентирования и отдельно подтверждать оригиналом.
- «Изучен» = источник просмотрен для текущих глав; **не** значит полный аудит каждого документа, релиза или доступного API.

## Unity: редактор, версии, лицензии
| ID | Источник | Класс | Для какой главы/проверенный факт |
|---|---|---|---|
| U01 | [Unity Docs](https://docs.unity.com/) | A | Версионированная входная точка в документацию |
| U02 | [Unity Learn](https://learn.unity.com/) | A | Уроки и пошаговые учебные проекты |
| U03 | [Install Unity (6.3)](https://docs.unity.com/en-us/engine/6000.3/manual/get-started/install-and-upgrade/getting-started-installing-unity) | A | Unity Hub является основным способом установки |
| U04 | [Unity Hub: Create project](https://docs.unity.com/en-us/hub/project-create) | A | Создание проекта, шаблон, Editor version, локальный путь, GitHub опция |
| U05 | [Unity 6.6 release](https://unity.com/releases/editor/whats-new/6000.6.0f1) | A | 6000.6.0f1: 31.08.2026 |
| U06 | [Unity 6.6 official announcement](https://discussions.unity.com/t/unity-6-6-is-now-available/1735357) | A | Unity 6.6 — Supported release (объявление 01.09.2026) |
| U07 | [Unity 6.3 LTS upgrade](https://docs.unity.com/en-us/engine/6000.6/manual/upgrade-guides/upgrade-guide-unity63) | A | Версия 6000.3 обозначена LTS |
| U08 | [Upgrade to Unity 6.6](https://docs.unity.com/en-us/engine/6000.6/manual/upgrade-guides/upgrade-guide-unity66) | A | 6.5→6.6, CineMachine 3 core/migration |
| U09 | [Unity Personal](https://unity.com/products/unity-personal) | A | Бесплатная редакция, финансовая eligibility $200k (детали в правилах) |
| U10 | [Plans & Pricing](https://unity.com/products) | A | Условия Personal/Pro/Enterprise; цены динамичны |
| U11 | [Licensing compliance](https://unity.com/pages/license-compliance) | A | Финансовые пороги, ограничения, условия лицензии |
| U12 | [Pricing updates](https://unity.com/products/pricing-updates) | A | Изменения тарифа и 2026 цены в USD |
| U13 | [Unity 6 Resources](https://unity.com/campaign/unity-6-resources) | A | Unity образцы проектов, архитектурные практики |

## Идея, предпроизводство и UX
| ID | Источник | Класс | Назначение |
|---|---|---|---|
| D01 | [Unity Learn: Prototyping](https://learn.unity.com/course/design-and-publish-your-original-game-unity-usc-games-unlocked/unit/prototyping) | A | Прототипирование ради проверки fun + asset planning |
| D02 | [Unity Learn: Milestones](https://learn.unity.com/course/design-and-publish-your-original-game-unity-usc-games-unlocked/unit/milestones) | A | Контрольные точки, vertical slice |
| D03 | [Unity Learn: Set up project](https://learn.unity.com/tutorial/66f53a14edbc2a0e75d4fe90) | A | Подготовка проекта, импорт, планирование работы, vertical slice |
| D04 | [Unity Game Designer Playbook](https://unity.com/resources/game-designer-playbook) | A | Дизайнерские приёмы, прототипы |
| D05 | [Introduction to level design](https://unity.com/resources/introduction-to-level-design-in-game-development-and-in-unity) | A | Level design, блокинг, проектирование уровней |

## Архитектура, скрипты, Git, пакеты
| ID | Источник | Класс | Назначение |
|---|---|---|---|
| E01 | [Default project directories 6.3](https://docs.unity.com/en-us/engine/6000.3/manual/get-started/project-configuration/default-directories) | A | Assets/Packages/ProjectSettings/Library/Temp/UserSettings и запрет cloud-sync как рабочего каталога |
| E02 | [Version control](https://docs.unity.com/en-us/engine/6000.0/manual/get-started/project-configuration/version-control) | A | Интеграции VCS, SmartMerge |
| E03 | [GitHub Unity.gitignore](https://github.com/github/gitignore/blob/main/Unity.gitignore) | B | Актуальный шаблон исключений кэша из Git |
| E04 | [Package source types](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages/upm-concepts) | A | Registry/Git/local/tarball и пакеты |
| E05 | [Manage Asset Store packages](https://docs.unity.com/en-us/engine/6000.3/manual/assets-and-media/asset-store/downloads/packages) | A | Различие .unitypackage и UPM |
| E06 | [Find packages](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/upm-ui-window/upm-ui-find) | A | Search/UI каталоги |
| E07 | [Package development](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/cus-pkg-lp/cus-pkg-development) | A | Структура собственного UPM пакета и его лицензирование |
| E08 | [Code reload / serialization](https://docs.unity.com/en-us/engine/6000.3/manual/programming-environment/code-reload-serialization) | A | Сохранение полей при сборке и перезагрузке |
| E09 | [Serialization rules](https://docs.unity.com/en-us/engine/6000.3/manual/programming-environment/code-reload-serialization/script-serialization/rules) | A | Какие C# поля/типы сериализуются |
| E10 | [Prefabs](https://docs.unity.com/en-us/engine/6000.0/manual/working-with-gameobjects/prefabs) | A | Reusable GameObjects |
| E11 | [Create prefabs](https://docs.unity.com/en-us/engine/6000.0/manual/working-with-gameobjects/prefabs/creating) | A | Префаб из объекта в Hierarchy |
| E12 | [Prefab instance override](https://docs.unity.com/en-us/engine/6000.3/manual/working-with-gameobjects/prefabs/override) | A | Переопределения в экземплярах |
| E13 | [Event execution order](https://docs.unity.com/en-us/engine/6000.3/manual/scripting/managing-update-order/execution-order) | A | Lifecycle и негарантированный порядок между объектами |
| E14 | [Programming best practices](https://docs.unity.com/en-us/engine/6000.3/manual/scripting/get-started/programming-best-practices) | A | Потоки и Unity API |
| E15 | [Awaitable](https://docs.unity.com/en-us/engine/6000.3/manual/scripting/programming-distribute-work-threads/async-await-support) | A | Async/await и Unity Awaitable |
| E16 | [Assembly definitions](https://docs.unity.com/en-us/engine/6000.0/manual/programming-environment/script-compilation/assembly-definition-files) | A | Разделение кода на assemblies |
| E17 | [asmdef file format](https://docs.unity.com/en-us/engine/6000.3/manual/programming-environment/script-compilation/assembly-definition-files/file-format) | A | JSON-поля, references |
| E18 | [asmdef inspector](https://docs.unity.com/en-us/engine/6000.3/manual/programming-environment/script-compilation/assembly-definition-files/class-assembly-definition-importer) | A | GUID reference, ограничения платформ |
| E19 | [Script compilation](https://docs.unity.com/en-us/engine/6000.3/manual/programming-environment/script-compilation) | A | Компиляция и организация C# скриптов |
| E20 | [Code optimization](https://docs.unity.com/en-us/engine/6000.3/manual/scripting/optimization) | A | Актуальные задачи оптимизации |
| E21 | [Asset import](https://docs.unity.com/en-us/engine/6000.0/manual/assets-and-media/import-assets/importing-assets) | A | Файлы в Assets и import workflow |

## Конкретные пакеты, библиотеки и примеры
| ID | Источник | Класс | Проверка |
|---|---|---|---|
| P01 | [Unity Input System 6.3](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-inputsystem) | A | В каталоге 6.3 есть 1.20.0/1.20.1; фактическая совместимость нашего проекта не тестировалась |
| P02 | [Unity DOTS Samples](https://github.com/Unity-Technologies/EntityComponentSystemSamples) | B | Официальный sample: Unity 6.2 + пакеты 1.4, не переносить слепо на 6.3 |
| P03 | [Cysharp UniTask original](https://github.com/Cysharp/UniTask) | B | Сторонняя async-библиотека, UPM Git install; лицензию/проектные тесты добавить |
| P04 | [Needle UPM mirror](https://github.com/needle-mirror) | C | Только справочное зеркало пакетов, явно не аффилировано с Unity Technologies |

## План верификации источников
- Переоценивать **финансовые условия** перед распространением/монетизацией и **версии пакетов** перед импортом.
- Для изучения любого пакета добавлять `LICENSE`, URL upstream, changelog, совместимость Editor, проверку на целевой платформе и build log.
- Для каждой изученной темы прикладывать ссылки на источники внутри главы, не ограничиваться этим реестром.
- Отдельным списком записывать проверенные противоречия, устаревшие советы и неработающие примеры.

**Оговорка:** конкретные live-тесты Unity на машине в этом исследовательском сеансе не производились.
