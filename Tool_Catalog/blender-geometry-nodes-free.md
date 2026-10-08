# Blender Geometry Nodes (встроенный)

**Категория:** Blender procedural scenes, vegetation, instancing. **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://docs.blender.org/manual/en/4.5/modeling/geometry_nodes/index.html |
| Скачать / получить | https://docs.blender.org/manual/en/4.5/modeling/geometry_nodes/index.html (официальная страница, releases/скачивание) |
| Лицензия | Blender GPL (инструмент); лицензию исходных моделей/текстур учитывать отдельно |
| Стоимость | Полностью встроено в бесплатный Blender |
| Версия, состав или совместимость | Blender 4.5 LTS manual; версии нод меняются |
| Функции | Node graphs, distribution/instances on points, randomize scale/rotation, fields, procedural scattering, bake |
| Риски и ограничения | Blender Geometry Nodes tree не становится автоматически Unity runtime procedural graph. При FBX/GLB обычно надо Realize Instances и Apply/bake; это может резко увеличить полигоны, поэтому часто лучше экспортировать отдельные meshes и точки размещения для Unity instancing. |
| Статус | Официальная документация, локально не тестировалось |

## Практическое применение
Собрать landscape mesh → Distribute Points on Faces → Instance on Points с CC0 травой/кустами → Seed и density exposed → проверить окружение → экспортировать реальные meshes/prefabs по мере необходимости.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
