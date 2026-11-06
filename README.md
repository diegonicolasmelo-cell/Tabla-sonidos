# Tablero de Sonidos

Un tablero de botones grandes para eventos (baby shower, juegos, fiestas), pensado para el celular.

- **Efectos incluidos** (aplausos, redoble + platillo, fanfarria, bocina, ¡correcto!, error, trombón triste, cuenta regresiva, suspenso, ba-dum-tss, sonajero). Se generan en el propio navegador, suenan al instante y no necesitan internet.
- **Tus propios archivos de audio** (mp3, m4a, wav). Quedan guardados en el navegador del celular.
- **Botones de Spotify** (canción, playlist o álbum), con segundo de inicio opcional.
- Varios tableros, modo edición, botón **Detener todo**, volumen general y por botón, modos *una vez*, *encender/apagar* y *bucle*, pantalla siempre encendida, y respaldo copiar/pegar.

## Archivos

- `app.html`: el código del tablero (HTML, CSS y JS en un solo archivo).
- `index.html`: la misma página con su encabezado completo, lista para GitHub Pages. Se regenera así:

```sh
{ printf '<!doctype html>\n<html lang="es">\n<head>\n<meta charset="utf-8">\n<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">\n<meta name="theme-color" content="#13151c">\n<style>[hidden]{display:none!important}body{margin:0}</style>\n'; cat app.html; printf '\n</html>\n'; } > index.html
```

## Control directo de Spotify

Sin conexión, un botón de Spotify abre la canción en la app de Spotify. Conectado, el tablero le da play directamente a la app de Spotify del celular (requiere Premium):

1. Activa GitHub Pages en este repositorio (Settings → Pages → rama principal, carpeta raíz).
2. En <https://developer.spotify.com/dashboard> crea una app con “Web API” y agrega como Redirect URI la dirección exacta de la página (por ejemplo `https://<usuario>.github.io/Tabla-sonidos/`).
3. Abre la página en el celular → Ajustes → pega el Client ID → **Conectar Spotify**.
4. Ten la app de Spotify abierta (con algo reproducido alguna vez) para que aparezca como dispositivo.

## Notas

- En iPhone, si el interruptor de silencio está activado, los efectos pueden no sonar en Safari antiguos; sube el volumen y desactiva el modo silencio.
- Los parlantes Bluetooth agregan un pequeño retraso.
