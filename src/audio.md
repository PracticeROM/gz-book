# Audio

The state of the audio is well separated from the state of the game, so
restoring the audio state is not necessary for the game to behave correctly
after a state load. The audio state is also quite complex and take up much
space. For these reasons, savestates only save minimal information about the
state of the audio. This has been known to sometimes cause audio bugs, such as
music failing to start playing, or sound effects not playing as they should.
