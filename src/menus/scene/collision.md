# Collision

**Show collision**, when enabled, shows the static and dynamic scene collision
in the current scene. The collision polygons are color-coded to show special
properties;

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
cause their appearance to be misleading. These effects can be disabled by
turning off the **shaded** option. The collision view **mode** decides how
collision polygons are drawn. The _decal_ setting will draw polygons overlaid
on scene textures, but will not produce any new surfaces (note however that
most emulators do not correctly emulate this behavior). The _surface_ setting
draws collision polygons as their own surfaces, but can produce depth
flickering on existing scene textures. Collision polygons can be configured to
be completely opaque, or see-through with the **translucent** option. Water
boundaries are displayed by default, but can be disabled with the
**waterboxes** option. Enabling **wifreframe** will display lines around the
edges of each polygon. The **reduced** option will reduce potential lag by only
rendering collision polygons with some special property (i.e. colored
polygons). When **auto update** is on, the collision view will update
automatically when a collision view setting is changed, or when the collision
changes. If turned off, the collision view must be manually disabled and
re-enabled in order to update.

The **show colliders** option shows simple collision bodies and damage sources
and sinks. The **translucent** and **shaded** options are identical to the
collision view options with the same names. Hitboxes are also color-coded by
their type;

-   **Red:** Hitboxes; deal damage.
-   **Blue:** Hurtboxes; take damage.
-   **White:** Bumpboxes; pushes and/or get pushed.

The types of colliders to show can be selected with the **hit**, **hurt**, and
**bump** options. It's common for objects to have multiple overlapping hitboxes
of different types.

Enabling **show paths** will display all of the paths that are defined in the
current scene. These are usually waypoints for NPC's. Each point in the path
will be displayed when **points** is enabled, and a line will be drawn between
subsequent points when **lines** is enabled. The path display can be
translucent or opaque as selected by the **translucent** option.
