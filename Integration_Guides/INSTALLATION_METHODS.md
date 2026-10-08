# Подключение найденных решений к Unity

**Дата:** 2026-10-08. Устанавливать зависимости в отдельной feature-ветке; перед подключением проверить LICENSE, поддерживаемую Editor, Unity Package Manager и GPU target.

## 1. Unity Registry (предпочтительно для официальных компонентов)
1. `Window → Package Manager` → Unity Registry.
2. Найти **Cinemachine** или **AI Navigation**; проверить Editor compatibility и версию пакета.
3. Установить и открыть Sample, если опубликован. Параллельно записать версию в проект и Git lock.
4. Протестировать в новой сцене, сделать player build, проверить Console.

## 2. Git UPM пакет
1. Проверить upstream, LICENSE, `package.json`, поддерживаемую Unity, есть ли подпапка пакета.
2. Установить Git (минимум 2.14) и Git LFS при необходимости.
3. Package Manager → `+` → `Install package from git URL` → указать upstream URL с фиксированной ревизией/tag, если допустимо.
4. Для пакета в подкаталоге использовать `?path=/subfolder`. Не путать этот путь с обычным Unity `.unitypackage`.
5. Проверить manifest+lockfile и build. При ошибке откатить lockfile/manifest коммит.

[Official Unity guide](https://docs.unity.com/en-us/engine/6000.6/manual/packages-list/managing-packages-window/upm-ui-actions/upm-ui-giturl).

## 3. Asset Store packages
1. Открыть официальную страницу Unity Asset Store из карточки.
2. Прочитать цену, лицензию, версии Editor и список зависимостей.
3. Установить через Asset Store → My Assets / Package Manager workflow.
4. Избегать перезаписи собственных сцен и глобального Input/camera managers. Сначала test clone проекта.

## 4. Полноценная игра / starter project
1. Клонировать upstream **отдельно**, а не внутрь живого проекта.
2. Учесть LFS и старую версию Unity: пример FPS Sample — Unity 2018.3, около 18GB ассетов, современные версии не проверены.
3. Отдельно изучить разрешение на использование исходников/ассетов (Unity Companion/другие лицензии).
4. Выделить воспроизводимые системные части, обдумать перенос только разрешённых.
5. При попытке интеграции фиксировать версии, изменённые файлы, конфликты, тесты, rollback.

## Общий тест совместимости
`Clean project → Install → Console clean → Demo Scene → target build → small integration → regression tests → performance snapshot → решение`.
