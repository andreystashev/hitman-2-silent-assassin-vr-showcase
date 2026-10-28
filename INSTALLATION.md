# Installation and updates

## Supported game builds

Use your own installed PC copy of **Hitman 2: Silent Assassin (2002)**. The installer and launcher verify `hitman2.exe` before enabling the game-specific hooks.

| Build | Supported executable SHA-256 |
| --- | --- |
| Steam, App 6850 | `f85765f1b36734165fc22122050ca39ca1b8873f9b2d430b50a8271cde5d5136` |
| Supported GOG PC build | `d885070dca88972a31e0c3eea298ae5c51a6e597350832a7dca2d1b2bbd1a621` |

A store/version label alone is insufficient. Modified executables, alternative releases and patches that change game or renderer code may be incompatible. Unknown builds are rejected. The mod does not supply an executable, original renderer or game assets.

## First installation

1. Install the game and confirm that it starts normally. Choose a working rendering resolution.
2. Close the game, VR host and old mod launcher. Save your progress first.
3. Run `Hitman2VR-Alpha1-Setup.exe`. Select the supported `hitman2.exe`; Steam libraries are searched automatically.
4. Choose a separate mod folder outside the game folder. The default is under your Windows user account; administrator rights are normally unnecessary.
5. Connect your headset through the PC VR software you plan to use.
6. Open **Hitman 2 VR**, select the connection profile and click **Save & play**.

VR starts automatically with the mod. **F7** recenters the view; **F9** toggles headset output while the game is focused.

## Headset connection profiles

| Profile | Setup |
| --- | --- |
| Automatic | Prefers the installed Meta runtime, otherwise the active OpenXR runtime. Choose an explicit profile when you want SteamVR or VDXR and Meta software is also installed. |
| Quest Link / Air Link (Meta) | Connect through Meta's PC Link software and enter the PC VR environment. This profile uses the installed x64 Meta runtime. |
| Virtual Desktop / VDXR | Start Virtual Desktop Streamer, connect the headset and use VDXR for the PC VR session. Select the VDXR profile. Meta software is not required for this path. |
| SteamVR / Steam Link | Start SteamVR, wait for the headset/controllers to be ready and select SteamVR. The launcher locates its x64 OpenXR manifest, including installations in other Steam libraries. |
| OpenXR | Connect through the PC software for the active OpenXR runtime, or select a compatible existing x64 runtime JSON manifest. The runtime must support D3D11. |

**OpenXR runtime JSON** is optional when the runtime can be detected. Browse to an existing runtime `.json` manifest only when needed, not to a DLL or the SteamVR executable. The manifest, referenced x64 runtime library and selected host are validated before launch.

Explicit profiles do not silently fall back to another connection. The choice applies to the mod and its child host and does not rewrite Windows' global OpenXR registration. Close the game before changing connections. Controllers with different layouts may require binding adjustments in their runtime.

## Rendering and resolution

**Original (recommended)** is the release default. **DXVK** and **OpenGL** are experimental alternatives. Keep the complete package together and close the game and host before switching renderers.

Renderer changes are reversible. A recognized unfinished OpenGL session is recovered automatically before another launch, using its verified journal. A damaged or externally modified journal is retained and reported instead of overwritten. Launches for the same game path are serialized.

The game controls its resolution through `hitman2.ini`; the VR transport does not reduce it to the old low-resolution limit. Frames up to **8192×8192 per eye** fit the transport, but the original game, driver, available memory and runtime must still support the mode. This is not an 8K performance guarantee.

For a native fullscreen error such as **Direct3D: Unable to create device**, try a supported resolution with:

```ini
Resolution 3840x2160
Window 1
```

Use your own desired supported resolution. Windowed 3840×2160 was checked with Original and DXVK; this does not fix every fullscreen mode or certify every GPU. The image submitted to VR and the headset's display resolution are different quantities.

The mod requests disabled desktop VSync. In fullscreen Original/DXVK it applies the game's native startup option. For windowed DXVK, the following setting in the game's `dxvk.conf` disables its presentation synchronization:

```ini
d3d9.presentInterval = 0
```

Preserve other settings in an existing file. Headset refresh timing and reprojection remain controlled by the VR runtime.

## Settings and sound

Fresh profiles have weapon crosshairs off, controller help on, cheats/console off, the startup mission selector off, and automatic reload on. Changes apply on the next mod launch. The original game configuration is backed up before relevant game-option edits; save files are preserved.

The game is routed to the selected headset/runtime's audio endpoint when it can be identified. Windows' default output and microphone are not changed. If automatic audio selection is ambiguous, review the selected PC VR connection and the mod's local audio status before changing devices.

## Updating, moving or repairing

Run the new installer to update or repair the mod. Existing `vr.ini` settings are preserved, so an updated profile may differ from fresh-install defaults.

For relocation, choose a separate new folder. The installer detects the previous installed copy automatically; there is no separate cleanup-path field. It also checks for a recognized mod already in the chosen destination or the standard per-user mod folder. After successful replacement, verified, unchanged old mod files are removed. Settings, recordings, edited files and unknown files are retained. An unregistered portable copy in an unrelated folder is not located by a broad disk scan. The original game and saves are preserved.

Close the old launcher, game and VR host first. The installer refuses an active installation and never terminates the game automatically. Do not nest the old/new mod folders or install through a junction/symbolic link. Use the updated shortcuts afterward.

## Removing the mod

Close the game and host, then uninstall **Hitman 2: Silent Assassin VR** through Windows Apps. The installed runtime and shortcuts are removed; user settings and recordings remain.

Renderer backups in the game folder are separate from installed mod files. If a renderer session was interrupted, recover it while the complete mod package is still available. Retain the backup if recovery reports a conflict.
