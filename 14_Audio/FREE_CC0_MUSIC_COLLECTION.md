# Бесплатные музыкальные темы и лупы для игры — конкретные CC0 наборы

**Дата исследования: 2026-10-09.** Мы проверяем **каждую страницу с лицензией**. Не объявлять весь OpenGameArt CC0: на сайте есть CC-BY, CC-BY-SA, GPL и другие виды лицензий.

| Музыка | Автор / точный источник | Количество | Лицензия | Тематика |
|---|---|---|---|---|
| [SubspaceAudio 12 Music Loops](../Tool_Catalog/music-opengameart-subspace-12.md) | https://opengameart.org/content/12-music-loops | **12** | CC0 на asset page | Retro/Chiptune/Action |
| [pauliuw Music Loops](../Tool_Catalog/music-opengameart-puzzle-loops.md) | https://opengameart.org/content/music-loops | **4** | CC0 на asset page | Puzzle/ambient/background |
| [qubodup Two Simple Game Loops](../Tool_Catalog/music-opengameart-qubodup-2.md) | https://opengameart.org/content/two-simple-game-music-loops | **2** | CC0 на asset page | Menu + level music |
| [drakzlin Music Loops](../Tool_Catalog/music-opengameart-drakzlin-loops.md) | https://opengameart.org/content/music-loops-0 | **неизвестно** (5 ZIP архивов) | CC0 на asset page | Action/battle/horror/chiptune |

**Минимум 18 точно заявленных композиций** из первых трёх карточек плюс непроверенное количество дорожек в пяти архивах drakzlin. Не придумывать общее число, пока сами ZIP файлы не изучены.

## Жанровая сетка
- **Платформер/ретро RPG:** SubspaceAudio 12 Loops, Kenney Music Jingles (короткие отбивки, не full BGM).
- **Логическая игра/викторина:** pauliuw Music Loops / qubodup menu tune.
- **RPG/боевые сцены:** drakzlin battle/action packs и Subspace chiptune; в каждом проверить ритм и seamless loops.
- **Хоррор:** drakzlin horror архив; не скачивать все 100+ MB, если нужен один файл.
- **Главное меню:** qubodup menu loop и OGG format.

## Правильное скачивание и внедрение
1. Открыть **конкретную карточку OpenGameArt**, визуально подтвердить `License(s): CC0`, автора, имя файла и URL.
2. Скачать только нужную композицию (для drakzlin минимальный соответствующий ZIP). Сохранить `audio_name, url, author, license_url, downloaded_at`.
3. Не заменять CC0 лицензии страницы на слова «royalty-free» без подтверждения: **royalty-free не всегда значит бесплатно или CC0**.
4. В Unity создавать `Assets/_Game/Audio/Music`, на базе AudioClip и AudioMixer. Проверить Loop, seamless seam, RMS/loudness и треск при перескоке между уровнями.
5. Настроить группы `Music/Effects/UI/Voice` и fade/crossfade без платного FMOD/Wwise.
6. Проверить размер и режим стриминга/декодирования. В коротких композициях против длинных треков оптимальные настройки могут различаться, **числа памяти измерить**.
7. Нужные исходные музыкальные файлы хранить в **рабочем проекте**, не в нашей библиотеке GitHub; общая библиотека хранит Markdown/URL/лицензию.

## Что пока не считаем подтверждённым
- Отсутствует проверка исходного состава ZIP, спектра/длительности, наличия Content ID conflicts, seamless loop, размера итоговых файлов Unity.
- Для старого [pauliuw](https://opengameart.org/content/music-loops) файлы FL Studio/Sibelius — платные DAW могут быть нужны для правки **исходного проекта**, однако готовый MP3 бесплатен.
- Нельзя утверждать, что авторская CC0 лицензия на странице исключает риск неавторизованных чужих сэмплов; при сомнениях в происхождении запросить сведения и выбрать прозрачный оригинальный звук.
- Отдельный исследовательский этап: найти **открытые бесплатные программы** для самостоятельного создания full soundtrack (LMMS, Ardour, Audacity, MuseScore) и проверить их лицензии, входящие samples и экспорт для коммерческой игры.

[Аудиопайплайн](FREE_SOUND_PIPELINE.md) · [Требование нулевой оплаты](../FREE_ONLY_POLICY.md).
