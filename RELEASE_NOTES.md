First public test build of the Pokemon Uranium 1.4.1 port to mkxp-z.

WHAT IT IS
----------
Unofficial port of Pokemon Uranium 1.4.1 to mkxp-z 2.4.2 (64-bit, Ruby 3.1). No game
data was modified: maps, events, graphics and audio are the originals. Only the scripts
were adapted so they run on Ruby 3.1 and in a 64-bit engine.

The archive contains no game assets. You need your own Pokemon Uranium 1.4.1 install.


INSTALL
-------
1. Download Pokemon-Uranium-MKXP-Z-v01.zip (13.5 MB).
2. Extract it into the folder that contains Uranium.exe, Uranium.rgssad, Audio/,
   Graphics/ and Fonts/.
3. Replace Uranium.ini when asked. The zip creates Data/.
4. Run mkxp-z.exe (NOT Uranium.exe).


REQUIREMENTS
------------
- Windows 10/11, 64-bit.
- Pokemon Uranium 1.4.1.


SAVES
-----
Saves and settings stay in %USERPROFILE%\Saved Games\Pokemon Uranium, the same folder the
original game uses, so an existing save is picked up. Back it up first.


KNOWN WARNINGS
--------------
Harmless, printed at startup:

    Primary font not found: Arial
    No soundfont specified, sound might be mute

Exceptions go to %USERPROFILE%\Saved Games\Pokemon Uranium\errorlog.txt.


NOTES
-----
- Do not delete or rename Uranium.rgssad: it holds the whole game.
- Do not rename mkxp.json: it says execName "Uranium", and the engine derives the .ini
  and .rgssad names from it.
- First public test build: report what breaks, with errorlog.txt contents.


SHA256 (zip)
------------
2060AAD8911F3E5BC81F8621665DCE00A07CCAD00E4CCDBC49523EAB8325FB0A


CREDITS
-------
Pokemon Uranium: ~JV~, Involuntary Twitch and the Uranium Team. mkxp-z: Ancurio and
contributors (GPLv2+). This port is unofficial and not affiliated with the original
authors.

Espanol: https://github.com/iKamus/pokemon-uranium-mkxp/blob/main/README.es.md
