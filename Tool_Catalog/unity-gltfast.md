# Unity glTFast

> **Категория:** Unity / glTF GLB Editor+runtime import/export. **Контракт:** никаких дополнительных расходов. **Проверено:** 2026-10-08. **Доказательство:** LICENSE/README/package.json/third-party notices проверены; Player Build не запускался..

| Поле | Данные |
|---|---|
| Название | Unity glTFast |
| Источник и автор | https://github.com/Unity-Technologies/com.unity.cloud.gltfast |
| Прямая точка доступа | Unity Package Manager → Unity Registry → com.unity.cloud.gltfast; Git monorepo link https://github.com/Unity-Technologies/com.unity.cloud.gltfast.git?path=/Packages/com.unity.cloud.gltfast для development. |
| Стоимость | 0 ₽ за официальную Unity Registry библиотеку, BYOK/оплаченный API не нужен. |
| Лицензия | Apache-2.0 по LICENSE.md upstream; third-party test models могут быть CC-BY, см. Third Party Notices.md |
| Версии/зависимости | Исходный main Packages/com.unity.cloud.gltfast/package.json = 6.20.1-pre.1, min Unity 6000.0. **Это PREVIEW из main, не рекомендация ставить preview в production.** В Registry выбирать совместимый стабильный release, точная версия зависит от Editor. |
| Готовые возможности | GLB/glTF editor import в Unity prefabs, runtime file/url loading, Editor+runtime export, support URP/HDRP/Built-in, расширения glTF. |
| Ограничения и конфликты | Ключевой upstream gotcha: custom shader graphs/variants нужно включать в Player build, иначе materials могут выглядеть правильно в Editor, но не в сборке. Direct Git URL без ?path после monorepo изменения может не работать. Не считать arbitrary Blender shaders переносимыми. |
| Альтернатива без оплаты | FBX importer built-in для нулевой дополнительной зависимости; если glTFast не работает — fallback FBX. |
| Где подтверждено | https://github.com/Unity-Technologies/com.unity.cloud.gltfast/blob/main/Packages/com.unity.cloud.gltfast/README.md |
| Статус проверки | LICENSE/README/package.json/third-party notices проверены; Player Build не запускался. |

## Как использовать с Unity / Blender
Unity Package Manager → установить стабильный glTFast → поместить GLB в Assets → проверить prefab, mesh, materials, animations → Build → Shader variants и URP materials QA; file path runtime только с надёжными локальными источниками.

## Приёмка и безопасность
1. Зафиксировать точную ссылку/версию пакета, лицензию конкретных импортируемых файлов и отсутствие платных обязательных зависимостей.
2. Провести тест в **отдельной** сцене или копии проекта (не менять пользовательские проекты).
3. В Unity проверить импортируемые ассеты, материалы/анимации или аудиособытия, Console/Player Build, FPS и размер билда.
4. До реального испытания статус только **DOCUMENTED**, не VERIFIED.
5. В GitHub хранить эту карточку и ссылку на оригинал, а не чужие большие бинарники.

[Политика проекта](../FREE_ONLY_POLICY.md) · [Пайплайн Blender → Unity](../18_Blender_Integration/FREE_ASSET_PIPELINE.md).
