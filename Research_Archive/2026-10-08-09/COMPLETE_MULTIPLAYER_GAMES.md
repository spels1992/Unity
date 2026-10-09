# Complete free multiplayer samples — research checkpoint (2026-10-09)
Status: DOCUMENTED / NOT_RUN. Cost: 0 ₽.

## Boss Room
- Unity Technologies: https://github.com/Unity-Technologies/com.unity.multiplayer.samples.coop
- Coop RPG up to 8 players, combat, classes, boss, RPC, NGO, NetworkTransform and Multiplayer Play Mode.
- Editor ProjectVersion 6000.0.52f1; sample v3.0.0.
- Manifest: Netcode for GameObjects 2.4.3, Transport 2.5.1, Multiplayer Play Mode 1.5.0, Multiplayer Services 1.1.4, Authentication 3.5.1, Input System 1.14.0, URP 17.0.4, AI Navigation 2.0.8, VContainer 1.16.8.
- Unity Companion License; not MIT. README permits local usage without UGS; no cloud/Relay/Lobby required for offline host-client test.
- Download via release ZIP or Git LFS. Unity 6.3 NOT_TESTED.

## Megacity Metro
- Unity Technologies: https://github.com/Unity-Technologies/megacity-metro
- Mass multiplayer shooter / ECS; up to 150 players claimed by upstream, not measured.
- Editor 6000.1.0f1; Netcode for Entities 1.3.6, Entities Graphics 1.4.12, Physics 1.3.14, URP 17.1.0, Input System 1.14.0, Transport 2.5.1, Multiplayer Services 1.1.3, Vivox 16.6.0.
- Unity Companion License. Free local single-player entry; network without UGS not verified. Git LFS required.
- Unity 6.3 NOT_TESTED. Do not merge NGO and Netcode for Entities stacks without an explicit adapter.

Sources: upstream README, LICENSE, ProjectVersion.txt and Packages/manifest.json in each repository. No project files copied.