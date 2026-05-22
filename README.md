```
>_// MACHINEPUNK
[MP] // IDM_BREAK_HARD_TECHNO_ACID
```

# MACHINEPUNK

> `> señal_detectada`
> `> ejecutando_live_set...`

Landing page del live set **MACHINEPUNK**. Estética glitch / VHS / RGB-shift, tipografía pixel, scanlines y mensajes corruptos que se escriben solos.

```
ERES REMPLAZABLE,
YA EXISTE TU COPIA.
```

## Páginas

| Archivo | Qué es |
|---|---|
| `index.html` | Landing principal. Logo, tracks, equipo, mensajes. Botón oculto → `secret.html`. |
| `secret.html` | Pantalla intermedia. Toca la imagen → reproduce poema → redirige. |
| `track_el_encuentro.html` | Track destacado en loop, glitch de título + logos generados procedural. |

## Live set

```
> machine punk
> Speed Souls
> nothing love
> shy guy pill
> Ritual 393
> Plastic Face
> Drive
> Distinto y Distante
```

## Equipo

```
> mc-101
> TD-3-MO
> mini Kaoss pad
> tr-6s
> electribe
> polyend tracker
> zoom h5
```

## Stack

- HTML + CSS puro, sin frameworks.
- Animaciones CSS (glitch shift, scanlines, flicker, RGB drop-shadow, typewriter).
- Audio servido desde **jsDelivr CDN** (Neocities free no permite hostear audio).
- Tipografía `PixelOperator SC Bold`.

## Audio

Los MP3 viven en `assets/audio/` de este repo y se sirven vía:

```
https://cdn.jsdelivr.net/gh/anticuchito/machinepunk@main/assets/audio/<archivo>.mp3
```

| Archivo | Página | Peso |
|---|---|---|
| `drive.mp3` | `index.html` (SFX inicial) | 12K |
| `bgmusic.mp3` | `index.html` (loop) | 902K |
| `secret.mp3` | `secret.html` (poema) | 110K |
| `encuentro.mp3` | `track_el_encuentro.html` (track loop) | 2.2M |

> Si reemplazás un audio: jsDelivr cachea `@main` hasta 12h. Para invalidar al instante, pineá a un commit hash (ej. `@f17b9b9`).

## Local

Cualquier servidor estático sirve. Por ejemplo:

```sh
python3 -m http.server 8000
# http://localhost:8000
```

Abrir directo con `file://` también funciona, pero la fuente puede no cargar por la política de orígenes y los audios del CDN siguen requiriendo internet.

## Deploy (Neocities)

Subir todo **menos** los MP3 (vienen del CDN):

```
index.html
secret.html
track_el_encuentro.html
robots.txt
styles/styles.css
fonts/PixelOperatorSC-Bold.ttf
assets/logo_machine_punk1.png
assets/tag.png
assets/the_last_pixel.jpg
```

## Estructura

```
.
├── index.html
├── secret.html
├── track_el_encuentro.html
├── robots.txt
├── styles/
│   └── styles.css
├── fonts/
│   └── PixelOperatorSC-Bold.ttf
└── assets/
    ├── audio/         # MP3 servidos por jsDelivr
    ├── logo_machine_punk1.png
    ├── tag.png
    └── the_last_pixel.jpg
```

```
[SYSTEM_ACTIVE]
SIGNAL//ERROR//MP
>// MACHINEPUNK.exe
```
