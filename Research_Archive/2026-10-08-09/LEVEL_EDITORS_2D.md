# Free 2D level editors and Unity importers (2026-10-09)
Status DOCUMENTED / NOT_RUN; cost 0 ₽.

| Tool | Upstream | Prior observed version | License | Purpose |
|---|---|---|---|---|
| Tiled | https://www.mapeditor.org/ | 1.12.2 | GPL | Tilemaps, objects, layers |
| SuperTiled2Unity | https://github.com/Seanba/SuperTiled2Unity | 2.4.0 | MIT | Tiled maps to Unity |
| LDtk | https://ldtk.io/ | 1.5.3 | MIT | 2D level editor |
| LDtkToUnity | https://github.com/Cammin/LDtkToUnity | 6.12.3 | MIT | LDtk importer for Unity |

Test in a separate Unity 6.3 project with tilemap collision, prefabs, layer order, data types, build and round-trip changes. Unity 6.3 compatibility not tested; confirm exact editor/UPM dependencies and release numbers before adoption. GPL applies to Tiled application, not automatically to independently created maps.