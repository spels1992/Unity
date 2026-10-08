# BEST_SOLUTIONS — выбор решений (осторожный старт)

**Дата:** 2026-10-08. **Важное обновление:** бывший FPS Microgame в Asset Store уже DEPRECATED, а вместо старого First-Person Controller представлен обновлённый объединённый First Person + Third Person контроллер. Список динамический. «Изучено по документации» **не равно** «проверено в Unity».

| Ситуация | Первым изучить | Причина | Статус |
|---|---|---|---|
| Учебный FPS | [Unity First Person + Third Person Controller](Tool_Catalog/official-starter-kits.md) | Новый бесплатный объединённый пакет Unity, версия 2.0.1 от 2026-09-17 | EULA нестандартная; требуется тест в Unity |
| TPS/движение персонажа | [Объединённые FPS+TPS Controllers](Tool_Catalog/official-starter-kits.md) | FREE, URP 6000.3, проверено по Asset Store | Non-standard EULA; не тестировалось |
| 2D платформер | [2D Game Kit](Tool_Catalog/2d-game-kit.md) | FREE, Asset Store v5.0 (2026-03-23), URP 6000.3 | Документально изучено, без Editor тестов |
| Камеры | [Cinemachine](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-cinemachine) | Официальный модуль; Unity 6.3: 3.1.7 | Изучено по документации |
| Навигация NPC | [AI Navigation](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-ai-navigation) | NavMesh и runtime/edit-time navigation; 6.3: 2.0.15 | Изучено по документации |
| Сетевой проект | [Mirror](Tool_Catalog/mirror-networking.md) | MIT, активный open source, комплексная сетевая система | Проверено по исходникам/лицензии, не тестировалось в Editor |
| Сложный async | [UniTask](Tool_Catalog/unitask.md) | MIT, поддерживаемый async toolkit | Изучено по исходникам; необходимость уточнить |
| Массовая ECS симуляция | [DOTS Samples](Tool_Catalog/unity-dots-samples.md) | Официальная подборка примеров ECS/Jobs/Physics/Netcode | Старые sample-версии: Unity 6.2, не заявлена совместимость с 6.3 |

**Не рекомендовать как новый production starter:** [FPSSample](Tool_Catalog/fps-sample-legacy.md) — сам README заявляет Unity 2018.3 и отсутствие поддержки. Важно различать красивую демонстрацию и поддерживаемую современную основу.

**Устарели/недоступны новым пользователям:** [FPS Microgame](Tool_Catalog/fps-microgame-deprecated.md) и отдельный старый [Starter Assets: FirstPerson](https://assetstore.unity.com/packages/essentials/starter-assets-firstperson-urp-196525). Первый официально deprecated; второй снят со страницы, использовать актуальный объединённый контроллер.
