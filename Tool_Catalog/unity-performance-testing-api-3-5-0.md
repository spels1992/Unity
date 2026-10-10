# Unity Performance Testing API — исследовательская карточка

- Статус: DOCUMENTED / EDITOR_NOT_TESTED.
- Назначение: автоматизированные измерения времени выполнения, кадров и выделений памяти в Unity Test Framework.
- Цена: пакет Unity доступен без отдельной платы; использование Unity Editor регулируется тарифом и условиями Unity.
- Пакет: `com.unity.test-framework.performance`.
- Версия-кандидат: 3.5.0; перед установкой сверить Package Manager и совместимость с конкретной Unity 6.3.
- Лицензия: Unity Companion License / условия пакета Unity; **не MIT**. Перепроверить LICENSE.md установленного пакета перед распространением.
- Источники: https://docs.unity3d.com/Packages/com.unity.test-framework.performance@3.5/manual/index.html ; https://docs.unity3d.com/Packages/com.unity.test-framework.performance@3.5/manual/reference.html
- Ограничения: документация не заменяет реальный Editor/CI тест; не обещать работоспособность в проекте до тестирования.
- Дубликаты: Unity Test Framework выполняет тесты; Performance Testing API добавляет измерения производительности, это отдельная функциональность.
- Следующий тест: изолированный Unity 6.3 проект, установка пакета, EditMode/PlayMode benchmark, проверка результатов и отсутствия платных зависимостей.
