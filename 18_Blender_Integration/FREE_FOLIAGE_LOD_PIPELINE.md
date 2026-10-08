# Бесплатный Blender → Unity: деревья, трава, леса, LOD и производительность

**Дата исследования: 2026-10-09. Статус: DOCUMENTED / NOT TESTED.** Все компоненты стоят 0 ₽ и имеют ссылку на официальный источник/лицензию; пользовательские Blender и Unity проекты не изменялись.

## Пять путей для создания деревьев и растений

| Путь | Что даёт | Blender | Лицензия | Когда брать |
|---|---|---|---|---|
| [Geometry Nodes](../Tool_Catalog/blender-geometry-nodes-free.md) | Процедурное размещение травы, листьев, камней, ветвей, instances | Blender 4.5 manual | Встроенный GPL-инструмент | Массовое окружение и скаттеринг по terrain |
| [Sapling Tree Gen](../Tool_Catalog/blender-sapling-tree.md) | Параметрические деревья через Curve | 4.4+ заявлено для v0.3.7 | GPLv3+ | Быстрые отдельные деревья; Blender5 animation проблемы |
| [YGForge Generate Tree](../Tool_Catalog/blender-lowpoly-tree-generator.md) | Low-poly деревья, листья, корни, seed variations | 5.0.1+, v1.1.5 | GPLv3+ | Стилизованные low-poly окружения |
| [Modular Tree](../Tool_Catalog/blender-modular-tree.md) | Процедурный node-based лес, Oak/Pine/Willow presets, Pivot Painter | 4.3.1+ v5.5.2 | GPLv3+ (addon), MIT (core) | Больше разнообразия и управляемая генерация |
| [Blender Decimate](../Tool_Catalog/blender-decimate-lod-free.md) | Уменьшение полигонажа для LOD1/LOD2 | Встроенный | Blender GPL tool | Оптимизировать созданные деревья |

**Ключевой принцип:** не переносить нодовые схемы Blender как будто это Unity runtime: `Geometry Nodes` и Blender curves требуют реализации в конечные meshes или собственного формата placement points для Unity. Избегать `Realize Instances` для сотен тысяч копий без бюджета памяти.

## Проектный сценарий: лес из одного семени
1. Скачать/создать законный базовый low-poly tree mesh (CC0 Quaternius/Kenney или создать GPL инструментом с нуля).
2. Выбрать один tree generator — YGForge (Blender 5+) или Modular Tree. Настроить seed, высоту/форму кроны, листики.
3. Создать 3–5 **действительно разных** семян/силуэтов (не обещать уникальность каждого листа без проверки).
4. Для каждого дерева UV/PBR: атлас коры/листвы по бесплатным CC0 источникам; material textures экспортировать, не ожидать переноса Blender node tree.
5. Получить `LOD0`, потом копии `LOD1`, `LOD2` с Decimate (инструмент, не автоматизированный Unity LOD switch).
6. Проверить silhouette, UV seam/normal/wind silhouette, полигональность каждой вариации. Значения ratios выбирать по тесту и платформе, а не универсально 50/25%.
7. Для scattering использовать Geometry Nodes → Instances on Points, seed/noise/density, зоны исключения дорожек.
8. Вариант экспорта A: отдельные дерева FBX/GLB, scatter размещение уже в Unity (предпочтительно для GPU instancing). Вариант B: превратить инстансы в реальные meshes для статической сцены, только при доказанно приемлемых затратах.
9. Unity: импорт meshes/materials/LODs → `Prefab` + `LODGroup`, включить batch/instancing по поддержке URP, коллайдер только где нужен.
10. Smoke test: 100, 1000, 5000 деревьев в **отдельной** тестовой сцене, real FPS/draw calls/CPU/VRAM, тени и переключения LOD; измерять, не выдумывать результаты.

## Ограничения бесплатной версии
- Платные vegetation packs, SpeedTree/текстуры, подписки/маркетплейсы и платные генераторы не обязательны.
- Sapling в новой Blender версии: пользовательские отзывы на официальной странице сообщают ошибки animation FCurves/Blender 5.x; сначала manual creation test.
- Modular Tree v5.5.2 заявляет совместимость 4.3.1+ и Blender5.1, но у нас теста нет.
- GPL относится к **распространению кода расширений**, сама созданная с нуля модель не становится по умолчанию GPL. CC0 исходная текстура остаётся по своей лицензии.
- Для мобильного ориентироваться на measured memory и GPU overdraw — листики alpha cutout и большое число теней могут стать дороже геометрии.

## Первичные источники
- https://docs.blender.org/manual/en/4.5/modeling/geometry_nodes/index.html
- https://docs.blender.org/manual/en/4.5/modeling/modifiers/generate/decimate.html
- https://extensions.blender.org/add-ons/sapling-tree-gen/
- https://extensions.blender.org/add-ons/generate-tree-plugin/
- https://extensions.blender.org/add-ons/modular-tree/
- [Базовый FBX/GLB путь](FREE_GLTF_RIG_UV_PRODUCTION.md)
