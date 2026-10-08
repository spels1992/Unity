# Edgar for Unity — Free Core

> **Индивидуальная карточка:** edgar-unity-free. **Дата:** 2026-10-08. **Статус:** изучено по upstream GitHub/LICENSE, не проверено в Unity Editor. **Правило:** нулевая дополнительная стоимость, сторонние платные функции отключены.

| Поле | Сведения, подтверждённые upstream или обозначенные как неизвестные |
|---|---|
| Точное название | Edgar for Unity — Free Core |
| Категория / жанры | 12_World_Generation / 2D roguelikes dungeon |
| Что решает | Бесплатный графовый 2D генератор уровней из готовых комнат, с коридорами, boss/shop layouts и Unity Tilemap templates. |
| Официальный сайт / GitHub | https://github.com/OndrejNepozitek/Edgar-Unity |
| Скачать / установить | https://github.com/OndrejNepozitek/Edgar-Unity/releases ; Git UPM https://github.com/OndrejNepozitek/Edgar-Unity.git#upm |
| Лицензия | MIT, https://github.com/OndrejNepozitek/Edgar-Unity/blob/master/LICENSE |
| Стоимость и платные границы | GitHub **Free Core = 0 ₽**; Edgar PRO Asset Store платный, **не использовать** |
| Unity / package versions | package.json com.ondrejnepozitek.edgar.unity v2.1.0, unity minimum 2019.3; README ≥2018.4; Unity 6 не верифицирована нашим Editor. |
| Зависимости | Unity Tilemap, graph room templates; optional PRO features unavailable; проверить plugin package deps. |
| Совместимость / конфликты | 2D Tilemap + собственные prefabs, C# post-processing; другие 2D dungeon generators альтернативы, не смешивать. |
| Готовые функции и сильные стороны | Готовая структурная генерация графов комнат, sample scenes, MIT, много исторических пользователей. |
| Недостатки / ограничения | Особенно важно: PRO-only platformer generator, isometric example, custom rooms/advanced examples и coroutines; часть заявленных возможностей недоступна в бесплатной версии; обновления могут ломать layout. |
| Инструкция подключения | Unity Package Manager → Git URL #upm → импортировать samples. Проверить package-specific limitations до создания roguelike. |
| Документация / демо | https://ondrejnepozitek.github.io/Edgar-Unity/docs/introduction/ ; GitHub example scenes |
| AI-автоматизация | AI может создавать room graph/room prefabs и воспроизводимые seeded tests, но только Free Core API. |
| Практическая оценка | ХОРОШАЯ БЕСПЛАТНАЯ АЛЬТЕРНАТИВА для 2D dungeon, не для free platformer PRO функций |
| Последняя проверка | 2026-10-08 |
| Статус проверки | Прочитаны LICENSE/README блок PRO и package.json; Editor не тестировался. |

## Что означает «проверено по документации»
GitHub README, фактический текст лицензии и package.json открывались отдельно. **Мы не загружали пакеты в наш GitHub и не запускали PlayMode/Build.** Для повышения статуса до VERIFIED необходимо: скачать с лицензией, установить в test Unity, проверить версии и Package Manager, demo, Console, проектную совместимость, Player build и сохранение лога.

## Следующий тест
1. Зафиксировать commit/tag upstream и нужный Unity release.
2. Подключить **без платных API/подписок**, создать отдельную сцену и smoke-тест.
3. Проверить license других ассетов / third party dependencies.
4. По итогам обновить [compatibility matrix](../COMPATIBILITY_MATRIX.md) и [free only policy](../FREE_ONLY_POLICY.md).
