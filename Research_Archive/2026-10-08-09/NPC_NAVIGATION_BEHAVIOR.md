# NPC navigation and behavior — research checkpoint (2026-10-09)
Status: DOCUMENTED / NOT_RUN. Cost: 0 ₽.

## NavMeshPlus
- Source: https://github.com/h8man/NavMeshPlus
- 2D Tilemap NavMesh pathfinding; release 0.2.23, Unity 2022.3 in package metadata; MIT.
- Unity 6.3 compatibility not tested. Check potential collision with official Navigation packages.

## Unity AI Navigation
- Official package com.unity.ai.navigation, version 2.0.15 for Unity 6000.3; Unity Companion License.
- 3D NavMesh, runtime baking and agents; local use without cloud.
- Source: https://docs.unity3d.com/6000.3/Documentation/Manual/com.unity.ai.navigation.html

## Unity Behavior
- com.unity.behavior 1.0.16 for Unity 6000.3, visual behavior graphs; governed by Unity terms, not MIT.
- Manual authoring only, no paid Muse/AI service needed.
- Source: https://docs.unity3d.com/6000.3/Documentation/Manual/com.unity.behavior.html

Do not claim runtime verification; test each package in isolated project, record editor/package versions and license.