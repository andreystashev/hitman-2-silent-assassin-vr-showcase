# Troubleshooting

## Steam waits before starting the game

The launcher asks the installed Steam client to start App **6850**. Steam may wait for a launch confirmation, cloud/update response or another prompt before it creates the game process. The launcher reports a known pending confirmation and waits for up to 120 seconds.

Check Steam on the **monitor and in the headset/dashboard**, and respond to its actual prompt. An ordinary game window opening is expected when `Window 1` is configured; VR output comes from the mod's separate host.

If Steam starts the game only after the launcher's timeout, close that instance and start again through **Hitman 2 VR → Save & play**. Starting the game directly from Steam does not by itself load the VR mod.

## No image in the headset

1. Confirm the PC VR application is running and its headset/controllers are connected.
2. Select the matching explicit connection in the mod: Meta, VDXR or SteamVR. Automatic can choose installed Meta software when you intended another runtime.
3. Keep both VR hosts and the OpenXR loader with the rest of the package. Re-run the installer to repair missing files.
4. Wear the headset and bring the game app to the foreground in the selected runtime. A running desktop game alone does not confirm that the VR host is ready.

A message that no headset is connected to VDXR does not establish a VDXR defect when the headset is currently connected through SteamVR. Connect through the selected software before retrying. The generic OpenXR profile follows the active runtime unless you supply a valid x64 runtime JSON.

## The executable or renderer is rejected

Use the supported original `hitman2.exe` and native renderer from the same installation. See [exact supported hashes](INSTALLATION.md#supported-game-builds). Restore altered game files through the store if necessary. Do not copy an executable or renderer from another person's installation, and do not bypass the checks by renaming files.

Code-changing patches and graphics wrappers can conflict with the game-specific hooks. Test Original with a clean supported game before adding other modifications.

## Interrupted renderer session or concurrent launch

Close the game and its host before switching renderers. A valid unfinished OpenGL journal is automatically recovered on the next mod launch. An invalid checksum, unexpected renderer value or changed backup is reported and retained.

Keep the complete mod and its backup available if recovery fails. Do not delete a journal or replace its hashes just to remove the error. A second launch for the same game path is blocked while the first launch/session owns it.

## Direct3D device or high-resolution startup error

First confirm that the original game can use the selected mode without VR. A native fullscreen failure can occur before any frame reaches the mod. `Window 1` in the game's `hitman2.ini` is a tested workaround; see [resolution setup](INSTALLATION.md#rendering-and-resolution).

The frame transport accepts sizes up to 8192×8192 per eye, but that is a capacity limit, not a guarantee of game/driver/runtime compatibility or FPS. Higher resolution increases readback, copying and upload work. The launcher does not automatically force 4K or change the monitor mode.

## Low FPS, flickering or different renderer results

Start with **Original (recommended)**. Compare the same scene, view, resolution, weapon and night-vision state when testing DXVK or OpenGL. Restart after switching; do not mix renderer files manually.

OpenGL draws the native monitor view plus stereo views and can be substantially slower. Its reported black-floor and close texture/draw-distance issues remain experimental-path limitations. Original/DXVK and OpenGL also count new stereo images differently: Original/DXVK alternate eyes, so 60 game frames are approximately 30 new stereo pairs. VR-host submission cadence can repeat existing images and is not the game's rendering FPS.

`Show-Hitman2VR-Performance.cmd` summarizes local per-session measurements. For windowed DXVK synchronization, see the `d3d9.presentInterval` setting in [installation](INSTALLATION.md#rendering-and-resolution). Headset refresh and reprojection remain runtime-controlled.

## Audio

Check the selected connection and its headset audio output. The mod routes the game, rather than changing Windows' global default output or microphone. With several endpoints active, automatic selection can be ambiguous. A game audio session opened before changing routing may need a game restart.

## Recording footage

Run `Record-Hitman2-VR.cmd` from the installed mod folder. The normal recording path includes the game and mod composition, menus and cutscenes. It writes a continuous **1920×1080 MP4**, at 60 FPS output by default, even when the game renders above 1080p. Output FPS does not create missing source motion frames.

Recording requires your own **Python 3**, **FFmpeg**, and the Python `numpy` and `soundcard` packages for audio. These are optional separate installations, not required to play the mod and not bundled by the installer. FFmpeg can be on PATH or in a supported existing Virtual Desktop Streamer installation.

The default output folder is `recordings` beside the mod. Focus the recording console and press **Enter** or **Q**, or use **Ctrl+C**, to finish. Wait for the final save message before closing it. Options are available through `Record-VR.ps1`, including `-NoAudio`, `-Seconds` and `-Output`; `-GameOnly` is a diagnostic view that omits the full mod composition.

## Reporting an issue

Include:

- **Alpha 1**, Steam/GOG build, headset and controllers.
- Connection profile/runtime, renderer and game resolution/window mode.
- The mission, outfit, weapon and steps needed to reproduce the problem.
- Whether it appears on the monitor, in the headset, in gameplay or only in a menu/cutscene.

Logs and status files are saved locally beside the mod. Review them before attaching excerpts: they can contain local paths or device information. Nothing is uploaded automatically. Do not post the game executable, original assets, credentials or a memory dump in a public issue.
