# Blender Integration

**Исследование:** начальный индекс от 2026-10-08. **Задачи:** FBX/glTF, armature, retargeting, PBR/textures, batch export/import, Blender Python scripts.

Искать **от крупного готового решения к маленькому компоненту**. Для каждого кандидата создавать карточку в [Tool_Catalog](../Tool_Catalog/INDEX.md), затем ссылаться сюда; не создавать дубликаты. Проверять лицензию, актуальность версий Unity, исходники и возможность интеграции с другими системами.

## Приоритетные вопросы
- Есть ли полноценный проект или поддерживаемый framework, выполняющий несколько задач сразу?
- Есть ли бесплатная официальная система Unity? Если нет — какой OSS вариант?
- Какие зависимости/версии, render pipeline и target platform обязательны?
- Может ли агент автоматизировать установку/проверку через Unity Editor API или CI?
- Какие альтернативы и известные риски, что тестировать перед производством?

**Статус:** каталог направления ещё не заполнен полностью; см. [ROADMAP](../ROADMAP.md).
## Бесплатный практический маршрут
[FREE_ASSET_PIPELINE.md](FREE_ASSET_PIPELINE.md) — лицензированные CC0 ассеты → Blender → FBX → Unity → prefab/rig/PlayMode/Build. Бесплатные модели: [Poly Haven](../Tool_Catalog/poly-haven.md), [Kenney](../Tool_Catalog/kenney-free-assets.md), [Quaternius](../Tool_Catalog/quaternius-free-assets.md).

[Provenance/лицензия каждого файла](../Integration_Guides/FREE_ASSET_LICENSE_LOG.md).


## Пайплайн 2.0 — больше возможностей без новых расходов
- [Rigify → UV/TexTools → Ucupaint/ambientCG → FBX/GLB → Unity](FREE_GLTF_RIG_UV_PRODUCTION.md), две законные и бесплатные стратегии импорта, включая glTFast.
- [Сравнение инструментов](../Comparisons/FREE_BLENDER_TEXTURE_AUDIO_GLTF.md).
- **Важный нюанс:** Khronos glTF exporter входит в Blender 2.8+, но Unity glTFast — отдельный бесплатный UPM. У preview main `6.20.1-pre.1` стабильность не доказана, выбирать стабильную совместимую версию Unity Registry.
- Rigify control rigs/Blender Shader Nodes не экспортируются в Unity магически: bake animations/material maps; затем проверять Player build.


## Расширение 09.10.2026: Geometry Nodes, low-poly лес и LOD
[FREE_FOLIAGE_LOD_PIPELINE.md](FREE_FOLIAGE_LOD_PIPELINE.md) — сравнение встроенных Geometry Nodes и Decimate с бесплатными Sapling, YGForge и Modular Tree. **Переход из процедурного Blender в Unity требует bake/real mesh, prefab и проверки LODGroup, Unity не импортирует сам Blender graph.** Подробнее [Retarget и lip-sync](../05_Animation/FREE_RETARGET_LIPSYNC_PIPELINE.md).
