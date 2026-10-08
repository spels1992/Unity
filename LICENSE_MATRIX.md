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


## Права комплексных решений, подтверждённые в GitHub (08.10.2026)
| Инструмент | License доказательство | Статус |
|---|---|---|
| [OpenEmpires](Tool_Catalog/open-empires-rts.md) | [MIT](https://github.com/Chilly5/OpenEmpires/blob/main/LICENSE) | Можно изучать и использовать исходники при сохранении notices; содержимое ассетов — отдельно |
| [Moonforge](Tool_Catalog/moonforge-rpg-engine.md) | [MIT](https://github.com/3583Bytes/moonforge-rpg-engine/blob/main/LICENSE) | Встроенный UPM LICENSE тоже MIT |
| [Yarn Spinner Unity](Tool_Catalog/yarn-spinner-unity.md) | [MIT](https://github.com/YarnSpinnerTool/YarnSpinner-Unity/blob/main/LICENSE.md) | Git бесплатен; Asset Store/Itch платные пакеты не нужны |
| [Ink Unity](Tool_Catalog/ink-unity-integration.md) | [MIT text](https://github.com/inkle/ink-unity-integration/blob/master/LICENCE.md) | GitHub metadata NOASSERTION, лицензию смотреть прямо в LICENCE.md |
| [OpenKCC](Tool_Catalog/openkcc-controller.md) | [MIT](https://github.com/nicholas-maltbie/OpenKCC/blob/main/LICENSE.txt) | Sample assets/третьи лица отдельно |
| [EZ Room Generator](Tool_Catalog/ezroomgenerator.md) | [MIT](https://github.com/jastrz/EZRoomGenerator/blob/main/LICENSE) | 0 ₽, UPM dependency requires verify |
| [Edgar Free](Tool_Catalog/edgar-unity-free.md) | [MIT](https://github.com/OndrejNepozitek/Edgar-Unity/blob/master/LICENSE) | PRO платный и запрещён к использованию |
| [Game Lattice + sample](Tool_Catalog/game-lattice-rpg.md) | [Apache-2.0](https://github.com/Toxic-Cookie/game-lattice/blob/main/LICENSE) | Licensed core, precompiled package third-party checking |
| [Unity Modular Inventory](Tool_Catalog/unity-modular-inventory.md) | [MIT](https://github.com/usmanbutt-dev/UnityModularInventorySystem/blob/main/LICENSE) | Kenney assets retain separate license notices |
| [Softlight](Tool_Catalog/softlight-unity6-rpg.md) | [MIT](https://github.com/Ziad-Amr1/softlight/blob/main/LICENSE) | Провести аудит art/audio assets |
| [Unity simple FPS controller](Tool_Catalog/simple-fps-controller-unity6-mit.md) | [MIT](https://github.com/yahiawork/The-First-Person-Controller-Unity-6/blob/main/LICENSE) | Small code set; не готовая игра |
| wendtcloud inventory | [README](https://github.com/wendtcloud/inventory-system) | **BLOCKED_LICENSE_PENDING**: нет файла LICENSE в GitHub tree; не включать как рекомендуемый инструмент |


## Незакрытый вопрос: права на арт из Moonforge Unity sample (08.10.2026)
Код Moonforge — MIT, подтверждено. README Unity Roguelike sample заявляет, что графика 0x72 DungeonTileset II распространяется под CC0 и что файл лицензии доступен по пути Art/DungeonTilesetII/LICENSE.txt. В проверенном полном GitHub tree этот файл по заявленному пути не обнаружен. До отдельной проверки первичного источника https://0x72.itch.io/dungeontileset-ii НЕ публиковать эти изображения и не переносить в выпускаемую игру. Лицензия кода не является лицензией каждого вложенного арт-ассета.
