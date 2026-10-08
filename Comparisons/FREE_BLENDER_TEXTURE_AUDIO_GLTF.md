# Бесплатные инструменты для полного производства графики и аудио Unity

**2026-10-08. Сравнение по официальным документам, а не Editor испытаниям.**

| Проблема | Лучше начинать | Права | Что готово | Риск |
|---|---|---|---|---|
| Риг персонажа | [Rigify](../Tool_Catalog/blender-rigify-free.md) | Blender GPL | Meta-rig/generate control rig | Для Unity деформационный риг и baked clips; не прямой экспорт constraints |
| UV/texture bake | Blender UV/Bake бесплатно или [TexTools](../Tool_Catalog/textools-blender-free.md) | TexTools GPLv3+ | UV layout, texel density, baking | На Blender 5.x совместимость не подтверждена |
| PBR-покраска | [Ucupaint](../Tool_Catalog/ucupaint-blender-free.md) | GPLv3+, min Blender 4.2 | Paint layers/material nodes | Bake outputs to images для Unity URP |
| glTF export Blender | [Khronos glTF I/O](../Tool_Catalog/khronos-blender-gltf-io.md) | Apache-2.0 | GLB export, round trip | Blender nodes/constraints нужно bake |
| glTF import/export Unity | [Unity glTFast](../Tool_Catalog/unity-gltfast.md) | Apache-2.0 | Editor/runtime GLB import/export | Версия main pre-release, shader variants в Player |
| PBR материалы | [ambientCG](../Tool_Catalog/ambientcg-cc0.md) или [Poly Haven](../Tool_Catalog/poly-haven.md) | CC0 на assets | Текстуры/HDRI/материалы | Важны normal convention, texture channels, LOD/VRAM |
| UI/impact/RPG/Sci-fi music cues | [Kenney audio packs](../14_Audio/FREE_SOUND_PIPELINE.md) | CC0 для 5 отдельных наборов | 385 файлов по авторским страницам | Это не game audio manager и не полная музыка |

## FBX или GLB?
- **FBX**: лучше для простого Unity workflow без новых UPM и для Humanoid/Animator, но PBR обычно настраивается вручную.
- **GLB**: стандартизирован для PBR materials/meshes, а [glTFast](../Tool_Catalog/unity-gltfast.md) даёт импорт/экспорт; дополнительный бесплатный Unity UPM. Проверить соответствие stable release.
- **Нельзя** считать один формат универсальным для Blender Geometry Nodes/Rigify constraints/procedural animation: нужно выпекать mesh и animation и проверять Player.

**Практический стандарт:** сперва выбрать один целевой Unity Editor+Render Pipeline, затем подбирать exporter/importer; статусы до тестов `DOCUMENTED`. [3D-гайд](../18_Blender_Integration/FREE_GLTF_RIG_UV_PRODUCTION.md).

## Что пока не покрыто
Full free soundtrack источники с лицензиями каждого трека, voice generation без paid API, бесплатные lip-sync/retarget tools, procedural vegetation, Unity6 mobile compression exact recipes, музыкальные transition layers. Это следующие направления, а не уже решённые задачи.
