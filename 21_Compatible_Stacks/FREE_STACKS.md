# FREE_STACKS — готовые связки 0 ₽: кандидатные архитектуры

**Последняя проверка первоисточников: 2026-10-08. Ни одна связка ещё не интегрирована в редактор Unity в рамках этого исследования. Все статусы = ASSUMED (по документации), не VERIFIED.** Каждая зависимость должна иметь бесплатную лицензию/право использования; не используется платный Source tier и подписки.

## 2D-PLATFORMER-FREE — 2D-платформер

**Игровой результат:** Прототип с героем, прыжками, платформами, сбором предметов, контрольными точками.

| Подсистема | Бесплатное решение | Права/версия |
|---|---|---|
| Графика | [Kenney New Platformer Pack](../Tool_Catalog/kenney-new-platformer-pack.md) | CC0; FREE download, 440 files |
| Ввод | [Unity Input System](../Tool_Catalog/input-system.md) | Unity 6.3: официально 1.20.1 |
| Физика | Встроенные Unity Rigidbody2D/Collider2D | Часть Unity Editor Personal при соблюдении лицензии |
| Уровни | [Unity Tilemap Extras](../Tool_Catalog/tilemap-extras.md) | Unity 6.3: официально 6.0.3 |
| Камера | Unity Camera (встроенная); опция [Cinemachine](../Tool_Catalog/cinemachine.md) | Нет сторонних обязательных платежей |

**Как собрать:** Создать 2D URP или 2D Core → импорт CC0 набора как Sprites → настроить PPU и Tilemap → ввод Jump/Move → Rigidbody2D+Collider2D → Camera следит за Player → построить 1 уровень и restart → EditMode/PlayMode smoke + Windows build.

**Условия/проблемы совместимости:** Версии пакетов 1.20.1 и 6.0.3 взяты из Unity 6.3 каталога, но совместимость друг с другом в нашей сцене не тестировалась; спрайтам нужен scale/filter, а collision нельзя строить только по визуальному размеру.

**Статус:** 0 ₽ обязательных инструментов согласно текущим источникам; compatibility ASSUMED; Unity Build/PlayMode не проверялись.

## 3D-RPG-EXPLORATION-FREE — 3D RPG / TPS exploration

**Игровой результат:** Ходьба 3D персонажа, камера, перемещения NPC, анимация walk/run, простой interaction.

| Подсистема | Бесплатное решение | Права/версия |
|---|---|---|
| Персонаж | [Quaternius Universal Base Characters (Standard)](../Tool_Catalog/quaternius-universal-base-characters.md) | CC0; только бесплатная часть |
| Анимация | [Quaternius Universal Animation Library (Standard)](../Tool_Catalog/quaternius-universal-animation-library.md) | CC0; только бесплатные клипы |
| Ввод | [Unity Input System](../Tool_Catalog/input-system.md) | Unity Registry 1.20.1 под Unity 6.3 |
| Перемещение | Unity встроенный CharacterController + собственный минимальный адаптер движения | Не требуется сторонний контроллер с неподтверждённой EULA |
| Камера | [Cinemachine](../Tool_Catalog/cinemachine.md) | Unity 6.3: 3.1.7, официальное |
| NPC navigation | [AI Navigation](../Tool_Catalog/ai-navigation.md) | Unity 6.3: 2.0.15, но NavMesh ≠ NPC интеллект |
| Текстуры / свет | [Poly Haven](../Tool_Catalog/poly-haven.md) | CC0 HDRI/PBR, оптимизацию проверять |

**Как собрать:** Создать URP 3D → скачать Base Characters Standard и Animation Library Standard → FBX import → Avatar Humanoid mapping → проверить rig/ретаргет → scene locomotion + CharacterController/Input → камера Cinemachine → NavMesh поверх пола → простой NPC follows waypoint → prefab и билд.

**Условия/проблемы совместимости:** Автор заявляет совместимость персонажей/анимаций, но точное содержимое Standard и retarget в Unity 6 не проверялись. Требуется бесплатная Blender/Unity обработка без Source версии. Никаких онлайн-нагрузок и платных AI сервисов.

