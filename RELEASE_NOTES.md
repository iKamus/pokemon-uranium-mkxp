Primera build pública de prueba del port de Pokemon Uranium 1.4.1 a mkxp-z.

QUE ES
------
Port no oficial de Pokemon Uranium 1.4.1 al motor mkxp-z 2.4.2 (Ruby 3.1), en
builds de 64 y 32 bits. No se modifico ningun dato del juego: mapas, eventos,
graficos y audio son los originales. Solo se adaptaron los scripts para que
corran en Ruby 3.1 y en el motor nuevo, en vez del reproductor RGSS de 32 bits.

El archivo no incluye assets del juego. Necesitas tu propia instalacion de Pokemon
Uranium 1.4.1.


INSTALACION
-----------
1. Descarga del [release](../../releases) el zip correspondiente a tu sistema:
   `Uranium-MKXPZ-Port-v0.1-win64.zip` (64 bits) o `Uranium-MKXPZ-Port-v0.1-win32.zip`
   (32 bits; tambien corre en 64). El motor es estatico: el zip no necesita DLLs.
2. Extraelo en la carpeta que contiene Uranium.exe, Uranium.rgssad, Audio/, Graphics/
   y Fonts/, manteniendo la estructura del zip.
3. Reemplaza Uranium.ini cuando lo pregunte. El zip crea la carpeta Data/.
4. Ejecuta mkxp-z.exe (NO Uranium.exe).


REQUISITOS
----------
- Windows 10/11, de 64 o 32 bits.
- Pokemon Uranium 1.4.1.


PARTIDAS
--------
Las partidas y la configuracion siguen en %USERPROFILE%\Saved Games\Pokemon Uranium, la
misma carpeta que usa el juego original, asi que la partida existente se toma sola.
Hace una copia de seguridad antes del primer arranque.


AVISOS CONOCIDOS
----------------
Inofensivos, aparecen al arrancar:

    Primary font not found: Arial
    No soundfont specified, sound might be mute

Las excepciones se escriben en %USERPROFILE%\Saved Games\Pokemon Uranium\errorlog.txt.


NOTAS
-----
- No borres ni renombres Uranium.rgssad: contiene todo el juego.
- No renombres mkxp.json: dice execName "Uranium", y el motor deriva de ahi el nombre del
  .ini y del .rgssad.
- Primera build publica de prueba: si algo falla, reportalo con el contenido de
  errorlog.txt y los pasos para reproducirlo.


SHA256
------
1CD12783D9ABB53B21E5BD0B4F123E8C31C5DBF347A46801056AAB567ED840F2  Uranium-MKXPZ-Port-v0.1-win64.zip
7CDFD7D143E6372E5372D7B60916A75F740B2B656AD5512281CA48C29051F33D  Uranium-MKXPZ-Port-v0.1-win32.zip

Verificacion de descarga: los mismos valores en el archivo SHA256SUMS.txt del release.


CREDITOS
--------
Pokemon Uranium: ~JV~, Involuntary Twitch y el Uranium Team. mkxp-z: Ancurio y
contribuidores (GPLv2+). Este port es no oficial y no esta afiliado a los autores
originales.

English README: https://github.com/iKamus/pokemon-uranium-mkxp/blob/main/README.en.md
