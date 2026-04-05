# LANDING-THOMAS

Sitio personal de **Thomas Gómez Serpa** (Física y Matemáticas, Universidad de los Andes): perfil, contenidos por categoría y contacto vía LinkedIn.

Aunque hoy el proyecto se sirve como **archivos HTML y CSS** (ideal para GitHub Pages u otro hosting estático), **el contenido no está congelado**: Thomas irá **actualizando tareas, apuntes, enlaces y demás materiales** editando las páginas en `contenidos/` y, cuando haga falta, la portada en `index.html`. Es un sitio **estático en la tecnología** (sin servidor propio obligatorio), pero **vivo en cuanto a contenido**.

## Estructura

| Ruta | Descripción |
|------|-------------|
| `index.html` | Página principal: hero, sobre mí, enlaces a contenidos, contacto |
| `css/site.css` | Estilos compartidos |
| `contenidos/` | Subpáginas por tipo: apuntes, tareas, código, programas-apps, poemas |
| `images/` | Imágenes del sitio (portada, biografía, etc.) |
| `logos/` | Logos Thomas / Ratabart666 |
| `robots.txt` / `sitemap.xml` | SEO y rastreo (URLs absolutas del sitio en producción) |

## Cómo actualizar contenido

1. Abre el HTML correspondiente, por ejemplo `contenidos/tareas.html`.
2. Sustituye el bloque `.content-placeholder` por listas, enlaces, párrafos o secciones nuevas.
3. Opcional: actualiza la fecha en `sitemap.xml` (`<lastmod>`) en las URLs que cambien.
4. Haz commit y push a la rama que uses en producción (p. ej. `main`).

Si más adelante se añade un generador de sitios, un CMS o otra capa dinámica, este README puede ampliarse con esos pasos.

## Vista local

Abre `index.html` en el navegador o sirve la carpeta con un servidor local, por ejemplo:

```bash
npx --yes serve .
```

Así las rutas relativas (`css/`, `contenidos/`) se comportan igual que en el servidor.

## Publicación

**Producción (Netlify):** [https://ratabart666.netlify.app/](https://ratabart666.netlify.app/) — despliegue conectado al repositorio; cada push a `main` puede disparar un nuevo build si está configurado.

**Repositorio:** el código vive en GitHub (`LANDING-THOMAS`). Si además quieres **GitHub Pages**, en el repo: **Settings → Pages** → rama `main`, carpeta `/ (root)`; entonces habría que alinear `canonical`, Open Graph, `sitemap.xml` y `robots.txt` con la URL `*.github.io` o usar un dominio personalizado coherente en todos los archivos.

Si cambias de dominio (Netlify custom domain u otro), actualiza las mismas URLs absolutas en `index.html`, `contenidos/*.html`, `sitemap.xml` y `robots.txt`.

## Licencia y créditos

Contenido y marca personal de Thomas Gómez Serpa. Los logos de terceros conservan sus respectivos derechos.
