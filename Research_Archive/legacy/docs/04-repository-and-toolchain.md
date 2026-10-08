# 04. Структура Unity-проекта, Git и инженерные инструменты

**Источники проверены:** 2026-10-08 · **Стадия:** технический стартовый чек-лист.

## Важно: этот GitHub-репозиторий — библиотека знаний, не игра
`spels1992/Unity` хранит статьи. Исходники конкретной игры лучше вести в отдельном игровом репозитории. `spels1992/GameLibrary` служит каталогом общих инструментов и опыта.

## Состав настоящего проекта
При создании Unity генерирует основные папки:
- `Assets/` — сцены, скрипты, спрайты, аудио, настройки ассетов.
- `Packages/manifest.json` — зависимости проекта; `Packages/packages-lock.json` — разрешённые зависимости (сохранять с проектом, если сгенерирован).
- `ProjectSettings/` — настройки версии/плеера/графики и проекта.
- `Library/` — импортированные артефакты и локальные кэши (**не коммитить**).
- `Temp/`, `Logs/`, `UserSettings/` — временные/локальные данные (**не коммитить**).
Ссылка: [Unity 6.3 default project directories](https://docs.unity.com/en-us/engine/6000.3/manual/get-started/project-configuration/default-directories).

Рекомендуемая организация **своих файлов** (не системных):
```text
Assets/
  _Game/
    Art/{Sprites,Models,Materials,Animations}
    Audio/{Music,SFX}
    Code/{Core,Gameplay,UI,Editor}
    Data/{Configs,Levels}
    Prefabs/
    Scenes/{Bootstrap,Menu,Gameplay}
    Tests/{EditMode,PlayMode}
  ThirdParty/       # только если лицензия и способ доставки требуют
Packages/
  manifest.json
  packages-lock.json
ProjectSettings/
README.md
.gitignore
.gitattributes
```
Папки с зарезервированными именами Unity (например `Editor`, `Resources`, `StreamingAssets`) должны использоваться осознанно: они влияют на сборку и импорт.

## Что коммитить
- `Assets` + соответствующие **.meta** файлы: Unity связывает ресурсы/ссылки через GUID; удаление .meta или невнимательное копирование ломает связи.
- `Packages/` + `ProjectSettings/`.
- `UserSettings/`, `Library/`, `Temp/`, `Obj/`, `Logs/`, финальные `Builds/` **обычно не коммитить**.
- Точные правила брать из актуального [GitHub Unity.gitignore](https://github.com/github/gitignore/blob/main/Unity.gitignore), а не вручную копировать список с устаревшего блога.

Пример **минимального** `.gitignore` (не исчерпывающий):
```gitignore
/[Ll]ibrary/
/[Tt]emp/
/[Oo]bj/
/[Ll]ogs/
/[Bb]uild/
/[Bb]uilds/
/[Uu]ser[Ss]ettings/
.vs/
.idea/
*.csproj
*.sln
*.slnx
```
Файлы `.meta` **не игнорировать глобальным правилом**; для игнорируемых generated assets надо согласовать соответствующие .meta.

## Git LFS и большие двоичные файлы
- Git удобен для `.cs`, YAML-сцен, prefabs, JSON/MD, плохо работает с частыми правками больших бинарных моделей/звуков/PSD.
- При необходимости подключить Git LFS на **конкретные расширения** (например `*.psd`, `*.fbx`, `*.wav`, `*.blend`), сохранять `.gitattributes` в Git.
- Проверить квоту GitHub LFS и условия тарифа прежде, чем переносить сотни гигабайт.
- Не переписывать историю Git для внедрения LFS, пока не согласован миграционный план и backup.

## Конфигурация редактора и командная работа
- Использовать текстовую сериализацию ассетов/сцен для сравнимых diffs там, где возможно.
- Изучить **SmartMerge/UnityYAMLMerge** для конфликтов YAML-сцен и префабов.
- Один изменяемый большой Scene-файл на двух разработчиков требует аккуратного слияния. Снижать конфликтность через Prefabs и additive scenes.
- Зафиксировать Editor version (Unity создаёт `ProjectSettings/ProjectVersion.txt`) и статус зависимостей; не апгрейдить все редакторы одновременно без теста.
- Разработку вести в feature branches, PR с тестами и понятными acceptance criteria.
- CI сборка должна запускать batchmode Editor только после настройки лицензирования, целевого модуля и зависимостей на runner; **не добавлять платный CI без сравнения**.

## Пакеты и .NET
- В Unity Package Manager доступны источники registry, Git, локальная папка и tarball. Сторонний Git URL только из доверенного первоисточника и по возможности с фиксированным tag/commit; наугад тянуть `main` опасно.
- Для собственного модульного кода использовать `.asmdef`, отдельные runtime/editor/tests сборки.
- Не смешивать редакторные API `UnityEditor` с кодом, который должен попадать в Player.
- Не считать версию .NET из Visual Studio автоматическим эквивалентом среды исполнения Unity; проверить профили и особенности Editor/Player.

## Репродуцируемая проверка репозитория
1. `git clone` на другой каталог/компьютер.
2. Открыть проект в **закреплённой** версии Unity Editor через Hub.
3. Дождаться импорта с нуля (без `Library/`).
4. Проверить `Console`: 0 compile errors.
5. Открыть входную сцену, запустить Play Mode.
6. Собрать target Build и запустить вне редактора.
7. Повторить при восстановлении из clean checkout — это тест «репозиторий самодостаточен».

## Проблемы, которые предотвращаем
| Ошибка | Симптом | Решение |
|---|---|---|
| Не сохранён .meta | Missing Script/Material или broken references | Вернуть .meta с правильным GUID из Git |
| Закоммичен Library | Огромный diff, платформенный шум, конфликты | Правильный .gitignore, убрать cache из индекса |
| Git пакет «плавает» | Разные сборки у людей | Фиксировать версию/commit, lock-файл |
| Облачная синхронизация рабочего каталога | Конфликты/повреждения | Локальная рабочая папка и version control |
| Одна огромная сцена | Сложные merge-конфликты | Prefab/additive сцены и ответственное редактирование |

## Источники
- [Default project directories](https://docs.unity.com/en-us/engine/6000.3/manual/get-started/project-configuration/default-directories)
- [Version control](https://docs.unity.com/en-us/engine/6000.0/manual/get-started/project-configuration/version-control)
- [Package concepts](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages/upm-concepts)
- [Package development](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/cus-pkg-lp/cus-pkg-development)
- [GitHub Unity.gitignore](https://github.com/github/gitignore/blob/main/Unity.gitignore)
- [Asset import](https://docs.unity.com/en-us/engine/6000.0/manual/assets-and-media/import-assets/importing-assets)

## Не закрыто
Выбор IDE в реальной среде; Unity SmartMerge конкретные команды; pipeline GitHub Actions с валидной бесплатной квотой и лицензией; security scan сторонних пакетов; готовый пример игрового репозитория с настоящими .meta.
