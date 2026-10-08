# Khronos glTF-Blender-IO

> **Категория:** Blender / экспорт моделей, материалов и анимаций. **Контракт:** никаких дополнительных расходов. **Проверено:** 2026-10-08. **Доказательство:** LICENSE и README upstream прочитаны; локальный экспорт не тестировался..

| Поле | Данные |
|---|---|
| Название | Khronos glTF-Blender-IO |
| Источник и автор | https://github.com/KhronosGroup/glTF-Blender-IO |
| Прямая точка доступа | Уже встроено и включено по умолчанию в Blender 2.80+; File → Export → glTF 2.0 |
| Стоимость | 0 ₽, Blender штатный импортёр/экспортёр |
| Лицензия | Apache-2.0 по LICENSE.txt исходного GitHub проекта |
| Версии/зависимости | Официальный upstream документирует Blender 4.5 LTS/5.0/5.1; exact local Blender version не проверена. |
| Готовые возможности | glTF 2.0/GLB export/import: mesh, PBR, textures, skeletal/shape key animation, morph, lights/camera where supported; round-trip tests в upstream. |
| Ограничения и конфликты | Не переносит произвольные Blender Shader Nodes, процедурные materials без baking, constraints, geometry nodes. Проверять texture color space, armature, axis, shape keys. |
| Альтернатива без оплаты | FBX + отдельные текстуры без дополнительного Unity package, если glTFast недоступен. |
| Где подтверждено | https://github.com/KhronosGroup/glTF-Blender-IO/blob/main/README.md |
| Статус проверки | LICENSE и README upstream прочитаны; локальный экспорт не тестировался. |

## Как использовать с Unity / Blender
Blender UV/texture/PBR Principled BSDF → File Export glTF 2.0 → GLB → Unity glTFast com.unity.cloud.gltfast → импорт prefab → проверка материалов и анимаций в Build.

## Приёмка и безопасность
1. Зафиксировать точную ссылку/версию пакета, лицензию конкретных импортируемых файлов и отсутствие платных обязательных зависимостей.
2. Провести тест в **отдельной** сцене или копии проекта (не менять пользовательские проекты).
3. В Unity проверить импортируемые ассеты, материалы/анимации или аудиособытия, Console/Player Build, FPS и размер билда.
4. До реального испытания статус только **DOCUMENTED**, не VERIFIED.
5. В GitHub хранить эту карточку и ссылку на оригинал, а не чужие большие бинарники.

[Политика проекта](../FREE_ONLY_POLICY.md) · [Пайплайн Blender → Unity](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
