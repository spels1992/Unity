# UniTask

**База знаний Игрульки:** каноническая карточка `unitask`. **Никаких файлов upstream в этом репозитории не хранится.**

## ID, категория
unitask; Внутренние подсистемы / async

## Жанры
Любые Unity жанры

## Назначение
Асинхронное программирование с Unity player loop и низкими аллокациями по заявлению авторов.

## Готовые функции
UniTask<T>, Unity AsyncOperation awaiters, PlayerLoop yield/delay, cancellation, event streams, UniTaskTracker.

## Официальный источник
https://github.com/Cysharp/UniTask

## Upstream исходники
https://github.com/Cysharp/UniTask

## Скачать / установить
https://github.com/Cysharp/UniTask/releases

## Документация
https://github.com/Cysharp/UniTask#readme

## Демо/примеры
Примеры кода в README upstream

## Лицензия
MIT; файл https://github.com/Cysharp/UniTask/blob/master/LICENSE прочитан

## Цена
бесплатно, MIT

## Unity и версии
Конкретная версия Editor 6000.3 требует отдельной проверки с выбранным тегом UniTask

## Зависимости
UPM Git URL либо .unitypackage из release; конкретную ветку фиксировать

## Совместимость/конфликты
Учитывать возможности встроенного Unity Awaitable и собственные правила отмены

## Преимущества
Широкая интеграция с Unity async и документация; MIT

## Недостатки/ограничения
Внешняя зависимость не всегда нужна; misuse async может дать ошибки жизненного цикла, Editor теста нет

## ИИ-автоматизация
Агент может преобразовывать корутины/создавать cancellable tasks и тесты, но должен учитывать main thread

## Обновления / активность
GitHub push 2026-10-06; проверено 2026-10-08

## Итоговая оценка
Хорошая альтернатива для сложной асинхронности, не обязательный пакет первой игры

## Статус проверки
изучено README и LICENSE; не тестировалось

## Дата проверки
2026-10-08

## Источники
https://github.com/Cysharp/UniTask/blob/master/LICENSE

## Порядок пилотирования
1. Уточнить и сохранить LICENSE/EULA, цену и точный tag/package.
2. Установить отдельно, в чистом проекте с зафиксированной Unity-версией.
3. Запустить demo/настроить минимальную сцену, проверить Console, версии, compile/build и FPS.
4. Только после воспроизводимого теста записать verified stack с другими системами и ссылкой на коммит/лог.

**Не делать:** приравнивать изучение сайта к практически проверенной совместимости.
