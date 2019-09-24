# Scene

Selecting **explorer** will bring up the scene explorer, which shows an overlay
of the current scene. Use the D-Pad up and down to navigate forwards and
backwards through the scene, and D-Pad left and right to rotate the view. While
holding Z, the D-Pad up and down will navigate vertically through the scene,
and D-Pad left and right will move sideways. Use the `explore prev room` and
`explore next room` commands to cycle through the rooms of the scene (bound to
`R + D-Down` and `R + D-Up` by default). Pressing L will teleport link to the
location and orientation of the crosshair and close the scene explorer.

**set entrance point** sets link's current position and orientation as the
point where he will respawn after voiding out. **clear flags** and **set
flags** modifies the temporary and permanent flags for the current scene, which
keep track of things such as which chests have been opened, which items have
been collected, which enemies have been defeated, etc. The **load room** option
loads the room with the specified index, if a room which such an index exists
within the current scene. If that room is already the currently loaded room,
it will be unloaded. **collision view**, when enabled, shows the static scene
collision in the current scene. The collision polygons are color-coded to show
special properties;

-   **Blue:** Hookshotable surface.
-   **Purple:** Surface with special interaction (ladder, vine, crawlspace, not
    climbable, grabbable).
-   **Red:** Void trigger.
-   **Green:** Load trigger.
-   **Light green:** Surface with special behavior (sand, quicksand, ice, lava,
    jabu wall, damaging wall, no recoil wall, void).
-   **Light yellow:** Slippery slope.
-   **White:** Normal surface.

Note that collision polygons are affected by scene lighting and fog, which can
cause their appearance to be misleading. The collision view **mode** decides
how collision polygons are drawn. The _decal_ setting will draw polygons
overlaid on scene textures, but will not produce any new surfaces (note however
that most emulators do not correctly emulate this behavior). The _surface_
setting draws collision polygons as their own surfaces, but can produce depth
flickering on existing scene textures. Collision polygons can be configured to
be completely opaque, or see-through with the **translucent** option. Enabling
**wifreframe** will display lines around the edges of each polygon. The
**reduced** option will reduce potential lag by only rendering collision
polygons with some special property (i.e. colored polygons). When entering a
new scene, or changing a collision view setting, the collision view must be
disabled and re-enabled in order to update. **teleport slot** selects which
position to save and load when using the teleportation commands (this can also
be bound to a button combination, but is unbound by default). The bottom of the
scene menu shows information about the current scene.
