# Habita Madrid — sitio estático

Web estática de Habita Madrid, lista para publicar en **GitHub Pages**.

## Estructura

```text
index.html          Página única: portada, impacto social, formulario de 6 pasos (ES/EN)
assets/img/         Imágenes (sol.jpg, desahucio.jpg, vacias.jpg, bot.png)
.nojekyll           Evita que Jekyll procese el sitio en GitHub Pages
```

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `habita-madrid`) y sube estos archivos.
2. En el repositorio: **Settings → Pages → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`.
3. La web quedará en `https://<tu-usuario>.github.io/habita-madrid/`.

Las rutas de las imágenes son relativas (`assets/img/...`), así que funcionan tanto en la raíz como en un subpath de GitHub Pages.

## Webhook de Make

El formulario envía todos los campos en JSON (POST) al webhook de Make configurado en `index.html` (constante `MAKE_WEBHOOK_URL`). Al ser un sitio estático, la URL del webhook es visible en el código fuente: es un webhook público de Make, pero conviene no compartirla fuera del equipo y rotarla si se detecta abuso.

## Contenido generado con IA

Todas las imágenes de `assets/img/` están generadas con IA y llevan el pie visible «Contenido generado con IA» / «AI-generated content» en la página.
