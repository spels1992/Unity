# Multiplayer-FPS (Armour)

**Фильтр: 0 ₽ дополнительных расходов, законное переиспользование.** Источник изучен по GitHub — работоспособность в нашем Unity Editor НЕ тестировалась.

## Название
Multiplayer-FPS (Armour)

## Назначение/тип
Большой multiplayer FPS пример

## Авторский проект
https://github.com/Armour/Multiplayer-FPS

## Описание функций
Lobby/name/room, player HP, weapon fire, blend tree movement, network rooms via Photon Unity Networking 2.

## Скачать
https://github.com/Armour/Multiplayer-FPS (README → clone/download)

## Лицензия
MIT root LICENSE для кода; Photon PUN2, Mixamo characters и Asset Store оружие имеют отдельные условия, требующие проверки

## Стоимость
MIT код бесплатен, но полноценный multiplayer зависит от сервиса Photon PUN2 с собственными тарифами/квотами, а ассеты не покрываются только MIT.

## Editor compatibility
2022.3.55f1 (ProjectVersion and README)

## Зависимости
Photon Unity Networking 2, Mixamo animations, Unity Asset Store gun model, Unity physics

## Совместимость/интеграции
UI multiplayer lobby, player movement state, combat animations; не копировать всё целиком без лицензий.

## Инструкция
Использовать преимущественно как архитектурный референс кода; Photon имеет внешние облачные тарифы/лимиты, не допускать его как незаменимый production backend. При тесте только free offline/test if legally supported.

## Преимущества
Lobby/name/room, player HP, weapon fire, blend tree movement, network rooms via Photon Unity Networking 2.

## Недостатки и риски
Большой репозиторий (~795 MB), старые периферийные ветки с 2020 не поддерживаются, Photon PUN2 и Mixamo/Asset Store лицензии надо проверять. Не zero-cost гарантированная multiplayer основа.

## AI-автоматизация
Модели/скрипты/параметры можно изучать и автоматизировать через разрешённый Unity Editor API, но без платных AI API и без добавления чужих binaries в GitHub.

## Оценка
REFERENCE_ONLY по многопользовательскому FPS, лучше смотреть [Mirror](mirror-networking.md) при выборе free self-host

## Дата проверки
2026-10-08

## Статус
LICENSE, README, ProjectVersion, Photon requirements verified; actual Photon costs and Unity Editor not tested

## Отдельный validation gate
1. Уточнить все third-party LICENSE и платные/квотные внешние зависимости.
2. Зафиксировать commit SHA и точную версию Unity, скачать только при подтверждённом нулевом бюджете.
3. Запустить изолированную scene, Console + PlayMode + Windows Build без изменения чужих пользовательских сцен.
4. Занести тест и конфликты в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md). Не называть документальную проверку словом TESTED.

[Глобальное правило ZERO COST](../FREE_ONLY_POLICY.md).
