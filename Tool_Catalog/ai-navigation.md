# Unity AI Navigation

**База знаний Игрульки:** каноническая карточка `ai-navigation`. **Никаких файлов upstream в этом репозитории не хранится.**

## ID, категория
ai-navigation; AI / NavMesh

## Жанры
TPS, RPG, RTS, stealth, adventure

## Назначение
Компоненты построения NavMesh и навигации персонажей.

## Готовые функции
Build NavMesh runtime/edit-time, dynamic obstacles, links for jumps/specific transitions.

## Официальный источник
https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-ai-navigation

## Upstream исходники
не найден официальный публичный upstream для выбранной версии

## Скачать / установить
Unity Editor → Package Manager → Unity Registry → AI Navigation

## Документация
https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-ai-navigation

## Демо/примеры
Сэмплы искать внутри выбранной версии UPM package

## Лицензия
официальный Unity package, уточнить package license при установке

## Цена
доступен в Unity Registry, цена дополнительной лицензии не заявлена

## Unity и версии
Unity Editor 6000.3: AI Navigation 2.0.15

## Зависимости
Навигационные компоненты, geometry/agents в сцене

## Совместимость/конфликты
NavMesh НЕ является поведением NPC, BT/GOAP/combat AI надо добавлять отдельно

## Преимущества
Официальный, подходит для базового pathfinding и dynamic navmesh

## Недостатки/ограничения
Массовые RTS/процедурные миры требуют профилирования, нет автоматически боевого AI

## ИИ-автоматизация
Агент может собрать NavMesh surfaces/agents и проверить прохождение waypoint-тестами

## Обновления / активность
Документация 2026-10-08

## Итоговая оценка
Рекомендуется как базовый NavMesh слой при подходящих сценариях

## Статус проверки
официальная документация, Editor не тестировался

## Дата проверки
2026-10-08

## Источники
https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-safe/com-unity-ai-navigation

## Порядок пилотирования
1. Уточнить и сохранить LICENSE/EULA, цену и точный tag/package.
2. Установить отдельно, в чистом проекте с зафиксированной Unity-версией.
3. Запустить demo/настроить минимальную сцену, проверить Console, версии, compile/build и FPS.
4. Только после воспроизводимого теста записать verified stack с другими системами и ссылкой на коммит/лог.

**Не делать:** приравнивать изучение сайта к практически проверенной совместимости.
