# TexTools for Blender (community)

> **Категория:** Blender / UV layout, texel density, texture baking. **Контракт:** никаких дополнительных расходов. **Проверено:** 2026-10-08. **Доказательство:** GPL text, README и активность проверены; Blender теста нет..

| Поле | Данные |
|---|---|
| Название | TexTools for Blender (community) |
| Источник и автор | https://github.com/franMarz/TexTools-Blender |
| Прямая точка доступа | https://github.com/franMarz/TexTools-Blender → Code/ZIP или Releases → Install add-on from disk, если совместимо с установленным Blender |
| Стоимость | 0 ₽, донат не требуется. |
| Лицензия | GPL-3.0-or-later текст LICENSE.txt (особые части/авторство читать целиком перед распространением) |
| Версии/зависимости | README: полностью совместим с Blender 3.2+, про Blender 4.5/5.1/5.2 явно не гарантирует; последний GitHub push в 2024, требуется smoke test. |
| Готовые возможности | UV align/rectify/sort, texel density get/set, texture baking, UV island tools, Color ID, tools for texture manipulation. |
| Ограничения и конфликты | Устаревшая установка описана для прежнего Blender; на 4.5+/5.x конкретный API может потребовать адаптацию. Это редакторный addon, не компонент Unity runtime. |
| Альтернатива без оплаты | Штатные Blender UV Editor/Bake и Geometry Nodes, бесплатные без TexTools. |
| Где подтверждено | https://github.com/franMarz/TexTools-Blender/blob/master/LICENSE.txt |
| Статус проверки | GPL text, README и активность проверены; Blender теста нет. |

## Как использовать с Unity / Blender
В тестовом Blender → установить addon → выделить примитив с UV → unwrap/align/texel density → bake texture → экспорт FBX/GLB → проверить Unity prefab.

## Приёмка и безопасность
1. Зафиксировать точную ссылку/версию пакета, лицензию конкретных импортируемых файлов и отсутствие платных обязательных зависимостей.
2. Провести тест в **отдельной** сцене или копии проекта (не менять пользовательские проекты).
3. В Unity проверить импортируемые ассеты, материалы/анимации или аудиособытия, Console/Player Build, FPS и размер билда.
4. До реального испытания статус только **DOCUMENTED**, не VERIFIED.
5. В GitHub хранить эту карточку и ссылку на оригинал, а не чужие большие бинарники.

[Политика проекта](../FREE_ONLY_POLICY.md) · [Пайплайн Blender → Unity](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
