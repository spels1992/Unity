# Rhubarb Lip Sync NG — Blender addon

**Категория:** Blender face animation / viseme lipsync from audio. **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://github.com/Premik/blender_rhubarb_lipsync_ng |
| Скачать / получить | https://github.com/Premik/blender_rhubarb_lipsync_ng (официальная страница, releases/скачивание) |
| Лицензия | MIT по LICENSE и blender_manifest.toml; базовый Rhubarb engine имеет свои MIT/BSD/Boost notices |
| Стоимость | GitHub releases бесплатно, хотя manifest также ссылается на платную/добровольную BlenderMarket страницу: выбирать GitHub, не покупать |
| Версия, состав или совместимость | v1.8.1 manifest, Blender min 3.3.0, Blender 4.2+ extension installation; Windows/macOS/Linux release archives |
| Функции | Автоматические mouth-shape keyframes для pose library/shape keys из готовой речи; 2D planes/3D faces |
| Риски и ограничения | Русская речь — качество отдельного распознавателя не подтверждено, PocketSphinx обычно заточен под английский, phonetic recognizer может дать иной результат; lip-sync motion требует локальной оценки. API/Blender 5 compatibility не доказана тестом. |
| Статус | README MIT/LICENSE и manifest проверены; синхронизация не запускалась |

## Практическое применение
Подготовить запись голоса и blendshapes/poses A..X для рта → скачать совместимый Windows ZIP release (engine included) → Blender Extension Install → проверить Rhubarb CLI → импорт audio → generate mouth shape keys → bake и экспорт morph targets/animations в Unity.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
