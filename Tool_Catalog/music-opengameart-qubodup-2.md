# qubodup Two Simple Game Music Loops

**Категория:** CC0 menu / in-game music (OGG+WAV). **Дата исследования:** 2026-10-09. **Состояние:** DOCUMENTED, не тестировалось локально. **Дополнительный бюджет:** 0 ₽.

| Поле | Доказанные сведения / ограничения |
|---|---|
| Официальная страница/источник | https://opengameart.org/content/two-simple-game-music-loops |
| Скачать / получить | https://opengameart.org/content/two-simple-game-music-loops (официальная страница, releases/скачивание) |
| Лицензия | CC0, original asset page; credit optional |
| Стоимость | 0 ₽, готовые OGG downloads, без Ableton Live проекта |
| Версия, состав или совместимость | 2 композиции, каждая в OGG и WAV, опубликовано 2025-04-06 |
| Функции | Main menu wait tune и in-game level music, сразу подходят для looped soundtrack |
| Риски и ограничения | Автор использовал Ableton stock instruments: исходные DAW-проекты не нужны, при высоких требованиях к rights возможен дополнительный аудит происхождения samples. Лицензия CC0 подтверждена на странице. |
| Статус | CC0 on upstream OpenGameArt, audio loop runtime не тестировался |

## Практическое применение
Скачать OGG для Unity (экономнее WAV) → import AudioClip → AudioMixer/MusicBus, плавное переключение меню/игры, loop QA.

## Приёмка без выдуманных тестов
1. Уточнить точный tag/версию Blender/Unity и права на используемые **входные** аудио, модели и текстуры.
2. Скачать только конкретную бесплатную версию без карточки оплаты и создать **отдельный тестовый проект**.
3. Проверить заявленную функцию, Blender render/Unity PlayMode, экспорт morph/mesh/animation/music и Windows Player Build, затем зафиксировать ошибки и тестовую конфигурацию.
4. Пока этих доказательств нет, статус не выше `DOCUMENTED`; совместимость с рабочими проектами пользователя **не гарантируется**.
5. В GameLibrary хранить **ссылку и инструкцию**, не чужие ZIP/бинарные материалы.

[ZERO COST Policy](../FREE_ONLY_POLICY.md) · [Blender/Unity Pipeline](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
