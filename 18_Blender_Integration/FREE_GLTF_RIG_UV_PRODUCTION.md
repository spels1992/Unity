# Бесплатное производство 3D-контента: Rigify → UV → PBR → glTFast / FBX → Unity

**Документ 2026-10-08.** Все компоненты без дополнительных расходов. Это воспроизводимая инструкция, **не отчёт об уже запущенных Blender или Unity тестах**.

## Исходные бесплатные источники
- Персонажи: [Quaternius Standard](../Tool_Catalog/quaternius-free-assets.md), [Kenney](../Tool_Catalog/kenney-free-assets.md) — по конкретной CC0 странице; скачать только Standard/Free.
- PBR материалы: [ambientCG](../Tool_Catalog/ambientcg-cc0.md), [Poly Haven](../Tool_Catalog/poly-haven.md) — отдельные assets CC0. Для конкретного файла сохранить URL + лицензию.
- Риг и UV: [Blender Rigify](../Tool_Catalog/blender-rigify-free.md) — встроенный GPL; [TexTools](../Tool_Catalog/textools-blender-free.md) — бесплатный GPL addon для UV/bake, или встроенный Blender UV Editor.
- Покраска: [Ucupaint](../Tool_Catalog/ucupaint-blender-free.md) — GPL-3.0, 3.0.0 manifest / Blender min 4.2, или Blender Texture Paint без дополнений.
- Транспорт моделей: [Blender Khronos glTF I/O](../Tool_Catalog/khronos-blender-gltf-io.md) (Apache-2.0 встроен в Blender) + [Unity glTFast](../Tool_Catalog/unity-gltfast.md) (Apache-2.0 UPM). Или **встроенный FBX importer** в Unity, без дополнительного пакета.

## Как выбрать формат
| Сценарий | Приоритет | Почему | На что смотреть |
|---|---|---|---|
| Простой static mesh с PBR/текстурами | GLB + glTFast | Texture materials/mesh вместе, стандарт glTF 2.0 | Нужен бесплатный официальный Unity UPM и его shader variants |
| Humanoid с отдельными клипами, Unity Avatar retarget | FBX + PNG textures | Привычный Unity ModelImporter/Humanoid pipeline | Bake deform bones, animation clips, scale, morphs |
| Runtime export созданного пользователем 3D | glTFast | Автор документации поддерживает runtime export | Экспортируемые assets и безопасность путей; Player build тест |
| Без доп. UPM / проблемная glTFast версия | FBX | Unity встроенная поддержка | PBR nodes Blender не переносятся 1:1, назначить Unity материалы |
| Сложные procedural Blender nodes / Geometry Nodes | Bake → FBX/GLB | Custom shader graphs/procedural components не переносимы как есть | Apply/realize geometry and bake texture maps |
| Blender scene, напрямую .blend | Не production default | Unity может требовать Blender и отличаться от CI среды | Использовать проверенный .fbx/.glb вместо зависимости от .blend file importer |

**Важная поправка:** «FBX — формат по умолчанию» остаётся хорошей стратегией **без сторонних зависимостей**, но **GLB + glTFast** полезнее там, где важны PBR и перенос текстур. Оба пути допустимы бесплатно.

## Пошаговая технология
1. Сохранить точный `asset_name, author, source_url, license_url, downloaded_at, version` и **не копировать чужие ZIP в базу**.
2. Blender → открыть исходный mesh; проверить `unit scale`, transform, forward/up axes, origin/pivot и topology. Желательно реальная 1м тестовая кубическая мера.
3. UV Editor → Smart UV Project / ручная развертка; TexTools по необходимости → проверить stretching, texel density и seams.
4. PBR Texture → принципы channels: BaseColor как sRGB, roughness/metallic/normal/height как linear data, OpenGL normal orientation (+Y) vs DirectX (-Y). Blender node networks сложнее стандартного PBR сначала bake в изображения.
5. Rigify при необходимости → meta-rig alignment → generate → parent mesh / check skin weights → **bake animation onto deform bones**. Экспортировать deform rig, не контроллерную внутреннюю механику Rigify, иначе Unity Humanoid может не совпадать.
6. Экспорт A: GLB через File → Export → glTF 2.0. Blender Khronos glTF 2.0 I/O уже входит в Blender; не устанавливать archived glTF-Blender-Exporter.
7. Unity A: Window → Package Manager → установить официальную стабильную `com.unity.cloud.gltfast`. Не фиксировать автоматически main preview **6.20.1-pre.1**. После установки скопировать GLB в `Assets/_Game/Art/Imported`, проверить prefab и материалы.
8. Экспорт B: FBX + отдельные PNG files; Unity встроенный Model Importer, Animation Type Humanoid / Avatar Configure.
9. URP materials: Unity smoothness может требовать инверсию Blender roughness и упаковку metallic/smoothness каналов. Проверить normal orientation, Alpha blend vs cutoff, texture compression/mobile memory.
10. **Shader-variant gotcha glTFast:** автор предупреждает, что кастомные shader graphs должны попадать в **Player Build**, иначе в Editor материалы хорошие, в Player розовые/неправильные. Проверить билд на target platform.
11. Создать prefab, collider, LOD, Animator Controller, AnimationClip. Измерить triangles, draw calls, animation cost, VRAM и FPS. В Windows Build проверить для обычной сцены и худшего случая.

## 0 ₽ тест-конверсия «одна модель, одно движение»
- Blender: выбранный CC0 Quaternius mesh, если rigged — simple Idle/Walk.
- Сохранить A: `test.glb`; B: `test.fbx` + textures.
- Unity 6.x: два объекта рядом, одинаковые материалы/освещение; сравнить geospatial orientation, material color, rig/animations, shadows и размер билдов.
- 60 секунд PlayMode без ошибок, сохранение снимка Console, Windows Player Build.
- **До фактического запуска тестов:** `NOT_RUN`, не сравнивать FPS/качество по воображаемым цифрам.

## Лицензионные тонкости
- Blender GPL — лицензия **софта**; созданные автором модели не становятся GPL автоматически: https://www.blender.org/about/license/.
- Khronos glTF exporter и Unity glTFast — Apache-2.0. glTFast `Third Party Notices.md` содержит **CC-BY 4.0 тестовые модели**: не переносить их в свой продукт без атрибуции/аудита.
- Ucupaint и TexTools GPL для add-on **не требуют публиковать созданную в них текстуру как GPL** (конкретная исходная графика по своей лицензии).
- Платные Auto-Rig Pro, UVPackmaster, Substance и облачные BYOK texturing не входят в путь.
- При установке Blender extensions проверить требуемые permissions; Ucupaint manifest разрешает files/network для сохранения и обновлений — бесплатная оффлайн работа возможна.

## Источники
- https://github.com/KhronosGroup/glTF-Blender-IO
- https://github.com/Unity-Technologies/com.unity.cloud.gltfast
- https://github.com/Unity-Technologies/com.unity.cloud.gltfast/blob/main/Packages/com.unity.cloud.gltfast/README.md
- https://github.com/ucupumar/ucupaint/blob/master/blender_manifest.toml
- https://github.com/franMarz/TexTools-Blender/blob/master/LICENSE.txt
- https://docs.blender.org/manual/en/4.5/addons/rigging/rigify/index.html
