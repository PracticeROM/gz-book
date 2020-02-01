# Settings

This is where most of the functionality of The Practice ROM is configured.

The **profile** option selects which profile to save and load settings to and
from. When the game starts, the settings saved to profile zero are
automatically loaded, if any.

The appearance of the menu can be configured  with the **font** and
**drop shadow** options. Disabling drop shadow can reduce the graphical
computation impact of the menu, but may also reduce readability. The visibility
of the on-screen display elements can be configured with the **input display**,
**log**, **lag counter**, **timer**, and **pause display** options. The screen
position of the utility menu, input display, log, lag counter, and timer can be
configured by their respective positioning buttons. Holding Z when positioning
an element will move it faster.The display unit of the lag counter can be set
to *frames* or *seconds*. **macro input** enables or disables controller input
when macro playback is active. The **break type** option decides how the
*break free* command will function. When the break type is *normal*, the
command will end textboxes, certain events and traditional cutscenes. The
*aggressive* break type will cause the command to also try to reset the camera
and some of Link's state flags. **save settings** and **load settings** will
save and load the current settings to the currently selected profile.
**restore defaults** will restore all saved settings to their default values
(Does not affect saved profiles). If the saved settings were to become
corrupted in such a way that they prevent the game from starting, holding the
Start button when the game is starting will load the default settings instead
of loading profile zero. The following settings are saved:

-   Menu and on-screen displays appearances and settings.
-   Saved positions and the currently selected position slot number.
-   Watches.
-   Command button binds.
-   Activated cheats.
-   Warp menu age, cutscene index, and entrance index.
-   Disk file loading settings.

The **commands** menu lets you bind commands to custom button combinations
and/or activate them manually. Pressing the name of a command will activate
that command, and pressing the button combo in the right column will bind a
button combo to the corresponding command. If you want to unbind a command,
press and keep holding L when starting the binding. A button combo for any
given command can contain at most four buttons. When activating a command with
a button combo, the button combo must explicitly be input the way it appears in
the commands menu. For example, a command with the button combo `R + A` will
only be activated if you press R first and then A, or R and A at the same
time. `A + R`, or `R + B + A` will not activate the corresponding command. If
the set of buttons in one button combo is a subset of those in another button
combo, the former will be overridden by the latter when both are active
simultaneously.

The following commands are available:

-   **show/hide menu:** Opens the utility menu if it's closed, closes it if
    it's opened. *Default: `R + L`*
-   **return from menu:** Returns to the previous menu, as if the *return*
    button was pressed. *Default: `R + D-Left`*
-   **break free:** Attempts to break any effect that removes control of Link.
    *Default: `C-Up + L`* *VC Default: `Start + L`*
-   **levitate:** The classic L to levitate command. *Default: `L`*
-   **fall:** Makes Link fall through the floor, as if there was no floor.
    *Default: `Z + L`*
-   **turbo:** Sets Link's linear velocity to 27. *Default: `unbound`*
-   **file select:** Returns (or proceeds) to the game's file select menu.
    *Default: `B + L`*
-   **reload scene:** Reloads the current scene, starting from the last scene
    entrance. *Default: `A + L`*
-   **void out:** Reloads the current scene, starting from the last room
    entrance as if Link voided out. *Default: `A + B + L`*
-   **toggle age:** Toggles between Adult and Child Link. Takes effect when
    entering a new area. *Default: `unbound`*
-   **save state:** Save the state of the game to the currently selected state
    slot. *Default: `D-Left`*
-   **load state:** Load the state saved in the currently selected state slot.
    *Default: `D-Right`*
-   **save memfile:** Saves the current state of the game to the memory file in
    the current memory file slot. Everything that would be saved when saving
    the game normally is saved to the memory file. *Default: `unbound`*
-   **load memfile:** Loads the state of the current memory file.
    *Default: `unbound`*
-   **save position:** Saves Link's current position and orientation to the
    current position slot. *Default: `unbound`*
-   **load position:** Teleports Link to the position in the current position
    slot. *Default: `unbound`*
-   **previous state:** Selects the previous savestate slot.
    *Default: `unbound`*
-   **next state:** Selects the next savestate slot. *Default: `unbound`*
-   **previous memfile:** Selects the previous memory file slot.
    *Default: `unbound`*
-   **next memfile:** Selects the next memory file slot. *Default: `unbound`*
-   **previous position:** Selects the previous position slot to be used for
    teleportation. *Default: `unbound`*
-   **next position:** Selects the next position slot to be used for
    teleportation. *Default: `unbound`*
-   **pause/unpause:** Pauses the gameplay, effectively freezing the state of
    the game. If the game is already frozen, resumes gameplay as normal. While
    the game is frozen, a pause icon will appear on the top-left of the screen
    (enabled by default, can be turned off). *Default: `D-Down`*
-   **frame advance:** If the game is frozen by the pause command, advances one
    frame of gameplay. Otherwise, freezes the game as if the pause command was
    activated. *Default: `D-Up`*
-   **record macro:** Start/stop input macro recording. *Default: `unbound`*
-   **play macro:** Start/stop input macro playback. This command can be held
    down to loop the macro. *Default: `unbound`*
-   **collision view:** Toggle the collision view on or off.
    *Default: `unbound`*
-   **hitbox view:** Toggle the hitbox view on or off.
    *Default: `unbound`*
-   **explore prev room:** Loads the previous room while using the scene
    explorer. *Default: `R + D-Down`*
-   **explore next room:** Loads the next room while using the scene explorer.
    *Default: `R + D-Up`*
-   **reset lag counter:** Resets the number of lag frames recorded to zero.
    *Default: `R + B + D-Right`*
-   **toggle watches:** Shows or hides watches globally.
    *Default: `R + D-Right`*
-   **start/stop timer:** Starts the on-screen timer if it is stopped, stops it
    if it's running. *Default: `R + A + D-Left`*
-   **reset timer:** Sets the time of the on-screen timer to zero.
    *Default: `R + B + D-Left`*
-   **start timer:** Starts the on-screen timer if it is stopped.
    *Default: `unbound`*
-   **stop timer:** Stops the on-screen timer if it is running.
    *Default: `unbound`*
-   **reset:** Reset the game, as if the reset button had been pressed.
    *Default: `unbound`*

**_Warning:_** Unbinding the *show/hide menu* or *return from menu* commands,
or binding them to a button combination that will interfere with menu
navigation can make it impossible to use the utility menu. If this happens,
you can restore the default settings by entering the following button sequence:
`D-Up D-Up D-Down D-Down D-Left D-Right D-Left D-Right B A`.

_Note:_ Button combos that interfere with menu navigation for commands that
aren't related to menuing are disabled while the utility menu is active.