**Статус:** 0 ₽ обязательных инструментов согласно текущим источникам; compatibility ASSUMED; Unity Build/PlayMode не проверялись.

## 3D-SCI-FI-CORRIDOR-FREE — Sci-fi FPS / exploration

**Игровой результат:** Мини-сцена модульного научно-фантастического коридора с дверью, камерой и ходьбой.

| Подсистема | Бесплатное решение | Права/версия |
|---|---|---|
| 3D окружение | [Quaternius Modular Sci-Fi MegaKit (Standard)](../Tool_Catalog/quaternius-modular-sci-fi-megakit.md) | CC0, бесплатные ~60–70% моделей, НЕ готовые Unity сцены Source |
| Игрок | Unity встроенный CharacterController + [Input System](../Tool_Catalog/input-system.md) | 0 дополнительных расходов |
| Камера | Встроенная Unity Camera или [Cinemachine](../Tool_Catalog/cinemachine.md) | Не смешивать несколько managers |
| Освещение/материалы | [Poly Haven](../Tool_Catalog/poly-haven.md) + URP | CC0 материалы, настройки вручную |
| AI pathfinding при необходимости | [AI Navigation](../Tool_Catalog/ai-navigation.md) | Опциональный пакет |

**Как собрать:** Получить бесплатные FBX/OBJ из Standard → выбрать повторяемые modules → импорт в Unity 3D URP → Snap to Grid / prefabs → collision geometry → first person движение/камера → один interaction (дверь) → профайлинг и Windows build.

**Условия/проблемы совместимости:** Платная Source версия содержит преднастроенные Unity URP shaders и collision, но в бесплатном Standard их наличие не гарантировано. Не выдавать сцену за готовую игру; проверить вручную материалов, LOD и свет.

**Статус:** 0 ₽ обязательных инструментов согласно текущим источникам; compatibility ASSUMED; Unity Build/PlayMode не проверялись.

## 3D-BOAT-RACING-REFERENCE — Racing / water sim

**Игровой результат:** Исследовать готовую demo игру и бесплатные альтернативы созданию физики лодки.

| Подсистема | Бесплатное решение | Права/версия |
|---|---|---|
| Полный демонстрационный проект | [Boat Attack](../Tool_Catalog/boat-attack-urp-demo.md) | Unity Companion License и старый Unity Editor |
| Подсистема воды | [Boat Attack Water](../Tool_Catalog/boat-attack-water.md) | Условия Unity Companion; тесты нет |
| 3D models/hdris | [Poly Haven](../Tool_Catalog/poly-haven.md) | CC0, но высокополигональные объекты |

**Как собрать:** НЕ внедрять в Unity6 без портирования. Сначала изучить старый readme и версию пакетов, оценить потребность в готовой воде/физике, найти современные Unity Registry alternatives, затем протестировать копию отдельного demo проекта.

**Условия/проблемы совместимости:** Демонстрация устаревшая, README явно не production-ready; нельзя считать стек подтверждённо совместимым с Unity 6.

**Статус:** 0 ₽ обязательных инструментов согласно текущим источникам; compatibility ASSUMED; Unity Build/PlayMode не проверялись.

## Общий протокол перехода ASSUMED → VERIFIED
1. Зафиксировать exact Unity build, целевую платформу, пакеты и URL/LICENSE каждого ассета.
2. Установить пакеты/ассеты **в новый тестовый проект**, не смешивая сразу 2 больших фреймворка.
3. Unity Console без compile errors; playable сцена проверена действием, а не просто скриншотом.
4. Проверить экспорт FBX и Humanoid rig/retarget при соответствующих пакетах.
5. Собрать target Player, запустить, сделать FPS/memory snapshot, отметить UX и лицензии.
6. Сохранить GitHub ссылку на test commit/log, список конфликтов и миграцию.

## Блокировки
- Платный Quaternius **Source** не разрешён.
- Kenney **All-in-1** не разрешён.
- Unity cloud AI/BYOK генераторы, платный API, сервер — не входят в эти стеки.
- Asset Store Non-standard EULA требует чтения; не является нашим default бесплатным контроллером.
