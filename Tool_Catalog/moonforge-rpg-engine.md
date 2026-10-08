# Moonforge RPG Engine

> **Индивидуальная карточка:** moonforge-rpg-engine. **Дата:** 2026-10-08. **Статус:** изучено по upstream GitHub/LICENSE, не проверено в Unity Editor. **Правило:** нулевая дополнительная стоимость, сторонние платные функции отключены.

| Поле | Сведения, подтверждённые upstream или обозначенные как неизвестные |
|---|---|
| Точное название | Moonforge RPG Engine |
| Категория / жанры | 03_Complete_Frameworks / 11_RPG_Systems |
| Что решает | Модульный C# движок turn-based RPG, не отдельная полностью нарисованная игра: combat, party, quests, loot/inventory, dialogue, economy, shops, crafting, stat/equipment, save-load. |
| Официальный сайт / GitHub | https://github.com/3583Bytes/moonforge-rpg-engine |
| Скачать / установить | https://github.com/3583Bytes/moonforge-rpg-engine/tree/main/unity-packages/com.moonforge.core ; NuGet https://www.nuget.org/packages/Moonforge.Core (не считать NuGet автоматическим UPM) |
| Лицензия | MIT — https://github.com/3583Bytes/moonforge-rpg-engine/blob/main/LICENSE и LICENSE.md внутри unity-packages/com.moonforge.core проверены |
| Стоимость и платные границы | бесплатно, локальный C#/UPM; обязательных облаков не обнаружено в исходных документах |
| Unity / package versions | UPM package.json заявляет Unity 2022.3+ и com.moonforge.core 1.2.0; Unity 6.3/6.6 не проверены в Editor. |
| Зависимости | Чистый .NET netstandard2.1, собственные Unity адаптеры и визуальный UI/объекты; зависимости пакета и third-party notice проверять по tag. |
| Совместимость / конфликты | Не готовая action-RPG механика перемещения/рендера; можно поверх Unity Input/Prefab, но все интеграции считаются ASSUMED. |
| Готовые функции и сильные стороны | Несколько главных RPG систем уже связаны, детерминированная логика и event-driven quests; большой выигрыш перед десятками отдельных скриптов. |
| Недостатки / ограничения | Молодой проект (создан/активен 2026), мало сообщества, возможно API changes; это gameplay domain без готового полного 3D RPG UI; производительность неизвестна. |
| Инструкция подключения | Изучить unity-packages/com.moonforge.core/package.json; использовать UPM embedded folder или проверенную tagged Git URL/path; не заменять `dotnet add package` на Unity UPM без теста; примеры запускать отдельно. |
| Документация / демо | README содержит Getting Started и sample game; https://github.com/3583Bytes/moonforge-rpg-engine |
| AI-автоматизация | AI может создавать конфиги предметов, навыков, тесты deterministic combat и quest callbacks. |
| Практическая оценка | РЕКОМЕНДУЕТСЯ к пилотному сравнению как самый комплексный бесплатный вариант turn-based RPG, не подтверждён в Editor |
| Последняя проверка | 2026-10-08 |
| Статус проверки | Корневой LICENSE/embedded LICENSE, README, UPM version прочитаны; нет PlayMode/Build. |

## Что означает «проверено по документации»
GitHub README, фактический текст лицензии и package.json открывались отдельно. **Мы не загружали пакеты в наш GitHub и не запускали PlayMode/Build.** Для повышения статуса до VERIFIED необходимо: скачать с лицензией, установить в test Unity, проверить версии и Package Manager, demo, Console, проектную совместимость, Player build и сохранение лога.

## Следующий тест
1. Зафиксировать commit/tag upstream и нужный Unity release.
2. Подключить **без платных API/подписок**, создать отдельную сцену и smoke-тест.
3. Проверить license других ассетов / third party dependencies.
4. По итогам обновить [compatibility matrix](../COMPATIBILITY_MATRIX.md) и [free only policy](../FREE_ONLY_POLICY.md).
