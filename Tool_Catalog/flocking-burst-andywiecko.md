# Flocking — andywiecko (Unity Burst/Jobs)

**Категория:** AI / NPC, оптимизация стаи на CPU.  
**Первоисточник:** https://github.com/andywiecko/Flocking  
**Автор:** Andrzej Więckowski. **Проверено:** 2026-10-09.  
**Статус:** DOCUMENTED / NOT_RUN. **Стоимость:** 0 ₽, исходники MIT.

## Готовые функции
- Boids flocking с `Unity.Burst` и `Unity.Jobs`, сравнение brute-force и ускорения запросов через `Native2dTree` (k-d tree).
- Upstream предлагает Windows build и WebGL demo; README предупреждает об ограничениях Burst/WebGL и снижении числа boids.
- **Не готовая боевая AI-система:** avoidance препятствий и path-following остаются в TODO.

## Проверенные технические данные
- `ProjectSettings/ProjectVersion.txt`: **Unity 2021.2.0f1** (revision `4bf1ec4b23c9`).
- `Packages/manifest.json`: `com.unity.burst` **1.6.4**, `com.unity.collections` **1.1.0**, `com.unity.2d.tilemap.extras` **2.2.0**, `com.unity.test-framework` **1.1.29**.
- Git dependencies: `com.andywiecko.burst.collections` **BurstCollections v1.4.0**, `com.andywiecko.burst.mathutils` **BurstMathUtils v1.1.0**; проверить **их отдельные лицензии** до включения в распространяемую игру.
- `LICENSE.md`: **MIT**, Copyright (c) 2022 Andrzej Więckowski.
- **Unity 6000.3 не тестировалась**. Потребуется аудит API Burst/Collections и git dependencies.

## Интеграция (план, НЕ выполнен)
1. Изолированный проект на 2021.2.0f1, затем отдельная копия для 6000.3.
2. Зафиксировать git commit и `packages-lock.json`; отдельно проверить лицензии BurstCollections и BurstMathUtils.
3. Сравнить 100/1000/5000 boids, Burst on/off, brute-force vs tree; записать profiler и Player Build.
4. Добавить собственное avoidance и steering arbitration; не утверждать поддержку мобильных/WebGL без тестов.

**Рекомендация:** референс оптимизации большого количества агентов на CPU, не plug-and-play Unity 6.

**Доказательства:** [README](https://github.com/andywiecko/Flocking/blob/main/README.md), [ProjectVersion](https://github.com/andywiecko/Flocking/blob/main/ProjectSettings/ProjectVersion.txt), [manifest](https://github.com/andywiecko/Flocking/blob/main/Packages/manifest.json), [LICENSE](https://github.com/andywiecko/Flocking/blob/main/LICENSE.md).
