# Бесплатные анимации и губы: ретаргет, face/viseme, Unity без платных API

**Дата: 2026-10-09. Состояние: DOCUMENTED.** Это план применения, а не запись об успешном Blender/Unity запуске.

## Какой инструмент выбирать

| Нужна возможность | Бесплатное решение | Версия / лицензия | Критическое условие |
|---|---|---|---|
| Перенос FBX animation Mixamo/Unreal/VRoid/MMD на персонажа | [Retarget KBS-DEV](../Tool_Catalog/blender-retarget-kbs.md) | Blender 5+, GPLv3+, v5.2.0 | Не подходит к Blender 4.x в этой версии |
| Перенос движения на другая Armature с авто bone mapping | [Rokoko Blender addon](../Tool_Catalog/blender-rokoko-retarget.md) | LGPL-3.0 по фактическому LICENSE.md | **README MIT badge неверен; не путать с платными capture/studio features** |
| Липсинк из готового голоса с генерацией shape key poses | [Rhubarb Lipsync NG](../Tool_Catalog/rhubarb-lip-sync-ng-blender.md) | MIT, v1.8.1, Windows/Blender 4.2+ extension install | Подвижные губы не гарантируют качественный русский дубляж |
| Mouth cues offline, пригодные для 2D и 3D | [Rhubarb CLI](../Tool_Catalog/rhubarb-cli-open-source.md) | MIT core, дополнительные notices в LICENSE.md | Входной голос должен быть законно получен/сгенерирован отдельно |

## Путь A: перенос анимаций между персонажами
1. Выбрать анимацию с подтверждёнными правами (например бесплатная часть Quaternius Standard, если source license действительно подтверждена), а не произвольный файл из интернета.
2. Импортировать Source FBX (с action) и Target armature в отдельный Blender test file, проверить object scale и T-pose / A-pose.
3. Под Blender 5.x: Retarget KBS-DEV → preset/bone list → сопоставить pelvis/legs/arms/fingers → retarget action.
4. Альтернатива Rokoko: Source/Target armatures → Build Bone List → Auto Scale (если полезно) → Use Pose → Retarget. Официальная справка говорит: **retargeting бесплатно, Premium не нужен**.
5. Bake animation на deform bones, сохранив root motion/foot contact/clip lengths; проверить ключи и цикличность.
6. Export FBX/glTF → Unity `Animation Type Humanoid` и Avatar mapping → Animator → locomotion blend tree. Проверить плечи/таз/скольжение ног.
7. Do NOT mix multiple plugins into the active user Blender scene before testing their compatibility.

## Путь B: движение губ под озвучку
1. Получить готовый MP3/WAV диктора; сам Rhubarb **не создаёт аудио** и не является голосовым генератором.
2. Подготовить mouth shape keys/pose library. Их количество/названия берём из документации выбранной release, не придумываем экспортные названия заранее.
3. Blender Rhubarb NG бесплатный ZIP из `Premik/blender_rhubarb_lipsync_ng/releases` (не BlenderMarket как обязательный путь). Проверить включённый Rhubarb executable.
4. Импортировать audio → generate keyframes/cues → вручную просмотреть Russian/English phrase frames в preview, поправить неправильные visemes.
5. Bake/render; если Unity game runtime: экспорт morph targets + соответствующие keyframes/animation clips, проверить GLB/FBX behavior на целевом Editor.
6. Для 2D вместо 3D morphs: mouth sprite switching по таймингам offline Rhubarb CLI.
7. При рассинхронизации помимо viseme recognizer проверить frame rate (FPS) Blender и actual AudioClip duration Unity.

## Правовые и бесплатные границы
- Rokoko code LICENSE LGPL-3.0, не MIT, несмотря на README shield.
- Rokoko hardware/live streaming могут требовать оплату. Наш сценарий — **offline FBX retarget**, бесплатный по заявлению разработчика.
- Rhubarb MIT с third-party notices. Произведённые mouth cues принадлежат автору контента по указанному LICENSE; исходный голос имеет отдельные права.
- Для чужих «бесплатных» animations отдельно проверять commercial use and redistribution/credits.
- Новые платные AI голосовые API не нужны: для теста достаточно самостоятельно записанной реплики или пользовательской озвучки.
- На Blender 4.x Retarget v5 не применим, fallback встроенные Blender constraints/ручное bone mapping, затем bake.

## Тест принятия
`retarget_test`: 2 rigs, 1 walking clip → одинаковый target skeleton, без foot slide, кривых рук и console errors.
`lipsync_test`: одна десятисекундная самостоятельно записанная русская фраза → mouth cues → ручная коррекция → проверка Blender render и Unity Player lip-sync. **NOT_RUN до запуска.**

Источники: https://extensions.blender.org/add-ons/retarget/ ; https://github.com/Rokoko/rokoko-studio-live-blender ; https://support.rokoko.com/hc/en-us/articles/4410463481489-Retarget-an-animation-in-Blender ; https://github.com/Premik/blender_rhubarb_lipsync_ng .
