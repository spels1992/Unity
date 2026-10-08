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

| CoplayDev MCP for Unity | AI/Editor MCP | MIT | Unity Authorized Agentic Access НЕ подтверждён | [CoplayDev](coplaydev-unity-mcp.md) |
| CoderGamester MCP Unity | AI/Editor MCP | MIT | Unity Authorized Agentic Access НЕ подтверждён | [CoderGamester](codergamester-mcp-unity.md) |

[Важные условия подключения MCP](../19_AI_Automation/UNITY_MCP_AND_TERMS.md).

## Бесплатные библиотеки 2D/3D ассетов (проверено 2026-10-08)
| Решение | Назначение | Бесплатный объём | Карточка |
|---|---|---|---|
| Poly Haven | Библиотека 3D моделей, PBR-текстур, HDRI | Отдельные ассеты бесплатны без paywall и регистрации. Подписка/Vault, массовые скачивания и нек | [Открыть](poly-haven.md) |
| Kenney — бесплатные отдельные игровые наборы | 2D/3D UI, иконки, тайлы, анимации, музыка | Отдельные наборы бесплатно через «Continue without donating». **All-in-1 bundle на itch.io — пл | [Открыть](kenney-free-assets.md) |
| Kenney New Platformer Pack | Полный набор 2D спрайтов и тайлов для платформера | Бесплатно (donation optional); не переходить на платный All-in-1 bundle. | [Открыть](kenney-new-platformer-pack.md) |
| Kenney Platformer Kit (3D) | Комплексный 3D тематический набор моделей | Бесплатно отдельно, платный Kenney All-in-1 не нужен. | [Открыть](kenney-platformer-kit-3d.md) |
| Quaternius — бесплатные Standard ассеты | CC0 low-poly 3D персонажи, окружение, анимации | **Standard/Free часть обычно 60–70% моделей**; расширенная Source version, Blend и готовые Unit | [Открыть](quaternius-free-assets.md) |
| Quaternius Universal Base Characters | Набор humanoid 3D базовых персонажей | Free Standard лишь часть содержимого; Source с полными assets, готовым Unity проектом и .blend  | [Открыть](quaternius-universal-base-characters.md) |
| Quaternius Universal Animation Library | Библиотека анимаций humanoid | Free часть доступна; Source/.blend и готовые engine-проекты относятся к платной версии; полный  | [Открыть](quaternius-universal-animation-library.md) |
| Quaternius Modular Sci-Fi MegaKit | Модульное 3D окружение sci-fi | Только Standard бесплатен; Source со всеми Unity/Blender-сценами, collision и shaders требует о | [Открыть](quaternius-modular-sci-fi-megakit.md) |

**Критично:** отдельные пакеты Kenney бесплатны, но All-in-1 bundle платный. Quaternius Standard частично бесплатен, Source version с Unity/Blender projects — платная. Не приписывать бесплатной версии функции Source.
