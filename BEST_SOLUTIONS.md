# BEST_SOLUTIONS — выбор решений (осторожный старт)

**Дата:** 2026-10-08. Список динамический. «Изучено по документации» **не равно** «проверено в Unity».

| Ситуация | Первым изучить | Причина | Статус |
|---|---|---|---|
| Учебный FPS | [FPS Microgame](https://unity.com/campaign/unity-6-resources) | Официальный обучающий/стартовый проект Unity 6 | Изучено по каталогу Unity, подробный пакет не проверен |
| TPS/движение персонажа | [Starter Assets: Third-Person Controller](https://unity.com/campaign/unity-6-resources) | Официальный стартовый контроллер | Изучено по каталогу Unity, точную лицензию читать в Asset Store |
| Камеры | [Cinemachine](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-cinemachine) | Официальный модуль; Unity 6.3: 3.1.7 | Изучено по документации |
| Навигация NPC | [AI Navigation](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-ai-navigation) | NavMesh и runtime/edit-time navigation; 6.3: 2.0.15 | Изучено по документации |
| Сетевой проект | [Mirror](Tool_Catalog/mirror-networking.md) | MIT, активный open source, комплексная сетевая система | Проверено по исходникам/лицензии, не тестировалось в Editor |
| Сложный async | [UniTask](Tool_Catalog/unitask.md) | MIT, поддерживаемый async toolkit | Изучено по исходникам; необходимость уточнить |
| Массовая ECS симуляция | [DOTS Samples](Tool_Catalog/unity-dots-samples.md) | Официальная подборка примеров ECS/Jobs/Physics/Netcode | Старые sample-версии: Unity 6.2, не заявлена совместимость с 6.3 |

**Не рекомендовать как новый production starter:** [FPSSample](Tool_Catalog/fps-sample-legacy.md) — сам README заявляет Unity 2018.3 и отсутствие поддержки. Важно различать красивую демонстрацию и поддерживаемую современную основу.
