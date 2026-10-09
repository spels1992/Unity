# Multiplayer technology — zero cost comparison (2026-10-09)
Status DOCUMENTED / NOT_RUN; no cloud subscriptions.

| Candidate | Upstream | License | Notes |
|---|---|---|---|
| Mirror | https://github.com/MirrorNetworking/Mirror | MIT | Host/server-client; no mandatory hosted relay. Prior research recorded 96.11.3; recheck release before installation. |
| FishNet | https://github.com/FirstGearGames/FishNet | FishNet custom license | Free base tier; review restrictions and paid Pro features. Prior research recorded 4.7.3; recheck. |
| Netcode for GameObjects | https://docs.unity3d.com/Packages/com.unity.netcode.gameobjects@2.0/manual/index.html | Unity Companion License | Official Unity stack; use Unity 6.3-compatible 2.x. Prior research recorded 2.13.2; verify package registry. |

Unity NGO 3.0 requires newer Unity than 6.3 according to prior research; check exact release notes before adoption. Avoid paid Relay, Lobby, server hosting. Use LAN/localhost in isolated test project. Existing Mirror/FishNet catalog cards should not be duplicated.