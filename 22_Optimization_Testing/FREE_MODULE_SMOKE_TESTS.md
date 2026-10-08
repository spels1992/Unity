# Тесты бесплатных Unity игровых систем — план без дополнительных расходов

Дата: 2026-10-08. **Это инструкция к будущим тестам, а не отчёт об уже выполненном запуске.**

## Подготовка
1. Проверить свободное место, видеопамять и версию Editor до скачивания. Для тяжёлого OpenEmpires большого размера искать сначала GitHub manifest/lfs, ограничить ненужные ветки и **не копировать содержимое в spels1992/Unity**.
2. Перед любым скачиванием фиксировать первоисточник, revision/tag, точный MIT/Apache/CC0/Unity Companion LICENSE и отдельные разрешения ассетов. [FREE_ONLY_POLICY](../FREE_ONLY_POLICY.md) — **0 ₽**.
3. Тестировать в **отдельных одноразовых проектах**, не изменять существующие пользовательские Unity сцены и Blender файлы.
4. Избегать платных AI model/provider calls, облачных серверов, подписок/хостинга, Asset Store покупок.
5. Unity MCP использовать только через законно разрешённую авторизацию. При недоступности перейти к обычному Unity Editor и разрешённым локальным инструментам, не обходить ограничения.

## Проверка каждого модуля
| № | Действие | Доказательство |
|---|---|---|
| 1 | ProjectVersion точно совпадает с выбранной Unity Editor | ProjectVersion.txt и Editor About |
| 2 | Package Manager установил зависимости без платных внешних сервисов | manifest.json / packages-lock.json |
| 3 | Скрипты скомпилировались | Unity Console: 0 compile errors |
| 4 | Открывается демосцена или sample | Скриншот, scene path, список assets |
| 5 | Выполняется основная функция | Пошаговый test action → expected → actual |
| 6 | Проект запускается в Play Mode без exceptions | Console snapshots |
| 7 | Собирается Windows Player при необходимости | Build report exit/result, версия, log |
| 8 | Проверены ограничения лицензий вложенных ассетов | asset provenance register |
| 9 | Нет избыточных владений Input / AI / Save / Camera | Сравнение ответственности на схеме |
| 10 | Устойчивость и FPS на целевой машине | Profiler CPU/GPU/memory snapshot |
| 11 | Очистка временных данных без затрагивания существующего проекта | diff/исходные контрольные файлы |

## Приоритеты
- **Smoke 01:** `YarnSpinner-Unity` package 3.2.8 или `Ink Unity Integration` package 2.0.0 на Unity 6000.3 — попробовать оба по **отдельности**, не смешивать.
- **Smoke 02:** `EZRoomGenerator` 0.1.0 + Unity6.3 (проверить com.unity.formats.fbx 5.1.5; создать maze, коллайдеры).
- **Smoke 03:** `Moonforge` 1.2.0: deterministic combat + quest/inventory save/load EditMode tests.
- **Smoke 04:** `Game Lattice Playground` точно Unity 6000.4.11f1, выполнить 9 уроков и проверить отсутствие дубликата Microsoft.CSharp.dll.
- **Smoke 05:** `OpenEmpires` точно Unity 6000.5.9f1, local simulation first, сетевую Rust/PostgreSQL на localhost только если нужно.
- **Smoke 06:** `Edgar Free` граф уровня/room template в Unity6, без PRO.
- **Smoke 07:** `UnityModularInventorySystem` 6000.0.50f1, stack/split/drop UI, без обещаний сохранения.
- **Smoke 08:** `OpenKCC` и маленький FPS controller в Unity6, отдельно проверить input/ground/slope/camera.

## Шаблон протокола
```yaml
module: "repo/name"
commit_or_release: "..."
unity_editor: "6000.x.yf1"
render_pipeline: "URP"
os: "Windows 11"
license: "MIT"
price_paid: 0
dependencies: []
test_scenario: "..."
expected: "..."
actual: "..."
playmode_result: "PASS/FAIL/NOT_RUN"
build_result: "PASS/FAIL/NOT_RUN"
console_errors: 0
performance_fps: null
evidence_links: []
tested_at: "YYYY-MM-DD"
tested_by: "..."
```

**Не путать:** проверка github+LICENSE = DOCUMENTED; запуск sample в Editor = SMOKE TESTED; подтверждение совместимого стека и Player build = INTEGRATION TESTED; полноценное QA с устройствами = PRODUCTION EVALUATED. Никогда не объявлять higher verification, чем подтверждают доказательства.
