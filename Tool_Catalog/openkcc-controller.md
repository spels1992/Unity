# OpenKCC — Open Kinematic Character Controller

> **Индивидуальная карточка:** openkcc-controller. **Дата:** 2026-10-08. **Статус:** изучено по upstream GitHub/LICENSE, не проверено в Unity Editor. **Правило:** нулевая дополнительная стоимость, сторонние платные функции отключены.

| Поле | Сведения, подтверждённые upstream или обозначенные как неизвестные |
|---|---|
| Точное название | OpenKCC — Open Kinematic Character Controller |
| Категория / жанры | 04_Character_Systems / FPS TPS Platformer |
| Что решает | Готовый кинематический контроллер движения персонажа в Unity, компонентные samples для FPS, движение/ground/camera. |
| Официальный сайт / GitHub | https://github.com/nicholas-maltbie/OpenKCC |
| Скачать / установить | https://github.com/nicholas-maltbie/OpenKCC/tree/main/Packages/com.nickmaltbie.openkcc ; документация https://nickmaltbie.com/OpenKCC/docs |
| Лицензия | MIT из реально проверенного https://github.com/nicholas-maltbie/OpenKCC/blob/main/LICENSE.txt; изображения/примеры могут содержать third-party licensed assets |
| Стоимость и платные границы | 0 ₽, source и samples без оплаты |
| Unity / package versions | UPM com.nickmaltbie.openkcc v1.5.0 заявляет минимальную Unity 2019.4; README dev-проект Unity 2023.1; последняя активность upstream 2023-09-15, Unity 6 не проверена. |
| Зависимости | Unity Input System >=1.0 по README и нужные camera/physics пакеты/optional netcode; отдельные расширения Cinemachine/Netcode имеют свои package.json. |
| Совместимость / конфликты | Функции movement должны адаптироваться под Input System/Cinemachine. Нельзя считать legacy controller готовым к Unity 6 без компиляции. |
| Готовые функции и сильные стороны | MIT, архитектура KCC и несколько samples, демо в браузере. |
| Недостатки / ограничения | Мало активности с 2023, потенциальный конфликт Unity 6 physics API/input; demo versions старые; объём настройки выше официального Starter Assets. |
| Инструкция подключения | Не импортировать гигантский sample проект вслепую, начать с com.nickmaltbie.openkcc в чистом Unity проекте; установить зависимости, открыть Samples~, проверить Physics+camera. Для полной демо игры требуется Git LFS. |
| Документация / демо | https://nickmaltbie.com/OpenKCC/ |
| AI-автоматизация | Агент создаёт prefab контроллера, тестирует ground/slope/jump и версию API. |
| Практическая оценка | ПЕРСПЕКТИВНАЯ БЕСПЛАТНАЯ АЛЬТЕРНАТИВА, но не объявлять поддерживаемым Unity 6 |
| Последняя проверка | 2026-10-08 |
| Статус проверки | MIT/UPM manifest/README проверены; запуск Unity 6 отсутствует. |

## Что означает «проверено по документации»
GitHub README, фактический текст лицензии и package.json открывались отдельно. **Мы не загружали пакеты в наш GitHub и не запускали PlayMode/Build.** Для повышения статуса до VERIFIED необходимо: скачать с лицензией, установить в test Unity, проверить версии и Package Manager, demo, Console, проектную совместимость, Player build и сохранение лога.

## Следующий тест
1. Зафиксировать commit/tag upstream и нужный Unity release.
2. Подключить **без платных API/подписок**, создать отдельную сцену и smoke-тест.
3. Проверить license других ассетов / third party dependencies.
4. По итогам обновить [compatibility matrix](../COMPATIBILITY_MATRIX.md) и [free only policy](../FREE_ONLY_POLICY.md).
