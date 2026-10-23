Primera build pública de prueba del port de Pokemon Uranium 1.4.1 a mkxp-z.

QUE ES
------
Port no oficial de Pokemon Uranium 1.4.1 al motor mkxp-z 2.4.2 (64 bits, Ruby 3.1).
No se modifico ningun dato del juego: mapas, eventos, graficos y audio son los
originales. Solo se adaptaron los scripts para que corran en Ruby 3.1 y en un motor de
64 bits.

El archivo no incluye assets del juego. Necesitas tu propia instalacion de Pokemon
Uranium 1.4.1.


INSTALACION
-----------
1. Descarga Pokemon-Uranium-MKXP-Z-v01.zip (13,5 MB).
2. Extraelo en la carpeta que contiene Uranium.exe, Uranium.rgssad, Audio/, Graphics/
   y Fonts/.
3. Reemplaza Uranium.ini cuando lo pregunte. El zip crea la carpeta Data/.
4. Ejecuta mkxp-z.exe (NO Uranium.exe).


REQUISITOS
----------
- Windows 10/11 de 64 bits.
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


SHA256 (zip)
------------
2060AAD8911F3E5BC81F8621665DCE00A07CCAD00E4CCDBC49523EAB8325FB0A


CREDITOS
--------
Pokemon Uranium: ~JV~, Involuntary Twitch y el Uranium Team. mkxp-z: Ancurio y
contribuidores (GPLv2+). Este port es no oficial y no esta afiliado a los autores
originales.

English README: https://github.com/iKamus/pokemon-uranium-mkxp/blob/main/README.en.md
