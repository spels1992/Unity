# TLabVehiclePhysics

**Фильтр: 0 ₽ дополнительных расходов, законное переиспользование.** Источник изучен по GitHub — работоспособность в нашем Unity Editor НЕ тестировалась.

## Название
TLabVehiclePhysics

## Назначение/тип
Pacejka WheelCollider / racing simulation toolkit

## Авторский проект
https://github.com/TLabAltoh/TLabVehiclePhysics

## Описание функций
Pacejka tire physics, slip angle/ratio, LUT/force, downforce torque curves, wheel collider alternative, screenshot examples.

## Скачать
https://github.com/TLabAltoh/TLabVehiclePhysics (README → clone/download)

## Лицензия
MIT root LICENSE.md; встроены git submodules TLabCurveTool, Unity-SDF-UI-Toolkit, TLab-Spline: лицензии ВСЕХ сабмодулей ещё не подтверждены, внедрение блокируется

## Стоимость
MIT core бесплатен; проверка вложенных submodules обязательна для законного zero-cost внедрения. Buy Me a Coffee — добровольная поддержка, не покупать.

## Editor compatibility
2022.3.19f1 (фактический ProjectVersion)

## Зависимости
TLabCurveTool, Unity-SDF-UI-Toolkit, TLab-Spline, Unity physics, custom shader/tooling

## Совместимость/интеграции
Pacejka tire curves and LUT tunables; при сравнении с ArcadeVehiclePhysics нужны контролируемые одинаковые тесты.

## Инструкция
Перед клоном проверить права ВСЕХ .gitmodules и required dependencies. Затем git submodule update --init, открыть на Unity 2022.3.19f1, прогнать локальную ездую сцену без облака.

## Преимущества
Pacejka tire physics, slip angle/ratio, LUT/force, downforce torque curves, wheel collider alternative, screenshot examples.

## Недостатки и риски
Сложная физика колёс, .gitmodules, большой размер репозитория (~427 MB GitHub metadata), Unity6 port unknown, не готовая arcade racing game.

## AI-автоматизация
Модели/скрипты/параметры можно изучать и автоматизировать через разрешённый Unity Editor API, но без платных AI API и без добавления чужих binaries в GitHub.

## Оценка
RESEARCH_ONLY до лицензий всех сабмодулей; перспективен для реалистичной физики

## Дата проверки
2026-10-08

## Статус
MIT LICENSE, README, .gitmodules, ProjectVersion проверены; submodule license audit НЕ ЗАВЕРШЁН

## Отдельный validation gate
1. Уточнить все third-party LICENSE и платные/квотные внешние зависимости.
2. Зафиксировать commit SHA и точную версию Unity, скачать только при подтверждённом нулевом бюджете.
3. Запустить изолированную scene, Console + PlayMode + Windows Build без изменения чужих пользовательских сцен.
4. Занести тест и конфликты в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md). Не называть документальную проверку словом TESTED.

[Глобальное правило ZERO COST](../FREE_ONLY_POLICY.md).
