# Unity FPS Sample (FPSSample)

**База знаний Игрульки:** каноническая карточка `fps-sample-legacy`. **Никаких файлов upstream в этом репозитории не хранится.**

## ID, категория
fps-sample-legacy; Готовая игра / legacy FPS multiplayer

## Жанры
FPS / multiplayer

## Назначение
Полная FPS multiplayer игра с клиентом/сервером, исходниками и ассетами для изучения архитектуры.

## Готовые функции
Демонстрационная multiplayer gameplay, уровни, asset bundles, project tools, HDRP legacy pipeline.

## Официальный источник
https://unity.com/fps-sample

## Upstream исходники
https://github.com/Unity-Technologies/FPSSample

## Скачать / установить
git clone https://github.com/Unity-Technologies/FPSSample.git + Git LFS

## Документация
https://github.com/Unity-Technologies/FPSSample/blob/master/README.md

## Демо/примеры
https://github.com/Unity-Technologies/FPSSample#readme

## Лицензия
Unity Companion License; https://github.com/Unity-Technologies/FPSSample/blob/master/LICENSE.md

## Цена
публичный исходный проект, но license restrictions обязательны; загрузка/хранение тяжёлые

## Unity и версии
README: Unity 2018.3.8f1; поддержка современных 6000.x НЕ подтверждена

## Зависимости
Git LFS обязательно; старые пакеты HDRP, ECS, network transport

## Совместимость/конфликты
Старые HDRP/пакеты; перенос на Unity 6 — самостоятельная миграция с высоким риском

## Преимущества
Целая игра, много рабочих игровых систем для анализа

## Недостатки/ограничения
README сам утверждает NOT actively maintained; ~18GB ассетов, clone может занимать ещё больше; не стартер для нового проекта

## ИИ-автоматизация
Агент может изучать архитектуру/состав компонентов, но не автоматически портировать 2018→6

## Обновления / активность
README прочитан 2026-10-08, состояние игры — legacy

## Итоговая оценка
УСТАРЕВШЕЕ: для обучения/идей, не рекомендуется как база современного продакшена

## Статус проверки
изучено README и LICENSE; не тестировалось

## Дата проверки
2026-10-08

## Источники
https://github.com/Unity-Technologies/FPSSample/blob/master/README.md

## Порядок пилотирования
1. Уточнить и сохранить LICENSE/EULA, цену и точный tag/package.
2. Установить отдельно, в чистом проекте с зафиксированной Unity-версией.
3. Запустить demo/настроить минимальную сцену, проверить Console, версии, compile/build и FPS.
4. Только после воспроизводимого теста записать verified stack с другими системами и ссылкой на коммит/лог.

**Не делать:** приравнивать изучение сайта к практически проверенной совместимости.
