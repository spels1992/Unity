# Cross-repository recovery audit: Unity ↔ Blender (2026-10-09)

## Verified source of truth
- Unity: `Research_Archive/H16_PENDING_FULL_METADATA_20261009.json` (7 entries) and `Research_Archive/H15_UNITY_NINE_FULL_METADATA_RECOVERY_20261009.json` (9 entries) were already archived; this recovery cycle promoted all 16 to `Tool_Catalog/recovered-*.md`, checked readback and updated `Tool_Catalog/INDEX.md` and `PROGRESS.md`.
- Blender: `Catalog/Expansion/H16_PENDING_FULL_METADATA_20261009.json` contains 23 candidate metadata entries; `Catalog/Expansion/H16_PENDING_RECOVERY_20261009.md` tracks their URLs. Blender `PROGRESS.md` reports 23/23 URLs merged to `Catalog/MASTER_SEARCH_INDEX.json` and readback of 624 unique URLs. **Therefore do not re-add all 23 as purportedly missing links.**
- Blender source count, item count and binary sizes are different concepts. 23 links indexed does not establish 23 independent downloadable 3D models. Download sizes remain UNKNOWN/null; no Editor import tests.

## Remaining work (NOT COMPLETE)
1. Compare original full backup archives to actual GitHub records, including absent backup copies that may live outside the repositories.
2. Blender 23 candidates: semantic deduplication against canonical asset cards, independent per-asset LICENSE check, format/dependency and exact download-size audit when accessible, without downloading large third-party archives.
3. Unity 16 recovered cards: new primary-source version, LICENSE and dependency verification before promotion from RECOVERED_METADATA to canonical adoption.
4. Locate and reconcile earlier detailed backups of multiplayer, 2D generation, level editors, audio, localization and packaging with existing archive summaries.
5. Run Unity/Blender practical tests only when expressly allowed and available; until then DOCUMENTED/NOT_RUN.

## Safety and economics
0 ₽ additional expenses. No paid API, asset, plugin, subscription, hosting; no user project edits or application installs. This file is a verified *reconciliation checkpoint*, not proof every historical research note has been recovered.
