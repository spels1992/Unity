# Ucupaint

> **Категория:** Blender / многослойная текстурная покраска и baking. **Контракт:** никаких дополнительных расходов. **Проверено:** 2026-10-08. **Доказательство:** Upstream COPYING, README, manifest проверены; в Blender не запускалось..

| Поле | Данные |
|---|---|
| Название | Ucupaint |
| Источник и автор | https://github.com/ucupumar/ucupaint |
| Прямая точка доступа | Blender 4.2+ → Preferences → Get Extensions → Ucupaint; или официальный https://github.com/ucupumar/ucupaint/releases |
| Стоимость | 0 ₽; без платной Substance-подписки; network permission на update можно не использовать для offline workflow. |
| Лицензия | GPL-3.0-or-later подтверждено в COPYING и blender_manifest.toml |
| Версии/зависимости | blender_manifest.toml: Ucupaint 3.0.0, min Blender 4.2.0; README отмечает старые версии с меньшим набором функций. |
| Готовые возможности | Texture layers for Eevee/Cycles, baked texture outputs, paint/edit materials, multi-layer management, node-based workflow. |
| Ограничения и конфликты | Blender material node graphs Ucupaint не импортируются автоматически в Unity URP — сначала bake в PBR images. Распространяемый addon под GPL, сгенерированные изображения определяются лицензией исходных источников/собственных работ. |
| Альтернатива без оплаты | Встроенный Blender Texture Paint и baking без стороннего add-on. |
| Где подтверждено | https://github.com/ucupumar/ucupaint/blob/master/blender_manifest.toml |
| Статус проверки | Upstream COPYING, README, manifest проверены; в Blender не запускалось. |

## Как использовать с Unity / Blender
Установить бесплатное расширение → paint layer masks/colors/roughness → bake/export Base Color, Metallic, Roughness, Normal, AO as images → Unity import PBR maps → проверить roughness→smoothness conversion.

## Приёмка и безопасность
1. Зафиксировать точную ссылку/версию пакета, лицензию конкретных импортируемых файлов и отсутствие платных обязательных зависимостей.
2. Провести тест в **отдельной** сцене или копии проекта (не менять пользовательские проекты).
3. В Unity проверить импортируемые ассеты, материалы/анимации или аудиособытия, Console/Player Build, FPS и размер билда.
4. До реального испытания статус только **DOCUMENTED**, не VERIFIED.
5. В GitHub хранить эту карточку и ссылку на оригинал, а не чужие большие бинарники.

[Политика проекта](../FREE_ONLY_POLICY.md) · [Пайплайн Blender → Unity](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
