# Warps

The **places** menu provides a list of all scenes and their respective
entrances, grouped into eight categories. Selecting a scene with multiple
entrances will show a list of all entrances for that scene. Selecting an
entrance will instantly warp you to that entrance. Scenes with only one
entrance will warp you to that entrance when selected, without showing an
entrance list. If you want to warp to a specific entrance index, you can enter
that index in the warps menu and select **warp**. The **age** and **cutscene**
options specify which age Link will be at when performing a warp, and which
cutscene should be played for that scene. These options apply to both the
places menu and warping using an entrance index.

**clear cs pointer** will point the cutscene pointer to an empty cutscene,
which is useful for preventing certain wrong warps from crashing. The bottom of
the warps menu shows information about the game's current warp parameters.

**_Warning:_** Attempting to load a beta scene will cause a crash on all but
the debug version of Ocarina of Time, which is currently unsupported.

**_Warning:_** Starting a game (with a warp or scene loading command) when no
file data is loaded (i.e. from the N64 logo and, to a lesser extent, the file
select menu) will cause *undefined behavior*.