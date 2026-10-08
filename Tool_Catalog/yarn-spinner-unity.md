# Yarn Spinner for Unity

> **Индивидуальная карточка:** yarn-spinner-unity. **Дата:** 2026-10-08. **Статус:** изучено по upstream GitHub/LICENSE, не проверено в Unity Editor. **Правило:** нулевая дополнительная стоимость, сторонние платные функции отключены.

| Поле | Сведения, подтверждённые upstream или обозначенные как неизвестные |
|---|---|
| Точное название | Yarn Spinner for Unity |
| Категория / жанры | 11_RPG_Systems / Диалоги / Visual novel |
| Что решает | Система диалогов и разветвлённых реплик для игр, позволяющая сценаристу писать текст, а разработчику подключать к Unity. |
| Официальный сайт / GitHub | https://github.com/YarnSpinnerTool/YarnSpinner-Unity |
| Скачать / установить | Бесплатно из Git UPM: https://github.com/YarnSpinnerTool/YarnSpinner-Unity.git#current ; документация https://docs.yarnspinner.dev/yarn-spinner-for-unity/installation-and-setup |
| Лицензия | MIT — upstream https://github.com/YarnSpinnerTool/YarnSpinner-Unity/blob/main/LICENSE.md реально прочитан; проверять third-party notices |
| Стоимость и платные границы | GitHub/OpenUPM сборка бесплатна. Asset Store/Itch.io продаются для поддержки автора, **не покупать** |
| Unity / package versions | Unity package.json: dev.yarnspinner.unity 3.2.8, минимальная Unity 2022.3; точная Unity 6.3 не тестировалась. |
| Зависимости | Yarn Spinner Unity UPM package + UI/компоненты, Core Yarn Spinner compiler; проверить Third-Party Notices.txt и локализацию при импорте. |
| Совместимость / конфликты | С Ink — альтернативная система диалогов, не ставить сразу обе без причины; с RPG inventory интеграция событий требует адаптера. |
| Готовые функции и сильные стороны | Многофункциональные диалоги, современный Unity пакет, MIT, официальная документация и демо. |
| Недостатки / ограничения | Продаваемые версии могут отличаться готовыми обновлениями, конкретный UPM branch pin нужен для воспроизводимости; runtime/UI тест не проведён. |
| Инструкция подключения | Unity Package Manager → Install from git URL → точный URL выше, зафиксировать commit/tag и package-lock; открыть official sample/dialogue scene; не использовать Asset Store paid. |
| Документация / демо | https://yarnspinner.dev/docs/unity/02-installation-and-setup/01-quick-start/ |
| AI-автоматизация | AI может писать Yarn сценарии, локализацию, валидировать переходы и запускать PlayMode smoke-test. |
| Практическая оценка | РЕКОМЕНДУЕТСЯ как бесплатная система интерактивных диалогов, сначала demo и проверка лицензионных notices |
| Последняя проверка | 2026-10-08 |
| Статус проверки | Корневой MIT LICENSE, package.json, официальная инструкция Git install проверены; нет live теста. |

## Что означает «проверено по документации»
GitHub README, фактический текст лицензии и package.json открывались отдельно. **Мы не загружали пакеты в наш GitHub и не запускали PlayMode/Build.** Для повышения статуса до VERIFIED необходимо: скачать с лицензией, установить в test Unity, проверить версии и Package Manager, demo, Console, проектную совместимость, Player build и сохранение лога.

## Следующий тест
1. Зафиксировать commit/tag upstream и нужный Unity release.
2. Подключить **без платных API/подписок**, создать отдельную сцену и smoke-тест.
3. Проверить license других ассетов / third party dependencies.
4. По итогам обновить [compatibility matrix](../COMPATIBILITY_MATRIX.md) и [free only policy](../FREE_ONLY_POLICY.md).
