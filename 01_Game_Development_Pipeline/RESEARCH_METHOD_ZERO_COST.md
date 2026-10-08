# Систематический поиск готовых игровых решений (0 ₽)

**Версия 2026-10-08. Цель — построить руководство «где искать и как проверять» для любой игры Unity/Blender, а не склад чужих ZIP-файлов.**

## Алгоритм для каждой механики и жанра
1. **Сформулировать потребность**: жанр, платформа, core loop, системы Input/Movement/Camera/AI/Save/Physics/Network/UI/Art/Animation/Audio.
2. **Проверить свою базу:** [Tool Catalog](../Tool_Catalog/INDEX.md), [жанры](../02_Game_Genres/GENRE_MATRIX.md), [готовые стеки](../21_Compatible_Stacks/README.md), [производственный цикл](PIPELINE.md). Не искать уже исследованное заново, пока версия не устарела.
3. **Приоритет поиска:** готовая бесплатная игра → полный framework → starter kit → подсистема → пакет/модуль → отдельный алгоритм → только затем собственный код.
4. **Первичные источники:** Unity Manual/Registry/Asset Store, Blender Manual, GitHub GitLab авторов; читать README, LICENSE, ProjectVersion.txt, package.json, dependencies, CHANGELOG и samples.
5. **Разные поисковые формулировки:** `unity 6 city builder source`, `unity survival crafting save MIT`, `Unity racing vehicle physics open source`, `Unity UPM controller`, `Blender addon free GPL`; не ограничиваться «game».
6. **Смежные источники:** игровые сообщества, Reddit, документация авторов, форумы и видеодемо для поиска; окончательную лицензию/стоимость проверять у первоисточника.
7. **Разобрать все зависимости:** исходники MIT, но отдельные Unity Companion assets, LGPL код, Mixamo/Asset Store модели, Photon/Paid API могут менять пригодность. Бесплатный trial/кредит не гарантирует zero-cost production.
8. **Проверить полезность:** реализованные функции, а не roadmap, готовая сцена, размер проекта/Unity, поддержка, Unity6 совместимость, количество необходимых адаптеров.
9. **Создать карточку:** ссылка на original source, точная цена, версия, доказательство LICENSE, функционал, плюсы/минусы, known issues, статус, дата, 0 ₽ fallback, AI-assisted workflow.
10. **Собрать только одну совместимую архитектуру**, заранее решить ownership: Input, Camera, Save, Inventory, Network, AI, Physics.
11. **Реальный тест:** изолированный Unity/Blender проект, PlayMode+build+perf+errors. До запуска помечать DOCUMENTED/ASSUMED, не TESTED.
12. **Сохранить GitHub:** canonical card, index, source list, comparison, issue/progress checkpoint, readback. При отсутствии находки документировать GAP и альтернативные запросы.

## Статусы, которые нельзя смешивать
| Статус | Значение |
|---|---|
| FREE_DOCUMENTED | Основной код/ресурс бесплатен и лицензия проверена; редакторный тест отсутствует |
| FREE_WITH_RESTRICTIONS | 0 ₽ вариант есть, но нужны условия Unity Companion/Asset Store или права стороннего контента |
| ASSUMED_STACK | Комбинация предполагается; runtime интеграция не доказана |
| BLOCKED_LICENSE / BLOCKED_DEPENDENCY | Не найдена/не подтверждена лицензия обязательного модуля или платная преграда |
| REFERENCE_ONLY | Изучать архитектуру, но не переносить всё как free starter |
| VERIFIED | Конкретная версия Editor/UPM, тест, результаты Console/PlayMode/build и доказательства записаны |

## Система оценки: сначала фильтр, потом выбор
- **GATE A:** правовой статус и отсутствие дополнительной оплаты; если FAIL, внедрение нельзя.
- **GATE B:** основные игровые функции уже готовы? Полная игра или маленький пример? Что ещё писать самим?
- **GATE C:** Unity exact Editor, renderer, Input, third-party dependencies совпадают?
- **GATE D:** нет двух владельцев Inventory/Save/Camera/Network?
- **GATE E:** PlayMode/Build/воспроизводимость и профайлер.

Не выставлять субъективный рейтинг «100/100» без доказательств. Каждый неудачный поиск сохранять как GAP, чтобы другие агенты не тратили лимит повторно.

## Результат применения метода
Задав запрос **«сделать survival с крафтом»**, сначала получаем [Project Wanderer](../Tool_Catalog/project-wanderer-survival.md), [Grid-Based Crafting](../Tool_Catalog/grid-based-crafting-system.md) и сравнительную матрицу, а не просьбу сгенерировать 500 строк C#. Если готового решения нет — ищем смежные модули, только затем пишем сами.

**Правило:** [ZERO COST](../FREE_ONLY_POLICY.md) и проверка по [GitHub Issue #2](https://github.com/spels1992/Unity/issues/2).
