# Mirror Networking

**База знаний Игрульки:** каноническая карточка `mirror-networking`. **Никаких файлов upstream в этом репозитории не хранится.**

## ID, категория
mirror-networking; Сеть / multiplayer

## Жанры
Co-op, FPS, RPG, небольшие MMO и др.

## Назначение
Сетевой framework клиент/сервер для Unity.

## Готовые функции
Transports (TCP/UDP/WebSocket/Steam/relay варианты), authority, sync, interest management, lag simulation, batching — по README.

## Официальный источник
https://mirror-networking.gitbook.io/

## Upstream исходники
https://github.com/MirrorNetworking/Mirror

## Скачать / установить
https://assetstore.unity.com/packages/tools/network/mirror-129321

## Документация
https://mirror-networking.gitbook.io/docs/

## Демо/примеры
https://github.com/MirrorNetworking/Mirror#readme

## Лицензия
MIT; файл LICENSE прочитан: https://github.com/MirrorNetworking/Mirror/blob/master/LICENSE

## Цена
бесплатный open-source framework; сторонние hosting/transport могут стоить денег

## Unity и версии
Точная поддержка Unity 6000.3 в просмотренных файлах не подтверждена

## Зависимости
Зависимости зависят от выбранного transport и проекта; не аудированы

## Совместимость/конфликты
Mirror и FishNet — альтернативы в роли основной сетевой системы, совместная установка не доказана

## Преимущества
Исходники, MIT, доступные docs, несколько транспортов

## Недостатки/ограничения
Сетевой проект сложнее single player; безопасность/authority и баланс bandwidth требуют опыта; Editor тест не выполнен

## ИИ-автоматизация
ИИ-агент может создать тестовую server/client сцену, сгенерировать regression tests и записать конфигурацию — после установки

## Обновления / активность
GitHub push 2026-09-19, проверено 2026-10-08

## Итоговая оценка
Хорошая альтернатива официальному Netcode, кандидат на пилот

## Статус проверки
изучено по README и LICENSE; НЕ тестировалось в Unity

## Дата проверки
2026-10-08

## Источники
https://github.com/MirrorNetworking/Mirror/blob/master/LICENSE

## Порядок пилотирования
1. Уточнить и сохранить LICENSE/EULA, цену и точный tag/package.
2. Установить отдельно, в чистом проекте с зафиксированной Unity-версией.
3. Запустить demo/настроить минимальную сцену, проверить Console, версии, compile/build и FPS.
4. Только после воспроизводимого теста записать verified stack с другими системами и ссылкой на коммит/лог.

**Не делать:** приравнивать изучение сайта к практически проверенной совместимости.
