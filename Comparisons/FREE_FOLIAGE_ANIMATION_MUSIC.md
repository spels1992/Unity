# Бесплатные Blender-инструменты и музыка — быстрый выбор

Исследование 2026-10-09. Цена обязательной части = 0 ₽, **реальных запусков не было**.

| Задача | Рекомендуемые бесплатные источники | Лицензия / ограничение | Вывод |
|---|---|---|---|
| Лес, камни, трава — расстановка | [Geometry Nodes](../Tool_Catalog/blender-geometry-nodes-free.md) | Встроенный Blender GPL; bake перед Unity | FIRST CHOICE без addons |
| Одиночное параметрическое дерево | [Sapling](../Tool_Catalog/blender-sapling-tree.md) | GPL; в Blender 5.x жалобы на animation | С осторожностью |
| Low-poly деревья для игры | [YGForge](../Tool_Catalog/blender-lowpoly-tree-generator.md) | GPLv3+, Blender 5.0.1+ | Хороший современный кандидат |
| Обширные botanical trees | [Modular Tree](../Tool_Catalog/blender-modular-tree.md) | GPL addon/MIT core, v5.5.2 | На Windows доступна free сборка |
| LOD0→LOD2 и mesh reduction | [Decimate](../Tool_Catalog/blender-decimate-lod-free.md) | Встроенный Blender GPL | Нужен контроль UV/силуэта |
| Перенос animations | [Retarget](../Tool_Catalog/blender-retarget-kbs.md) | GPL Blender5+ | Приоритет в Blender 5 |
| Альтернативный retarget | [Rokoko](../Tool_Catalog/blender-rokoko-retarget.md) | **LGPL** LICENSE vs README MIT badge | Бесплатный retarget, live hardware необязателен |
| Губы по аудио | [Rhubarb Lipsync NG](../Tool_Catalog/rhubarb-lip-sync-ng-blender.md) | MIT wrapper + CLI MIT third-party notices | Test Russian needed |
| 2D/3D offline mouth cues | [Rhubarb CLI](../Tool_Catalog/rhubarb-cli-open-source.md) | MIT base | Без подписки, не TTS |
| Игровая CC0 музыка | [4 музыкальных набора](../14_Audio/FREE_CC0_MUSIC_COLLECTION.md) | CC0 на отдельных OpenGameArt asset pages | ≥18 заявленных tracks плюс 5 ZIP неизвестного размера |

### Почему не всё сразу?
- Geometry Nodes + Modular Tree + Sapling одновременно почти никогда не нужны для одной маленькой сцены. Выбрать **один tree generator**, сохранить 3–5 вариантов, затем расставить их средствами Geometry Nodes.
- Retarget и Rokoko решают схожую задачу. Сначала знать **Blender version** и исходный rig.
- Rhubarb CLI — underlying engine Rhubarb NG; не дублировать установку CLI, если release NG уже его включает.
- CC0 песни — готовый игровой звук, но AudioMixer/transition manager всё равно требуется создать в Unity.
- Shader/morph/LOD/source mesh не переносятся идеально автоматически — mandatory Blender/Unity PlayMode + Player QA.

[Лес/LOD гайд](../18_Blender_Integration/FREE_FOLIAGE_LOD_PIPELINE.md) · [Анимация/губы гайд](../05_Animation/FREE_RETARGET_LIPSYNC_PIPELINE.md) · [Музыка гайд](../14_Audio/FREE_CC0_MUSIC_COLLECTION.md).
