# GitHub Copilot / AI agent — 3D model production

## 🚨🚨 КРИТИЧЕСКОЕ ПРАВИЛО ОКОН: ВСЕГДА ЗАКРЫВАТЬ

**МАКСИМАЛЬНЫЙ ПРИОРИТЕТ ДЛЯ КАЖДОГО АГЕНТА И СУБАГЕНТА.** Открыл Блокнот, картинку, папку, приложение, браузер, PowerShell, CMD, Blender, Unity или временный фоновый процесс → поработал → ЗАКРЫЛ → проверил отсутствие своего временного окна и PID. Делать сразу после каждого этапа, включая сбои; скрытие/сворачивание не считается закрытием. Не оставлять мусор, не затрагивать пользовательские окна и постоянные MCP-службы. **Обязательно прочитать [../docs/PROCESS_HYGIENE.md](../docs/PROCESS_HYGIENE.md).** В отчёте: CLOSED / PRESERVED / BLOCKED; незакрытый свой процесс = NOT READY.

## 🚨 3D-МОДЕЛИ И АНИМАЦИИ — РАЗНЫЕ ОБЯЗАТЕЛЬНЫЕ СКИЛЛЫ

**Модель:** 3D Craft (3d-craft, @3d-craft) → Hunyuan3D-2GP → Blender QA 42 ракурса и проверка анатомии. **Кости и анимации:** Bones = технический скилл rig-motion, сейчас отображается Rig / @Rig; @Bones только после подтверждённого переименования. Использовать SkinTokens CPU при пригодности, затем проверять движения в Unity. Сначала одобрить качество модели, затем создавать rig; не принимать мультяшную подмену реалистичного животного. Подробности: [docs/LOCAL_AI_3D_PIPELINE.md](../docs/LOCAL_AI_3D_PIPELINE.md). Результаты локально, без GitHub push без явного нового поручения.


Before creating, modifying or repairing any original 3D model (including parts, clothes and accessories), read [docs/3D_CRAFT.md](../docs/3D_CRAFT.md) and root [AGENTS.md](../AGENTS.md), then use the installed **3D Craft / 3Д Крафт** skill (`3d-craft`), available at https://chatgpt.com/plugins/plugins_6acdc74c86888191b2101b657a2e8f8d. Verify it is actually loaded; a text mention is not proof. If unavailable, report BLOCKED instead of silently switching pipelines.
