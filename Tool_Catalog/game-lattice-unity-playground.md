# Game Lattice Unity Playground

**Правило внедрения: только 0 ₽.** [FREE_ONLY_POLICY](../FREE_ONLY_POLICY.md). **Готовность и Editor tests:** не проводились.

## Название
Game Lattice Unity Playground

## Категория и жанры
Готовый обучающий RPG/AI/quests пример

## Назначение и уже готовые системы
Целый демонстрационный Unity6 проект с девятью уроками, JSON hot reload, визуальной top-down картой и отладочным окном событий. Не полноценная игра, а готовая песочница.

## Официальная страница/GitHub
https://github.com/Toxic-Cookie/game-lattice-unity-example

## Как получить/подключить
Clone repo и открыть Unity project Unity 6000.4.11f1, не импортировать в активный проект без аудит package.

## Документация/демо
https://github.com/Toxic-Cookie/game-lattice-unity-example#readme

## Лицензия и условия
Корневой Apache-2.0, внутри Packages/com.gamelattice.lattice/LICENSE.md также Apache-2.0; исключения сторонних зависимостей проверять.

## Цена
0 ₽ за код и local Unity project; Runtime сама без облаков.

## Совместимость Unity
ProjectVersion.txt: 6000.4.11f1 (README говорит 6000.4, не автоматически Unity 6000.3)

## Зависимости
Embedded com.gamelattice.lattice package, precompiled netstandard2.1 binaries, optional dialogue Yarn

## Совместимость с другими решениями
Известный конфликт из README: дубликат Microsoft.CSharp.dll вызывает CS1703; в embedded copy этот dll уже убран. Это подтверждённый upstream conflict, не наш live test.

## Плюсы
9 практических уроков с quest/dialogue, items/effects, formulas, AI, hot reload; реальная демонстрация framework.

## Недостатки и ограничения
Без собственной игровой сцены/арт-контента; менеджмент precompiled DLL и редакторные версии нужно тестировать.

## ИИ автоматизация
Данные JSON удобно генерировать и тестировать агентами, но оставлять редакторные permissions ограниченными.

## Оценка
ПЕРВОЕ, ЧТО ТЕСТИРОВАТЬ ПЕРЕД ВНЕДРЕНИЕМ Game Lattice

## Последняя проверка
2026-10-08

## Статус
Изучено GitHub README, LICENSE, metadata; не проверено в живом Unity Editor.

## Перед использованием
1. Проверить точный snapshot/tag, ThirdParty NOTICE, версии редактора и стоимость всех зависимостей.
2. Установить в изолированном проекте без платных дополнений.
3. Проверить Editor Console, demo scene, управление, PlayMode, Player build, performance.
4. Занести реальные версии/тест в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md), затем повышать статус.
