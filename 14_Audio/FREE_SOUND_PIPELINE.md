# Бесплатный аудиопайплайн игровой разработки — от SFX до сборки

**Исследование 2026-10-08, Unity live тесты не выполнялись.** Цель: закрыть звуки UI, ударов, RPG и sci-fi, а также короткие победные музыкальные отбивки без платных звуковых библиотек.

## Конкретные CC0 наборы
| Название | Содержание | Файлы на официальной странице | Лицензия | Карточка |
|---|---|---:|---|---|
| Kenney UI Audio | Click, switch, button | 50 | CC0 | [Открыть](../Tool_Catalog/kenney-ui-audio.md) |
| Kenney Impact Sounds | Impact, foley | 130 | CC0 | [Открыть](../Tool_Catalog/kenney-impact-sounds.md) |
| Kenney RPG Audio | RPG footsteps/weapon/foley | 50 | CC0 | [Открыть](../Tool_Catalog/kenney-rpg-audio.md) |
| Kenney Sci-fi Sounds | Space/laser/engine | 70 | CC0 | [Открыть](../Tool_Catalog/kenney-sci-fi-sounds.md) |
| Kenney Music Jingles | Short success/failure cues | 85 | CC0 | [Открыть](../Tool_Catalog/kenney-music-jingles.md) |

Суммарно авторские страницы заявляют **385 файлов** (не означает 385 уникальных игровых механик). Каждый отдельный набор можно скачать за **0 ₽** через `Continue without donating`; **платный All-in-1 не нужен**. Лицензии CC0 прямо на странице каждого набора.

## Два слоя аудиосистемы
**Данные:** URL + CC0 license + конкретные WAV/OGG/MP3, собственный каталог `Assets/_Game/Audio/{UI,Effects,Environment,Music,Voice}`, импорт в AudioClip. Сначала проверить формат скачанного пакета и sample rate, нельзя считать архив уже импортированным.

**Логика:** встроенные бесплатные Unity AudioSource/AudioListener/AudioMixer, события UI Click/Impact/Footstep/Win; простая централизованная диспетчеризация AudioEvent ID → pool AudioSources; разные mixer groups и gain.

## Принципы качества
1. **UI**: 2D короткие clips, не запускать повторно dozens voices при быстром клике. Установить лимит одновременного воспроизведения.
2. **Impact**: материалы поверхности должны выбирать разные банки; разрешить random pitch небольшого диапазона для вариативности.
3. **3D world**: volume rolloff и max distance, spatial blend и occlusion проверить в PlayMode, не объявлять автоматическим.
4. **Music jingles**: не использовать короткие отбивки как длительный зацикленный soundtrack без оценки швов; сделать fade/crossfade и mixer levels.
5. **Сборка**: для частых коротких эффектов использовать подходящий load type/компрессию; сравнить memory/CPU в профайлере на PC/mobile, не выдумывать bitrate и FPS.
6. **Мобильная платформа**: проверить размер аудиобанка, sample rate, decode/load cost, фоновые/тихие режимы.
7. **Юридический реестр**: даже при CC0 сохранять `source_url, license_url, asset_name, downloaded_at`; бесплатные Kenney не означают, что любой найденный в интернете трек тоже CC0.

## Жанровые готовые связки
- **Платформер**: Kenney UI Audio + Impact Sounds + Music Jingles.
- **RPG/Roguelike**: Kenney RPG Audio + Impact Sounds + UI Audio, отдельно проверить музыкантский CC0 для полноформатной фоновой музыки.
- **Sci-fi FPS**: Sci-fi Sounds + Impact + UI Audio; для weapons выбирать соответствующий AudioEvent, не требуются платные аудиосистемы.
- **Racing**: Sci-fi для futuristic engines, Impact для столкновений, Music Jingles для finish; real engines/wheels underrepresented — позже найти CC0 запись с оригинальной лицензией.

## AI-assisted, но 0 ₽
ИИ-агент может заполнять каталог с URL, лицензиями, создавать локальные Unity AudioMixer assets через Editor API, присваивать SoundEvent tags, проверять сцену/Console и формировать сценарий теста. Генерация аудио через платные внешние API **не требуется и не разрешена**.

## Смоук-тест при доступной Unity
1. Создать отдельную чистую scene, без изменений в рабочих проектах.
2. Импортировать три файла из каждого CC0 архива.
3. Одно UI событие, одно impact с трёхмерным источником, один musical jingle.
4. Проверить несколько быстрых clicks, 3D distance rolloff, restart/stop/fade, PlayMode, Player Build и mobile/desktop audio decoding.
5. Записать version Editor, exact clips, actual memory/CPU, баги/ссылки. До этого статус `NOT_RUN`.

**Бесплатная альтернатива:** штатные Unity AudioSource/AudioMixer и собственные записи, без обязательной интеграции Wwise/FMOD commercial tiers.
