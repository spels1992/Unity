# COMPATIBILITY_MATRIX — версии, зависимости, реальные тесты

Дата: 2026-10-08. Статусы: **DOC** документально заявлено; **TESTED** наш воспроизводимый тест; **UNKNOWN** не установлено; **CONFLICT** известный конфликт. **На текущий момент TESTED нет.**

| Решение | Официально указана версия | Тип | Статус с Unity 6.3 | Внутренние конфликты |
|---|---|---|---|---|
| Cinemachine | 3.1.7 для 6000.3 | Unity Package | DOC: 6000.3 | При миграции с 2.x есть breaking changes |
| AI Navigation | 2.0.15 для 6000.3 | Unity Package | DOC: 6000.3 | Система навигации, не behavior-tree и не combat AI |
| DOTS Samples | Unity 6.2 + Entities 1.4 и др. | демонстрационные проекты | UNKNOWN; не переносить без теста | ECS и обычный MonoBehaviour workflow требуют специальной интеграции |
| Mirror | Версию 6.3 в проверенном README не подтверждали | Сетевой фреймворк | UNKNOWN | Не устанавливать вместе с FishNet «для улучшения сети» без проектной архитектуры |
| FishNet | В проверенном README версия 6.3 не указана | Сетевой фреймворк | UNKNOWN | Custom licence, не смешивать с Mirror как один transport |
| UniTask | Точная ветка 6.3 требует проверки | Async библиотека | UNKNOWN | Проверять lifetime и отмену async |
| FPS Sample | Unity 2018.3.8f1 | учебная игра | UNKNOWN/legacy | HDRP старой версии; требуется портирование |
| Unity 2d-extras Git repo | upstream объявил прекращение развития | Tilemap scripts | Legacy | Предпочесть Unity Tilemap Extras через UPM |

## Правила записи результата теста
`stack ID | Unity editor exact | package versions | render pipeline | OS+GPU+target | сценарий | результат | crash log/PR/commit | дата | tester`.

**Никогда** не повышать «UNKNOWN» до «TESTED» по удачному ответу нейросети, Reddit-комментарию или README.

### Подозрительные сочетания
- Два разных сетевых стека как центральные транспорты без адаптера — технически конфликтующие концепции.
- Набор камер и контроллеров с собственными input/camera managers может дублировать управление.
- HDRP-only ассеты нельзя считать совместимыми с URP автоматически.
- Один giant framework и 5 отдельных manager-пакетов часто дублируют инвентарь, input, save и AI: проверить границы ответственности.

| Input System | com.unity.inputsystem 1.20.1 для 6000.3 | Unity Registry | DOC 6000.3 | Согласовать mappings со Starter Controller |
| Tilemap Extras | com.unity.2d.tilemap.extras 6.0.3 для 6000.3 | Unity Registry | DOC 6000.3 | Старый 2d-extras Git объявлен read-only |
| First Person + Third Person Controller | Asset Store 2.0.1 (17.09.2026) | Free Asset | DOC URP 6000.3.0f1; Built-in/HDRP нет | Non standard EULA |
| 2D Game Kit | Asset Store 5.0 (23.03.2026) | Free Asset | DOC URP 6000.3.0f1 | Standard EULA, Extension Asset |
| FPS Microgame | Asset Store DEPRECATED | Old Asset | Недоступен новым пользователям | НЕ рекомендовать как новый starter |

## Предлагаемые полностью бесплатные стеки — ПОКА не проверены
| Стек | Основные компоненты | Статус и основание |
|---|---|---|
| [2D-PLATFORMER-FREE](21_Compatible_Stacks/FREE_STACKS.md) | Kenney CC0 + Input System + Physics2D + Tilemap Extras | ASSUMED: официальные компоненты и бесплатная графика, live теста нет |
| [3D-RPG-EXPLORATION-FREE](21_Compatible_Stacks/FREE_STACKS.md) | Quaternius Standard Characters/Animations + Unity Input, Cinemachine, AI Navigation | ASSUMED: Quaternius заявляет совместимые rig, но retarget не тестировался |
| [3D-SCI-FI-CORRIDOR-FREE](21_Compatible_Stacks/FREE_STACKS.md) | Quaternius Standard Sci-Fi + Unity Camera/Input + URP | ASSUMED: FBX импорт и prefab/коллизии не проверены |
| [BOAT-RACING-REFERENCE](21_Compatible_Stacks/FREE_STACKS.md) | Boat Attack + Water | LEGACY: Unity 2019 demo, Unity 6 не подтверждена |

**В нашей базе значение VERIFIED = 0** до живых tests/build на целевой машине. Ссылки на package версии не заменяют результаты тестов.


## Фреймворки Unity 6: проверка README против исходной конфигурации
| Система | Upstream evidence | Статус интеграции у нас |
|---|---|---|
| [OpenEmpires](Tool_Catalog/open-empires-rts.md) | README 6000.3.9f1; фактический ProjectVersion.txt = **6000.5.9f1** | DOC-конфликт; build UNKNOWN |
| [Moonforge](Tool_Catalog/moonforge-rpg-engine.md) | UPM 1.2.0, Unity 2022.3+ | UNKNOWN на 6000.3 |
| [Yarn Spinner](Tool_Catalog/yarn-spinner-unity.md) | 3.2.8 UPM / 2022.3+ | UNKNOWN на 6000.3 |
| [Ink](Tool_Catalog/ink-unity-integration.md) | 2.0.0 UPM / 2022.3+ | UNKNOWN на 6000.3 |
| [Game Lattice](Tool_Catalog/game-lattice-rpg.md) | 0.0.0-dev UPM / 2021.2+; example ProjectVersion 6000.4.11f1 | DOC package, no Player test |
| [Softlight](Tool_Catalog/softlight-unity6-rpg.md) | ProjectVersion.txt 6000.3.7f1 | DOC only, early prototype |
| [Unity Modular Inventory](Tool_Catalog/unity-modular-inventory.md) | ProjectVersion.txt 6000.0.50f1 | DOC only, newer variants unknown |
| [EZ Room](Tool_Catalog/ezroomgenerator.md) | 0.1.0 UPM Unity 6000.0+, FBX Exporter 5.1.5 declared | DOC, integration dependency needs test |
| [Edgar Free](Tool_Catalog/edgar-unity-free.md) | 2.1.0 UPM Unity 2019.3+; PRO features paid | DOC only; newer Unity unknown |
| [OpenKCC](Tool_Catalog/openkcc-controller.md) | 1.5.0 UPM Unity 2019.4+, development last 2023 | Unity 6 unknown |

**VERIFIED still equals zero**: source code/README/manifest checks do not mean runtime compatibility.
