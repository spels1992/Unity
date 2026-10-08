# COMPATIBILITY_MATRIX — версии, зависимости, реальные тесты

Дата: 2026-10-08. Статусы: **DOC** документально заявлено; **TESTED** наш воспроизводимый тест; **UNKNOWN** не установлено; **CONFLICT** известный конфликт. **На текущий момент TESTED нет.**

| Решение | Официально указана версия | Тип | Статус с Unity 6.3 | Внутренние конфликты |
|---|---|---|---|---|
| Cinemachine | 3.1.7 для 6000.3 | Unity Package | DOC: 6000.3 | При миграции с 2.x есть breaking changes |
| AI Navigation | 2.0.15 для 6000.3 | Unity Package | DOC: 6000.3 | Система навигации, не behavior-tree и не combat AI |
| DOTS Samples | Unity 6.2 + Entities 1.4 и др. | демонстрационные проекты | UNKNOWN; не переносить без теста | ECS и обычный MonoBehaviour workflow требуют специальной интеграции |
| Mirror | Версию 6.3 в проверенном README не подтверждали | Сетевой фреймворк | UNKNOWN | Не устанавливать вместе с FishNet «для улучшения сети» без проектной архитектуры |
| FishNet | В проверенном README версия 6.3 не указана | Сетевой фреймворк | UNKNOWN | Альтернатива Mirror, не прямое дополнение |
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
