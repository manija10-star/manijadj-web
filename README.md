# manijadj.com

Web oficial de **MANIJA** (Gabriel Giraldi), DJ residente en Crush · Alicante.
Publicada en **https://manijadj.com**.

## Estructura

```
index.html   → toda la web (HTML + CSS + JS en un solo archivo, sin dependencias ni build)
img/         → fotos ya optimizadas para web (~1400 px, JPG calidad 80)
video/       → (opcional) hero.mp4 para la portada; si no existe, se muestra img/hero.jpg
```

- Es una web estática: no hay framework, ni npm, ni paso de compilación.
- Para verla en local basta con abrir `index.html` en el navegador, o servir la carpeta con cualquier servidor estático (por ejemplo `npx serve .` o `python -m http.server`).

## Cómo funciona

- **Portada** (`.home`): foto a pantalla completa, nombre arriba, lema y menú abajo.
- **Secciones** (`.panel`): Sesiones, Fechas, Galería, Bio y Booking. Cada una se abre como capa a pantalla completa según el `#hash` de la URL (`#sesiones`, `#fechas`, …). La lógica está en el `<script>` al final de `index.html`.
- **Vídeos**: se cargan desde YouTube (youtube-nocookie) solo al pulsar play.
- **Tipografías** (Google Fonts): Montserrat (textos y nombre) y Herr Von Muellerhoff (lema en caligrafía).

## Reglas de marca (importante)

- MANIJA es **"una experiencia, no un género"**: no etiquetar la música con subgéneros concretos (nada de "deep house", "tech house", etc.).
- Lema: **"la música fluye, la pista decide..."**, siempre en minúsculas y en la caligrafía Herr Von Muellerhoff.
- Paleta sobria: negro (`#0a0a0a`), blanco roto (`#ececec`) y un único acento dorado tenue (`#e8c48e`).
- La foto de portada debe dejar la **cara visible**: el nombre va encima de la cabeza y el lema debajo.

## Cómo proponer cambios

La rama `main` está protegida: **nadie puede subir cambios directamente**.

1. Haz un *fork* del repositorio (o crea una rama si tienes acceso).
2. Haz tus cambios y abre un **Pull Request** hacia `main`, explicando qué has cambiado y por qué (con capturas si es algo visual).
3. El propietario revisa el Pull Request y, si está bien, lo aprueba y lo une a `main`.

## Publicación

La web está alojada en **Netlify** (proyecto `manijadj`). Los cambios **no se publican solos**: después de aprobar un Pull Request, el propietario sube la versión nueva a Netlify.

## Pendiente

- En la portada, que la palabra **"Crush"** de *"DJ residente en Crush · Alicante"* sea un enlace a https://www.crushculture.es/es.
- Sustituir las fotos por las de la próxima sesión de estudio (portada horizontal con espacio sobre la cabeza + versión vertical para móvil).
