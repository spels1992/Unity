# UnityHFSM — состояния персонажей и NPC

- **Категория:** AI / Gameplay / State Machines
- **Решает:** состояния Idle/Patrol/Chase/Attack/Dead, оружие, задания, вложенные режимы поведения.
- **Автор и первоисточник:** [Inspiaaa/UnityHFSM](https://github.com/Inspiaaa/UnityHFSM).
- **Лицензия:** MIT; [LICENSE.md](https://github.com/Inspiaaa/UnityHFSM/blob/master/LICENSE.md) просмотрен напрямую.
- **Цена / статус:** 0 ₽, FREE, DOCUMENTED (не тестировался в Unity 6.3).
- **Пакет:** `com.inspiaaa.unityhfsm`; `package.json` master сообщает **2.3.0**, MIT.
- **Установка:** Unity Package Manager → Add package from Git URL → `https://github.com/Inspiaaa/UnityHFSM.git#upm` (upstream обозначает стабильную ветку); для точной воспроизводимости закрепить commit/tag после пилотной проверки.
- **Доступные образцы:** `Samples~/GuardAI` и `Samples~/Sample3d`, согласно package.json.
- **Unity:** автор указывает Git-установку на Unity 2019.4+, точной проверки Unity 6000.3.25f1 нет.
- **Практическое применение:** NPC охранник, противники RPG, боевые состояния, анимационные переходы; State Machine не заменяет NavMesh/pathfinding и Animator.
- **Возможные конфликты:** не делать два независимых владельца переходов (Animator StateMachine и HFSM) для одной механики; HFSM — логика, Animator — воспроизведение; проверять корутины и остановку при уничтожении объекта.
- **Зависимости / скрытые платежи:** обязательных платных не заявлено; проверить фактический UPM dependency graph. `requires_card=false` при Git-установке.
- **FREE fallback:** собственный enum/switch FSM в C#, без внешних зависимостей.
- **Сценарий проверки:** отдельный новый проект Unity → добавить пакет → открыть Guard AI sample → собрать patrol/chase/return → console errors=0 → PlayMode → Windows build.
- **AI автоматизация:** MCP читает API/пишет тесты/проверяет сообщения Console только в специально выделенном тестовом проекте.
- **last_checked:** 2026-10-08; **verification:** DOCUMENTED; **price_paid:** 0; **Editor tested:** NO.
