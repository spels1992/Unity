# Ink Unity Integration 2.0

> **Индивидуальная карточка:** ink-unity-integration. **Дата:** 2026-10-08. **Статус:** изучено по upstream GitHub/LICENSE, не проверено в Unity Editor. **Правило:** нулевая дополнительная стоимость, сторонние платные функции отключены.

| Поле | Сведения, подтверждённые upstream или обозначенные как неизвестные |
|---|---|
| Точное название | Ink Unity Integration 2.0 |
| Категория / жанры | 11_RPG_Systems / интерактивный нарратив |
| Что решает | Unity интеграция сценарного языка ink: ветвящиеся истории/условия/диалоги, компиляция .ink как asset, инспектор и Ink Player. |
| Официальный сайт / GitHub | https://github.com/inkle/ink-unity-integration |
| Скачать / установить | Бесплатный UPM: https://github.com/inkle/ink-unity-integration.git#upm ; https://github.com/inkle/ink-unity-integration/releases |
| Лицензия | MIT (проверен LICENCE.md и встроенный package LICENCE); не путать с Github metadata NOASSERTION |
| Стоимость и платные границы | 0 ₽ через GitHub/OpenUPM; необходимость платных средств отсутствует |
| Unity / package versions | com.inkle.ink-unity-integration 2.0.0, Unity 2022.3+; release 2.0 имеет breaking changes против версии 1.х; Unity 6.3 конкретно не проверена. |
| Зависимости | C# runtime/compiler ink, Unity ScriptedImporter; UI для вывода диалогов нужно привязать. Inky редактор отдельный бесплатный. |
| Совместимость / конфликты | С Yarn Spinner альтернативная narrative технология; если автор использует оба, понадобятся мост/разделение ответственности. Unity 6 support в релиз-нотах, но нет нашего Build. |
| Готовые функции и сильные стороны | MIT, активно обновлён в июле 2026, удобная отдельная литературная логика, примеры. |
| Недостатки / ограничения | Это не готовый UI диалога или quest/inventory; миграция v1→v2 может ломать JSON-потоки и API; автоматический import нужно проверять. |
| Инструкция подключения | Package Manager → Install package from git URL → #upm; открыть demos и изучить InkFile.storyJson + Story API. Не копировать устаревшие примеры TextAsset JSON с v1. |
| Документация / демо | https://github.com/inkle/ink-unity-integration/tree/master/Documentation ; https://github.com/inkle/ink/blob/master/Documentation/RunningYourInk.md |
| AI-автоматизация | AI может генерировать .ink сценарии, проверять ветвления/тестовые прохождения без платных облачных API. |
| Практическая оценка | РЕКОМЕНДУЕТСЯ как бесплатный нарративный язык, особенно сюжетным играм и RPG |
| Последняя проверка | 2026-10-08 |
| Статус проверки | Проверены README, LICENCE.md, package.json и release notes; Editor не запускался. |

## Что означает «проверено по документации»
GitHub README, фактический текст лицензии и package.json открывались отдельно. **Мы не загружали пакеты в наш GitHub и не запускали PlayMode/Build.** Для повышения статуса до VERIFIED необходимо: скачать с лицензией, установить в test Unity, проверить версии и Package Manager, demo, Console, проектную совместимость, Player build и сохранение лога.

## Следующий тест
1. Зафиксировать commit/tag upstream и нужный Unity release.
2. Подключить **без платных API/подписок**, создать отдельную сцену и smoke-тест.
3. Проверить license других ассетов / third party dependencies.
4. По итогам обновить [compatibility matrix](../COMPATIBILITY_MATRIX.md) и [free only policy](../FREE_ONLY_POLICY.md).
