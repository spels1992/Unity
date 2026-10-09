# Free procedural 2D map generation (2026-10-09)
Status DOCUMENTED / NOT_RUN; cost 0 ₽.

## Unity Tilemap Extras
- com.unity.2d.tilemap.extras 6.0.3 officially released for Unity 6000.3, Unity Companion License.
- RuleTile, AnimatedTile, RuleOverrideTile, Random/Line/Group/GameObject brushes.
- Not a complete dungeon generator; only auto-tile painting.
- Source: https://docs.unity3d.com/6000.3/Documentation/Manual/com.unity.2d.tilemap.extras.html

## WaveFunctionCollapse
- https://github.com/mxgmn/WaveFunctionCollapse
- MIT code; bundled sample tiles/images not automatically licensed under MIT.
- C#/.NET reference implementation, not Unity plug-and-play. Version and Unity minimum UNKNOWN.

## DeBroglie
- https://github.com/BorisTheBrave/DeBroglie
- MIT; C# WFC with backtracking and global constraints; NuGet/Unity dependencies require audit; Unity 6.3 NOT_TESTED.

## LayerProcGen
- https://github.com/runevision/LayerProcGen
- MPL-2.0; deterministic infinite-world chunk scheduling, not a world-generation algorithm itself.
- README Unity 2019.4+; Unity 6.3 NOT_TESTED. Git UPM branch #upm, pin SHA. FBPP for save; Terrain Sample needs Burst/Input System/unsafe code, tested by upstream with Built-in Render Pipeline.

Architecture candidate: WFC/DeBroglie -> RuleTile -> BFS/FloodFill path validation -> doors/keys/enemies. Large worlds: LayerProcGen + generator + Tilemap + save. All combinations ASSUMED, not tested.