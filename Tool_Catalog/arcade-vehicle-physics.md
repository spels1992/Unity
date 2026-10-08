# ArcadeVehiclePhysics

**Фильтр: 0 ₽ дополнительных расходов, законное переиспользование.** Источник изучен по GitHub — работоспособность в нашем Unity Editor НЕ тестировалась.

## Название
ArcadeVehiclePhysics

## Назначение/тип
Готовая arcade physics автомобиля

## Авторский проект
https://github.com/benmcinnes/ArcadeVehiclePhysics

## Описание функций
Скрипты физики аркадного авто, дрифтов и экзотических трюков; input через legacy Unity Input Manager.

## Скачать
https://github.com/benmcinnes/ArcadeVehiclePhysics (README → clone/download)

## Лицензия
MIT на root code, внешний Sketchfab muscle-car model требует отдельной лицензии/источника

## Стоимость
Основные scripts доступны без оплаты по MIT; модель со Sketchfab отдельно, заменить на CC0 Kenney для отсутствия скрытой цены.

## Editor compatibility
2018.4.5f1 по README и ProjectVersion

## Зависимости
Unity built-in physics, старый Input Manager, Cinemachine; сторонняя Sketchfab модель для образцовой сцены

## Совместимость/интеграции
Аркадное ускорение/занос и силы в Rigidbody, адаптировать отдельно.

## Инструкция
Скачать репозиторий в отдельно созданную Unity 2018.4 sample или извлечь только MIT scripts по лицензии; при переносе в Unity6 проверить Rigidbody/camera/Input и установить свежий бесплатный Cinemachine.

## Преимущества
Скрипты физики аркадного авто, дрифтов и экзотических трюков; input через legacy Unity Input Manager.

## Недостатки и риски
Старый Editor, 0.1V и нерегулярное развитие; tutorial code ≠ robust VehicleController; совместимость с Unity 6 не тестировалась.

## AI-автоматизация
Модели/скрипты/параметры можно изучать и автоматизировать через разрешённый Unity Editor API, но без платных AI API и без добавления чужих binaries в GitHub.

## Оценка
УЧЕБНЫЙ РЕФЕРЕНС по arcade physics, не современный turnkey kit

## Дата проверки
2026-10-08

## Статус
LICENSE, README и ProjectVersion прочитаны; Unity6 не тестировалась

## Отдельный validation gate
1. Уточнить все third-party LICENSE и платные/квотные внешние зависимости.
2. Зафиксировать commit SHA и точную версию Unity, скачать только при подтверждённом нулевом бюджете.
3. Запустить изолированную scene, Console + PlayMode + Windows Build без изменения чужих пользовательских сцен.
4. Занести тест и конфликты в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md). Не называть документальную проверку словом TESTED.

[Глобальное правило ZERO COST](../FREE_ONLY_POLICY.md).
