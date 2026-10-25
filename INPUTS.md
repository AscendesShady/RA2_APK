# Input and controls guide

Controls for Red Alert 2 Native ARM64, version 0.1.4.

## Finger controls

| Gesture | Action |
|---|---|
| One-finger tap | Normal left click: select a unit, issue a command or activate a menu button. |
| One-finger drag | Hold the left button and draw a selection box. |
| Quick two-finger tap | Right click at the first finger's position; cancel an action or deselect units. |
| Two-finger drag | Hold the right button for fast map scrolling. Lift either finger to stop. |
| Quick three-finger tap | Escape: open the mission menu or skip a full-screen movie. |

For a two- or three-finger tap, touch and release all fingers within about 350 ms with little movement. The action fires when the last finger lifts. Start a two-finger pan with both fingers together. Adding a finger after a one-finger selection drag has already begun ends that selection instead of turning it into a right click. Three-finger swipes do not send Escape.

## S Pen

- **Hover:** move the game cursor without clicking.
- **Tip contact:** left click. Drag the tip for a normal selection drag.
- **Side/barrel button:** maps to the right mouse button while hovering or touching; move while holding it for right-button map scrolling.
- **Alternative right click:** hover over the target, then tap the toolbar's **Right click** button with your other hand.
- Hold the toolbar **Right click** button while moving the pen to pan the map.

Menus have a visible pen-cursor fallback; the battlefield keeps the original game cursor. Bluetooth Air Actions are not required or implemented. Physical Samsung pen delivery remains unverified. If the pen shortcut intercepts the side button, use the toolbar alternative.

## USB OTG and Bluetooth mouse

Connect the mouse to Android, using an OTG adapter if required.

| Mouse input | Action |
|---|---|
| Move the mouse | Move the game cursor. |
| Left click | Select, command or activate a button. |
| Hold left and drag | Draw a selection box. |
| Right click | Cancel/deselect, as in the PC game. |
| Hold right and drag | Fast map scrolling. |

Left, right and middle button states are forwarded. Mouse buttons beyond those three are ignored. Wheel zooming/scrolling is not implemented in this build. Physical OTG/Bluetooth hardware testing is still required.

## Bottom toolbar and keyboard

| Button | Action / keyboard equivalent |
|---|---|
| Hide | Hide the toolbar. Tap the highlighted **Controls** button to restore it. |
| Menu / Esc | Escape: mission options or skipping a full-screen movie. |
| Deploy | D: deploy the selected eligible unit. |
| Base | H: center on the base. |
| Stop | S: stop selected units. |
| Ctrl | Toggle Control held down; tap again to release. |
| Shift | Toggle Shift held down; tap again to release. |
| Right click | Right click at the current pointer. Hold it while dragging another finger or moving the S Pen to pan. |
| Left / Up / Down / Right | Hold an arrow to scroll the map in that direction. |

Buttons show pressed feedback. Ctrl and Shift remain highlighted while enabled. Hardware keyboard input is supported, including the shortcuts above.

## Movies, saving and leaving the game

- **Skip a full-screen movie:** tap **Menu / Esc**, press Escape on a keyboard, or make a quick three-finger tap. Embedded radar videos were not checked for skipping.
- **Save without typing:** Menu / Esc > Save Game > Save > OK > Resume Mission. The name is prefilled with the mission and local date/time. Selecting an existing save still permits an intentional overwrite.
- **Load:** select the save from the original game's Load Game menu.
- **Switch titles:** use the original **Exit Game** option to return to the Android RA2 / Yuri chooser.

Emulator injection checks do not establish physical-device touch latency, pen behavior or mouse compatibility. See [README.md](README.md) for installation and build limits.
