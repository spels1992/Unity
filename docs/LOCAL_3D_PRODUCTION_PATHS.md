# Локальный 3D-конвейер: референс → модель → скелет → анимации → Unity

**Обязательный справочник для Farm, Blender и Unity.** Проверено на пользовательском Windows-ПК 13.10.2026 через Windows MCP. Пути абсолютные, Windows; на другой машине проверять существование, не предполагать, что диск D: смонтирован. **Codex Cloud не получает локальный доступ автоматически**: для работы с ПК нужны реально подключённые Windows MCP/WinApp MCP или другое разрешённое средство. Упоминание инструмента в SKILL.md не создаёт подключение.

## 1. Где установлены программы и где хранятся результаты

| Этап | Установка / точка запуска | Данные / результаты |
|---|---|---|
| Hunyuan3D-2GP / 2mv Turbo | D:\Program Files\Hunyuan3D-2GP; Python .venv; веса models-cache и models-local; локальный MCP D:\AI-MCP\hunyuan-local\hunyuan_mcp.py | D:\AI-MCP\hunyuan-local\jobs\<job_id>\result.glb; четыре PNG внутри папки ассета |
| Blender 5.2 | `D:\Program Files\Blender Foundation\Blender 5.2\blender.exe` | `D:\Blender\Models\<Asset>\`; общие инструменты `D:\Blender\Tools\`; временное `D:\Blender\Temp\` |
| SkinTokens CPU | `D:\Program Files\SkinTokens\runtime\bin\skintokens-cli.exe`; веса `D:\Program Files\SkinTokens\models\SkinTokens-GGUF\F16` | Риги и отчёты в подпапке соответствующей модели, **не** внутри каталога программы |
| Bonix (скилл) | ChatGPT-плагин Bonix; локальная **устаревшая копия** `D:\Blender\Tools\RigMotion\` может содержать старое имя | Скилл координирует SkinTokens/Blender/Unity, сам не является отдельным исполняемым риггером |
| Unity Editor | `D:\Program Files\Unity\Hub\Editor\6000.3.25f1\Editor\Unity.exe` | `D:\Unity\Projects\Farm\`; Git/workspace `D:\Unity\Projects\Farm\Source\`; QA `D:\Unity\Projects\Farm\QA\` |
| Blender MCP | `D:\Blender\Tools\Overtli-Blender\`, `D:\Blender\Tools\Start-BlenderMcp.py` | Управление сценой при фактической доступности MCP |
| Unity MCP | `D:\Unity\Tools\AnkleBreaker\` | Управление редактором при фактической доступности MCP |

**Не использовать** UniRig/ComfyUI (НЕ ИСПОЛЬЗОВАТЬ) как обязательную зависимость: ComfyUI (НЕ ИСПОЛЬЗОВАТЬ) — опциональный этап подготовки изображения; UniRig не входит в утверждённый конвейер. Не скачивать и не переустанавливать программы без диагностики. Существование путей проверено, но не означает, что все процессы запущены или что выполнен сквозной тест генерации.

## 2. Полная производственная цепочка

1. **Preflight:** прочитать `AGENTS.md`, `PROJECT_INSTRUCTIONS.md`, проектные ограничения и этот документ; проверить `Test-Path` для программ, весов и папок. Проверить реальные доступные инструменты, место на диске, свободную память и рабочую копию. Не трогать чужие staged/unstaged/untracked файлы и не удалять ассеты.
2. **Референс:** один цельный проверенный лист с четырьмя ортографическими видами (перед, спина, левый и правый профили) и согласованной асимметрией; затем четыре отдельные PNG front/back/left/right.
3. **3D Craft — подготовка:** один общий четырёхвидовой sheet, распознавание реальных сторон, четыре crop PNG без растягивания фигуры; при одиночном фото сначала создать один общий лист.
4. **Hunyuan3D-2GP:** через локальный stdio MCP hunyuan3dLocal передать front/back/left/right, дождаться GLB в D:\AI-MCP\hunyuan-local\jobs\<job_id>\result.glb; текстуры отдельно в Blender.
5. **Blender — сборка и локальный ремонт:** импортировать GLB, сравнить с каноническими видами, соединить/подогнать детали, исправить швы, сетку, UV, материалы, ориентацию и масштаб. **Не заменять исходную хорошую модель примитивами** и не изменять узнаваемый силуэт. Работать на копии; сохранять `.blend` и экспорты в `D:\Blender\Models\<Asset>\`.
6. **Гейт качества геометрии:** проверка 42 ракурсов, силуэта, анатомии, нормалей, UV, текстур, симметрии там, где требуется, целостности и пропорций; скриншоты/рендеры и журнал дефектов. Пока модель не принята, **не переходить к скелету**.
7. **Bonix — скелет и skinning:** классифицировать модель (человек, четвероногое, птица, монстр, механика). Для подходящей органики использовать **SkinTokens на CPU**; для механики — иерархию жёстких частей в Blender. Проверить кости, суставы, веса, деформации, хвосты, дополнительные конечности. Исходную геометрию не менять.
8. **Bonix — анимации:** составить перечень реально нужных игровых движений (idle, ходьба/бег, атака, реакция, смерть и др. по роли); использовать лицензируемые исходные клипы/ретаргетинг либо создавать в Blender. Раздельные Actions/NLA, корректные loop, root motion, FPS, контакты с землёй, переходы и физика движений.
9. **Анимационный QA:** проверять позы, деформации, проникновения, проскальзывание ног, loop seams, root motion, 42 ракурса и ключевые фазы; исправлять дефекты и повторять. Не считать созданный клип проверенным без фактического воспроизведения.
10. **Unity:** экспортировать пригодный FBX/GLB с материалами, skeleton и клипами; импортировать в правильный Unity-проект; проверить Generic/Humanoid, Avatar, Animator, Blend Trees, переходы, масштаб, материалы, производительность и тест в редакторе/сборке. **Для Farm** учитывать, что игра использует 2D-изометрию: 3D может служить источником рендеров/спрайтов; импортировать полноценный 3D-ассет в игру только если это действительно требуется архитектурой.
11. **Сдача:** сохранить финальные `.blend`, экспорты, превью, план клипов и результаты QA локально; записать пути и PASS/FAIL. Закрыть только собственные временные окна/процессы, не закрывать пользовательские окна и MCP-туннели.

## 3. Команды проверки (read-only)

```powershell
$paths = @(
 'D:\Program Files\ComfyUI (НЕ ИСПОЛЬЗОВАТЬ)\ComfyUI (НЕ ИСПОЛЬЗОВАТЬ)_windows_portable\run_nvidia_gpu.bat',
 'D:\AI-MCP\hunyuan-local\hunyuan_mcp.py',
 'D:\Program Files\Blender Foundation\Blender 5.2\blender.exe',
 'D:\Program Files\SkinTokens\runtime\bin\skintokens-cli.exe',
 'D:\Program Files\SkinTokens\models\SkinTokens-GGUF\F16',
 'D:\Program Files\Unity\Hub\Editor\6000.3.25f1\Editor\Unity.exe',
 'D:\Blender\Models', 'D:\Unity\Projects\Farm\Source'
)
$paths | ForEach-Object { '{0} {1}' -f (Test-Path -LiteralPath $_), $_ }
```

SkinTokens CPU (после подтверждения путей и резервной копии, с разными входом и выходом):
```powershell
$exe='D:\Program Files\SkinTokens\runtime\bin\skintokens-cli.exe'
$weights='D:\Program Files\SkinTokens\models\SkinTokens-GGUF\F16'
& $exe inspect $weights --device cpu
# Синтаксис проверять по локальному --help:
# & $exe rig $weights '<INPUT>.glb' '<OUTPUT>.glb' --device cpu --postprocess
# & $exe skin $weights '<MESH>.glb' '<SKELETON>.glb' '<OUTPUT>.glb' --device cpu --postprocess
```

## 4. Правила безопасности и сохранения

- **Вычисления и тяжёлые результаты — локально.** Не публиковать веса, модели, текстуры, кэши, логи с секретами или резервные копии в GitHub. Этот документ — справочник, не разрешение агентам делать push. Если правила текущего проекта запрещают push, запрет сохраняется.
- При грязной рабочей копии не блокировать безопасное read-only исследование, но не смешивать чужие изменения со своими; изолировать новую работу, не сбрасывать `git reset/clean`, не удалять чужие файлы.
- **WinApp MCP — основной Windows UI-инструмент ChatGPT**; Desktop Commander — только восстановление WinApp. Локальный Hunyuan MCP Codex не использует туннель.
- Для риггинга использовать **Bonix** (старые упоминания Rig/Rig Motion/Bones — устаревшие); для создания модели — **3D Craft**. Superpowers — методики делегирования и проверки, не гарантия запуска субагентов.
- **Открыл → сделал → сохранил → закрыл → проверил**. Не запускать Blender/Unity в автозагрузке и не ставить им сторожей. Не останавливать чужие процессы.


## Актуальный локальный Hunyuan3D-2GP — четыре ракурса

Рабочий генератор: **Hunyuan3D-2GP / Hunyuan3D-2mv Turbo**, папка D:\Program Files\Hunyuan3D-2GP, веса D:\Program Files\Hunyuan3D-2GP\models-local, локальный MCP Codex Desktop **hunyuan3dLocal** (D:\AI-MCP\hunyuan-local\hunyuan_mcp.py, stdio без туннеля). **Один единый 4-view turnaround-лист** (front/back/left/right, одинаковый масштаб) → четыре отдельные картинки front.png/back.png/left.png/right.png → MCP hunyuan_generate_multiview → проверенный GLB в D:\AI-MCP\hunyuan-local\jobs\<job_id>\result.glb → Blender для текстур/QA → Unity. Если есть лишь одиночное фото, сначала создать один согласованный лист с четырьмя видами; запрещены четыре независимые генерации. Левый и правый профили должны быть противоположны, асимметричные конечности и головы — совпадать на всех видах. Проверить GLB и 42 ракурса, запускать только одну тяжёлую CUDA-задачу. В ChatGPT Windows UI — WinApp MCP; Desktop Commander только для диагностики/ремонта WinApp. **Раскраска Hunyuan в текущем MCP не подтверждена — материалы и текстуры через Blender.** Старые бинарные программы и уже созданные модели не удалять.
