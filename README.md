# Simulaciones de flujos ambientales

Videos complementarios de las simulaciones numéricas de **Tim Redel** (Departamento de Ingeniería Hidráulica y Ambiental, Pontificia Universidad Católica de Chile). El sitio se publica con GitHub Pages desde `index.html`.

## Proyectos

| Proyecto | Descripción | Videos |
|---|---|---|
| **Plumas subglaciales y cuña salina** | DNS de la descarga subglacial de agua dulce en un tanque de agua salada: cuña salina bajo el hielo y pluma en el frente. | [`videos/subglacial`](videos/subglacial/) |
| **Sedimentación convectiva en plumas fluviales** | Plumas fluviales con sedimentos que descargan en agua salada (CTR Summer Program 2026, Stanford). | [`videos/ctr`](videos/ctr/) |
| **Casos adicionales: mezcla turbulenta** | Flujos de referencia: mezcla por corte (Kelvin–Helmholtz) y por convección (Rayleigh–Bénard). | [`videos/mezcla`](videos/mezcla/) |
| **Quebrada Honda** | Respuesta lluvia-escorrentía de la cuenca durante la crecida del 8 de octubre de 2026 (modelo ATS). | [`videos/honda`](videos/honda/) |

Cada carpeta de videos tiene su propio `README.md` con la descripción de cada simulación.

## Estructura

```
index.html        página principal
thumbs/           imagen de vista previa de cada video
videos/
  subglacial/     plumas subglaciales (2D y 3D)
  ctr/            plumas fluviales con sedimentos
  mezcla/         casos de referencia de mezcla turbulenta
  honda/          Quebrada Honda (ATS)
```

## Publicar con GitHub Pages

1. Subir el contenido de esta carpeta a un repositorio público.
2. En el repositorio: **Settings → Pages → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`.
3. El sitio queda en `https://<usuario>.github.io/<repositorio>/`. Cada proyecto tiene su enlace directo, por ejemplo `#subglacial`.

## Agregar un video

1. Copiar el `.mp4` (H.264) en la carpeta del proyecto.
2. Crear su vista previa: `ffmpeg -ss 10 -i video.mp4 -frames:v 1 -vf scale=900:-2 thumbs/video.jpg`.
3. Agregar una tarjeta en `index.html` y una fila en el `README.md` de la carpeta.

Contacto: tredel@uc.cl
