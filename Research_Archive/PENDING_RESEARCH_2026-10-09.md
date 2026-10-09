# Очередь несохранённых исследований — 2026-10-09

Статус: DOCUMENTED / NOT_RUN. Это конспект исследований; практические Unity/Blender тесты не проводились. Дополнительные расходы: 0 ₽. Перед созданием канонических карточек сверять существующие записи и первоисточники.

| Блок | Решения | Основные источники |
|---|---|---|
| Локализация и доступность | Unity Localization 1.5.13, Unity Accessibility, LetterSpell (Unity 2023.3.0b3) | https://github.com/Unity-Technologies/a11y-public-sample ; https://docs.unity3d.com/6000.3/Documentation/Manual/com.unity.localization.html |
| Локальная доставка ассетов | Unity Addressables, Scriptable Build Pipeline | https://docs.unity3d.com/6000.3/Documentation/Manual/com.unity.addressables.html ; https://docs.unity3d.com/6000.3/Documentation/Manual/com.unity.scriptablebuildpipeline.html |
| NPC | NavMeshPlus 0.2.23, Unity AI Navigation 2.0.15, Unity Behavior 1.0.16 | https://github.com/h8man/NavMeshPlus ; https://docs.unity3d.com/6000.3/Documentation/Manual/com.unity.ai.navigation.html |
| Готовые сетевые игры | Boss Room (Editor 6000.0.52f1), Megacity Metro (Editor 6000.1.0f1) | https://github.com/Unity-Technologies/com.unity.multiplayer.samples.coop ; https://github.com/Unity-Technologies/megacity-metro |
| Networking | Mirror, FishNet, Unity Netcode for GameObjects 2.x | https://github.com/MirrorNetworking/Mirror ; https://github.com/FirstGearGames/FishNet |
| Редакторы 2D-карт | Tiled, SuperTiled2Unity, LDtk, LDtkToUnity | https://www.mapeditor.org/ ; https://github.com/Seanba/SuperTiled2Unity ; https://ldtk.io ; https://github.com/Cammin/LDtkToUnity |
| 2D процедурная генерация | Tilemap Extras 6.0.3, WaveFunctionCollapse, DeBroglie, LayerProcGen | https://github.com/mxgmn/WaveFunctionCollapse ; https://github.com/BorisTheBrave/DeBroglie ; https://github.com/runevision/LayerProcGen |
| Аудио | LMMS, Audacity, MuseScore Studio | https://lmms.io ; https://www.audacityteam.org ; https://musescore.org |

Лицензии: Unity пакеты и sample могут иметь Unity Companion License или Unity Terms, а не MIT. WFC MIT касается кода, не всех примеров ассетов. LayerProcGen MPL-2.0. Проверять точные зависимости и версии по конкретному commit/manifest; не приписывать совместимость Unity 6.3 без запуска. Облачные платные сервисы не использовать.

Следующие действия: разделить блоки на карточки и сравнительные матрицы; обновить Tool_Catalog/INDEX.md, PROGRESS.md и issue #2 после успешных коммитов. Не дублировать уже сохранённые карточки.