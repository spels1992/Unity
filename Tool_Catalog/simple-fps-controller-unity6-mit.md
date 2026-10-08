# Unity First Person Controller (yahiawork)

**Правило внедрения: только 0 ₽.** [FREE_ONLY_POLICY](../FREE_ONLY_POLICY.md). **Готовность и Editor tests:** не проводились.

## Название
Unity First Person Controller (yahiawork)

## Категория и жанры
FPS controller / 3D movement

## Назначение и уже готовые системы
Небольшой готовый FPS controller для Unity 6 с мышиной камерой, ходьбой, ускорением, crouch, jump, gravity, smooth acceleration и cursor lock.

## Официальная страница/GitHub
https://github.com/yahiawork/The-First-Person-Controller-Unity-6

## Как получить/подключить
Clone/Download ZIP; README содержит подробные шаги по добавлению CharacterController + Script на Player. Проект не UPM package.

## Документация/демо
https://github.com/yahiawork/The-First-Person-Controller-Unity-6#readme

## Лицензия и условия
MIT из корневого LICENSE, прочитан.

## Цена
0 ₽; README прямо говорит no extra packages. Исключить коммерческие ассеты, если не лицензированы.

## Совместимость Unity
README Unity 6, но репо состоит из 4 файлов и не содержит полного Unity project/ProjectVersion.txt — exact Editor version НЕ УСТАНОВЛЕНА.

## Зависимости
Встроенный UnityEngine.CharacterController, classic Input Manager (смотреть README Project Settings → Input Manager); New Input System в Future Ideas, не реализован.

## Совместимость с другими решениями
Не сочетать вслепую с Unity Input System-only проектом, нужна конверсия ввода; FPS обстрел/оружие/NPC не входят.

## Плюсы
Простой MIT скрипт, удобно изучить и адаптировать; без сложного фреймворка.

## Недостатки и ограничения
Только 4 коммита и очень маленький набор; недостаёт New Input System, weapon system, stamina, тестов. Долго не считать production ready.

## ИИ автоматизация
AI может адаптировать классический ввод к Unity Input System, прогнать тесты разных FPS/коллизий.

## Оценка
ЗАПАСНОЙ ПРОСТОЙ БЕСПЛАТНЫЙ КОНТРОЛЛЕР, не приоритет цельной FPS игре

## Последняя проверка
2026-10-08

## Статус
Изучено GitHub README, LICENSE, metadata; не проверено в живом Unity Editor.

## Перед использованием
1. Проверить точный snapshot/tag, ThirdParty NOTICE, версии редактора и стоимость всех зависимостей.
2. Установить в изолированном проекте без платных дополнений.
3. Проверить Editor Console, demo scene, управление, PlayMode, Player build, performance.
4. Занести реальные версии/тест в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md), затем повышать статус.
