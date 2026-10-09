# Localization and accessibility (2026-10-08/09)
Status DOCUMENTED / NOT_RUN; cost 0 ₽.

- Unity Localization package com.unity.localization, prior research version 1.5.13 for Unity 6.3. String Tables, Asset Tables, locale switching, smart strings. Confirm current exact package dependencies via registry and package lock.
- Unity Accessibility package: native accessibility framework; check exact package/version and platform support before adoption. Source: https://docs.unity3d.com/6000.3/Documentation/Manual/accessibility.html
- LetterSpell accessibility demo: Unity 2023.3.0b3 upstream project; treat as reference only, not proof of Unity 6.3 compatibility.
- No paid translation API. Use manual CSV/XLIFF and community/open dictionaries with verified licensing; never automatically send user content to paid services.
- Test screen reader/keyboard/gamepad focus, UI scale, contrast, subtitles, localization fallback, pluralization, fonts and build.
- No editor tests performed.