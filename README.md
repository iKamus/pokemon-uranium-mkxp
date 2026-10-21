# Pokémon Uranium on mkxp-z — builds

[Español](README.es.md) · **English**

Windows builds (x64 and 32-bit) of **Pokémon Uranium 1.4.0c** running on the modern
[mkxp-z](https://github.com/mkxp-z/mkxp-z) engine instead of the old RGSS player.

This repository only hosts the **release binaries**. It contains no game assets and
no source code.

## Requirements

- **Windows 10/11.** Use the `win64` archive on 64-bit Windows, `win32` on 32-bit.
- Your own copy of **Pokémon Uranium 1.4.0c** (the game's `Audio/`, `Graphics/`,
  `Fonts/` and `Data/` folders). The game is not distributed here.

## Install

1. Get a clean Pokémon Uranium 1.4.0c folder.
2. Download `uranium-mkxp-engine-win64.zip` (or `uranium-mkxp-engine-win32.zip`)
   from [Releases](../../releases).
3. Extract it **over** the game folder, replacing files when asked.
4. Run **`mkxp-z.exe`**.

The archive contains `mkxp-z.exe`, `x64-msvcrt-ruby310.dll` (`msvcrt-ruby310.dll` on
32-bit), `zlib1.dll`, `stdlib/`, `Data/Scripts.rxdata` and `mkxp.json`.

Saves live in `%USERPROFILE%\Saved Games\Pokemon Uranium`; engine settings in
`%APPDATA%\Pokemon Uranium\mkxp.json`.

## What's new

- **Gamepad works** — legacy save bindings are migrated to mkxp-z's controller codes
  and analog sticks get their defaults back.
- **No RGSS archive / no startup crash** on the save-folder lookup.
- **In-game engine settings** (see below).
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

## Engine options

Last five entries of the in-game *Options* menu. They are written to your user
`mkxp.json` and **read only at startup**, so restart the game to apply them. Delete
`%APPDATA%\Pokemon Uranium\mkxp.json` to reset everything.

| Option | Values | What it does |
| --- | --- | --- |
| **Frame Rate** | Monitor, 60, Off | Target frame rate. `Monitor` follows the screen refresh (mkxp-z forces VSync and reports the real refresh rate to the game). `60` caps at 60 fps. `Off` disables the frame limiter entirely — as fast as the machine allows. |
| **Smoothing** | Off, Bilinear, xBRZ | Filter used when upscaling. `Off` = crisp pixels, `Bilinear` = soft edges, `xBRZ` = smooths pixel art. |
| **Integer Scaling** | On, Off | Whole-number scaling so pixels stay even and sharp. Turn off only if you prefer stretching. |
| **FPS Counter** | On, Off | Average FPS in the window title (same as `F2`). |
| **Blit Mode** | On, Off | GPU blit path. Turn off only if text or tiles fail to render. |

### Recommended settings

| | Most faithful to the original | Smoothest on a modern PC |
| --- | --- | --- |
| Frame Rate | `60` | `Monitor` or `Off` |
| Smoothing | `Off` | `Off` or `Bilinear` |
| Integer Scaling | `On` | `On` |
| FPS Counter | `Off` | `Off` |
| Blit Mode | `On` | `On` |

**Important:** Uranium is frame-based, with no delta-time compensation. Raising the
frame rate speeds up the whole game (this is intended). The original ran at 40 fps;
`60` is 1.5x faster, `Monitor` on 144 Hz ~3.6x, `Off` as fast as the machine allows.

### Window size

*Options → Screen Size* (`S` / `M` / `L` / `F`) changes the window scale and
`Alt` + `Enter` toggles fullscreen. The game renders at 512×384, so larger windows
are upscaled; use *Integer Scaling* to keep pixels sharp.

## Credits

- **Pokémon Uranium** — ~JV~ and the Uranium Team. All game content belongs to them.
- **mkxp-z** — Ancurio and contributors, GPLv2+.
- **[warmwinter](https://codeberg.org/warmwinter/mkxp-z)** — the mkxp-z fork this
  port is built on.
- Port maintained by [@iKamus](https://github.com/iKamus).

## License

Engine binaries are GPL (mkxp-z is GPLv2+; built with HTTPS support, effectively
GPLv3). Game content and scripts remain the property of the Uranium Team.
