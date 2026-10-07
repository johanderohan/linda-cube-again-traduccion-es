# Linda³ Again — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/playstation/linda-cube-again)**.

Traducción al **español de España** de *Linda³ Again* (リンダキューブ アゲイン, PlayStation, 1997),
el RPG de captura de animales de Alfa System y Shoji Masuda, que nunca salió de Japón.

La traducción se distribuye como **parche**. No incluye el juego: necesitas tu propia copia
japonesa para aplicarlo.

## Estado

Última versión: **[v1.0](../../releases/tag/v1.0)**, la primera.

| Parte | Estado |
|---|---|
| Guion de los tres escenarios (A, B y C) y mensajes de los mapas | 6.156 mensajes traducidos |
| Menús, objetos, animales, equipo, técnicas, lugares y avisos del sistema | 1.177 textos traducidos |
| Combate (mensajes, órdenes, estados) | Traducido |
| Pantalla de nombre | Teclado silábico en castellano, con tildes y ñ |
| Rótulos dibujados (libreta del banco, carteles, créditos de la introducción, textos del final, tablas del reñidero) | 31 imágenes redibujadas |
| Rótulos de estadísticas de la fuente pequeña | «Atq.», «Def.», «Vel.» |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « »** |
| Revisión durante una partida | Parcial (ver abajo) |

Detalles técnicos:

- Fuente nueva de ancho variable, con dígrafos para que el texto quepa donde el juego lo carga, y
  con el mismo color y trazo que la original.
- Las ventanas que se ajustan al texto miden lo justo, como en el original.
- Los nombres que escribes con el teclado se guardan de forma estable: las partidas de la tarjeta
  de memoria seguirán sirviendo con versiones futuras del parche.

Se quedan como en el original:

- El logotipo del título y los créditos finales del personal.
- La voz y los rótulos grabados dentro de los vídeos, que no llevan subtítulos.
- La crónica del epílogo, que el juego monta con piezas de palabras dibujadas.

### Comprobaciones y trabajo pendiente

Se ha jugado en emulador desde partida nueva en los tres escenarios:

- **Escenario A**: hasta la primera visita a Linda en Minago (cuartel, banco, reunión, registro
  de Ken como tripulante del Arca, combates, capturas y tiendas).
- **Escenario B**: hasta la escena del doctor Emori en Hospico (casa de Linda, iglesia, la noche
  del ataque y el laboratorio).
- **Escenario C**: hasta la primavera del segundo año, tras el coma de Ken.
- Además: título, selección de escenario y dificultad, todos los menús, teléfono, lotería, banco,
  tiendas, teclado de nombres, varios combates y guardar y cargar desde la tarjeta de memoria.

Una auditoría automática comprueba en cada versión los límites de memoria conocidos del juego
(tamaño de cada mapa, de cada mensaje y de la fuente) y los menús que podrían dejar el juego sin
respuesta. El parche se ha aplicado sobre el BIN japonés original y el resultado se ha comparado
byte a byte con la imagen probada.

**No se ha jugado una partida completa de principio a fin** ni se ha probado en consola real.
Las conversaciones nocturnas de la acampada, los finales y la mayor parte de la segunda mitad
de cada escenario no se han recorrido en las pruebas. La traducción y su revisión se han hecho
con asistencia de IA, sin revisores humanos independientes. Si encuentras un error, abre una
incidencia con una captura.

Limitaciones conocidas:

- Los perros de caza solo admiten nombres de dos sílabas del teclado (el juego guarda 4 bytes por
  nombre): «Luna», «Toby», «Max»… Las especies nuevas y la hija admiten cuatro.
- En las opciones de una misma línea, el recuadro del cursor tapa la barra «/» de al lado.
- Algunas cifras dentro de los diálogos usan la fuente pequeña, como en el original.
- Los estados guardados del emulador (savestates) no sirven entre versiones del parche: usa la
  tarjeta de memoria del juego.

## Cambios

- **v1.0** (02-10-2026): primera versión.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia de **Linda³ Again (Japón) (Rev 1)**, SCPS-10039, en formato BIN/CUE de una
   sola pista.
3. **Comprueba que tu copia es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Linda^3 Again (Japan) (Rev 1).bin` |
   | Tamaño | 733.160.736 bytes |
   | MD5 | `71f138f8287ef3377c119116e0c44b7e` |

   ```bash
   md5sum "Linda^3 Again (Japan) (Rev 1).bin"            # Linux
   md5 "Linda^3 Again (Japan) (Rev 1).bin"               # macOS
   CertUtil -hashfile "Linda^3 Again (Japan) (Rev 1).bin" MD5   # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "original.bin" parche.xdelta "Linda3 Again (ES).bin"`
5. Comprueba que el BIN resultante tiene el MD5 **`23e31fdaed0da201cb198ad2ec216126`** (v1.0).
6. Crea un CUE para el nuevo BIN, por ejemplo `Linda3 Again (ES).cue`:

   ```
   FILE "Linda3 Again (ES).bin" BINARY
     TRACK 01 MODE2/2352
       INDEX 01 00:00:00
   ```

7. Carga el CUE en tu emulador y empieza una partida nueva.

Aplica el parche sobre el **BIN japonés original**, no sobre una copia ya parcheada.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación alguna
con Alfa System, MARS, NEC ni Sony. Aquí no se distribuye el juego ni ninguna parte de él: solo
un parche que modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo hago.
