# manijadj.com

Web oficial de **MANIJA** (Gabriel Giraldi), DJ residente en Crush · Alicante.
Publicada en **https://manijadj.com**.

## Estructura

```
index.html   → toda la web (HTML + CSS + JS en un solo archivo, sin dependencias ni build)
img/         → fotos optimizadas (JPG ~1400 px)
img/webp/    → versiones ligeras en WebP (si falta alguna, la web usa el JPG)
fonts/       → Montserrat y Herr Von Muellerhoff alojadas en la propia web (licencia SIL OFL, ver los .txt)
video/       → (opcional) hero.mp4 para la portada
```

- Es una web estática: no hay framework, ni npm, ni paso de compilación.
- Para verla en local: abre `index.html` en el navegador o sirve la carpeta con un servidor estático (`npx serve .` o `python -m http.server`).

## Cómo funciona

Una sola página con scroll: **Portada → El sonido (manifiesto) → Sesiones → Fechas → Galería → Bio → Booking**.

- **Portada**: foto a pantalla completa, nombre arriba, lema y menú abajo. "Crush" enlaza a https://www.crushculture.es/es.
- **Intro**: animación de entrada solo la primera vez por sesión (y nunca con "reducir movimiento").
- **Sesiones**: vídeo destacado con vinilo que gira al reproducir; el resto se abre en un reproductor tipo cine. Los vídeos (youtube-nocookie) solo se cargan al pulsar play.
- **Fechas**: cada fecha es un `<li data-date="AAAA-MM-DD">`. Las futuras pasan solas a "Próximas".
- **Galería**: tira horizontal en escritorio, deslizable con el dedo en móvil, visor con flechas y teclado.
- **Vídeo de portada**: sube `video/hero.mp4` y pon `data-video="video/hero.mp4"` en `<section class="hero">`.
- Accesibilidad: respeta "reducir movimiento", navegable con teclado, enlace "Saltar al contenido".

Decisiones tomadas: **sin cursor personalizado y sin grano de película** (se quitaron para mantener un estilo sobrio).

## Reglas de marca (importante)

- MANIJA es **"una experiencia, no un género"**: no etiquetar la música con subgéneros concretos (nada de "deep house", "tech house", etc.).
- Lema: **"la música fluye, la pista decide..."**, siempre en minúsculas y en la caligrafía Herr Von Muellerhoff.
- Paleta sobria: negro (`#0a0a0a`), blanco roto (`#ececec`) y un único acento dorado tenue (`#e8c48e`).
- La foto de portada debe dejar la **cara visible**: el nombre va encima de la cabeza y el lema debajo.
- No mostrar listas de fechas en los textos de la bio, ni la fecha de NEO DARK.

## Cómo proponer cambios

La rama `main` está protegida: **nadie puede subir cambios directamente**.

1. Haz un *fork* del repositorio (o crea una rama si tienes acceso).
2. Haz tus cambios y abre un **Pull Request** hacia `main`, explicando qué has cambiado y por qué (con capturas si es algo visual).
3. El propietario revisa el Pull Request y, si está bien, lo aprueba y lo une a `main`.

Por favor, envía los cambios siempre como Pull Request (no por ZIP) y no borres este README.

## Publicación

La web está alojada en **Netlify** (proyecto `manijadj`). Los cambios **no se publican solos**: después de aprobar un Pull Request, el propietario sube la versión nueva a Netlify.

## Pendiente

- Sustituir las fotos por las de la próxima sesión de estudio (portada horizontal con espacio sobre la cabeza + versión vertical para móvil).
