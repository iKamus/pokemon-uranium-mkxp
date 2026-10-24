# Pokémon Uranium en mkxp-z

**Español** · [English](README.en.md)

Port no oficial de **Pokémon Uranium 1.4.1** al motor
[mkxp-z](https://github.com/mkxp-z/mkxp-z) 2.4.2 (Ruby 3.1), en reemplazo del
reproductor RGSS de 32 bits original.

Este repositorio solo aloja los **binarios de release**. No contiene assets del juego ni
código fuente; el código del port vive en un repositorio privado.

## Requisitos

- **Windows 10/11.** Elegí la build que corresponda a tu sistema: x64 (64 bits) o x86 (32 bits).
- Tu propia instalación de **Pokémon Uranium 1.4.1**: `Uranium.rgssad`, `Audio/`,
  `Graphics/`, `Fonts/`. El juego no se distribuye acá.

## Instalación

1. Descargá la build que corresponda desde [Releases](../../releases).
2. Extraela en la carpeta que contiene `Uranium.exe`, `Uranium.rgssad`, `Audio/`,
   `Graphics/` y `Fonts/`.
3. Reemplazá `Uranium.ini` cuando lo pida.
4. Ejecutá **`mkxp-z.exe`**, no `Uranium.exe` (ese es el reproductor viejo de 32 bits).

| Archivo | Para qué |
| --- | --- |
| `mkxp-z.exe` | motor (estático: no necesita DLLs junto al exe) |
| `stdlib/` y `scripts/` | runtime de Ruby y helpers del motor |
| `mkxp.json` | configuración del motor |
| `Uranium.ini` | configuración del juego (la línea `Scripts=` apunta al port) |
| `Data/PortScripts.rxdata` | scripts del port |

Nada más cambia: mapas, eventos, gráficos y audio siguen saliendo de tu
`Uranium.rgssad`.

## Partidas

Las partidas siguen en `%USERPROFILE%\Saved Games\Pokemon Uranium`, la misma carpeta que
usa el juego original, así que la partida existente se toma sola. Te recomendamos hacer
una copia de seguridad antes del primer arranque.

## No tocar

- **`Uranium.rgssad`** contiene todo el juego. Si se borra o se renombra, no carga nada.
- **`mkxp.json`** dice `execName: "Uranium"`. mkxp-z deriva de ahí el nombre del `.ini` y
  del `.rgssad`; si se renombra, el juego arranca con un diálogo de error.
- **`Uranium.ini`**, línea `Scripts=Data\PortScripts.rxdata`.
- **`Data/PortScripts.rxdata`** son los scripts del port.

## Avisos conocidos

Aparecen al arrancar y son inofensivos:

```
Primary font not found: Arial
No soundfont specified, sound might be mute
```

Las excepciones, si las hay, se escriben en
`%USERPROFILE%\Saved Games\Pokemon Uranium\errorlog.txt`.

## Estado

Primera build pública de prueba. El juego arranca y lee la partida original. Si algo
falla, reportalo con el contenido de `errorlog.txt` y los pasos para reproducirlo.

## Créditos

- **Pokémon Uranium**: ~JV~, Involuntary Twitch y el Uranium Team. Todo el contenido del
  juego es suyo.
- **mkxp-z**: Ancurio y los contribuidores de mkxp-z. GPLv2+.

## Licencia

Los binarios del motor son GPL (mkxp-z es GPLv2+). El contenido y los scripts originales
del juego siguen siendo propiedad del Uranium Team.
