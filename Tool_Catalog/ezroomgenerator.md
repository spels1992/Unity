# EZ Room Generator

> **Индивидуальная карточка:** ezroomgenerator. **Дата:** 2026-10-08. **Статус:** изучено по upstream GitHub/LICENSE, не проверено в Unity Editor. **Правило:** нулевая дополнительная стоимость, сторонние платные функции отключены.

| Поле | Сведения, подтверждённые upstream или обозначенные как неизвестные |
|---|---|
| Точное название | EZ Room Generator |
| Категория / жанры | 12_World_Generation / 3D procedural levels |
| Что решает | Редакторский 3D генератор комнат, коридоров, лабиринтов и подземелий в Unity 6, интерактивная grid-разметка. |
| Официальный сайт / GitHub | https://github.com/jastrz/EZRoomGenerator |
| Скачать / установить | https://github.com/jastrz/EZRoomGenerator/releases ; Git UPM https://github.com/jastrz/EZRoomGenerator.git |
| Лицензия | MIT — прочитан https://github.com/jastrz/EZRoomGenerator/blob/main/LICENSE |
| Стоимость и платные границы | 0 ₽ за инструмент; встроенный FBX Exporter из Unity Registry требует проверки доступности и версии |
| Unity / package versions | package.json com.houkii.ezroomgenerator v0.1.0, Unity 6000.0+ (Unity 6); конкретная 6.3/6.6 не проверена. |
| Зависимости | В package.json dependency com.unity.formats.fbx 5.1.5; README указывает exporter feature с USE_FBX_EXPORTER, хотя manifest сейчас включает dependency: проверить при установке. |
| Совместимость / конфликты | Сгенерированные meshes/prefabs/colliders и URP sample materials; на Built-In/HDRP пере-настроить shaders; exported FBX Blender4.5 заявлен автором. |
| Готовые функции и сильные стороны | Готовый набор generator/layout/editor инструментов, лёгкий способ создать 3D labyrinth без написания алгоритма. |
| Недостатки / ограничения | Очень маленькое сообщество, v0.1.0, ячейка max 100x100 в примере, не проверена оптимизация на больших уровнях/лицензии примеров. |
| Инструкция подключения | В чистом Unity 6 Package Manager → add package from Git URL; проверить FBX Exporter 5.1.5 availability; добавить RoomGenerator на GameObject; sample и mesh generation тесты. |
| Документация / демо | README GIF/screenshots и YouTube демонстрация; https://github.com/jastrz/EZRoomGenerator |
| AI-автоматизация | AI может настраивать grid layouts через Editor API, генерировать комнаты, экспортировать FBX и проверить коллайдеры. |
| Практическая оценка | РЕКОМЕНДУЕТСЯ как кандидат для быстрого 3D прототипа, качество требует smoke-test |
| Последняя проверка | 2026-10-08 |
| Статус проверки | LICENSE, package.json, README и описание Unity6 подтверждены; наша Unity сборка отсутствует. |

## Что означает «проверено по документации»
GitHub README, фактический текст лицензии и package.json открывались отдельно. **Мы не загружали пакеты в наш GitHub и не запускали PlayMode/Build.** Для повышения статуса до VERIFIED необходимо: скачать с лицензией, установить в test Unity, проверить версии и Package Manager, demo, Console, проектную совместимость, Player build и сохранение лога.

## Следующий тест
1. Зафиксировать commit/tag upstream и нужный Unity release.
2. Подключить **без платных API/подписок**, создать отдельную сцену и smoke-тест.
3. Проверить license других ассетов / third party dependencies.
4. По итогам обновить [compatibility matrix](../COMPATIBILITY_MATRIX.md) и [free only policy](../FREE_ONLY_POLICY.md).
