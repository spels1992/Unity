# Street Racing Unity

**Фильтр: 0 ₽ дополнительных расходов, законное переиспользование.** Источник изучен по GitHub — работоспособность в нашем Unity Editor НЕ тестировалась.

## Название
Street Racing Unity

## Назначение/тип
3D тайм-триал racing учебная игра

## Авторский проект
https://github.com/is-cout/street-racing-unity

## Описание функций
Готовый loop гонки на время, автомобиль, дороги, WebGL play example.

## Скачать
https://github.com/is-cout/street-racing-unity (README → clone/download)

## Лицензия
MIT root LICENSE для кода, Unity Asset Store EULA отдельно для Cartoon Car Vehicle Pack и Low Poly Road Pack

## Стоимость
0 ₽ за MIT код; модели/дороги официально отмечены как free Asset Store на момент README, текущая цена и лицензии не проверены — нельзя объявлять бесплатным пакетом без новой проверки.

## Editor compatibility
2020.3.25f1 по ProjectVersion и README 2020.3+

## Зависимости
Cartoon Car Vehicle Pack; Low Poly Road Pack; Unity WebGL build sample (условия скачать отдельно)

## Совместимость/интеграции
Таймер/гонка/зоны, проще чем PolyRace и менее подходит для сетевых гонок.

## Инструкция
Git clone → Unity Hub открыть Programming-Theory, Unity 2020.3; исходные Asset Store packs скачивать только если бесплатно доступны по действующей EULA; иначе заменить на Kenney/Quaternius CC0 models.

## Преимущества
Готовый loop гонки на время, автомобиль, дороги, WebGL play example.

## Недостатки и риски
Школьный учебный проект, старый Unity, не physics system общего назначения, зависим от лицензии двух Store ассетов.

## AI-автоматизация
Модели/скрипты/параметры можно изучать и автоматизировать через разрешённый Unity Editor API, но без платных AI API и без добавления чужих binaries в GitHub.

## Оценка
ХОРОШИЙ LEARNING REFERENCE, для production выбрать отдельно лицензированные 0 ₽ модели

## Дата проверки
2026-10-08

## Статус
README, MIT, ProjectVersion прочитаны, Store EULA/цены не проверены, Editor не тестировался

## Отдельный validation gate
1. Уточнить все third-party LICENSE и платные/квотные внешние зависимости.
2. Зафиксировать commit SHA и точную версию Unity, скачать только при подтверждённом нулевом бюджете.
3. Запустить изолированную scene, Console + PlayMode + Windows Build без изменения чужих пользовательских сцен.
4. Занести тест и конфликты в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md). Не называть документальную проверку словом TESTED.

[Глобальное правило ZERO COST](../FREE_ONLY_POLICY.md).
