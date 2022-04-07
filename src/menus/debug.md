# Debug

_Note: These features are for advanced users. Be careful._

This menu contains various debug features to use for testing;

-   **heap:** Displays information about the game's dynamic memory arena.
-   **display lists:** Displays information about display list usage.
-   **objects:** Shows a list of currently loaded objects, which contain
    graphical assets. The **push** option loads the object file of the given id
    at the end of the list, and the **pop** option unloads the last object in
    the list.
-   **actors:** Browse the currently loaded actors, and spawn new actors.
    Select an actor type and use the arrows to scroll between all the loaded
    actors of that type. The address and id of the selected actor is displayed
    below, as well as the actor variable in that actor instance. The **kill**
    option marks the currently selected actor for deletion, and the **go to**
    option teleports Link to the location of that actor. Pressing **cull zone**
    will display the field of view for the selected actor. When the actor is
    outside of its field of view, it will be culled. To spawn a new actor,
    enter an actor id, variable, the x, y, and z components of the position and
    rotation to spawn the actor at, and press **spawn**. The **fetch from
    link** option loads Link's current position and rotation into the position
    and rotation fields.
-   **flags:** Display and edit saved game flags. The flags are grouped by the
    records they are kept in. Use the arrows to cycle between flag records.
    Press a flag to toggle its state. A red flag is "off", and a green flag is
    "on". The **log** menu displays a list of recent flag events. When a flag
    changes, its record, id, and new value is inserted at the top off the list.
    The **undo** option reverts the effect of the most recent flag event and
    removes it from the log. The **clear** option removes all flag events from
    the log, but does not affect the state of the given flags. _Note:_ The flag
    log only records changes when the log menu is open. If a flag changes and
    then changes back while the log is closed, these changes will not be
    recorded. _Note:_ Scene-related flags only affect the currently loaded
    scene. If a scene flag event that occurred in one scene is undone in a
    different scene, it will not have the desired effect.
-   **memory:** Memory editor. Use the horizontal arrows to cycle between
    memory domains, and the vertical arrows to scroll up and down between
    addresses. Holding Z while scrolling will scroll faster. You can also enter
    an address manually in the address field. To edit memory, select the
    desired data type and press a memory cell to modify it. The leftmost column
    shows the starting address of each row of memory cells. Pressing an address
    will open the watches menu and create a new watch at that address.
-   **rdb:** Remote debugging interface through ED64 USB FIFO. Press **start
    rdb** to attach the debugger and halt the program, and **stop rdb** to
    detach the debugger. Press **break** to hit a breakpoint on the graph
    thread.