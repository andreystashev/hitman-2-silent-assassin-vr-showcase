# Alpha 2 RC1 preview status and known issues

Alpha 2 RC1 is designed for playing the original game in VR while keeping its native gameplay systems. It is an early preview, not a claim that every mission, outfit, interaction and hardware combination has completed an end-to-end validation pass.

## Gameplay and interactions

- Locomotion uses the sticks. Room-scale walking is not implemented.
- Reloading uses the game's native animations and ammunition logic; physical magazine manipulation is not implemented.
- Controller weapon handling is added to the original inventory and contextual-action systems. It does not turn every world object or body into a freely grabbable physics object.
- Weapon transfers, support grips and hand/body alignment should still be checked across different weapon models, outfits and postures. Use the native inventory/actions when an interaction is awkward.
- Scoped-rifle proximity handling is tied to supported right-hand native optics. Do not assume every unusual off-hand weapon arrangement has the same optic behavior.

## Rendering and performance

- **Original (recommended)** is the starting renderer. DXVK and OpenGL are experimental alternatives, and results vary with drivers and scene complexity.
- OpenGL can be significantly slower because the scene is drawn for the monitor and both eyes. Black-floor and close texture/draw-distance problems have been reported on that path. Small state-query changes have not established a meaningful FPS improvement.
- Some native fullscreen high-resolution modes fail before VR frame capture begins. Windowed 4K worked with Original and DXVK on the tested system; it is a workaround, not a universal fullscreen fix.
- Transport capacity up to 8192×8192 per eye does not demonstrate stable 8K gameplay or compatibility with every GPU/runtime.

## Headsets and startup

- Five connection profiles are available. Meta installations can take priority in Automatic; choose SteamVR or VDXR explicitly when using them.
- Live SteamVR output and Steam game-frame submission were checked, alongside automated connection/runtime fixtures. This does not establish support for every headset, controller binding or graphics driver.
- Steam can require a user response before opening the original game. Check its monitor/headset prompt when the launcher reports a wait.

## Recording

The optional recorder currently outputs 1920×1080 video at up to 60 FPS. It does not automatically match a 4K/8K game rendering resolution.

Please save regularly and report reproducible issues with the details listed in [troubleshooting](TROUBLESHOOTING.md#reporting-an-issue).

## Alpha 2 RC1 checks and limits

The Tunnel Rat nested ladder-camera problem was reproduced, fixed and retested by the player with repeated ladder entry, cancellation and exit. The matching native mode1 recovery was observed in diagnostics. This is not a full campaign or every-action validation.

On12 GPU is optional and depends on installed Windows/DirectX components, graphics-driver sharing support and the game/headset adapter. Microsoft x86 D3DX9_43 is required. Visual checks and exact-pixel fixtures do not cover every mission effect or driver. Game presents, newly rendered stereo pairs and runtime submissions are different rates; submission rate may include repeated images.
