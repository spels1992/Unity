# FREE_PIPELINE: Blender → Unity без платных ассетов, конвертеров и облачных API

**Первая редакция: 2026-10-08. Документ подготовлен по официальной документации Unity 6.3/6.6 и Blender. Live импорт на ПК в этом исследовательском цикле не выполнялся.**

## Основная архитектура
```text
Бесплатная CC0 модель/текстура (Poly Haven, Kenney, Quaternius STANDARD)
       ↓ [license/provenance check]
Blender (бесплатно, GPL программа)
       ↓ [scale/pivot/UV/normals/materials/rig]
FBX экспорт + независимые PNG/JPEG текстуры
       ↓ [локальный диск, без облака]
Unity 6.3 LTS → Assets/_Game/Art/SourceModels
       ↓ [Model Importer, materials, rig/Avatar]
Prefab + collision + LOD + animation controller
       ↓ [PlayMode + Player build + screenshots + profiler]
GitHub = ТОЛЬКО документация и ссылки, не большие исходники
```

## Почему FBX — стандарт по умолчанию
Официальная документация Unity 6.3 рекомендует FBX для внешних DCC: https://docs.unity.com/en-us/engine/6000.3/manual/assets-and-media/asset-types/models/creating-dccassets/3d-formats . Unity поддерживает FBX/OBJ/DAE/DXF, а прямой .blend import требует Blender на каждой машине и может усложнять CI. https://docs.unity.com/en-us/engine/6000.6/manual/assets-and-media/asset-types/models/importing/importing-model-files

Blender поддерживает FBX экспорт (и glTF/GLB), см. https://docs.blender.org/manual/en/latest/files/import_export/index.html . **GLB удобен для обмена и PBR**, но Unity 6.3 не следует считать имеющим нативный GLB importer без проверки/бесплатного дополнительного UPM. Поэтому для проекта без сторонних зависимостей использовать FBX + textures.

**О правах:** Blender распространяется по GPL; **результат авторского моделирования не становится GPL из-за Blender**. Сведения об этом размещены на https://www.blender.org/about/license/ . Чужой CC0 ассет остаётся CC0 по лицензии источника, если мы лишь импортируем его в Blender.

## Шаг 1 — каталогизация ресурса
1. Выбрать оригинальную страницу конкретного бесплатного пакета и нужных моделей.
2. Отметить, сколько процентов пакета реально бесплатно. Quaternius Standard обычно содержит 60–70% полного объёма, а готовые Unity/Blender Source проекты могут продаваться.
3. Сохранить `source_url`, `asset_name`, `download_date`, `license_url`, `author`, `file_format`, `commercial_allowed`, `third_party_content` в локальном provenance реестре проекта.
4. Не получать платный Kenney All-in-1 или Quaternius Source: они не нужны. Не сохранять лицензии только со слов агрегатора.

## Шаг 2 — обработка в Blender
1. Сохранить резервную копию исходного файла локально, открыть модель (FBX/OBJ/glTF) через File → Import.
2. Проверить системы координат, размеры в метрах, начало координат, направление «вперёд», scale и transforms.
3. Для неподвижного объекта: сохранить нормали/UV, проверить материалы, треугольники, скрытые поверхности и pivot.
4. Для персонажа: найти armature, проверить bone names/hierarchy и skin weights; проверить retarget humanoid.
5. Не использовать чужие непроверенные .blend-скрипты из архива как executable plugin. Не запускать автоматический генератор с платным API.
6. Экспортировать выделенные нужные объекты как FBX, выбрать параметры apply transform/unit/armature с учётом текущего Blender; проверить повторным импортом.

