PCSXr360
PS1 Emulator from Ced2911
and other developers
- 
----------------

v2.1.1a PNG Fix
---------------
* Changelog:
  
   - Improvements:
      - Remove.jpg format
      - Added .png format for all image         and covers files

v2.1.1a
-------
* Changelog:
    - Compatibillity:
        - Added Swizzy's ROM loading data support from Aurora, now with gameprofile support.
        - Re-Added psx.iso autoboot for Freestyle Dash / Aurora cover mode, now with gameprofile support. 
            You have to put psx.iso in emulator root folder, and psx.iso.ini in the gameprofile folder and set AutobootIso = 1 in pcsx.ini on the emulator root.

    - Improvements:
        - Fixed sync game selected between cover modes.
        - Fixed profile menu setup, now every game profile setup is individual (as it was initialy supposed to).
        - Emulator assets are now packed into 'PsxSkin.xzp'.
        - Fixed LoadGameProfile at current selection, so you dont have to press Y button to load gamesettings for booting game profile correctly.
        - Fixed game profile loading after exit a game, to select new game to play.
        - Fixed shaders to re-add it into gameprofile settings, instead of another .ini file in gameshaders (since it doesnt make much sense).
        - Some code cleanups.
        
    - UI:
        - Added image for Devices.
        - Added psedo new OsdMenu.
        - New osdmenu ingame combo LB + RB + ABXY, now you dont need to change Freestyle Dash / Aurora screenshot combo anymore.

    - Regression/Freeze Fixes:
        - Fixed ui freeze (press LT+RT to get back to function properly before).
        - Fixed covermode initial value (cover modes freeze).

* Whats not included in this release yet for the lack of time/ not finished:
    - Html Game Guide.
    - Games sorting by first letter.
    - 4 player multitap support.
        
* Known Issues:
    - XUI Issue on osdmenu: if you autoboot psx.iso or load a rom from aurora, it kinda works. but it will open main scene first then you have to select a game and it will open osdmenu and resume the supposed action. after that you can use it normaly

v2.1.0
  ------
* 2 Variants
    - Base 2.1.0 version.
    - CTR-Fix version.

* Changelog:
    - Just one build, no more old and new cdr plugin builds, everthing is in a single default.xex.
    - Fixed text encoding issues on the end of the text, when the game guide is loaded (Byte order mark issues). 
        Still, remember to set any gameguide text on notepad to unicode big endian format (File->save as, then change from ansi to unicode big endian, then save the gameguide.txt).

    - Compatibillity
        - CDDA games are working fine and the compatibility was maintained (Noticiable in games like Dead or Alive Series).
        - Added cpu bias option. 
            Turning this option "on" will make the emulator run faster, setting the bias in the core to "3", but it will underclock the psx cpu. 
            It's good for some games that dont use the full psx power, most 2d games or some 3d games with less cpu demand like brigandine. 
            Heavy cpu games (tekken 2,3) will suffer from a lot of slowdowns.

    - UI
        - Added option to exit to dash on main menu (right thumb click button).
        - Added linear filter options (again).
        - Fixes the "B" (Back) button, now it correctly returns to the main menu. 
            On previous version, this button was used to load the profile settings, sorry for my stupidity :P.

    - Regression/Freeze Fixes:
        - Soul Calibur (when you finish the game).
        - Tomb Raider 3 (when entering on ingame menu and try to return to the game again).
        - Brave Fencer Musashi (voices).
        - Valkirie Profile (BGM).
        - Front Mission 3 (Random freezes in the main menu and during battles, when your wanzer or the enemy wanzer has the legs smashed).

v2.0.9
------
* 2 Variants:
    - Old CDR Plugin.
    - New CDR Plugin.

* Changelog:
    - New shaders by retroarch added (new hls folder).
    - Virtual Memory was removed (VM broke some games).
    - Fix on SPU caused a overall improvement on sound effects for all games (Noticiable in games like Ridge Race Type 4 / Megamen X Series and others).
    - Fix some gameguide problems
    - Fix on PPC Dynarec from the PCSX Reloaded source code.
