# Settings

This menu provides advanced settings for savestates and macro recording. The Practice ROM
implements certain hacks to keep macros in sync (See
[About Frame Advancing and Recording](./aboutframeadvancing.html)).
All hacks are enabled by default. Disabling the hacks can cause issues and
desyncs, and should only be done if required. For example, when recording a
setup that is sensitive to room loading lag. For such use cases, the hacks
should not be kept disabled longer than necessary (i.e. disable only when
recording that particular section).

The **wii vc camera** setting enables a camera quirk that is present on the Wii
VC versions of the game. This setting can be used to sync macros that were made
on Wii VC when played back on N64, or vice versa. It is enabled by default on
Wii VC versions of The Practice ROM. The **ignore state's z-target** option will keep the
current z-targetting mode when loading states that have a different setting,
which is useful for practicing with savestates made by someone with different
preferences.