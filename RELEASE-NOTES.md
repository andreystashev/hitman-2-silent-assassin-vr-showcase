# Hitman 2: Silent Assassin VR ? Alpha 2 RC1 Preview

**[Download Hitman2VR-Alpha2-RC1-Setup.exe](https://github.com/andreystashev/hitman-2-silent-assassin-vr-showcase/releases/download/alpha-2-rc1/Hitman2VR-Alpha2-RC1-Setup.exe)**

## Changes since Alpha 1

- Optional **On12 GPU** rendering: D3D8 to Microsoft's D3D9On12, shared D3D12 scene textures/fences and the Meta/OpenXR D3D11 host. The game's XRGB backbuffer is converted on the GPU. Accepted scenes skip CPU pixel readback; menus, optics and unsupported cases retain CPU fallback.
- On12 selection, prerequisite checking before renderer replacement, exact original-DLL/absence backup, restoration after exit and recovery when switching renderers. Restore-Hitman2-On12.cmd works without a headset. Original remains the default.
- Fix for returning from nested native action/ladder cameras. In Tunnel Rat, delayed native cleanup could overwrite a premature first-person push and leave the camera inside the character. The fix preserves the action observer, waits for a stable healthy idle actor, and uses checked native stack operations to recover first person.
- GPU-transfer/camera-return diagnostics and the complete On12 runtime, license and recovery files in the installer. Update/relocation cleanup preserves edited and unknown files.

The existing controls, tracked native arms/weapons, reloads, optics, night vision, menus, recording and connection profiles from Alpha 1 remain available.

## Validation and performance

The player retested repeated Tunnel Rat ladder entry, cancellation and exit in the headset and confirmed normal first-person return. The matching native camera recovery was observed in the new session. Automated checks covered the production camera callback and GOG/Steam native stack helpers, independent reloads, exact ARGB/XRGB GPU transfer and Reset/fallback transitions, Meta/OpenXR host fixtures, and isolated installer install/update/relocate/uninstall workflows.

A controlled RTX 4060 / 1600x1200 Anathema test measured approximately **121 game presents/s with Original versus 142 with On12 GPU** (+17%). Same-process GPU/CPU/CPU/GPU samples on On12 measured approximately 142 versus 103 presents/s (+38% for GPU transfer). Those controlled measurements used a fixed-pose diagnostic host without a headset compositor. They are not measured headset FPS or a guarantee for other scenes. Separate real-headset play confirmed GPU transport; submission rate can include repeated images.

This remains a preview, not a completed campaign-wide compatibility pass. OpenGL remains experimental. On12 requires compatible Windows/graphics-driver sharing support, Microsoft x86 D3DX9_43 and the game/headset on the same GPU. See [installation](INSTALLATION.md), [known issues](KNOWN-ISSUES.md) and [troubleshooting](TROUBLESHOOTING.md).

The original game is required and is not included. No global OpenXR registration or driver settings are changed.
