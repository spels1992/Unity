# Unity Memory Profiler — снимки памяти и поиск утечек

- **Пакет:** `com.unity.memoryprofiler`.
- **Стоимость:** официальный released Unity package без отдельной покупки; 0 ₽ дополнительных инструментов, с соблюдением лицензии Unity Editor.
- **Лицензия:** условия пакета/Unity, **не заявлять MIT или CC0**; до копирования кода смотреть установленный `LICENSE`.
- **Unity 6000.3:** **1.1.12 released**; **1.2.0-pre.1 compatible preview**, не выбирать preview для стабильного production без отдельной проверки.
- **Функция:** snapshots памяти и анализ аллокаций/объектов, в том числе Editor и подключённого Player.
- **Статус:** DOCUMENTED / NOT_RUN; снимки памяти ещё не сделаны.

## Проверка для игры
1. Установить Memory Profiler из Unity Package Manager.
2. Снять snapshot после запуска, после генерации карты, после 10 волн и после возврата в меню.
3. Сравнить удержанные объекты, native/managed memory и повторяющиеся инстансы; убедиться, что разница не объясняется прогревом или кешированием.
4. Повторить сценарий на одинаковой платформе/сборке и зафиксировать размеры и версии.
5. Не считать результат Unity Editor репрезентативным для Player без отдельного замера.

## Источники (проверено 2026-10-09)
- Unity 6000.3, версия и статус: https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-memoryprofiler
- MemoryProfiler API: https://docs.unity.com/en-us/engine/6000.5/script-reference/unity/profiling/memory/memoryprofiler
