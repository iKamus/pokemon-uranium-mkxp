# Pokémon Uranium on mkxp-z — builds

Windows x64 builds of **Pokémon Uranium 1.4.0c** running on the modern
[mkxp-z](https://github.com/mkxp-z/mkxp-z) engine instead of the old RGSS player.

This repository only hosts the **release binaries**. It contains no game assets
and no source code.

## Requirements

- **Windows 10/11, 64-bit.**
- Your own copy of **Pokémon Uranium 1.4.0c** (the game's `Audio/`, `Graphics/`,
  `Fonts/` and `Data/` folders). The game is not distributed here.

## Install

1. Get a clean Pokémon Uranium 1.4.0c folder.
2. Download `uranium-mkxp-engine-win64.zip` from
   [Releases](../../releases).
3. Extract it **over** the game folder, replacing files when asked.
4. Run **`mkxp-z.exe`**.

The archive contains:

```
mkxp-z.exe                  engine
x64-msvcrt-ruby310.dll      Ruby 3.1 runtime
zlib1.dll
stdlib/                     Ruby standard library
Data/Scripts.rxdata         compiled game scripts (required to run)
mkxp.json                   engine configuration for this port
```

Saves live in `%USERPROFILE%\Saved Games\Pokemon Uranium`; engine settings in
`%APPDATA%\Pokemon Uranium\mkxp.json`.

## What's new

- **Gamepad works** — legacy save bindings are migrated to mkxp-z's controller
  codes and analog sticks get their defaults back.
- **No RGSS archive / no startup crash** on the save-folder lookup.
- **In-game engine settings** — *Options* exposes frame rate (Monitor / 40 / 60 /
  120 / 144), smoothing, integer scaling, FPS counter and blit mode. Changes are
  written to your user `mkxp.json` and apply after a restart.
- **Rebindable controls** — *Options → Set Controls*, keyboard and gamepad.
- **Scaling** — integer scaling and smoothing for high-resolution displays.

## Controls

| | |
| --- | --- |
| Move / confirm / cancel | keyboard and gamepad (rebindable) |
| `Alt` + `Enter` | toggle fullscreen |
| `F2` | toggle FPS display |
| `F8` | screenshot |
| `F12` | reset the game |

## Credits

- **Pokémon Uranium** — ~JV~ and the Uranium Team. All game content belongs to them.
- **mkxp-z** — Ancurio and contributors, GPLv2+.
- **[warmwinter](https://codeberg.org/warmwinter/mkxp-z)** — the mkxp-z fork this
  port is built on.
- Port maintained by [@iKamus](https://github.com/iKamus).

## License

Engine binaries are GPL (mkxp-z is GPLv2+; built with HTTPS support, effectively
GPLv3). Game content and scripts remain the property of the Uranium Team.
