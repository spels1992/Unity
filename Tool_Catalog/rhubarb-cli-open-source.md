# Rhubarb Lip Sync (offline CLI)

**Категория:** Local phoneme / mouth cue extractor for animation pipelines. **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://github.com/DanielSWolf/rhubarb-lip-sync |
| Скачать / получить | https://github.com/DanielSWolf/rhubarb-lip-sync (официальная страница, releases/скачивание) |
| Лицензия | Основной Rhubarb MIT; LICENSE.md перечисляет third-party MIT/BSD/Boost и другие notices, учитывать при распространении бинарника. |
| Стоимость | 0 ₽, локальный CLI, облачный сервис/токены не нужны |
| Версия, состав или совместимость | Утилита Windows/macOS/Linux из релизов, не Blender addon сама по себе; язык/recognizer по release документации |
| Функции | Принимает аудиозапись, выдаёт тайминги mouth shapes для 2D/3D губ, потенциально доступен JSON/TSV |
| Риски и ограничения | Не генерирует голос и не заменяет диктора. Точность для русского, сложных голосов/шумов и неверной транскрипции не обещать. Бинарник может иметь сторонние notice obligations. |
| Статус | Официальный LICENSE.md прочитан; локально CLI не выполнялся |

## Практическое применение
Подготовить audio законно → скачать официальную CLI release → запустить recognizer и экспорт mouth cues → Blender Shape Keys/Animation Actions или Unity runtime facial rig → вручную QA таймингов.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
