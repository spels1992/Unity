# Blender Decimate для LOD (встроенный)

**Категория:** Blender polygon reduction / LOD mesh preparation. **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://docs.blender.org/manual/en/4.5/modeling/modifiers/generate/decimate.html |
| Скачать / получить | https://docs.blender.org/manual/en/4.5/modeling/modifiers/generate/decimate.html (официальная страница, releases/скачивание) |
| Лицензия | Blender GPL tool; создаваемые meshes под лицензией автора/источника |
| Стоимость | 0 ₽, встроенный Blender modifier, без платного LOD addon |
| Версия, состав или совместимость | Blender 4.5 LTS |
| Функции | Collapse/Un-Subdivide/Planar decimation, сохранение части silhouette, уменьшение количества faces |
| Риски и ограничения | Decimate не равен умной автоматической генерации UV-aware/rig-preserving LODs. Проценты исходной геометрии не универсальные; контуры и silhouette могут деградировать, требуется ручное QA. |
| Статус | Blender manual, реального LOD benchmark нет |

## Практическое применение
Дублировать highpoly model → на копиях Decimate с контролируемыми ratios → не ломать UV/weighted normals/rig → экспортировать LOD0/LOD1/LOD2 FBX/glTF → в Unity создать LODGroup и протестировать переключение и pop artifacts.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
