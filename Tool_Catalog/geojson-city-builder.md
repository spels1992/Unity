# GeoJSON City Builder

**Фильтр: 0 ₽ дополнительных расходов, законное переиспользование.** Источник изучен по GitHub — работоспособность в нашем Unity Editor НЕ тестировалась.

## Название
GeoJSON City Builder

## Назначение/тип
Генерация городского окружения по GeoJSON

## Авторский проект
https://github.com/ElmarJ/GeoJsonCityBuilder

## Описание функций
Генерация экструзии зданий из GeoJSON полигонов, prefab размещение по геоточкам, origin lat/long. НЕ city-management game и нет экономики.

## Скачать
https://github.com/ElmarJ/GeoJsonCityBuilder (README → clone/download)

## Лицензия
MIT на основной пакет; лицензия обязательной зависимости com.virgis.geojson.net 1.2.17 требует отдельного подтверждения

## Стоимость
MIT код 0 ₽, но открытый вопрос лицензии и доступности com.virgis.geojson.net (обязательная зависимость) — НЕ ГОТОВ К ВНЕДРЕНИЮ пока не проверено.

## Editor compatibility
package.json 0.4.3: минимальная Unity 2019.1; Unity 6 не тестировалась

## Зависимости
com.unity.probuilder=4.5.2; com.virgis.geojson.net=1.2.17; package.json

## Совместимость/интеграции
Зависит от полигонов, высот, границ и геодезических данных; нужны source-rights и корректные координаты.

## Инструкция
Unity UPM git URL https://github.com/ElmarJ/GeoJsonCityBuilder.git или OpenUPM; сначала убедиться, что com.unity.probuilder 4.5.2 и com.virgis.geojson.net 1.2.17 доступны бесплатно и законно; загрузить разрешённый GeoJSON.

## Преимущества
Генерация экструзии зданий из GeoJSON полигонов, prefab размещение по геоточкам, origin lat/long. НЕ city-management game и нет экономики.

## Недостатки и риски
Древняя минимальная версия; реальный импорт GeoJSON зависит от лицензии источника карт/координат и условий OpenStreetMap/других данных. Не путать с полной city-building игрой.

## AI-автоматизация
Модели/скрипты/параметры можно изучать и автоматизировать через разрешённый Unity Editor API, но без платных AI API и без добавления чужих binaries в GitHub.

## Оценка
RESEARCH_ONLY до подтверждения лицензии обязательной зависимости; затем тестовый генератор окружения

## Дата проверки
2026-10-08

## Статус
LICENSE, README, package.json прочитаны; обязательный dependency license не подтверждён; Editor не тестировался

## Отдельный validation gate
1. Уточнить все third-party LICENSE и платные/квотные внешние зависимости.
2. Зафиксировать commit SHA и точную версию Unity, скачать только при подтверждённом нулевом бюджете.
3. Запустить изолированную scene, Console + PlayMode + Windows Build без изменения чужих пользовательских сцен.
4. Занести тест и конфликты в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md). Не называть документальную проверку словом TESTED.

[Глобальное правило ZERO COST](../FREE_ONLY_POLICY.md).
