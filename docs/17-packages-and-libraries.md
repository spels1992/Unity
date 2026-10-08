# 17. Каталог библиотек, пакетов и инструментов Unity

**Первый проход:** 2026-10-08. **Статус:** кандидаты для тестирования, не готовый рекомендованный production-стек. **Не импортировать/не копировать** чужие репозитории или ассеты без проверки лицензий и необходимости.

## Как устанавливать пакеты
`Window → Package Manager`: выбрать `Unity Registry`, `In Project`, `My Assets` или добавить пакет по поддерживаемому источнику (Git URL/локальная папка). Часть ресурсов Asset Store ставится как `.unitypackage`, другие — как UPM; формат установки отличается. Проверять работу пакета после импортирования на чистой сцене.

Источники: [Find packages](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/upm-ui-window/upm-ui-find), [Package sources](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages/upm-concepts), [Asset Store packages](https://docs.unity.com/en-us/engine/6000.3/manual/assets-and-media/asset-store/downloads/packages).

## Стартовая матрица (есть официальный источник, но совместимость проверяется под наш проект)

| Пакет / инструмент | Для чего | Статус проверки | Ссылка |
|---|---|---|---|
| **Input System** (`com.unity.inputsystem`) | Клавиатура, геймпад, касания, переназначение действий | Официальный Unity package; для Unity 6.3 в каталоге указана линия 1.20.x; тесты в нашем проекте не проведены | [Unity Docs](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-inputsystem) |
| **URP** | Универсальный современный рендер для многих 2D/3D игр | Подбирать через шаблон и Package Manager, платформа/Shader compatibility не проверены | [Unity 6 Resources](https://unity.com/campaign/unity-6-resources) |
| **Addressables** | Адресуемый доступ к ассетам и управление контентом | Обязательная версия и схема доставки ещё не выбраны | [UPM mirror, не первоисточник](https://github.com/needle-mirror/com.unity.addressables) |
| **Unity Test Framework** | EditMode/PlayMode тестирование | Проверить Editor-compatible выпуск, тест-runner и CI | [Unity Package Manager](https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/upm-ui-window/upm-ui-find) |
| **Cinemachine 3** | Камеры, слежение и кинематография | **В Unity 6.6 становится core package; миграция с Cinemachine 2 несёт breaking changes** | [Upgrade 6.6](https://docs.unity.com/en-us/engine/6000.6/manual/upgrade-guides/upgrade-guide-unity66) |
| **DOTS / Entities / Jobs / Burst** | Массовые сущности/параллельные вычисления | **Не нужна в простом первом прототипе**; образцы DOTS 101 основаны на Unity 6.2 + пакеты 1.4 | [Официальные DOTS Samples](https://github.com/Unity-Technologies/EntityComponentSystemSamples) |
| **UniTask (Cysharp)** | Async/await, интегрированный с жизненным циклом Unity | Сторонняя Git-библиотека, **кандидат**, требуется проверка лицензии/версии под Unity 6.3/6.6 | [Original GitHub](https://github.com/Cysharp/UniTask) |

## Рабочие правила выбора
1. **Проблема перед пакетом.** Сначала написать, какое конкретное требование пакет закроет и можно ли обойтись встроенным API.
2. **В первую очередь официальные Unity Registry packages** — если они подходят, сокращается зависимость от сторонних разработчиков.
3. Сторонний пакет — смотреть оригинальный репозиторий, LICENSE, выпуск, issues, безопасность и фиксировать tag/commit (не `main`).
4. Проверять совместимость с Editor/платформой/URP/HDRP и лицензией **по состоянию на дату установки**, а не по названию пакета.
5. Если бесплатность не доказана — цена **не определена**; платную подписку не включать без осознанного решения.
6. Импортировать только по одному пакету, тестировать минимальный сценарий, сверять влияние на сборку и FPS, сохранять rollback commit.
7. Отличать **mirror** от upstream: `needle-mirror` удобно для чтения Unity UPM-пакетов, но не официальный репозиторий издателя Unity.

## Пример исследования сторонней библиотеки: UniTask
- **Факт (по README):** библиотека расширяет асинхронность Unity, умеет устанавливаться по Git URL в UPM.
- **Применение:** потенциально удобна для загрузок/ожиданий/таймеров с отменой.
- **Риски:** управление отменой и жизненным циклом UnityObject; конфликт версий; сложность отладки; лицензия и версия на целевом Editor ещё не проверены.
- **Решение:** пока **отложить**. Учебный прототип может использовать корутины или встроенный async там, где это соответствует API и требованиям.

## Шаблон проверки следующего инструмента
```text
Имя/URL:
Первичный производитель:
Версия/release date:
Editor + платформа + рендер:
Лицензия/attribution:
Цена/лимиты:
Как ставить:
Сценарий применения:
Пример запуска:
Как удалить/откатить:
Метрика сравнения с встроенным решением:
Прошёл тест на реальном проекте? [нет/да и commit]
Решение: принять / пилот / отложить / отказаться
```

## Следующие направления каталога
- Устройство ввода и UI: Input System, UI Toolkit, uGUI, TextMeshPro.
- Камеры и анимация: Cinemachine, Timeline, Animation Rigging.
- Уровни и навигация: ProBuilder, AI Navigation, генераторы контента.
- Ассеты: Addressables, оптимизация импорта, Unity Localization.
- Профилирование/тесты: Profiler, Profile Analyzer, Test Framework.
- Сеть: Netcode for GameObjects, Multiplayer Services и *сравнение с Mirror/FishNet*.
- 2D: Sprite, Tilemap, 2D Animation, URP 2D.
- Внешние инструменты: Blender, Krita, Audacity — изучить реальные экспорты и лицензии отдельно.

## Обнаруженные ограничения
Не проводилось тестирования библиотек в настоящем Unity-проекте; не проверены все LICENSE и поддержка всех инструментов; запрещено делать вывод о полной готовности этого списка.
