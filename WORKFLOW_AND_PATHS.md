# Единый производственный процесс Farm / Blender / Unity (Windows, обновлено 2026-10-13)

**Один и тот же документ** в репозиториях `spels1992/Farm`, `spels1992/Unity`, `spels1992/Blender`. Канонический стандарт хранения — файл `LOCAL_ASSET_PATHS.md` (одинаковый во всех трёх). Уточнения для конкретного проекта не могут отменять этот стандарт.

## Плагины ChatGPT: точные названия и назначения

- **Windows MCP** и **WinApp MCP** — два **основных** инструмента управления компьютером. Windows MCP: процессы, PowerShell, файлы, туннели, диагностика. WinApp MCP: окна, UI Automation, запуск через обычный пользовательский интерфейс, управление приложениями. Если один недоступен — проверять/восстанавливать через другой.
- **Blender MCP** (локальный Overtli-Blender) — **основной и обязательный** инструмент действий в Blender: сцены, геометрия, материалы, UV, риг/анимация, экспорт. При сбое Blender MCP **Windows MCP или WinApp MCP** восстанавливают Blender, его аддон и MCP-туннель, после чего проверяется реальная команда Blender MCP.
- **Unity MCP** (установлен **AnkleBreaker Unity MCP Server**, плагин ChatGPT «Unity MCP Server») — **основной инструмент** управления Unity Editor, сценами, объектами, импортом и тестами. При сбое Unity MCP **Windows MCP или WinApp MCP** восстанавливают Unity Hub/Editor, лицензирование, сервер и туннель ABS MCP Tunnel. Затем проверить реальный `unity_editor_ping`. Unity Hub/Editor/лицензирование запускать с одинаковыми обычными правами, не через повышенный PowerShell.
- **Desktop Commander** (плагин также может отображаться как **Remote Desktop Commander**) — **строго ТОЛЬКО** для восстановления **Windows MCP и WinApp MCP**, включая их процессы и туннели. **Запрещено** применять его для Unity MCP, Blender MCP, моделирования, разработки, GitHub, обычных операций с файлами, SF3D и любых иных задач. Даже если оба специализированных MCP неисправны, Desktop Commander не превращается в общий инструмент: он чинит лишь Windows MCP/WinApp MCP.

Если Blender MCP в конкретном чате не предоставлен, но доступен Windows MCP, разрешён локальный резерв: `D:\Blender\Tools\Tunnel\Blender-MCP-Fallback.py --command get_scene_info` через Python `D:\Blender\Tools\Overtli-Blender\.venv\Scripts\python.exe`. Сам Blender может автоматически открыться по MCP-запросу; не требовать ручного запуска без проверки. Подробности — `spels1992/Farm/docs/BLENDER_MCP_AUTO_RECOVERY.md`. Отсутствие инструмента в конкретном чате не означает его отсутствия на ПК.

## Бесплатный конвейер нового/перерабатываемого 3D-ассета — 3D Craft

