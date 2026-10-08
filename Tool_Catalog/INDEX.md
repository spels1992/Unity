# TOOL_CATALOG — канонические карточки

**Одна библиотека = одна основная карточка.** Из жанров/систем/стеков используются относительные ссылки. Поиск начинается с крупной готовой основы.

| Инструмент | Категория | Цена/лицензия | Проверка | Карточка |
|---|---|---|---|---|
| Unity FPS Sample | Готовая игра, FPS | Unity Companion License, legacy | README+license; не тестировалось | [FPSSample](fps-sample-legacy.md) |
| Unity DOTS Samples | ECS/физика/сеть | лицензия уточняется | README; не тестировалось | [DOTS Samples](unity-dots-samples.md) |
| Mirror | Multiplayer | MIT / бесплатный OSS | license+repo; не тестировалось | [Mirror](mirror-networking.md) |
| UniTask | Async/core | MIT / бесплатный OSS | license+repo; не тестировалось | [UniTask](unitask.md) |
| FishNet | Multiplayer | custom FishNet license, НЕ MIT; прочитана | README; не тестировалось | [FishNet](fishnet-networking.md) |
| Cinemachine | Camera | official Unity package, terms проверить | Unity 6.3 docs | [Cinemachine](cinemachine.md) |
| AI Navigation | Navigation | official Unity package, terms проверить | Unity 6.3 docs | [AI Navigation](ai-navigation.md) |
| Unity First Person + Third Person Controller | Starter kits | FREE, Non standard EULA | Asset Store: 2.0.1, URP 6000.3; не тестировалось | [Controllers](official-starter-kits.md) |
| Unity 2D Game Kit | 2D sample project | FREE, Asset Store standard EULA/Extension Asset | v5.0, URP 6000.3; не тестировалось | [2D Game Kit](2d-game-kit.md) |
| Input System | Ввод | Unity package | 1.20.1 Unity 6.3 docs | [Input System](input-system.md) |
| FPS Microgame (legacy) | FPS starter, недоступен новым пользователям | deprecated | Asset Store directly says deprecated | [FPS Microgame](fps-microgame-deprecated.md) |
| Unity Tilemap Extras | 2D level tools | условия проверить | подтверждён переход с 2d-extras | [Tilemap Extras](tilemap-extras.md) |

## Фильтры
- **Лицензия MIT:** Mirror, UniTask (подтверждено LICENSE upstream).
- **Бесплатные официальные образцы:** FPS Microgame / Starter Assets — условия скачивания/применения уточнить.
- **Сетевые альтернативы:** Mirror, FishNet (не смешивать без явной архитектуры).
- **Старое/legacy:** Unity FPS Sample (старое, огромный Git LFS проект), 2d-extras Git.
- **Требует live-теста:** **все** карточки первого прохода.

**Критично:** Unity FPS Microgame и старый FirstPerson пакет DEPRECATED. Не ориентироваться на старую страничку Unity 6 Resources как единственный источник доступности; открывать сам Asset Store.
