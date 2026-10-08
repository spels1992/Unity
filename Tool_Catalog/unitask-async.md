# UniTask — эффективные async/await операции Unity

- **Категория:** C# / Async / Performance / Loading
- **Первоисточник:** [Cysharp/UniTask](https://github.com/Cysharp/UniTask).
- **Лицензия:** MIT, [LICENSE](https://github.com/Cysharp/UniTask/blob/master/LICENSE) прочитан напрямую.
- **Цена:** 0 ₽, FREE, не требует платного API или аккаунта для Git UPM установки.
- **Версия:** пакет `com.cysharp.unitask` имеет `version: 2.5.11` на проверенной ветке master; `unity: 2018.4` в package.json (это минимум, не доказательство Unity 6.3).
- **Установка:** `https://github.com/Cysharp/UniTask.git?path=src/UniTask/Assets/Plugins/UniTask` через Package Manager → Git URL. Для production фиксировать конкретный release/tag/commit.
- **Что даёт:** await для Unity AsyncOperation, корутин, задержек кадров, таймеров, реактивных и асинхронных потоков; TaskTracker; оптимизация выделений памяти.
- **Когда применять:** загрузка уровней, ресурсов, UI диалогов, сетевые запросы (только собственный бесплатный backend), последовательности логики.
- **Ограничения:** не заменяет Unity main thread; cancellation при уничтожении GameObject обязательна; избегать `async void` и непроверенных необрабатываемых исключений.
- **Конфликты:** сначала сравнить с встроенным Unity Awaitable и корутинами; не добавлять лишнюю стороннюю зависимость, когда достаточно стандартного API.
- **FREE fallback:** корутины Unity и встроенный Awaitable, если доступен в используемой версии Editor.
- **Smoke:** отдельный проект: await scene load + cancellation token при уничтожении, обработка исключений, EditMode/PlayMode тест, отсутствие leaked tasks и compile errors.
- **last_checked:** 2026-10-08; **verification:** DOCUMENTED; **price_paid:** 0; **Editor tested:** NO.
