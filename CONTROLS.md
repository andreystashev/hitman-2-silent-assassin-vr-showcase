# Controller controls

Names below use the Meta Touch layout. OpenXR profiles map corresponding controls to the same actions; other controllers may need runtime binding adjustments. **Controller help** is enabled by default and displays compact labels beside the hands.

## Gameplay

| Input | Action |
| --- | --- |
| Left stick | Move relative to the viewing direction. |
| Left stick click | Toggle sprint. Sneaking, crouching and starting a body drag cancel sprint. |
| Right stick | Turn. |
| Right stick click | Open/close the native inventory. |
| Hold right stick click | Recenter after about 650 ms. |
| Right trigger | Fire/use the right-hand weapon. Melee uses the game's native attack rules. |
| Left trigger | Fire the left-hand firearm. |
| A | Request the game's native reload. Automatic reload is enabled by default. |
| B tap | Toggle sneak posture. |
| B hold | Latch crouch after about 450 ms; press B again to clear the posture. |
| Hold X | Show contextual actions and health/ammunition information beside the left hand. Use a stick to select; release X to perform the selected native action. |
| Y tap | Holster/unholster. |
| Y hold | Drop the held item after about 650 ms. |
| Grip near the other held weapon | Transfer a supported weapon to the receiving hand. Release the triggers before transferring. |
| Hold left grip near a right-held long gun's fore-end | Support the weapon with the second hand; release to stop supporting it. |
| Menu | Open the original pause menu. |

Separate firearms use their respective triggers. When one weapon is reloading, the other can fire if its own native weapon state permits it. Reloads use the game's ammunition and animation systems; physical magazine manipulation is not provided.

Use the original action list for nearby pickups, doors, disguises, body interactions and other contextual actions. The preview does not make every world object physically grabbable. The headset's system button retains its runtime function.

## Inventory and native menus

| Input | Action |
| --- | --- |
| Either stick | Navigate entries. |
| A / right trigger | Confirm or equip. |
| B / Menu | Back or close. Right stick click also closes the inventory. |
| X / Y in native menu panels | Change tabs/focus groups where supported. |

In Load/Save screens, **Y** can switch between the scrolling save list and the lower controls, including **Cancel**. Release a held input after changing context, then press again for the next action.

## Actions, map and briefing

Hold **X** for the hand-adjacent action list. **Map** and **Mission briefing** are available there alongside the game's contextual actions. Select with a stick and release X to activate.

| Map input | Action |
| --- | --- |
| Left stick | Pan the map. |
| Right stick | Navigate map buttons. |
| A | Activate the selected button or floor-picker entry. |
| Right trigger / left trigger | Zoom in / out. |
| B / Menu | Back from a submenu or close the map. |

Briefing and other native panels use stick navigation, A/right trigger to confirm and B/Menu to go back.

## Sniper optics, binoculars and night vision

Bring a supported **right-hand scoped rifle** toward the headset to enter its native scope view. Lower it to leave. The support grip by itself does not select the scope. Use the **right stick up/down** for optic zoom and **B/Menu** to exit; reloading also leaves the rifle optic. Binoculars retain the game's optical mode.

Night vision remains a native equipment/action feature and is presented through the VR renderer. Optional weapon crosshair markers are separate from sniper optics; the release defaults to crosshairs off.

## Cutscenes and keyboard fallbacks

Movies and scripted cameras use a virtual screen. **A**, **B**, **Menu** or the **right trigger** requests the game's native skip/back action when that sequence permits it.

**F7** recenters the view. **F9** toggles headset output while the game is focused. VR starts automatically on launching the mod. The original keyboard/mouse controls and save system remain available.
