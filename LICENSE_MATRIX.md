# LICENSE_MATRIX — проверенные условия и риски

**Дата:** 2026-10-08. Не является юридической консультацией. **GitHub public ≠ open source**.

| Решение | Первичный источник | Статус лицензии | Практическое правило |
|---|---|---|---|
| Mirror | [LICENSE](https://github.com/MirrorNetworking/Mirror/blob/master/LICENSE) | MIT, файл прочитан | Можно использовать и изменять с сохранением copyright/лицензии |
| UniTask | [LICENSE](https://github.com/Cysharp/UniTask/blob/master/LICENSE) | MIT, файл прочитан | Сохранять copyright/лицензионное уведомление |
| FPS Sample | [LICENSE.md](https://github.com/Unity-Technologies/FPSSample/blob/master/LICENSE.md) | Unity Companion License, файл прочитан | Не классифицировать как MIT; проверить отдельные ограничения |
| FishNet | [LICENSE.md](https://github.com/FirstGearGames/FishNet/blob/main/LICENSE.md) | **Custom FishNet License**, файл прочитан 2026-10-08 | Безвозмездное использование для игр; **запрет использования в конкурирующих networking products**; Pro/third-party — отдельные условия |
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

| First Person + Third Person Controller | [Asset Store](https://assetstore.unity.com/packages/3d/characters/first-person-third-person-character-controllers-196526) | **Non standard EULA**, текст ещё требует отдельной проверки | Не объявлять стандартной Asset Store лицензией |
| 2D Game Kit | [Asset Store](https://assetstore.unity.com/packages/templates/packs/2d-game-kit-2d-sample-project-107098) | Standard Asset Store EULA, Extension Asset | Изучить ограничения redistribution, особенно при упаковке в reusable tool |

| CoplayDev MCP for Unity | [LICENSE](https://github.com/CoplayDev/unity-mcp/blob/main/LICENSE) | MIT | Право использовать код ≠ Unity-authorized AI gateway |
| CoderGamester MCP Unity | [LICENSE.md](https://github.com/CoderGamester/mcp-unity/blob/main/LICENSE.md) | MIT | Право использовать код ≠ Unity-authorized AI gateway |

## Дополнение 2026-10-08: источники ассетов и крупных проектов
| Решение | Лицензия и ссылка | Цена внедрения | Правило |
|---|---|---|---|
| [Poly Haven](Tool_Catalog/poly-haven.md) | [CC0](https://polyhaven.com/license) | Отдельные assets: 0 ₽ | Не путать с лицензией сайта/платными сервисами |
| [Kenney](Tool_Catalog/kenney-free-assets.md) | [CC0](https://kenney.nl/support) | Отдельные packs: 0 ₽ | All-in-1 bundle платный, запрещён |
| [Quaternius](Tool_Catalog/quaternius-free-assets.md) | [CC0](https://quaternius.com/faq.html) | Standard: 0 ₽ | Paid Source с готовыми Unity projects не использовать |
| [Chop Chop](Tool_Catalog/chop-chop-open-project-1.md) | [Apache-2.0](https://github.com/UnityTechnologies/open-project-1/blob/main/LICENSE) | Source: 0 ₽ | Проверить лицензии ассетов отдельно |
| [Boat Attack](Tool_Catalog/boat-attack-urp-demo.md) | [Unity Companion](https://github.com/Unity-Technologies/BoatAttack/blob/master/LICENSE.md) | Source: 0 ₽ | Не MIT, Unity project dependent restrictions |
| [Boat Attack Water](Tool_Catalog/boat-attack-water.md) | [Unity Companion](https://github.com/Unity-Technologies/boat-attack-water/blob/master/LICENSE.md) | Source: 0 ₽ | Совместимость Unity 6 не установлена |

**Все решения, реально используемые в проекте, должны иметь нулевую дополнительную стоимость.** Условия доступа к бесплатным assets и продуктам могут измениться, проверять перед скачиванием.
