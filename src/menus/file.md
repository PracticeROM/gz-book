# File

The **restore skulltulas** option clears all the gold skulltula flags in the
current file, thus restoring all destroyed gold skulltulas. The gold skulltulas
in the current scene are not affected until the scene is reloaded. **call
navi** sets Navi's advice timer to a value which will make her want to
talk to you. This will not have any effect until you enter an area where Navi
normally appears. **load debug file** loads the default file that used on the
title screen and when starting the first file on the debug version file select
menu. The current time of day can be manually adjusted, or automatically
fast-forwarded to day or night with the corresponding buttons. **epona freed**,
**carpenters freed**, **intro cutscenes**, and **rewards obtained** let's you
set and clear various useful flags in the current file. Pressing the checkmark
will set the pertinent flags such that they have been "completed", and the
cross will clear them (setting them to the state that they were in when the
file was created).

The **timer 1** and **timer 2** options display and modify the state of the two
types of timers in the game. The first timer is used for hot rooms and races,
and the second timer is used for trade items and the Castle Collapse sequence.
The numbers represent the number of seconds left on the timers, and the options
show the current state of the timers. Both of these can be modified manually.
*Note:* When the first timer is set to a heat state, the game will instantly
deactivate it if the current room is not "hot". **_Warning:_** Modifying the
state of the timers can yield strange behavior. In general, it is safest to use
the the *starting* and *stopped* states when doing this.

The **file index** option decides which file the game will be saved to when
saving from the start menu or the Game Over screen. When the file index is set
to FFh, as it is by default on the title screen, saving will have no effect.
There's also a **language** and **z targeting** option, which apply to the
current file.

Save files can be saved to and and loaded from an SD card with the **save to
disk** and **load from disk** options. Pressing _load from disk_ will bring up
the file browser. Pressing the name of a save file will load it and return to
the file menu. The **load file to** and **after loading** options decide where
in memory the file will be loaded to (the current zelda file, the currently
selected memfile slot, or both), and what should happen when the loading is
completed (reload scene, void out, or nothing). The _after loading_ option will
have no effect when loading only to the current memfile. The file extension
used for save files on disk is `.ootsave`, and the default filename is `file`.
The filename can be changed by pressing the name field. Pressing **clear** will
set the name field to be empty. When the name field is empty, the default
filename is `untitled`. When saving, pressing the name of a save file in the
file browser will copy that name to the name field. Pressing accept will save
the file to the current folder in the file browser with the specified file
name. If the file exists, you will be prompted to overwrite it.