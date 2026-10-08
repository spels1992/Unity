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
