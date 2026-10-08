# Unity Input System

**База знаний Игрульки:** каноническая карточка `input-system`. **Никаких файлов upstream в этом репозитории не хранится.**

## ID, категория
input-system; Ввод / core system

## Жанры
Все жанры, Windows, mobile, console, VR/XR (по поддержке проекта)

## Назначение
Система устройств и действий, расширяемая альтернатива UnityEngine.Input.

## Готовые функции
Keyboard, mouse, gamepad, touch, VR/XR input actions; привязки, maps.

## Официальный источник
https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-inputsystem

## Upstream исходники
не установлен официальный первичный репозиторий пакета

## Скачать / установить
Unity Registry: com.unity.inputsystem

## Документация
https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-inputsystem

## Демо/примеры
Проверить Samples в Package Manager

## Лицензия
Unity package: LICENSE внутри установленного пакета требует проверки

## Цена
официальный Unity package, цена дополнительной лицензии не выявлена

## Unity и версии
Официальный каталог Unity 6000.3: com.unity.inputsystem 1.20.1

## Зависимости
При необходимости InputSystemUIInputModule и адаптеры в конкретном UI

## Совместимость/конфликты
Сторонние controllers могут ожидать старую Input Manager/свой setup Input Actions

## Преимущества
Унифицированные действия и устройства вместо ручной обработки каждого девайса

## Недостатки/ограничения
Неправильное переключение input backend и bindings ломает Starter Kit контроллеры

## ИИ-автоматизация
Агент может создать Input Actions/контроллеры и smoke-test на keyboard/gamepad

## Обновления / активность
Официальные docs 2026-10-08

## Итоговая оценка
Рекомендуется в новых проектах после проверки с контроллером/платформой

## Статус проверки
официальные Docs, Editor не тестировался

## Дата проверки
2026-10-08

## Источники
https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-inputsystem

## Порядок пилотирования
1. Уточнить и сохранить LICENSE/EULA, цену и точный tag/package.
2. Установить отдельно, в чистом проекте с зафиксированной Unity-версией.
3. Запустить demo/настроить минимальную сцену, проверить Console, версии, compile/build и FPS.
4. Только после воспроизводимого теста записать verified stack с другими системами и ссылкой на коммит/лог.

**Не делать:** приравнивать изучение сайта к практически проверенной совместимости.
