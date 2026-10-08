# Project Wanderer

**Фильтр: 0 ₽ дополнительных расходов, законное переиспользование.** Источник изучен по GitHub — работоспособность в нашем Unity Editor НЕ тестировалась.

## Название
Project Wanderer

## Назначение/тип
Сюжетно-нейтральная 3D survival/sandbox demo

## Авторский проект
https://github.com/RaunakGameDev/Project-Wanderer

## Описание функций
Ресурсы: рубка деревьев, добыча камня и железа; inventory/hotbar/stack; крафт рецептов, прочность инструментов, сундуки, day-night, JSON save/load, процедурное размещение ресурсов.

## Скачать
https://github.com/RaunakGameDev/Project-Wanderer (README → clone/download)

## Лицензия
MIT корневой LICENSE; Assets/Resources/StarterAssets/license.txt = Unity Companion License

## Стоимость
0 ₽ за открытый код, но прежде чем переиспользовать StarterAssets, выполнить условия Unity Companion License; лицензии остальных художественных ассетов проверять отдельно.

## Editor compatibility
6000.3.13f1 (фактический ProjectVersion.txt)

## Зависимости
Unity 6 + TextMeshPro + Unity Input System, ScriptableObjects и JSON (по README)

## Совместимость/интеграции
Gameplay loop: gather → store → craft → improve tools → expand; events/separation of UI and persistence требуют практического изучения.

## Инструкция
Клонировать в отдельный проект; Unity Hub выбрать Unity 6000.3.13f1 или совместимую после проверки; открыть сцену по README/дереву; оценить взаимодействия, craft, save/load; сверить Asset Store/Unity Companion отдельно.

## Преимущества
Ресурсы: рубка деревьев, добыча камня и железа; inventory/hotbar/stack; крафт рецептов, прочность инструментов, сундуки, day-night, JSON save/load, процедурное размещение ресурсов.

## Недостатки и риски
Молодой небольшой портфолио-проект, заявлен функционал README, а не QA; не MMO, нет доказанной готовой сетевой части и production build.

## AI-автоматизация
Модели/скрипты/параметры можно изучать и автоматизировать через разрешённый Unity Editor API, но без платных AI API и без добавления чужих binaries в GitHub.

## Оценка
ПРИОРИТЕТНЫЙ КАНДИДАТ для изучения готового survival gameplay loop

## Дата проверки
2026-10-08

## Статус
README, MIT root и Unity Companion StarterAssets license, ProjectVersion проверены; Editor НЕ ТЕСТИРОВАЛСЯ

## Отдельный validation gate
1. Уточнить все third-party LICENSE и платные/квотные внешние зависимости.
2. Зафиксировать commit SHA и точную версию Unity, скачать только при подтверждённом нулевом бюджете.
3. Запустить изолированную scene, Console + PlayMode + Windows Build без изменения чужих пользовательских сцен.
4. Занести тест и конфликты в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md). Не называть документальную проверку словом TESTED.

[Глобальное правило ZERO COST](../FREE_ONLY_POLICY.md).
