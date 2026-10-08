# Стеки: кандидаты, не выданы за проверенные

**На 2026-10-08: все предложения ниже = ASSUMED, без реального запуска Unity Editor.**

| ID | Жанр | Кандидатные компоненты | Что проверить |
|---|---|---|---|
| TPS-01 | TPS / RPG | Starter Assets Third Person + Cinemachine + AI Navigation + инвентарь (пока не выбран) | Input conflicts, камера, движение, лицензия starter assets |
| FPS-01 | FPS | FPS Microgame (цельный проект) **ИЛИ** First Person Starter Assets + отдельная стрельба | Не смешивать комплект целой игры с самостоятельной системой без аудита |
| RTS-01 | RTS | Unity Input System + AI Navigation + собственный selector + UI Toolkit | RTS units на NavMesh, количество сущностей, path conflicts |
| NET-01 | Co-op | Mirror **ИЛИ** FishNet + простая gameplay scene | Лицензия FishNet, Unity 6 совместимость, transport, authority |
| DOTS-01 | Массовая симуляция | ECS Samples в соответствующей версии Unity 6.2 + Entities 1.4 | Воспроизводимость, перенос на новую версию |
| 2D-01 | Платформер | Platformer Microgame **ИЛИ** 2D Game Kit + Tilemap Extras | Версия проекта, правила использования ассетов, collisions |

**Условие статуса VERIFIED:** указать версии всех пакетов, API адаптеры, лицензии, сцену, команду сборки, платформу и воспроизводимый тест/коммит. Нельзя считать два пакета совместимыми просто из-за того, что по отдельности они работают на Unity.
