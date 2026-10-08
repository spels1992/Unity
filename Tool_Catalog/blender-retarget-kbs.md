# Retarget (KBS-DEV)

**Категория:** Blender 5 animation retarget / Rigify conversion. **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://github.com/KBSBAUDRICE/Retarget |
| Скачать / получить | https://github.com/KBSBAUDRICE/Retarget (официальная страница, releases/скачивание) |
| Лицензия | GPL-3.0 или позднее по официальной Blender Extensions; GitHub LICENSE содержит GPLv3 |
| Стоимость | Бесплатное официальное расширение https://extensions.blender.org/add-ons/retarget/; без SaaS |
| Версия, состав или совместимость | v5.2.0 (2026-08-23), Blender 5.0+; **НЕ подходит для Blender 4.x** в версии 5 |
| Функции | Animation retargeting rigs, presets Mixamo/Unreal/VRoid/MMD, bind metarig to Rigify, action/NLA manager |
| Риски и ограничения | Неизвестно насколько подходит к нестандартным скелетам и hard-surface rigs; third-party presets не дают прав на исходную mocap-анимацию. Blender 4.x требует другую версию инструмента. |
| Статус | GitHub README/LICENSE и официальный version history проверены, Blender test нет |

## Практическое применение
Получить исходный FBX motion законно → импортировать 2 armatures → Source/Target bones/pose → preset или bone mapping → Bind/Retarget → bake результат на deform bones → Unity Humanoid Avatar test.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
