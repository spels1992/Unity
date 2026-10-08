# PolyRace — futuristic hover racing game

**Фильтр: 0 ₽ дополнительных расходов, законное переиспользование.** Источник изучен по GitHub — работоспособность в нашем Unity Editor НЕ тестировалась.

## Название
PolyRace — futuristic hover racing game

## Назначение/тип
Целая 3D arcade sci-fi racing game (legacy)

## Авторский проект
https://github.com/vthem/PolyRace

## Описание функций
Четыре hovercraft с разной физикой, процедурная трасса (холмы, долины), shield, локальный racing loop; онлайн режимы удалены из GitHub версии.

## Скачать
https://github.com/vthem/PolyRace (README → clone/download)

## Лицензия
Root License = MIT для собственного кода; README перечисляет сторонние модели/музыку, DOTween, LibNoise.Unity под LGPL и другие авторские источники.

## Стоимость
Доступ к исходникам бесплатен, но MIT корня НЕ разрешает автоматически перепродавать/перераспространять сторонние racer meshes, музыку и другие ассеты.

## Editor compatibility
2020.3.25f1 (README и ProjectVersion совпадают); Blender 3.0 требуется для импорта 3D assets

## Зависимости
DOTween, LibNoise.Unity LGPL, MeshFragmentation, Blender, модели/музыка и шрифты; лицензии отдельно

## Совместимость/интеграции
Пример сцены с транспортной физикой, racing level generation и управлением, полезен для изучения архитектуры.

## Инструкция
Клонировать отдельно, Blender 3.0 (по README), Unity 2020.3.25f1, сцена Scenes/Main_Scene; для современных Unity искать совместимость URP/shaders и перепроверять весь third-party контент.

## Преимущества
Четыре hovercraft с разной физикой, процедурная трасса (холмы, долины), shield, локальный racing loop; онлайн режимы удалены из GitHub версии.

## Недостатки и риски
Legacy Editor 2020, online gameplay вырезан, third-party licensing неоднороден (LGPL LibNoise/отдельная музыка), UNITY6 UNKNOWN.

## AI-автоматизация
Модели/скрипты/параметры можно изучать и автоматизировать через разрешённый Unity Editor API, но без платных AI API и без добавления чужих binaries в GitHub.

## Оценка
УЧЕБНАЯ КОМПЛЕКСНАЯ ИГРА, не чистый zero-risk production starter

## Дата проверки
2026-10-08

## Статус
README и root LICENSE, ProjectVersion, наличие LGPL file проверены; не тестировалось

## Отдельный validation gate
1. Уточнить все third-party LICENSE и платные/квотные внешние зависимости.
2. Зафиксировать commit SHA и точную версию Unity, скачать только при подтверждённом нулевом бюджете.
3. Запустить изолированную scene, Console + PlayMode + Windows Build без изменения чужих пользовательских сцен.
4. Занести тест и конфликты в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md). Не называть документальную проверку словом TESTED.

[Глобальное правило ZERO COST](../FREE_ONLY_POLICY.md).
