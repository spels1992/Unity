# Unity Modular Inventory System

**Правило внедрения: только 0 ₽.** [FREE_ONLY_POLICY](../FREE_ONLY_POLICY.md). **Готовность и Editor tests:** не проводились.

## Название
Unity Modular Inventory System

## Категория и жанры
RPG / Survival / Crafting / Inventory

## Назначение и уже готовые системы
Готовая система инвентаря 2D/3D: ScriptableObject item definitions, stackable items, drag&drop UI, выброс/подбор, demo scene.

## Официальная страница/GitHub
https://github.com/usmanbutt-dev/UnityModularInventorySystem

## Как получить/подключить
Скачать ZIP/clone исходного Unity проекта, затем вручную переносить разрешённые компоненты через Export Package в отдельный тестовый проект (прямой UPM не заявлен).

## Документация/демо
https://github.com/usmanbutt-dev/UnityModularInventorySystem#readme

## Лицензия и условия
MIT в корневом LICENSE; присутствуют Kenney asset license files (отдельно проверять при копировании).

## Цена
0 ₽ за исходный проект по MIT; обязательные платные зависимости README не заявляет.

## Совместимость Unity
Проект ProjectSettings/ProjectVersion.txt: Unity 6000.0.50f1. Заявление README «or compatible newer» не подтверждает Unity 6000.3, требует тест.

## Зависимости
ScriptableObjects, Unity UI и prefab ItemDrop, проектные ассеты Kenney под собственными лицензиями.

## Совместимость с другими решениями
С внешним RPG/quest framework необходим adapter на получение/потерю предметов и save schema; готовую интеграцию автор не заявлял.

## Плюсы
Включает demo scene, предметы, drag-drop и стаки; полноценнее одного inventory script.

## Недостатки и ограничения
Актуальность последнего push 2025-06-08, маленький проект; saving/loading, equipment, hotbar обозначены в Roadmap как FUTURE, не считать готовыми.

## ИИ автоматизация
AI способен добавить item types, prefab, UI и тесты stack/drop, но миграции сохранений отдельно.

## Оценка
ПЕРСПЕКТИВНЫЙ БЕСПЛАТНЫЙ INVENTORY KIT, основные функции без save system

## Последняя проверка
2026-10-08

## Статус
Изучено GitHub README, LICENSE, metadata; не проверено в живом Unity Editor.

## Перед использованием
1. Проверить точный snapshot/tag, ThirdParty NOTICE, версии редактора и стоимость всех зависимостей.
2. Установить в изолированном проекте без платных дополнений.
3. Проверить Editor Console, demo scene, управление, PlayMode, Player build, performance.
4. Занести реальные версии/тест в [COMPATIBILITY_MATRIX](../COMPATIBILITY_MATRIX.md), затем повышать статус.
