# Hitman 2: Silent Assassin VR — Alpha 1 Preview

**[Download Hitman2VR-Alpha1-Setup.exe](https://github.com/andreystashev/hitman-2-silent-assassin-vr-showcase/releases/download/alpha-1/Hitman2VR-Alpha1-Setup.exe)**

Alpha 1 is a playable preview of a community VR conversion for **Hitman 2: Silent Assassin (2002)**. It is designed to let you play the original campaign in VR while retaining the game's missions, stealth, AI, disguises, inventory, contextual interactions, saves and progression.

The original game is required and is not included. This is an independent community project, not an official release.

## In this preview

- Stereo rendering and head tracking using the game's native camera and visibility paths.
- Tracked controller aiming with the character's own arms and held weapons, separate firing hands, native reloads and long-gun support grips.
- Firing with one hand while the other weapon reloads, supported weapon transfer, and native melee attack handling.
- Sniper optics, binoculars, night vision and virtual-screen presentation for menus and scripted cameras.
- Controller navigation of the native inventory, contextual actions, map, briefing and save/load screens.
- Hand-adjacent actions, health/ammunition information and controller help.
- Meta, VDXR, SteamVR, OpenXR and Automatic connection profiles, with runtime/host validation and no global OpenXR registration changes.
- A per-user installer with updates, relocation, automatic previous-installation detection and verified old-file cleanup, without a separate cleanup-path setting.
- Automatic VR startup, recovery of interrupted renderer sessions, protection against simultaneous launches, and clearer Steam confirmation diagnostics.

Fresh profiles use **Original (recommended)**, **Crosshair off**, **Controller help on**, **Cheats off**, **Mission selector off** and **Automatic reload on**.

## Preview status

The underlying game mechanics remain native. VR interaction and compatibility are still being refined. Stick locomotion and native animated reloads are used; this is not a promise of room-scale walking or physical magazine manipulation.

Original is the recommended starting renderer. OpenGL remains experimental and can be significantly slower, with reported native texture/draw-distance issues. Some fullscreen high-resolution setups fail before VR capture starts; windowed mode is a tested workaround. Higher supported frame sizes do not guarantee playable 4K/8K performance.

Release preparation included native camera/body/weapon/input, rendering, frame transport, host, audio and recording checks, plus isolated installer installation/update/relocation/uninstall tests. Live SteamVR headset output and Steam game-frame submission were also checked. These checks do not establish an independently completed campaign or support for every headset, driver, outfit and controller combination.

See [installation](INSTALLATION.md), [controls](CONTROLS.md), [known issues](KNOWN-ISSUES.md) and [troubleshooting](TROUBLESHOOTING.md). Save regularly and report reproducible problems through the public repository's issues.
