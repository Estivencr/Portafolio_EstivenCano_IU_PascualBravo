# Portafolio Estiven Cano — 2026-I

Portfolio académico del semestre 2026-I · Carrera Desarrollo de Software · Universidad Pascual Bravo

**Sitio desplegado:** https://estivencr.github.io/Portafolio_EstivenCano_IU_PascualBravo

---

## Stack

- [Jekyll](https://jekyllrb.com/) — generador de sitios estáticos
- [Bootstrap 5.3.3](https://getbootstrap.com/) — estilos y componentes
- [GLightbox 3.3.0](https://biati-digital.github.io/glightbox/) — galería de imágenes
- [GitHub Pages](https://pages.github.com/) — despliegue automático

---

## Requisitos previos

- Ruby >= 3.0
- Bundler (`gem install bundler`)

---

## Correr localmente

```bash
# 1. Instalar dependencias
bundle install

# 2. Levantar el servidor de desarrollo
bundle exec jekyll serve

# 3. Abrir en el navegador
# http://localhost:4000/Portafolio_EstivenCano_IU_PascualBravo/
```

Con live reload:

```bash
bundle exec jekyll serve --livereload
```

---

## Estructura del proyecto

```
portfolio-blog/
├── _config.yml               # Configuración de Jekyll y variables globales
├── _includes/                # Componentes reutilizables
│   ├── head.html             # Meta tags, fuentes, CDN
│   ├── nav.html              # Barra de navegación
│   ├── footer.html           # Pie de página
│   └── scripts.html          # Imports de JavaScript
├── _layouts/                 # Plantillas de página
│   ├── default.html          # Layout base
│   ├── blog.html             # Layout para entradas de blog
│   └── materia.html          # Layout para páginas de materia
├── _sass/                    # Estilos SCSS
├── assets/css/styles.scss    # Punto de entrada de estilos
├── img/                      # Imágenes del sitio
├── index.html                # Página principal
├── ingenieria-software/      # ISW-01 · Ingeniería de Software 1
├── herramientas-programacion/ # HDP-02 · Herramientas de Programación 3
├── programacion-movil/       # MOB-04 · Programación Móvil
├── redes-datos/              # RED-05 · Redes de Datos 1
└── seguridad-informatica/    # SEG-03 · Seguridad Informática
```

---

## Agregar una nueva entrada de blog

1. Crear un archivo `.html` dentro de la carpeta de la materia correspondiente.
2. Agregar el front matter con los campos requeridos:

```yaml
---
layout: blog
title: Título de la entrada
description: Descripción breve para SEO y Open Graph.
subject_code: ISW-01
subject_name: Ingeniería de Software 1
subject_url: /ingenieria-software/
blog_num: "II"
entry_type: Entrada de portafolio
year: 2026
exp_display: REQ
breadcrumb_current: Título corto
nav_back: Ingeniería de Software 1
nav_back_url: /ingenieria-software/
footer_label: "Ingeniería de Software 1 · ISW-01 · Blog No. II"
footer_link_text: "← Volver a la materia"
footer_link_url: /ingenieria-software/
image: /img/nombre-imagen.png   # opcional, para Open Graph
toc:
  - id: sec-1
    label: Primera sección
sidebar_entries:
  - title: Otra entrada
    url: /ingenieria-software/otra-entrada/
    num: "I"
---
```

3. Registrar la entrada en el `index.html` de la materia.

---

## Imágenes

- Formato preferido: **WebP** (mejor compresión que PNG/JPG)
- Ancho máximo: **1200px**
- Peso máximo recomendado: **150 KB** por imagen
- Guardar en `img/` con nombres en minúsculas y guiones (`mi-imagen.webp`)
- Para usar en un post, agregar `image: /img/nombre.webp` en el front matter

Convertir PNG/JPG a WebP:

```bash
# Con cwebp
cwebp -q 80 img/nombre.png -o img/nombre.webp

# Con ImageMagick
magick img/nombre.png -quality 80 img/nombre.webp
```

---

## Despliegue

El despliegue es automático via GitHub Pages al hacer push a la rama `main`.
