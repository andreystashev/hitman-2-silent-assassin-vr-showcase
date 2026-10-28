# Hitman 2: Silent Assassin VR — Alpha 1

**[Download Alpha 1 — Preview installer](https://github.com/andreystashev/hitman-2-silent-assassin-vr-showcase/releases/download/alpha-1/Hitman2VR-Alpha1-Setup.exe)** | [Release notes](RELEASE-NOTES.md) | [All releases](https://github.com/andreystashev/hitman-2-silent-assassin-vr-showcase/releases)

A community VR conversion for the original **Hitman 2: Silent Assassin (2002)** on PC, with stereo rendering, head tracking and controller-driven arms and weapons.

Alpha 1 is a **playable preview designed for playing the original campaign in VR with its original mechanics**. Missions, objectives, enemy AI, stealth, disguises, inventory, contextual actions, saves and progression continue to use the game's native systems. The mod adds VR viewing and controller-based weapon handling to that game.

It remains a preview. VR interactions, rendering and compatibility still need testing across missions, outfits, weapons, controllers and headsets. Original inventory and action menus remain available when a VR interaction is awkward. See [known issues and testing limits](KNOWN-ISSUES.md).

You need your own legitimate copy of the game. No game executable or game assets are included. This project is independent of IO Interactive and the game's publishers.

## What the mod adds

- Native stereo views and head tracking, with the original character's arms and held weapons driven by tracked controllers.
- Independent left/right firing, native weapon reloads and second-hand support for long guns. A firearm can continue firing while the other hand's weapon reloads.
- Controller-based aiming and weapon transfer between hands, while melee weapons retain the game's native attack rules.
- Sniper optics, binoculars and night vision integrated with the VR presentation.
- Controller access to the original inventory, contextual actions, map, briefing, pause and save/load menus.
- A compact action panel, health/ammunition information and optional control hints beside the hands.
- Menus, movies and scripted camera sequences presented on a virtual screen.
- Headset audio routing for the game without changing Windows' default speaker or microphone.
- A separate optional video recorder for preparing gameplay footage.

## Requirements

- Windows 10/11, 64-bit.
- The supported original Steam or GOG `hitman2.exe`. See [supported builds](INSTALLATION.md#supported-game-builds) for exact hashes. The Steam game is App **6850**.
- A connected PC VR headset, tracked controllers and a compatible PC VR runtime.
- A GPU and driver that support the original renderer and the runtime's D3D11 graphics path. DXVK additionally requires compatible Vulkan support.

Connection profiles are **Quest Link / Air Link (Meta)**, **Virtual Desktop / VDXR**, **SteamVR / Steam Link**, **OpenXR**, and **Automatic**. Choose the matching explicit profile when several PC VR applications are installed. The choice does not change Windows' global OpenXR registration. See [connection setup](INSTALLATION.md#headset-connection-profiles).

## Install and play

1. Download `Hitman2VR-Alpha1-Setup.exe` from [Releases](https://github.com/andreystashev/hitman-2-silent-assassin-vr-showcase/releases/tag/alpha-1).
2. Close the game and old VR launcher. Run the installer and select your supported `hitman2.exe`.
3. Install the mod in its own folder, outside the game folder.
4. Connect the headset through your chosen PC VR application.
5. Open **Hitman 2 VR**, select the connection and click **Save & play**. VR starts automatically.

Use **Original (recommended)** first. DXVK and OpenGL are alternative experimental renderers; OpenGL can be substantially slower. The game controls its rendering resolution. If its fullscreen device creation fails, `Window 1` in `hitman2.ini` is a tested workaround. See [rendering and resolution](INSTALLATION.md#rendering-and-resolution).

Steam may wait for a launch confirmation on the monitor or in the headset. Respond to that prompt before expecting the game to start. The launcher reports this wait; see [Steam startup](TROUBLESHOOTING.md#steam-waits-before-starting-the-game).

## Release defaults

| Setting | Alpha 1 default |
| --- | --- |
| VR startup | Automatic; no separate switch |
| Weapon crosshair | Off |
| Controller help | On |
| Cheats and console | Off |
| Startup mission selector | Off |
| Automatic reload | On |
| Game renderer | Original (recommended) |

Updates preserve existing settings. The installer detects a registered previous installation automatically and also checks recognized mod files in the selected destination or standard per-user mod folder. No separate cleanup path is required. Verified, unchanged old mod files are removed after successful installation; saved games, recordings and unknown or edited files are retained.

## Help and feedback

Read [installation and updates](INSTALLATION.md), [controller controls](CONTROLS.md), [troubleshooting](TROUBLESHOOTING.md) and [known issues](KNOWN-ISSUES.md).

Reports should include Alpha 1, the game build, headset, connection profile, renderer, resolution and reproducible steps. Review logs before sharing them: they may contain local paths and device information. Do not upload the game, saved credentials or memory dumps to a public issue.

## About this repository

This is the public documentation, support and release repository. Private development history, mod source code, personal configuration, recordings and crash dumps are not published here. Public visibility does not grant a source-code license for the mod. Bundled dependencies retain their own licenses; see [third-party notices](THIRD-PARTY-NOTICES.md).
