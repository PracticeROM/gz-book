# Free Camera

The free camera function provides full control of the game's camera. When
enabled, the camera can be controlled with the joystick, C buttons, and Z
trigger. These controls are disabled in the game when controlling the free
camera. Press **lock** to disable the manual camera controls and restore the
normal game controls.

The free camera has two **mode** settings; when set to *camera*, the game's
camera is physically moved, which affects the behavior of in-game objects that
react to the camera's position. When set to *view*, only the graphical
viewpoint is changed. The game's camera then behaves as usual and is disjoint
from the user's view of the scene.

The **behavior** setting decides how the camera moves and how the controls
work;

-   **manual:** The camera does not move by itself. Use the joystick to look
    around, and the C buttons to move. Hold Z to move with the joystick, look
    with C-left and right, and move vertically with C-up and down. The
    **distance min** and **distance max** settings do nothing.
-   **birdseye follow:** The camera automatically looks at Link, and moves
    forward and backward to stay within the specified *distance*. Controls
    are the same as for *manual*.
-   **radial follow:** The camera follows Link from a fixed viewing angle. It
    will move up, down, and sideways to keep Link in focus, and forward and
    backward to stay within the specified *distance*. Use the joystick,
    C-left, and C-right to rotate the viewing angle, and C-up and down to move
    towards and away from the focus point. Hold Z to swap the function of C-up
    and down with the vertical joystick axis.