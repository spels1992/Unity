# UNITY — глобальная библиотека готовых игровых решений

> **ОБЯЗАТЕЛЬНО: 0 ₽ новых расходов.** Используем только законные бесплатные инструменты и ассеты; платные сервисы только изучаем, не внедряем. [Полная политика бесплатности](FREE_ONLY_POLICY.md).

**Главная цель:** ускорять создание игр через **поиск, проверку и законное переиспользование уже существующих решений**. Это каталог инструментов, технологий, starter kits, открытых игровых проектов, комплексных фреймворков и совместимых наборов, а **не** переписанная документация Unity.

**Репозиторий:** [spels1992/Unity](https://github.com/spels1992/Unity) · **связанная библиотека:** [GameLibrary](https://github.com/spels1992/GameLibrary) · **новая концепция с 2026-10-08**.

## Как искать решение
1. Определить **жанр + платформу + необходимую игровую систему**.
2. Найти систему в [Tool_Catalog/INDEX.md](Tool_Catalog/INDEX.md), [матрице жанров](02_Game_Genres/GENRE_MATRIX.md) и [карте производства](01_Game_Development_Pipeline/PIPELINE.md).
3. Пойти от **готовой игры / полноценного фреймворка** к starter kit → подсистеме → библиотеке → скрипту → собственному коду.
4. Проверить [совместимость](COMPATIBILITY_MATRIX.md) + [лицензию](LICENSE_MATRIX.md), ограничения, стоимость, активность и тесты.
5. Подключать компоненты по [руководствам интеграции](Integration_Guides/) и собирать стеки из [21_Compatible_Stacks](21_Compatible_Stacks/README.md).
6. При отсутствии подтверждённой комбинации ставить статус **предполагается — требуется тест**, а не «совместимо».
7. Сохранять каждый завершённый поиск или эксперимент **в GitHub до перехода к следующему**.

## Навигация
| Что требуется | Где искать |
|---|---|
| Порядок разработки игры А–Я | [01_Game_Development_Pipeline/PIPELINE.md](01_Game_Development_Pipeline/PIPELINE.md) |
| Системы по жанру | [02_Game_Genres/GENRE_MATRIX.md](02_Game_Genres/GENRE_MATRIX.md) |
| Поиск инструментов и карточки | [Tool_Catalog/INDEX.md](Tool_Catalog/INDEX.md) |
| Самые полезные решения | [BEST_SOLUTIONS.md](BEST_SOLUTIONS.md) |
| Совместимость и готовые связки | [COMPATIBILITY_MATRIX.md](COMPATIBILITY_MATRIX.md), [21_Compatible_Stacks](21_Compatible_Stacks/README.md) |
| Бесплатность и лицензии | [FREE_ONLY_POLICY.md](FREE_ONLY_POLICY.md), [LICENSE_MATRIX.md](LICENSE_MATRIX.md) |
| Подходящие плагины и скиллы Unity/Blender | [AVAILABLE_PLUGINS_AND_SKILLS.md](19_AI_Automation/AVAILABLE_PLUGINS_AND_SKILLS.md) |
| Правила карточки | [Tool_Catalog/CARD_TEMPLATE.md](Tool_Catalog/CARD_TEMPLATE.md) |
| Глубокое исследование и очередь задач | [ROADMAP.md](ROADMAP.md), [PROGRESS.md](PROGRESS.md) |
| Проверенные источники | [SOURCES.md](SOURCES.md) |
| Как ставить библиотеки | [Integration_Guides/INSTALLATION_METHODS.md](Integration_Guides/INSTALLATION_METHODS.md) |
| История и прежняя документация | [Research_Archive/README.md](Research_Archive/README.md) |

## Тематический каталог
- [Этапы производства](01_Game_Development_Pipeline/README.md)
- [Жанры и требования](02_Game_Genres/README.md)
- [Комплексные фреймворки](03_Complete_Frameworks/README.md)
- [Контроллеры](04_Character_Systems/README.md)
- [Анимация](05_Animation/README.md)
- [Физика](06_Physics/README.md)
- [Боевые системы](07_Combat/README.md)
- [ИИ/NPC](08_Artificial_Intelligence/README.md)
- [Камеры](09_Cameras/README.md)
- [Интерфейсы](10_User_Interface/README.md)
- [RPG](11_RPG_Systems/README.md)
- [Мир и процедурная генерация](12_World_Generation/README.md)
- [Графика](13_Graphics/README.md)
- [Звук](14_Audio/README.md)
- [Сеть](15_Multiplayer/README.md)
- [Данные и подсистемы](16_Core_Game_Systems/README.md)
- [Инженерные инструменты](17_Development_Tools/README.md)
- [Blender → Unity](18_Blender_Integration/README.md)
- [ИИ-автоматизация](19_AI_Automation/README.md)
- [Готовые игры](20_Ready_Made_Games/README.md)
- [Готовые сочетания](21_Compatible_Stacks/README.md)
- [Производительность и QA](22_Optimization_Testing/README.md)
- [Выпуск и поддержка](23_Publishing/README.md)

## Статусы, не путать
- **Практически проверено**: выполнен воспроизводимый тест в Unity с записанными версиями, платформой и результатом.
- **Изучено по документации**: подтверждены конкретные ссылки/исходники, но интеграция **не тестировалась**.
- **Не проверено**: найден кандидат, данных недостаточно.
- **Устарело**: сам разработчик/официальная информация говорит об отсутствии поддержки или замене; сохранить для истории, не предлагать как основу нового проекта без специальной причины.

**Важно:** наличие открытого GitHub репозитория **не равно** разрешению на копирование, коммерческую продажу или изменение. Все скачивания — с официальных адресов, без зеркал чужого кода у нас.
## Примечание об устаревших источниках
По состоянию на 2026-10-08 в Asset Store FPS Microgame помечен **Deprecated**. Проверять живую страницу пакета, а не только ссылки в старом учебном списке. Обновлённый объединённый FPS/TPS Controller доступен как FREE с Non-standard EULA.

**Основная задача:** [#2 Глобальный каталог готовых решений Unity](https://github.com/spels1992/Unity/issues/2). Старое задание #1 закрыто. **Unity MCP/ИИ:** до подключения читать [ToS и authorized access](19_AI_Automation/UNITY_MCP_AND_TERMS.md).
