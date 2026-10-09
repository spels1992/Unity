# Offline Addressables and Scriptable Build Pipeline (2026-10-08)
Status DOCUMENTED / NOT_RUN; cost 0 ₽.

- Unity Addressables com.unity.addressables; prior research version 2.10.3 for Unity 6.3; use local AssetBundles and local catalog only, no CDN/paid hosting.
- Scriptable Build Pipeline com.unity.scriptablebuildpipeline; prior research version 2.6.2.
- Official sources: https://docs.unity3d.com/6000.3/Documentation/Manual/com.unity.addressables.html ; https://docs.unity3d.com/6000.3/Documentation/Manual/com.unity.scriptablebuildpipeline.html
- Test local catalog, build/load/unload, asset reference lifecycle, dependency deduplication, player build, versioned update and RAM.
- Verify package manifest, lockfile, license, dependencies and exact Unity 6.3 support at adoption time. No Editor tests.