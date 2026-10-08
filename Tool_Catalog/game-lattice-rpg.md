# Game Lattice

**Правило внедрения: только 0 ₽.** [FREE_ONLY_POLICY](../FREE_ONLY_POLICY.md). **Готовность и Editor tests:** не проводились.

## Название
Game Lattice

## Категория и жанры
RPG engine / AI NPC / quests / data-driven

## Назначение и уже готовые системы
Не просто quest scripts, а большая engine-agnostic RPG simulation платформа: JSON def registry, effect/condition/event vocabulary, NPC AI от FSM до GOAP/HTN, quests, dialogue, weather, deterministic world state.

## Официальная страница/GitHub
https://github.com/Toxic-Cookie/game-lattice

## Как получить/подключить
Официальная упаковка packaging/unity/upm (не путать с прямой ссылкой на NuGet); Unity example https://github.com/Toxic-Cookie/game-lattice-unity-example

## Документация/демо
https://github.com/Toxic-Cookie/game-lattice-unity-example ; https://github.com/Toxic-Cookie/game-lattice/blob/main/docs/llm-guide.md

## Лицензия и условия
Apache-2.0 из корневого LICENSE, пакет com.gamelattice.lattice также Apache-2.0. Для чужих зависимостей / .dll отдельно inspect notices.

## Цена
0 ₽ за исходники и запуск локальных примеров; платные облачные/серверные функции не требуются авторским README

## Совместимость Unity
UPM metadata: unity 2021.2 minimum, package version 0.0.0-dev. Тестовый playground реально имеет ProjectVersion 6000.4.11f1, но наш Editor ещё не тестировал.

## Зависимости
Pure netstandard2.1, Unity host адаптеры clock, navigation, animation, physics; Yarn dialogue bridge возможен, требуется Yarn package. Поставляется precompiled DLL, проверить license внутри сборки.

## Совместимость с другими решениями
Пример Game Lattice Playground + Yarn: upstream показывает интеграцию. Только этот пример заявлен, с Moonforge не совмещать два engines без архитектурного обоснования.

## Плюсы
Большой мультисистемный стек, контент генерируется JSON без C# changes; пять уровней NPC AI, квесты и предметы.

## Недостатки и ограничения
Версия 0.0.0-dev, небольшой комьюнити, host адаптеры/JSON схема сложнее стандартной Unity, риск конфликтов DLL Microsoft.CSharp CS1703, разные gameplay semantics.

## ИИ автоматизация
LLM может создавать JSON definitions и проверять Golden deterministic transcripts без оплаченного API.

## Оценка
ПЕРСПЕКТИВНЫЙ БОЛЬШОЙ БЕСПЛАТНЫЙ RPG FRAMEWORK, сначала проверить upstream sample

## Последняя проверка
2026-10-08

## Статус
Изучено GitHub README, LICENSE, metadata; не проверено в живом Unity Editor.

## Перед использованием
1. Проверить точный snapshot/tag, ThirdParty NOTICE, версии редактора и стоимость всех зависимостей.
2. Установить в изолированном проекте без платных дополнений.
3. Проверить Editor Console, demo scene, управление, PlayMode, Player build, performance.
4. Занести реальные версии/тест в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md), затем повышать статус.
