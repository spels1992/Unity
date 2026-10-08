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
