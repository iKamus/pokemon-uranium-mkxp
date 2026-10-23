# Pokémon Uranium on mkxp-z

[Español](README.md) · **English**

Unofficial port of **Pokémon Uranium 1.4.1** to the modern
[mkxp-z](https://github.com/mkxp-z/mkxp-z) 2.4.2 engine (Ruby 3.1), replacing the
original 32-bit RGSS player.

This repository only hosts the **release binaries**. It contains no game assets and no
source code; the port's source lives in a private repository.

## Requirements

- **Windows 10/11.** Pick the build that matches your system: x64 (64-bit) or x86 (32-bit).
- Your own **Pokémon Uranium 1.4.1** installation: `Uranium.rgssad`, `Audio/`,
  `Graphics/`, `Fonts/`. The game is not distributed here.

## Install

1. Download the build you need from [Releases](../../releases).
2. Extract it into the folder that contains `Uranium.exe`, `Uranium.rgssad`,
   `Audio/`, `Graphics/` and `Fonts/`.
3. Replace `Uranium.ini` when asked.
4. Run **`mkxp-z.exe`**, not `Uranium.exe`, which is the old 32-bit player.

| File | Purpose |
| --- | --- |
| `mkxp-z.exe` | engine |
| Ruby and zlib DLLs | engine runtime |
| `mkxp.json` | engine configuration |
| `Uranium.ini` | game configuration (the `Scripts=` line points at the port) |
| `Data/PortScripts.rxdata` | ported scripts |

Nothing else changes: maps, events, graphics and audio still come from your
`Uranium.rgssad`.

## Saves

Saves stay in `%USERPROFILE%\Saved Games\Pokemon Uranium`, the same folder the original
game uses, so an existing save is picked up automatically. We recommend backing it up
before the first run.

## Do not touch

- **`Uranium.rgssad`** holds the whole game. If it is deleted or renamed, nothing loads.
- **`mkxp.json`** says `execName: "Uranium"`. mkxp-z derives the `.ini` and `.rgssad`
  names from it; renaming it makes the game start with an error dialog.
- **`Uranium.ini`** line `Scripts=Data\PortScripts.rxdata`.

## Known warnings

These appear at startup and are harmless:

```
Primary font not found: Arial
No soundfont specified, sound might be mute
```

Exceptions, if any, are written to
`%USERPROFILE%\Saved Games\Pokemon Uranium\errorlog.txt`.

## Status

First public test build. The game boots and reads the original save. If something
breaks, report it with the contents of `errorlog.txt` and the steps that led to it.

## Credits

- **Pokémon Uranium**: ~JV~, Involuntary Twitch and the Uranium Team. All game content
  belongs to them.
- **mkxp-z**: Ancurio and the mkxp-z contributors. GPLv2+.

## License

Engine binaries are GPL (mkxp-z is GPLv2+). Game content and the original scripts remain
the property of the Uranium Team.
