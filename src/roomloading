# Room Loading

Room loading normally happens asynchronously. That means the game continues
playing while the room loads, and the room appears whenever it's finished
loading. This usually takes 1 frame, but can take longer, depending on the cpu
and cartridge load. Emulators typically don't emulate cartridge bandwidth
limitations, so the delay is usually 0 frames.

When recording or playing back a macro, room loading behavior is changed to
always load synchronously. Thus the game stops until the room has finished
loading, such that load delay variations can not cause macros to desync.

