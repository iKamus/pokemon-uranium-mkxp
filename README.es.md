# Pokémon Uranium en mkxp-z — builds

**Español** · [English](README.md)

Builds de Windows (x64 y 32 bits) de **Pokémon Uranium 1.4.0c** corriendo sobre el
motor moderno [mkxp-z](https://github.com/mkxp-z/mkxp-z) en lugar del viejo
reproductor RGSS.

Este repositorio solo aloja los **binarios de release**. No contiene assets del
juego ni código fuente.

## Requisitos

- **Windows 10/11.** Usa el archivo `win64` en Windows de 64 bits y `win32` en 32 bits.
- Tu propia copia de **Pokémon Uranium 1.4.0c** (las carpetas `Audio/`, `Graphics/`,
  `Fonts/` y `Data/`). El juego no se distribuye aquí.

## Instalación

1. Consigue una carpeta limpia de Pokémon Uranium 1.4.0c.
2. Descarga `uranium-mkxp-engine-win64.zip` (o `uranium-mkxp-engine-win32.zip`) desde
   [Releases](../../releases).
3. Extráelo **sobre** la carpeta del juego, reemplazando archivos cuando lo pregunte.
4. Ejecuta **`mkxp-z.exe`**.

El archivo contiene `mkxp-z.exe`, `x64-msvcrt-ruby310.dll` (`msvcrt-ruby310.dll` en
32 bits), `zlib1.dll`, `stdlib/`, `Data/Scripts.rxdata` y `mkxp.json`.

Las partidas están en `%USERPROFILE%\Saved Games\Pokemon Uranium` y las opciones del
motor en `%APPDATA%\Pokemon Uranium\mkxp.json`.

## Novedades

- **El gamepad funciona**: las partidas viejas migran sus botones a los códigos de
  mkxp-z y los sticks recuperan sus valores por defecto.
- **Sin archivo RGSS y sin cierre inesperado** al resolver la carpeta de partidas.
- **Opciones del motor dentro del juego** (ver abajo).
- **Controles reasignables** en *Options → Set Controls*, teclado y gamepad.
- **Escalado** con integer scaling y suavizado para pantallas de alta resolución.

## Controles

| | |
| --- | --- |
| Mover / confirmar / cancelar | teclado y gamepad (reasignables) |
| `Alt` + `Enter` | pantalla completa |
| `F2` | muestra u oculta los FPS |
| `F8` | captura de pantalla |
| `F12` | reinicia el juego |

## Opciones del motor

Son las últimas cinco entradas del menú *Options* del juego. Se guardan en tu
`mkxp.json` de usuario y **se leen solo al arrancar**, así que reinicia el juego para
aplicarlas. Para volver todo atrás, borra `%APPDATA%\Pokemon Uranium\mkxp.json`.

| Opción | Valores | Qué hace |
| --- | --- | --- |
| **Frame Rate** | Monitor, 60, Off | Cuadros por segundo objetivo. `Monitor` sigue la frecuencia del monitor (mkxp-z fuerza VSync y le informa al juego la frecuencia real). `60` limita a 60 fps. `Off` desactiva por completo el limitador: tan rápido como permita la máquina. |
| **Smoothing** | Off, Bilinear, xBRZ | Filtro al escalar la imagen. `Off` = píxeles nítidos, `Bilinear` = bordes suaves, `xBRZ` = suaviza el pixel art. |
| **Integer Scaling** | On, Off | Escala por números enteros para que los píxeles queden parejos y nítidos. Desactívalo solo si prefieres estirar la imagen. |
| **FPS Counter** | On, Off | FPS promedio en el título de la ventana (igual que `F2`). |
| **Blit Mode** | On, Off | Ruta de blit por GPU. Desactívalo solo si el texto o los tiles no se dibujan. |

### Ajustes recomendados

| | Lo más fiel al original | Lo más fluido en un PC moderno |
| --- | --- | --- |
| Frame Rate | `60` | `Monitor` u `Off` |
| Smoothing | `Off` | `Off` o `Bilinear` |
| Integer Scaling | `On` | `On` |
| FPS Counter | `Off` | `Off` |
| Blit Mode | `On` | `On` |

**Importante:** Uranium está hecho por cuadros, sin compensación de tiempo. Subir el
frame rate acelera todo el juego (es lo buscado). El original corría a 40 fps; `60` es
1,5 veces más rápido, `Monitor` en 144 Hz unas 3,6 veces, y `Off` tan rápido como
permita la máquina.

### Tamaño de ventana

*Options → Screen Size* (`S` / `M` / `L` / `F`) cambia la escala de la ventana y
`Alt` + `Enter` alterna pantalla completa. El juego se renderiza a 512×384, así que
las ventanas más grandes son un escalado: usa *Integer Scaling* para mantener los
píxeles nítidos.

## Créditos

- **Pokémon Uranium** — ~JV~ y el Uranium Team. Todo el contenido del juego es suyo.
- **mkxp-z** — Ancurio y contribuidores, GPLv2+.
- **[warmwinter](https://codeberg.org/warmwinter/mkxp-z)** — el fork de mkxp-z sobre
  el que se construye este port.
- Port mantenido por [@iKamus](https://github.com/iKamus).

## Licencia

Los binarios del motor son GPL (mkxp-z es GPLv2+; con soporte HTTPS, efectivamente
GPLv3). El contenido y los scripts del juego siguen siendo propiedad del Uranium Team.
