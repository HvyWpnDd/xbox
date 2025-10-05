# Anamorphic Widescreen Patch for Dungeons & Dragons Heroes on XBOX

This changes the horizontal field of view for 3d scenes in the game to be correct for 16:9 aspect ratio, so they don't look stretched when you put your television in widescreen mode. It does not change any UI, so the HUD, menus and splash screens will still look stretched. It has only been tested so far on the European release of the game, through the character selection screen, intro cutscene and start of the first level.

## Patch

In the `DEFAULT.XBE` file, change the bytes at position `2f7370` from `00 00 80 3f` to `ab aa aa 3f`.

If you prefer, you can do a "find and replace" from `8e 79 45 3e  00 00 80 3f` to `8e 79 45 3e  ab aa aa 3f`.

## Troubleshooting

- If you only have a `.xiso` file, you can extract the `DEFAULT.XBE` using [xdvdfs](https://github.com/antangelo/xdvdfs)
- If you need to resign the `DEFAULT.XBE` after applying the patch you can sign it with the habibi signature using [xbedump](https://github.com/XboxDev/xbedump)

## Acknowledgements

Many thanks to the authors of the following tools which I used extensively while working on this:

- [xdvdfs](https://github.com/antangelo/xdvdfs)
- [xbedump](https://github.com/XboxDev/xbedump)
- [ghidra-xbe](https://github.com/XboxDev/ghidra-xbe)
- [ghidra](https://github.com/NationalSecurityAgency/ghidra)
- [gdb](https://www.sourceware.org/gdb/)
- [xemu](https://xemu.app/)

