# Generate Tree Plugin (YGForge)

**Категория:** Blender 5+ procedural low-poly trees. **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://github.com/YGForge/LowPolyTreeGen |
| Скачать / получить | https://github.com/YGForge/LowPolyTreeGen (официальная страница, releases/скачивание) |
| Лицензия | GPL-3.0-or-later из blender_manifest.toml и официальной Blender Extensions |
| Стоимость | 0 ₽, скачать официально https://extensions.blender.org/add-ons/generate-tree-plugin/ |
| Версия, состав или совместимость | v1.1.5 manifest, Blender 5.0.1+ (2026-09-21 release) |
| Функции | Сгенерированные стволы/ветки/пучки листьев, корни, random seed, коллекция GeneratedTree |
| Риски и ограничения | Каждый Generate создаёт новую коллекцию, автоматически старые не удаляются. Проверить scale/UV, а licence на отдельно скачанные листовые текстуры не назначается самим генератором. |
| Статус | README+manifest и официальный Blender Extensions проверены, не запускалось |

## Практическое применение
Blender 5.0.1+ → установить бесплатное расширение → панель Tree Gen → выбрать seed и foliage/branch parameters → Generate → провести polycount/UV check → GLB/FBX → Unity prefab + LODGroup.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
