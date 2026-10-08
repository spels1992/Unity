# Unity Test Framework — бесплатные EditMode / PlayMode тесты

- **ID / теги:** unity-test-framework; QA, regression, unit-test, playmode, editor
- **Описание:** официальный Unity framework для NUnit-совместимых EditMode и PlayMode тестов. Не является симулятором живого игрока.
- **Что готово:** Test Runner, тестовые assembly definitions, `[Test]` и `[UnityTest]`, выполнение в Editor/Player, CLI `-runTests`, XML результаты.
- **Официальный источник:** https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-core/com-unity-test-framework
- **Документация:** https://docs.unity.com/en-us/engine/6000.6/manual/programming-environment/test-framework-introduction
- **CLI (Unity 6.3):** https://docs.unity.com/en-us/engine/6000.3/manual/scripting/test-framework-introduction/reference-command-line
- **UPM:** `com.unity.test-framework`, **core package**; версия жёстко связана с установленным Unity Editor, нельзя произвольно закрепить номер в Package Manager. Не подставлять старую 1.4.x из документации Unity 6.0 как версию Unity 6.3.
- **Цена / доступность:** официальный пакет Editor, без отдельной оплаты; `adoption: FREE`, `free_part: all documented test-runner features`, `payment_required: false`, `fallback: manual local Editor Test Runner`.
- **Лицензия:** для старых опубликованных UPM сборок зеркало показывает **Unity Companion License** (https://github.com/needle-mirror/com.unity.test-framework/blob/master/LICENSE.md). Зеркало не первоисточник: **перед распространением кода** проверить `LICENSE.md` именно в установленном пакете Unity 6.3; Unity Companion не MIT и ограничена Unity-зависимым применением.
- **Unity / render / platforms:** официально доступен в Unity 6000.3; EditMode/PlayMode в Editor и поддерживаемые Player test targets. Render pipeline не обязателен.
- **Зависимости:** установленный Unity Editor, NUnit внутри Test Framework; asmdef для собственных тестов; PlayMode тесты требуют сцены/объектов, если их проверяют.
- **Интеграции:** вместе с Input System `InputTestFixture` можно тестировать программный ввод; performance-тесты — через отдельный `com.unity.test-framework.performance`. Совместное выполнение **документировано**, не проверено в нашем Editor.
- **Плюсы:** повторяемые проверки сохранений, инвентаря, крафта, переходов между сценами; локальный запуск без облака.
- **Минусы:** тест не оценивает ощущение игры, визуальные баги, сложность, удобство управления или эмоции человека; для этого нужны игровые сессии.
- **Установка:** в отдельном тестовом Unity проекте открыть Window → General → Test Runner; если пакет отсутствует, добавить официальный core package по штатной документации версии Editor.
- **Пример CLI (план, НЕ запускалось):** `Unity.exe -batchmode -runTests -projectPath <ISOLATED_TEST_PROJECT> -testPlatform EditMode -testResults <LOCAL_RESULTS_XML>`. Не добавлять `-quit` к выполняющимся тестам: документация Unity предупреждает о несовместимости.
- **AI automation:** агент может генерировать тестовые сценарии и читать XML/Editor logs, но `PASS` только при реально сохранённых результатах; не выдавать скриптовые тесты за human-like playtest.
- **Рекомендация:** **рекомендуется как базовый локальный QA фундамент**; не заменяет ручной игровой тест.
- **Статус:** DOCUMENTED / NOT_RUN; **Editor / PlayMode / Build: 0 фактических запусков**.
- **accessed_at:** 2026-10-08; **tested:** false.
- **Открыто:** точная версия core пакета в конкретном Unity 6000.3.x и installed `LICENSE.md`, реальные XML/Console logs.

## Первоисточники
1. https://docs.unity.com/en-us/engine/6000.3/manual/packages-list/packages-all/pack-core/com-unity-test-framework
2. https://docs.unity.com/en-us/engine/6000.3/manual/scripting/test-framework-introduction/reference-command-line
3. https://docs.unity.com/en-us/engine/6000.6/manual/programming-environment/test-framework-introduction
4. https://github.com/needle-mirror/com.unity.test-framework/blob/master/LICENSE.md (неофициальное зеркало лицензии старой версии; не замена LICENSE установленного пакета)
