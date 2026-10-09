# Boids — Sebastian Lague (legacy teaching project)

**Категория:** AI / NPC, обучение flocking.  
**Первоисточник:** https://github.com/SebLague/Boids  
**Автор:** Sebastian Lague. **Проверено:** 2026-10-09.  
**Статус:** DOCUMENTED / LEGACY / NOT_RUN. **Стоимость исходников:** 0 ₽; не использовать облачные сервисы.

## Готовые функции
- Наглядная реализация boids (alignment, cohesion, separation), учебное видео.
- README сам рекомендует ECS sample от Unity как более производительный вариант.
- Не готовая система игрового врага/путь до цели.

## Проверенные технические данные
- `ProjectSettings/ProjectVersion.txt`: **Unity 2019.1.3f1** (revision `dc414eb9ed43`).
- `Packages/manifest.json`: `com.unity.ads` **2.0.8**, `com.unity.analytics` **3.3.2**, `com.unity.purchasing` **2.0.6**, `com.unity.textmeshpro` **2.0.0**, `com.unity.timeline` **1.0.0**.
- `LICENSE`: **MIT**, Copyright (c) 2019 Sebastian Lague.
- **Важно для правила 0 ₽:** старый manifest содержит Ads/Analytics/IAP. Не активировать, не настраивать и не переносить эти сервисы; прежде чем рассматривать проект как основу, подготовить изолированную копию с удалением необязательных пакетов и проверкой, что демо не зависит от них.
- **Unity 6000.3 не тестировалась**; прямой импорт в текущий игровой проект не рекомендован.

## План отдельного теста (НЕ выполнялся)
- Запуск в исторической Unity 2019.1.3f1, контроль отсутствия сервисных ключей/запросов, затем чистая копия алгоритма в современном пустом проекте с MIT notice.
- Измерить FPS/число boids и сравнить с более современными Burst/Jobs вариантами.

**Рекомендация:** только алгоритмический учебный референс, не базовый starter kit для Unity 6.

**Доказательства:** [README](https://github.com/SebLague/Boids/blob/master/README.md), [ProjectVersion](https://github.com/SebLague/Boids/blob/master/ProjectSettings/ProjectVersion.txt), [manifest](https://github.com/SebLague/Boids/blob/master/Packages/manifest.json), [LICENSE](https://github.com/SebLague/Boids/blob/master/LICENSE).
