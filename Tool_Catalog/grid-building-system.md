# Grid Building System

**Фильтр: 0 ₽ дополнительных расходов, законное переиспользование.** Источник изучен по GitHub — работоспособность в нашем Unity Editor НЕ тестировалась.

## Название
Grid Building System

## Назначение/тип
3D construction/factory/city builder framework

## Авторский проект
https://github.com/DanielJDeng1/Grid-Building-System

## Описание функций
Размещение пола, потолков, мебели, стен и проёмов, дверей, лестниц/лифтов; dynamic mesh chunking; многоэтажный A* с очередью; JSON save/load, prefab/state.

## Скачать
https://github.com/DanielJDeng1/Grid-Building-System (README → clone/download)

## Лицензия
MIT root LICENSE (текст прочитан), third-party art отдельно

## Стоимость
MIT исходники доступны 0 ₽; подтвердить лицензии демонстрационных ассетов и свои источники контента.

## Editor compatibility
6000.3.16f1 (ProjectVersion.txt + README)

## Зависимости
Unity 6; runtime mesh and custom A*, JSON, prefab dependencies из проекта

## Совместимость/интеграции
Single owner placement and save; multi-floor links; batching of rebuild and frame budget.

## Инструкция
Клонировать отдельно; открыть Assets/Scenes/SampleScene.unity на 6000.3.16f1; создать multi-floor building, проверить preview/collision/pathfinding и save-load; не подменять навигацию отдельным AI Navigation без адаптера.

## Преимущества
Размещение пола, потолков, мебели, стен и проёмов, дверей, лестниц/лифтов; dynamic mesh chunking; многоэтажный A* с очередью; JSON save/load, prefab/state.

## Недостатки и риски
Новый небольшой проект, самостоятельный навигационный grid pipeline, несовместимость из коробки с NavMesh возможна; не полная экономическая игра и не MMO.

## AI-автоматизация
Модели/скрипты/параметры можно изучать и автоматизировать через разрешённый Unity Editor API, но без платных AI API и без добавления чужих binaries в GitHub.

## Оценка
ПЕРСПЕКТИВЕН для конструкторов, colony sims, строительства баз

## Дата проверки
2026-10-08

## Статус
README, LICENSE и ProjectVersion проверены, PlayMode/Build отсутствуют

## Отдельный validation gate
1. Уточнить все third-party LICENSE и платные/квотные внешние зависимости.
2. Зафиксировать commit SHA и точную версию Unity, скачать только при подтверждённом нулевом бюджете.
3. Запустить изолированную scene, Console + PlayMode + Windows Build без изменения чужих пользовательских сцен.
4. Занести тест и конфликты в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md). Не называть документальную проверку словом TESTED.

[Глобальное правило ZERO COST](../FREE_ONLY_POLICY.md).
