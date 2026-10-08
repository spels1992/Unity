# Rokoko Studio Live Blender plugin (retargeting)

**Категория:** Blender animation retarget / optional live capture. **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://github.com/Rokoko/rokoko-studio-live-blender |
| Скачать / получить | https://github.com/Rokoko/rokoko-studio-live-blender (официальная страница, releases/скачивание) |
| Лицензия | **LGPL-3.0 в фактическом LICENSE.md**. README badge ошибочно указывает MIT. Обязательная явная пометка несоответствия. |
| Стоимость | Авторская справка говорит, что именно retargeting не является платной функцией и не требует premium account. Live capture через Rokoko Studio/оборудование НЕ обязательный бесплатный путь. |
| Версия, состав или совместимость | README Blender 2.80+, live streaming Rokoko Studio 2.4.8+; exact Blender 5 support не тестировалась |
| Функции | Map bones, auto scale, source/target T-pose, retarget motion, optional face/finger live capture |
| Риски и ограничения | Rokoko Studio/hardware может стоить денег, не использовать для нашей бесплатной цели; add-on требует network during install; README MIT badge против LGPL LICENSE; license notice соблюдать. |
| Статус | GitHub LICENSE/README и Rokoko support о free retarget проверены, плагин не запускался |

## Практическое применение
Для бесплатного retarget только записанная разрешённая FBX анимация + armatures, открыть панель Retargeting → Build Bone List → map bones → Retarget → bake to animation → Unity FBX import.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
