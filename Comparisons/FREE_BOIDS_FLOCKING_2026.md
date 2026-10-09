# Unity Boids / Flocking — сравнение бесплатных решений (2026-10-09)

| Решение | Unity Editor из ProjectVersion.txt | Лицензия | Особенности | Статус |
|---|---|---|---|---|
| [Vivian Ménard](../Tool_Catalog/boids-vivianmenard.md) | 2022.3.16f1 | MIT для исходников; ассеты проверить | 3D рыбы, хищники, obstacle avoidance | DOCUMENTED / NOT_RUN |
| [andywiecko/Flocking](../Tool_Catalog/flocking-burst-andywiecko.md) | 2021.2.0f1 | MIT, внешние зависимости проверить | Burst 1.6.4, Collections 1.1.0, Native2dTree | DOCUMENTED / NOT_RUN |
| [Sebastian Lague Boids](../Tool_Catalog/boids-seblague-legacy.md) | 2019.1.3f1 | MIT | Учебный алгоритм; legacy Ads 2.0.8, Analytics 3.3.2, IAP 2.0.6 | DOCUMENTED / NOT_RUN |

- andywiecko: две Git-зависимости BurstCollections v1.4.0 и BurstMathUtils v1.1.0 — лицензии проверить отдельно.
- SebLague: не включать старые Ads/Analytics/IAP и не переносить их в новую игру.
- Все три проекта **не тестировались на Unity 6.3**. Boids — только поведение группы, не полноценный NPC AI.
- **Стоимость:** 0 ₽ без платных API/облачных сервисов.
- **План тестирования:** изолированные копии, запуск сцен в заявленных версиях Editor, затем отдельная миграция на Unity 6.3; profiler для 100/500/1000 агентов, obstacle collision, Windows Build.
- **Первоисточники:** https://github.com/VivianMenard/boids ; https://github.com/andywiecko/Flocking ; https://github.com/SebLague/Boids