## Шаг 3 — импорт в Unity
1. В тестовом Unity-проекте закрепить Editor version и UPM packages.
2. Скопировать FBX и текстуры в `Assets/_Game/Art/Models/<pack>/`, не подключать напрямую платные облачные asset stores.
3. Открыть Model Import Settings: scale factor, normals, materials, animations, mesh compression, readable meshes только при необходимости.
4. Назначить совместимый с URP PBR материал. Текстуры Albedo/Metallic/Roughness/Normal могут требовать раздельной настройки канала; **нельзя ожидать идентичности шейдеров Blender и Unity**.
5. Для персонажа проверить Import Rig → Animation Type Humanoid и Avatar configuration. Для Quaternius Universal Animation Library сравнить имена и ориентации bone rig и провести retarget test.
6. Создать Prefab, collision mesh (по возможности проще видимого), LOD и сохранить материалы. Проверить все экземпляры в сцене.
7. Запустить PlayMode и Windows Player Build; проверить ошибки, clipping, размеры, FPS и анимации.

## Шаг 4 — автоматизация без денег
| Работа | Бесплатная основа | Запасной путь |
|---|---|---|
| Подбор CC0 моделей | Прямые страницы Poly Haven/Kenney/Quaternius | Официальные ссылки в нашем Tool_Catalog |
| Пакетный экспорт | Blender Python / CLI (локально) | UI File Export вручную |
| Передача Blender → Unity | Unity_MCP.blender_bridge **только если уже подключён и разрешён** | FBX в обычной папке Unity Assets |
| Создание Prefabs, коллайдеров | Unity Editor API + собственные C# Editor scripts | Inspector вручную |
| Проверка | Unity Test Framework + Unity Profiler + локальный Player Build | Ручной PlayMode и Console |

Подключение AI/Unity MCP выполнять с учётом [официальных условий Unity](../19_AI_Automation/UNITY_MCP_AND_TERMS.md). Никаких fal.ai, Meshy, Tripo или иных платных генераторов/облачного рендера в этой цепочке.

## Результаты и критерии
- Source URL + лицензия однозначны; цена необходимых файлов 0 ₽.
- Модель не искажена и соответствует масштабу.
- Материал, UV и освещение в Unity ожидаемы.
- Для персонажа анимация не деформирует скелет; есть test clip и корректный Avatar.
- Не добавлены обязательные платные пакеты/персональные API ключи.
- Тестовый Player запускается; лог/версии и известные ограничения записаны.
- Только после этих проверок стек может получить статус VERIFIED.

## Открытые вопросы
Точные настройки экспорта FBX для каждой версии Blender/Unity, масштаб и fallback glTFast (проверить лицензию), оптимальные импортеры больших сцен и batch pipeline, сравнение Blend vs FBX рендеринга на целевой видеокарте.


## Проверенное продолжение 2026-10-08: альтернатива FBX — GLB + Unity glTFast

Ранее в этом документе GLB импорт был отмечен как неопределённый fallback. Теперь **найдены и документально подтверждены**:
- [Khronos glTF I/O для Blender](../Tool_Catalog/khronos-blender-gltf-io.md): Apache-2.0, уже bundled в Blender.
- [Unity glTFast](../Tool_Catalog/unity-gltfast.md): Apache-2.0, официальный бесплатный UPM `com.unity.cloud.gltfast`, Editor/runtime import/export. Upstream `6.20.1-pre.1` main — **preview**, в обычном проекте выбирать stable/совместимый Registry package.
- [Полный сравнительный план](FREE_GLTF_RIG_UV_PRODUCTION.md) для PBR, UV, baked rig/deform bones, animation clips и Player material shader variants.
- [Бесплатные UV и текстуры](../Comparisons/FREE_BLENDER_TEXTURE_AUDIO_GLTF.md): Rigify, Ucupaint, TexTools, ambientCG.

**FBX остаётся рекомендуемым без внешних UPM**, а GLB+glTFast — бесплатной альтернативой для стандартизированных PBR материалов. В Unity Editor и Blender **ни один путь пока не испытан в данном исследовании**. Точные экспортные параметры выбираются только после smoke-теста.
