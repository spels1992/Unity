# Blender Rigify (встроенный автоматический риг)

> **Категория:** Blender / character rigging / animation. **Контракт:** никаких дополнительных расходов. **Проверено:** 2026-10-08. **Доказательство:** Проверено по Blender Manual, Blender не запускался..

| Поле | Данные |
|---|---|
| Название | Blender Rigify (встроенный автоматический риг) |
| Источник и автор | https://docs.blender.org/manual/en/4.5/addons/rigging/rigify/index.html |
| Прямая точка доступа | Входит в официальную Blender; в поддерживаемом выпуске включить add-on Rigify через Preferences / Add-ons |
| Стоимость | 0 ₽; установки платного плагина/авториггер-сервиса не требуется. |
| Лицензия | GPL — официальный Blender Rigify manual и Blender license https://www.blender.org/about/license/ |
| Версии/зависимости | Официальный manual Blender 4.5 LTS и 5.2 описывает встроенный Rigify; активную версию Blender на целевом ПК ещё не проверяли. |
| Готовые возможности | Meta-rigs, генерация control rig, готовые rig types spine/face/limbs/tail/fingers, animation controls; настройка костей и скининга. |
| Ограничения и конфликты | Rigify не магический one-click полноценный animation pack. Сгенерированный control rig со сложными constraints может не экспортироваться напрямую в Unity как Humanoid — нужен отдельный deformation skeleton, baking и ретаргет/Avatar. |
| Альтернатива без оплаты | Blender ручной Armature, Quaternius бесплатные ригнутые персонажи, но платные auto-rig add-ons не закладывать. |
| Где подтверждено | https://docs.blender.org/manual/en/4.5/addons/rigging/rigify/index.html |
| Статус проверки | Проверено по Blender Manual, Blender не запускался. |

## Как использовать с Unity / Blender
Смоделировать mesh → сделать UV → создать Armature/Meta-rig → подогнать к телу → Generate Rig → привязать mesh → анимировать → запечь в deform bones и экспортировать только нужные скелет/меш/клипы FBX/glTF → проверить Unity Humanoid.

## Приёмка и безопасность
1. Зафиксировать точную ссылку/версию пакета, лицензию конкретных импортируемых файлов и отсутствие платных обязательных зависимостей.
2. Провести тест в **отдельной** сцене или копии проекта (не менять пользовательские проекты).
3. В Unity проверить импортируемые ассеты, материалы/анимации или аудиособытия, Console/Player Build, FPS и размер билда.
4. До реального испытания статус только **DOCUMENTED**, не VERIFIED.
5. В GitHub хранить эту карточку и ссылку на оригинал, а не чужие большие бинарники.

[Политика проекта](../FREE_ONLY_POLICY.md) · [Пайплайн Blender → Unity](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
