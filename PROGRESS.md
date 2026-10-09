# PROGRESS — журнал работ и контрольные точки

**2026-10-08 — миграция концепции:** аудит существующего репозитория (15 старых Markdown), создана и проверена [backup branch](https://github.com/spels1992/Unity/tree/archive/pre-solution-catalog-2026-10-08) на исходном коммите `d687b9a95f773fd00247592e731fff4dd0107dae`. Старые файлы будут перемещены в [Research_Archive/legacy](Research_Archive/legacy), без удаления их содержания. Ни одной Unity-сборки в этом исследовательском цикле не запускалось.

| Задача | Статус | Что обязательно перед закрытием |
|---|---|---|
| Резервная ветка | выполнено | Сопоставлены SHA backup/main до изменения |
| Аудит прежних файлов | выполнено | Проверено дерево: 4 root + 11 docs |
| Миграция каталога | текущий этап | GitHub main tree/ссылки после коммита |
| Полная карта разработки | первая редакция | Глубокая проверка всех зависимостей и инструментов |
| Матрица жанров | первая редакция | Для каждого жанра — собственные starter kits/стек |
| Первый пилотный каталог | первая редакция | Карточки с лицензионным статусом и ссылками |
| Проверка в Editor | не начато | Версия, билд, тесты и результаты |
| Исследование остальных категорий | не начато | Пройти 23 папки + сравнения, стеки, обновления |

## Следующие задачи
1. Уточнять матрицы, проводить свежий поиск по всем категориям и жанрам.
2. Добавлять канонические карточки и подтверждать лицензии первоисточниками.
3. Делать кандидатные совместимые стеки и отдельно тестировать их в Unity на Windows.
4. Заносить логи, производительность, проблемы, решения и ссылки на коммиты после каждого завершённого блока.

## Контрольная точка 2026-10-08: первое предметное исследование
- Из официальных источников выяснилось: прежние FPS Microgame и standalone FirstPerson package больше не доступны новым пользователям; текущий бесплатный First Person + Third Person Controllers = Asset Store v2.0.1, URP Unity 6000.3, **Non standard EULA**.
- 2D Game Kit — FREE, Unity 6000.3 URP compatibility, v5.0 от 2026-03-23.
- FishNet **имеет LICENSE.md**: custom license, а не MIT (уточнено после просмотра точного имени LICENSE.md).
- Добавлены канонические карточки по 12 актуальным/устаревшим кандидатам и проведено документальное сравнение.
- **Live Unity Editor integration = 0, compatibility TESTED = 0**; перед статусом verified нужен воспроизводимый тест.

## 2026-10-08 — Unity MCP и правовые условия
- Создана основная задача [#2](https://github.com/spels1992/Unity/issues/2), #1 закрыта как устаревшая.
- Проверены Unity Terms of Service 30.06.2026 и ограничения AI/MCP/CLI агентного доступа (§17.2).
- Изучены MIT лицензии CoplayDev и CoderGamester, созданы два кандидата с непротестированным правом интеграции и отдельная инструкция по Unity AI Gateway.
- **На ПК Unity/сторонние MCP не устанавливались, тестов не было**.

## 2026-10-08 — без дополнительных расходов, инвентаризация инструментов
- Зафиксирована строгая политика [FREE_ONLY_POLICY](FREE_ONLY_POLICY.md): платные инструменты только изучать, не внедрять; free tiers с платными лимитами — не критический путь.
- На основании доступных tools и `skills__list` составлена [матрица плагинов и скиллов Unity/Blender](19_AI_Automation/AVAILABLE_PLUGINS_AND_SKILLS.md), fallback без жёсткой зависимости от одного MCP.
- Найден `Unity_MCP.blender_bridge` для связи с BlenderMCP addon. Сам addon/соединение не тестировались. 

## Контрольная точка 2026-10-08: бесплатные 2D/3D, законченные игры, стеки и импорт

**Задачи выполнены и зафиксированы коммитами:**
1. [001356ae](https://github.com/spels1992/Unity/commit/001356ae147148e75ec979ee2abb2859776b6a26) — восемь канонических бесплатных CC0 карточек: Poly Haven, Kenney, Quaternius и отдельные пакеты.
2. [fefe839](https://github.com/spels1992/Unity/commit/fefe839a472fff6e854aba09cefe4763c63e9166) — три крупных Unity проекта/подсистемы (Chop Chop, Boat Attack и Water) + comparison.
3. [6ddb0fc](https://github.com/spels1992/Unity/commit/6ddb0fc6be87ceca2e0a611f12e7b0b7ee425bcd) — четыре бесплатных жанровых стека со статусом ASSUMED.
4. [1466485](https://github.com/spels1992/Unity/commit/14664854d2f39242395f1ad2f5d29d5ec0847966) — бесплатный FBX/Blender→Unity pipeline, asset provenance.

**Итого новых карточек за цикл: 11, новых стеков: 4, ни один Editor тест не выполнялся.**

### Важные решения
- Kenney All-in-1 и Quaternius Source — платные расширения, в проекте запрещены; бесплатные отдельные версии разрешены согласно подтверждённой CC0.
- Chop Chop прекращён, Boat Attack legacy и не production ready; использовать как обучение, не главный шаблон Unity 6.
- FBX — базовый Unity импорт моделей по официальной документации, особенно для воспроизводимой сборки.

### Следующие задачи
- Полностью исследовать бесплатные open-source проекты под Unity 6.3+ по каждому жанру с активным выпуском и лицензией.
- Найти готовые бесплатные контроллеры/AI/Quest/RPG/Vehicle frameworks и подтвердить compatibility/лицензию.
- Протестировать Free Stacks на реальном Unity Editor и Blender, зафиксировав logs + screenshots + Player build.
- Построить машинно-читаемый индекс и автоматические проверки ссылок, строго избегая API с платными кредитами.


## Цикл 2026-10-08 — готовые бесплатные игровые фреймворки

Сохранённые самостоятельные блоки:
1. [923e6af](https://github.com/spels1992/Unity/commit/923e6af34da3d5ecc05cd17c38804727529de1c1) — 7 карточек: OpenEmpires, Moonforge, Yarn Spinner, Ink, OpenKCC, EZRoomGenerator, Edgar Free.
2. [448e7a3](https://github.com/spels1992/Unity/commit/448e7a31016801775f125d927fa216fbba9b2f8b) — 5 карточек: Game Lattice, playground, Modular Inventory, Softlight, FPS Controller.
3. [d8cd072](https://github.com/spels1992/Unity/commit/d8cd072004469f30299d2062695dd0289c59ec20) — сравнение и матрицы лицензий, исключение инвентаря без LICENSE.
4. [364f102](https://github.com/spels1992/Unity/commit/364f1020029da74c1a7b8b73a3d4e5d573bd6ffd) — 5 бесплатных связок и инструкция реальных smoke-тестов.
5. [42a11c9](https://github.com/spels1992/Unity/commit/42a11c928f63fe16021170a83a75aec5de201cbb) — подробный аудит Moonforge Unity roguelike sample, точный UPM URL и лицензионный пробел её тайлсета.

**Итого этого цикла: 12 новых карточек решений, 2 самостоятельных сравнения/исключения, 2 инженерные инструкции; 5 коммитов до этого журнала.** Платные средства НЕ использовались и НЕ внедрялись. Практических Unity/Blender live-tests не было: VERIFIED = 0.

Существенные результаты:
- OpenEmpires — полноценная RTS; README Unity 6000.3.9f1 и фактический ProjectVersion Unity 6000.5.9f1 расходятся. Rust/PostgreSQL бесплатно для localhost.
- Moonforge — большая RPG domain система с уже готовой импортируемой roguelike Unity sample (Town, Dungeon, Combat, Quest, Save/Load).
- Yarn Spinner бесплатен через Git UPM при MIT, а платная версия магазина необязательна. Ink — MIT альтернатива для диалогов.
- Game Lattice — Apache-2.0 JSON RPG и AI framework, версия UPM 0.0.0-dev; есть Unity 6000.4 playground.
- EZ Room Generator — MIT Unity 6000+, FBX Exporter dependency; Edgar Free — MIT с платной PRO, использовать только Core.
- Softlight — ранний прототип, RPG функции Planned, нельзя выдавать за готовые.
- wendtcloud/inventory-system без root LICENSE в дереве, не принят.
- Moonforge sample README утверждает CC0 DungeonTileset II и отдельный LICENSE.txt, но файл по указанному пути отсутствует в просмотренном GitHub tree. Перед переносом арт-ассетов перепроверять исходную лицензию.

Дальнейшие задачи:
1. Подтвердить происхождение и лицензию 0x72 DungeonTileset II у издателя или автора Moonforge.
2. Запустить отдельный бесплатный тест Moonforge Unity sample, не трогая рабочие проекты.
3. Отдельно проверить Yarn Spinner vs Ink, установку на актуальную Unity 6.
4. Протестировать EZRoom/Edgar Free и персонажные контроллеры.
5. Изучать полноценные бесплатные игры и framework по всем жанрам из ROADMAP.


### Уточнение лицензии 0x72 DungeonTileset II — 2026-10-08
После обнаружения отсутствующего LICENSE note в GitHub sample Moonforge найден и проверен **первичный авторский источник** https://0x72.itch.io/dungeontileset-ii. Автор помечает исходные sprites как CC0 1.0 и разрешает коммерческое использование. Оригинальная графика допускается к бесплатному использованию; не найденный файл LICENSE внутри чужой sample — вопрос provenance упаковки, а не отсутствие права на оригинальный pack. Создана отдельная карточка; в новых играх брать оригинальные PNG с itch.io и сохранять license evidence.


## Контрольная точка: 2026-10-08 — гонки, survival, строительство, FPS

**Три подтверждённых GitHub-коммита:**
1. [87616df](https://github.com/spels1992/Unity/commit/87616df29eb0413df21cc8706f06f10b3c5f4660) — **9 карточек** готовых бесплатных исходных решений по Survival, Building, Racing, Vehicle Physics, FPS.
2. [a8189b7](https://github.com/spels1992/Unity/commit/a8189b72e1d5173798e926671aa30e44ebdf3078) — сравнение, 4 архитектуры без оплаты, метод постоянного исследования и лицензионные исключения.
3. [883d63e](https://github.com/spels1992/Unity/commit/883d63eb812edbaf16229fc19f34dbefd264eb3b) — 9 навигационных и юридических индексных файлов обновлены.

**Содержательные находки:**
- [Project Wanderer](Tool_Catalog/project-wanderer-survival.md): Unity 6000.3.13f1, MIT code, day/night, gathering, crafting, storage и save; отдельный StarterAssets license = Unity Companion.
- [Grid Building System](Tool_Catalog/grid-building-system.md): Unity 6000.3.16f1, MIT, multi-floor building/pathfinding/mesh chunks/save. **Пока два приоритетных live-test кандидата**.
- [GeoJSON City Builder](Tool_Catalog/geojson-city-builder.md) MIT root, но `com.virgis.geojson.net` 1.2.17 dependency license не подтверждена — BLOCKED_DEPENDENCY.
- [PolyRace](Tool_Catalog/polyrace-legacy.md) цельная sci-fi racing игра, но Unity 2020 и сторонние art/music/LGPL код; не переносить wholesale в production.
- [Street Racing](Tool_Catalog/street-racing-free-demo.md) MIT code, однако Asset Store model/road EULA отдельно.
- [ArcadeVehiclePhysics](Tool_Catalog/arcade-vehicle-physics.md) MIT, Unity 2018 legacy.
- [TLabVehiclePhysics](Tool_Catalog/tlab-vehicle-physics.md) MIT core, но git-submodules TLab-Spline, TLabCurveTool и другие требуют LICENSE-аудита.
- [Grid-Based Crafting](Tool_Catalog/grid-based-crafting-system.md) MIT GitHub source; Asset Store путь из README не делать обязательным.
- [Armour FPS](Tool_Catalog/armour-multiplayer-fps.md) MIT root, но Photon PUN2/Asset Store/Mixamo — отдельные условия, REFERENCE_ONLY.

**Проверка после записи:** GitHub main snapshot содержал 117 файлов и 49 карточек каталога, проверены **284 внутренние ссылки в 12 ключевых документах**, 0 отсутствующих путей. Все девять новых карточек подтверждены в дереве. Эти цифры относятся к снимку перед данным журналом и не являются числом проверок живой игры.

**Без изменения пользовательских Unity/Blender проектов.** Ни одна новая система не проверена нами в PlayMode/Windows Build. Статусы DOCUMENTED или BLOCKED; **EDITOR_VERIFIED = 0**.

### В следующий цикл
- Приоритеты live-test (изолированные Unity проекты): Project Wanderer и Grid Building System на версиях из ProjectVersion; проверка реальных лицензий ассетов, сборки и сохранений.
- FPS/TPS: искать **новые полноценные бесплатные gameplay frameworks** без обязательного платного Photon hosting, сравнить с Mirror/бесплатными Unity пакетами.
- Racing: искать современный поддерживаемый Unity6 транспортный контроллер с полностью аудированной лицензией, в том числе git submodules.
- World/city: раздельные модули жителей, дорог, транспорта, экономики, зон и коллизий.
- Продолжить пополнять остальные жанры и Blender каталог бесплатных арт-инструментов.
- **Никаких дополнительных расходов**, подписок, платных ассетов, API и обязательных облачных серверов.


## Контрольная точка 2026-10-08 — Blender → Unity, PBR/UV/Rigging, игровые звуки

**3 подтверждённых GitHub коммита текущего блока до этого журнала:**
1. [8043a45](https://github.com/spels1992/Unity/commit/8043a45750439cfdc736812d36470f460fc2276f) — 10 карточек: Rigify, Khronos glTF Blender I/O, Unity glTFast, Ucupaint, TexTools, ambientCG, Kenney UI/Impact/RPG/Music Audio.
2. [dbf8759](https://github.com/spels1992/Unity/commit/dbf8759ee1a55da852005da5dc1d73d30664100e) — одиннадцатая карточка Kenney Sci-fi Sounds + новый 3D production guide, audio workflow и сравнение.
3. [6c39622](https://github.com/spels1992/Unity/commit/6c396223608923e6b8e69eabd71e857d113ae810) — обновлены индекс всех решений, Blender/Audio README, главные README/BEST_SOLUTIONS/LICENSE_MATRIX/COMPATIBILITY_MATRIX/SOURCES.

**Фактическая проверка GitHub main до этого checkpoint:** 131 Markdown/других файлов, **60 канонических карточек** (исключая INDEX/CARD_TEMPLATE), из них **11 новых**; все 11 присутствуют. Проверено **299 внутренних относительных Markdown-ссылок** в 14 основных документах: **0 broken, 0 read failures**.

### Что найдено
- **Бесплатная GLB/FBX развилка:** Blender Khronos glTF 2.0 I/O встроен в Blender (Apache-2.0), Unity glTFast (Apache-2.0) даёт Editor/runtime import/export. `Packages/com.unity.cloud.gltfast/package.json` main = `6.20.1-pre.1` минимум `6000.0`; брать **stable Registry** package, а не preview по умолчанию. Third Party Notices содержит CC-BY тестовые модели; не копировать чужие sample assets без атрибуции.
- **Rigify** (bundled GPL) для генерации 3D character control rig, **TexTools** (GPLv3+) для UV/texel density, **Ucupaint** (manifest 3.0.0, Blender min 4.2, GPL-3.0+) для текстурных слоёв. Процедурные Blender shaders/controls необходимо запекать для Unity.
- **ambientCG** CC0 PBR текстуры дополняют Poly Haven.
- **Kenney CC0 audio:** UI 50 + Impact 130 + RPG 50 + Sci-fi 70 + Music Jingles 85 = **385 файлов по пяти официальным страницам**. Каждый pack бесплатен отдельно без платного All-in-1.
- Руководство [Blender → Rigify/UV/PBR → glTFast/FBX → Unity](18_Blender_Integration/FREE_GLTF_RIG_UV_PRODUCTION.md), [Audio SFX → AudioSource/Mixer → Player Build](14_Audio/FREE_SOUND_PIPELINE.md), [Сравнение](Comparisons/FREE_BLENDER_TEXTURE_AUDIO_GLTF.md).

### Ограничения и следующая очередь
- Не было live Unity Editor / Blender test, Player Build, Audio playback или blender_bridge; **TESTED/VERIFIED = 0 для этого блока**.
- Восстановить URL/status стабильных версий glTFast для установленного Editor, проверить glTFast shader graph variants в Player Build.
- В отдельном тестовом проекте сравнить GLB vs FBX для CC0 персонажа с анимацией.
- Начать бесплатный каталог инструментов Blender: geometry nodes, retargeting, lip-sync, free HDRI/foliage, auto LOD (после лицензий), аудиомузыка CC0.
- Исследовать бесплатные собственные voice/sound/music creation workflows без оплаченных внешних API.
- Нулевой бюджет обязателен; никакие чужие большие ZIP, fonts или samples в нашу базу GitHub не загружены.


## 2026-10-09 — бесплатные деревья/Geometry Nodes/LOD, Retarget, Lipsync и CC0 BGM

**Доказанные результаты, сохранённые в GitHub:**
1. [66b3cbf](https://github.com/spels1992/Unity/commit/66b3cbfc51273f15397e9e535b6f0d11b04be287) — **13 новых canonical карточек**: Geometry Nodes, Decimate, Sapling Tree, YGForge Generate Tree, Modular Tree, KBS Retarget, Rokoko retarget, Rhubarb Lip Sync NG и CLI, четыре отдельных CC0 музыкальных набора.
2. [5512992](https://github.com/spels1992/Unity/commit/55129922f8409e9384ab83d9d92454d89f27b3dd) — четыре инструкции: free forest & LOD workflow, retarget + lipsync workflow, CC0 game music list, quick comparison.
3. [573f73c](https://github.com/spels1992/Unity/commit/573f73c2a0f031f5a223a71c58697814e5deeb41) — обновлены README, Tool Catalog index, Blender/Animation/Audio section READMEs, BEST_SOLUTIONS, LICENSE_MATRIX, COMPATIBILITY_MATRIX, SOURCES.

**GitHub QA перед этим checkpoint:** 149 файлов, **74 карточки решений** (кроме INDEX/CARD_TEMPLATE), все **13 новых присутствуют**; 354 внутренние Markdown-ссылки в 14 ключевых документах проверены — **0 broken**, ошибок чтения нет.

**Особенно полезно и важно:**
- [Blender Geometry Nodes](Tool_Catalog/blender-geometry-nodes-free.md) — бесплатно встроенный scattering, но Blender procedural instance graph нельзя просто импортировать в Unity.
- [Decimate](Tool_Catalog/blender-decimate-lod-free.md) — встроенное уменьшение геометрии для LOD, но silhouette/UV/rig обязательно проверять.
- [Sapling Tree](Tool_Catalog/blender-sapling-tree.md) v0.3.7 с заявленной Blender4.4+, но reports об ошибках дерева/анимации на Blender5; [YGForge](Tool_Catalog/blender-lowpoly-tree-generator.md) 1.1.5 Blender5.0.1+, [Modular Tree](Tool_Catalog/blender-modular-tree.md) 5.5.2 Blender4.3.1+.
- [KBS Retarget](Tool_Catalog/blender-retarget-kbs.md) Blender5+ GPL для Mixamo/Unreal/VRoid/MMD; [Rokoko](Tool_Catalog/blender-rokoko-retarget.md) free retarget LGPL-3.0 (**README MIT badge неправилен**), подписка/оборудование не нужны для обычного retarget.
- [Rhubarb NG](Tool_Catalog/rhubarb-lip-sync-ng-blender.md) бесплатный MIT инструмент, поддерживаемый [Rhubarb CLI](Tool_Catalog/rhubarb-cli-open-source.md); русский голос нужно проверить, Rhubarb не является TTS.
- OpenGameArt CC0 конкретные 4 авторские страницы: SubspaceAudio 12, pauliuw 4, qubodup 2 + drakzlin 5 тематических ZIP (количество треков в архивах неизвестно). Итого **18 подтверждённых отдельных композиций минимум**, не считать все ZIP как 5 дополнительных дорожек.

**Проверки в наших Unity/Blender Editor:** НЕ ПРОВОДИЛИСЬ. Все новые карточки = DOCUMENTED / NOT_RUN; FPS, audio quality и MIDI/skin/morph export не заявлять проверенными. Не загружали чужие ZIP/ассеты и не выполняли платных API вызовов. Правило 0 ₽ сохраняется.

### Следующие приоритеты
- Локально протестировать free Blender foliage generator/geometry nodes export → Unity6 LODGroup, не трогая существующие сцены; сравнить GLB vs FBX.
- Изучить бесплатно скачиваемые **полноценные** музыкальные библиотеки по жанрам с точными лицензиями каждого файла, а также открытые DAW (LMMS/Audacity/MuseScore) и условия их bundled samples.
- Проверить офлайн lip-sync для русской тестовой фразы и экспорт Blender Morph Targets → Unity; оценить редактор/voice input permissions.
- Продолжить заполнение редких жанров: RTS/FPS/survival/colony/racing и Unity6 project ready.


## 2026-10-08 — MuseScore Studio: один подтверждённый коммит
- [1d623dd](https://github.com/spels1992/Unity/commit/1d623dd09e9b04731fb232cbfde60fd06f421122) — [MuseScore Studio](Tool_Catalog/musescore-studio-free.md), v4.7.5, GPL-3.0, самостоятельная бесплатная версия; повторное чтение GitHub PASS.
- Исследованы также LMMS 1.2.2 (GPL-2.0) и Audacity 4.0.1 (GPLv3), но запись карточек заблокирована safety checks, не считать их сохранёнными.
- Unity/Blender/DAW не запускались. Дополнительные расходы 0 ₽. Следующее: сохранить LMMS/Audacity, сравнение и аудио workflow.


## 2026-10-09 H13 — save systems, CI, H12 recovery
- H12: 11 research references recovered in `Research_Archive/H12_20261009_RECOVERED_11.md`; no editor tests, exact sizes UNKNOWN; GPL and custom licenses LEGAL_REVIEW.
- H13: 3 save system candidates in `Research_Archive/H13_20261009_SAVE_CANDIDATES.md` and 3 testing/CI candidates in `Research_Archive/H13_20261009_TESTING_CANDIDATES.md`.
- H13 three audio framework candidates remain in local backup due to GitHub write block.
- No Unity projects changed. CI actions NOT_RUN; avoid paid GitHub minutes; editor tests NOT_TESTED.


## 2026-10-09 — восстановление сохранения накопленных исследований

- [Research_Archive/PENDING_RESEARCH_2026-10-09.md](Research_Archive/PENDING_RESEARCH_2026-10-09.md): резервный сводный реестр 8 направлений исследования с первоисточниками и предостережениями по лицензиям; коммит [0710845](https://github.com/spels1992/Unity/commit/0710845fe760c604e3e97b58cc68d573b493024c).
- **Статус:** DOCUMENTED / NOT_RUN; Unity/Blender не запускались, дополнительные расходы 0 ₽.
- **Осталось:** перенести подробные карточки и матрицы из резервных Markdown, сверить версии и уже существующие карточки; дополнить индекс и issue #2. Сводный реестр не означает, что все подробности сохранены.


## 2026-10-09: восстановление восьми конспектов

В Research_Archive/2026-10-08-09 сохранены и повторно прочитаны 8 документов: NPC, multiplayer games, networking, 2D editors, procgen, localization, Addressables и audio. DOCUMENTED / NOT_RUN, 0 ₽. Полные подробные резервные Markdown ещё не перенесены дословно; необходимо продолжить восстановление и сверить дубли.


## 2026-10-09 — H16 recovery, full backup metadata persisted
- Complete pending research metadata recovered and verified by GitHub readback. This is a research **queue**, not canonical adoption or editor PASS.
- 7 H13/H14 records: `Research_Archive/H16_PENDING_FULL_METADATA_20261009.json`; 9 H15 records: `Research_Archive/H15_UNITY_NINE_FULL_METADATA_RECOVERY_20261009.json`; URL list: `Research_Archive/H16_PENDING_RECOVERY_20261009.md`.
- Need master index deduplication, individual license/dependency review and canonical card promotion. Exact sizes UNKNOWN/null; Unity/Blender editor NOT_TESTED; no large archives downloaded, no new costs.
