# Modular Tree (MTree, GoodPie)

**Категория:** Blender procedural trees / node based foliage. **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://extensions.blender.org/add-ons/modular-tree/ |
| Скачать / получить | https://extensions.blender.org/add-ons/modular-tree/ (официальная страница, releases/скачивание) |
| Лицензия | GPL-3.0+ Blender addon; core library MIT (указано в официальной странице расширения) |
| Стоимость | Бесплатная Blender Extensions, оплата не требуется |
| Версия, состав или совместимость | v5.5.2, Blender 4.3.1+ по странице расширения; заявлена Blender 5.1 поддержка, Windows/Linux/macOS builds |
| Функции | Oak, Pine, Willow presets; node-based procedural branch/leaf generator; multiple crown shapes, growth and pivot painter texture export |
| Риски и ограничения | Не считать node tree совместимым с Unity. Расширение требует файловый доступ для экспорта pivot painter; высокополигональные деревья требуют отдельного LOD/atlasing. |
| Статус | Официальная карточка и версия/лицензия подтверждены; live тест нет |

## Практическое применение
Установить поддерживаемую платформенную сборку → дерево из preset Oak/Pine/Willow → tweak nodes/seed → запечь/экспортировать mesh + PBR textures → Unity collision/LOD/vegetation instancing.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
