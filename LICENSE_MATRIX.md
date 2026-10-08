# LICENSE_MATRIX — проверенные условия и риски

**Дата:** 2026-10-08. Не является юридической консультацией. **GitHub public ≠ open source**.

| Решение | Первичный источник | Статус лицензии | Практическое правило |
|---|---|---|---|
| Mirror | [LICENSE](https://github.com/MirrorNetworking/Mirror/blob/master/LICENSE) | MIT, файл прочитан | Можно использовать и изменять с сохранением copyright/лицензии |
| UniTask | [LICENSE](https://github.com/Cysharp/UniTask/blob/master/LICENSE) | MIT, файл прочитан | Сохранять copyright/лицензионное уведомление |
| FPS Sample | [LICENSE.md](https://github.com/Unity-Technologies/FPSSample/blob/master/LICENSE.md) | Unity Companion License, файл прочитан | Не классифицировать как MIT; проверить отдельные ограничения |
| FishNet | [Repo](https://github.com/FirstGearGames/FishNet) | **НЕ УСТАНОВЛЕНА**: root LICENSE не найден | Не делать правовых выводов до проверки Asset Store/условий отдельных компонентов |
| DOTS Samples | [Repo](https://github.com/Unity-Technologies/EntityComponentSystemSamples) | **НЕ УСТАНОВЛЕНА** (GitHub metadata NOASSERTION) | Искать LICENSE каждого подпроекта до копирования |
| Unity packages | [Unity terms](https://unity.com/legal) | Пакет-специфичные условия | Проверить Unity Companion/Package Terms и связанные лицензии |
| Asset Store starter assets | [Asset Store EULA](https://unity.com/legal/as-terms) | Подчиняются Asset Store EULA/типу лицензии | Бесплатная цена не означает разрешение распространять архив ассетов отдельно |

## Обязательный чек-лист лицензии
1. Upstream первоисточник и точная версия/commit.
2. LICENSE/NOTICE внутри устанавливаемого пакета; не полагаться на GitHub metadata.
3. Коммерческое использование, перераспространение, исходники, модификации, attribution.
4. Ограничения на использование Unity-специфичных ассетов вне Unity.
5. Совместимость нескольких лицензий при комбинации систем (GPL/LGPL/MPL/Unity Companion/Asset Store).
6. Если не найдено — статус **НЕ УСТАНОВЛЕНА**, не копировать и не публиковать бинарники на основе спорного кода.
