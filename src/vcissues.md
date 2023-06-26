# VC Issues

There are some known issues with the Wii VC version of The Practice ROM:

-   The D-Pad on the Classic/Gamecube Controller is mapped to the L button on
    the Virtual Console. The WAD patcher remaps the D-Pad to be functional
    again, and maps C-Stick Down to L on the Virtual Console to provide access
    to the utility menu.
-   The scene explorer has graphical glitches due to poor emulation.

# Using an N64 Controller on Wii Virtual Console

If you wish to use the Nintendo 64 controller, using an adapter, on
Wii Virtual Console you will notice some issues when it comes to the mapping
of the controller and using the menu system in The Practice ROM.

To get around these issues, you will need a Wii Remote synced with your
Nintendo Wii and will also have to boot the game using an application such
as [GeckoOS](https://drive.google.com/open?id=1Brw46Kp5BOaAGZC9DqsL8QpSEFFSGSbz)
to run a cheat file from your SD Card to enable the reconfigured mapping.

The following contents can be placed on your SD card at the following location
`/codes/NGZJ.gct` from the root of your SD Card. 

You can also [download a copy of the file here](https://drive.google.com/file/d/1g2anEuSXQInkyY3XU7KKGAIi-EXNxQ5W/view?usp=sharing) 
if you'd prefer to not make your own copy.

```
82110001 001C7E52
86300001 0000000C
86100001 00000100
82110002 001C7E52
86300002 00000001
86100002 00000200
82110003 001C7E52
86300003 00000002
86100003 00000080
82110004 001C7E52
86300004 00000C00
80000005 00000006
88600005 00000004
88200001 00000002
88200001 00000003
88200001 00000005
84110001 00E7445E
```