**Обязательно сначала загрузить актуальный скилл [3D Craft](https://chatgpt.com/plugins/plugins_6acdc74c86888191b2101b657a2e8f8d) (`3d-craft`), прочитать [docs/3D_CRAFT.md](docs/3D_CRAFT.md), [AGENTS.md](AGENTS.md) и локальные пути.** Правило действует во всех трёх репозиториях Farm, Blender, Unity, включая детали и аксессуары. Не подменять его несвязанным стеком.

2. **Локальный Stable Fast 3D:** Windows MCP запускает `D:\Program Files\StableFast3D\Run-SF3D.cmd` с отдельным PNG; подтверждать получение корректного GLB, логи/exit code; один GPU-прогон за раз. Установку проверять быстро, не заменять SF3D на Rodin.
3. **Blender MCP:** сравнить кандидаты частей рядом с основной моделью, проверить геометрию, выбрать и временно примерить. Сохранять исходник и backup, корректировать только плохую часть, не лепить с нуля качественную базу. Провести обязательный QA с 42 ракурсов после каждой принятой правки; повторять до отсутствия критических и серьёзных ошибок.
4. **Unity MCP:** при игровом экспорте проверить импорт, масштаб, PBR/UV, rig/анимации, LOD, коллизии, арт-гейты, EditMode/PlayMode и фактические FPS/сцену по задаче. Отсутствующий тест = `NOT_TESTED`, не PASS.
5. **Сохранение/агенты:** краткий отчёт об этапах без лишних команд, backup + версии + проверенный сохранённый файл. Для независимых аналитических задач подключать субагентов с той же моделью/мощностью, если поддерживается; основной .blend пишет один агент. Коммитировать в каноническую рабочую копию по правилам проекта; публикацию на GitHub проводить только в явно разрешённом этапе. Не грузить гигабайтные модели, секреты и кэши.

При отсутствии 3D Craft в текущей среде **сообщать `BLOCKED` и запрашивать подключение**, не утверждать, что скилл использован. Это не отменяет существующую политику бесплатности, лицензий и безопасного локального хранения.

## Единые абсолютные Windows-пути

| Объект | Каноническое размещение |
|---|---|
| Stable Fast 3D (программа) | `D:\Program Files\StableFast3D`, канонический запуск `Run-SF3D.cmd`, исходники `source\run.py` |
| SF3D: черновые mesh.glb/preview | `D:\Blender\Stable 3D\3D заготовки\<Имя>` |
| SF3D старый `outputs` | `D:\Program Files\StableFast3D\outputs` — проверенный **junction** на каноническую папку выше, не второй склад |
| Blender: утверждённые .blend/FBX/GLB | `D:\Blender\Models\<ИмяМодели>` |
| Blender: общие инструменты/MCP | `D:\Blender\Tools` |
| Unity: общие инструменты/MCP | `D:\Unity\Tools` |
| Farm: единый корень | `D:\Unity\Projects\Farm` |
| Farm: Git-источники | `D:\Unity\Projects\Farm\Source` |
| Farm: Unity Editor-проект | `D:\Unity\Projects\Farm\Source\world\v2\UnityProject` |
| Farm: исходные игровые ассеты | `D:\Unity\Projects\Farm\Source\world\v2\UnityProject\Assets` по сущностям |
| Farm: тестовые проекты, сборки, отчёты | `D:\Unity\Projects\Farm\QA`, `Builds`, `Reports`, `Experiments` (создавать при необходимости внутри Farm) |
| Farm: запускатель тестового Windows EXE | `D:\Unity\Projects\Farm\QA\Tools\Invoke-FarmOfflineQA.ps1` |
| Unity Hub и Editor | `D:\Program Files\Unity Hub` и `D:\Program Files\Unity\Hub\Editor` |
| Unity: скачивания и пользовательские данные | `D:\Program Files\Unity\Downloads`, `D:\Unity\HubData`, `D:\Unity\UserData` |

**Запрещено создавать новые Farm-проекты/QA-сборки в `D:\FarmDev`, `D:\Unity\QA`, `D:\CodexWork` или прямо в корне D:.** Уже существующие старые каталоги считать legacy: не удалять и не переносить до сопоставления Git, уникальных файлов и зависимостей. Не изменять утверждённые модели без отдельного version/checkpoint.

## Что осталось на C: после переноса

В ходе проверки обнаружены работающие Python 3.13/3.14 и Desktop Commander на C:, а также legacy junction Blender 5.2 с C: на D:. Это **не причина менять канонические выходные пути**. Не переносить Python и Desktop Commander автоматически: сначала обновить все зависимости Планировщика, проверить туннели/автозапуск и только потом мигрировать с безопасным откатом. Совместимые пользовательские AppData junction у Unity остаются допустимыми.

## Контроль перед началом работы / после переезда

**Проверка миграции в один запуск:** через Windows MCP запустить `D:\Monitoring\MigrationAudit\Test-FarmPathMigration.ps1` (проверенная локальная копия [Farm/NightRun/tools/windows/Test-FarmPathMigration.ps1](https://github.com/spels1992/Farm/blob/main/NightRun/tools/windows/Test-FarmPathMigration.ps1)). Скрипт работает только на чтение, сохраняет JSON в `D:\Monitoring\MigrationAudit`, отмечает `PASS/FAIL/WARN`; любой `FAIL` выяснять до новых переносов или создания копий. Не использовать его для автоматической публикации Git-коммитов.



Сверить GitHub main, локальный HEAD/ветку, `git status` (включая несохранённое и неопубликованное), реальный путь файла, output flags/junction и планировщик. Если документация и реально используемый путь расходятся — сначала исправить расхождение и проверить инструмент, **не плодить новые копии/директории**. Не считать успешным GitHub-save одно лишь наличие локального коммита; проверять точный SHA опубликованной ветки.
