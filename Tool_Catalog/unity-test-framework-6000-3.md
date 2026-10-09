# Unity Test Framework — бесплатные Edit Mode / Play Mode тесты

- **Пакет:** `com.unity.test-framework` (официальный core package Unity).
- **Стоимость:** не требует отдельной покупки пакета; использование Unity Editor — по действующей лицензии Unity. **0 ₽ дополнительных инструментов**.
- **Лицензия:** НЕ MIT. Для самого пакета проверить лицензионные файлы установленной версии и условия Unity Editor; не копировать код пакета в наш репозиторий.
- **Unity:** официальная документация Unity **6000.3**; core package закреплён за версией Editor, не указывать выдуманный номер.
- **Назначение:** тестирование игрового кода, редакторских инструментов, поведения в Play Mode и Player.
- **Статус:** DOCUMENTED / NOT_RUN; в нашем редакторе тесты не запускались.

## Как использовать
1. Unity Package Manager → убедиться, что Test Framework доступен в проекте.
2. Создать отдельные тестовые Assembly Definition (asmdef); для Edit Mode ограничить платформы `Editor`, для Play Mode выбрать runtime assembly. Добавить ссылку на тестируемую собственную assembly.
3. Для обычной логики использовать NUnit `[Test]`, для покадрового поведения — `[UnityTest]`.
4. Запустить Edit Mode и Play Mode через Test Runner, затем повторить на нужной целевой платформе, если требуется.
5. Зафиксировать версию Editor, платформу, число тестов, реальные PASS/FAIL и лог. Node.js headless тесты НЕ равны Unity Play Mode.

## Ограничения
- Код, находящийся в `Assembly-CSharp`, потребуется выделить в отдельную assembly для прямой ссылки из тестовой assembly.
- Тесты, требующие физики, сцен или кадров, не заменять Edit Mode тестами.
- Не объявлять поддержку конкретного проекта до запуска в его версии Unity.

## Источники (проверено 2026-10-09)
- Официальная карточка Unity 6000.3: https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-core/com-unity-test-framework
- Edit Mode и Play Mode: https://docs.unity.com/en-us/engine/6000.6/manual/scripting/test-framework-introduction/getting-started/edit-mode-vs-play-mode-tests
- Unity Companion License (если применима к конкретному файлу): https://unity.com/legal/licenses/unity-companion-license
