# Sapling Tree Gen (официальное расширение Blender)

**Категория:** Blender procedural trees / curves. **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://extensions.blender.org/add-ons/sapling-tree-gen/ |
| Скачать / получить | https://extensions.blender.org/add-ons/sapling-tree-gen/ (официальная страница, releases/скачивание) |
| Лицензия | GPL-3.0+ у версии 0.3.7 (Blender Extensions version history); предыдущая 0.3.6 GPL-2.0+ |
| Стоимость | 0 ₽, официальная Blender Extensions карточка, без платного доступа |
| Версия, состав или совместимость | Blender 4.4+ заявлено для v0.3.7, но пользователи сообщают сбои в Blender 5.x, особенно tree animation; v0.3.6 Blender 4.2 LTS+ |
| Функции | Parametric tree curves: branches, trunks, canopy settings, quick tree prototypes |
| Риски и ограничения | Official support limited; отзывы указывают, что animation/old API не работает в некоторых Blender 5.x. Тестировать именно на установленной версии перед массовым применением. |
| Статус | Версии, лицензии и жалобы в официальной Blender Extensions, live Blender test нет |

## Практическое применение
Blender Extensions → установить Sapling Tree Gen → Add → Curve → Sapling Tree Gen → задать seed/branch parameters → превратить curves в mesh при необходимости → листья отдельными оптимизированными low-poly planes → экспортить в Unity.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
