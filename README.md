# 🎓 Portafolio Académico — GitHub Pages

Portafolio académico personal con entradas por materia, desplegado con GitHub Pages.

## 📁 Estructura de archivos

```
portfolio-blog/
│
├── index.html                        ← HOME principal
├── shared.css                        ← Estilos compartidos
│
├── ingenieria-software/
│   ├── index.html                    ← Portafolio de la materia
│   └── blog-requisitos.html          ← Blog: Identificación de Requisitos
│
├── herramientas-programacion/
│   └── index.html
│
├── seguridad-informatica/
│   └── index.html
│
├── programacion-movil/
│   └── index.html
│
└── redes-datos/
    └── index.html
```

---

## 🚀 Cómo publicar en GitHub Pages (paso a paso)

### Paso 1 — Crea el repositorio en GitHub

1. Ve a [github.com](https://github.com) e inicia sesión
2. Haz clic en **"New repository"** (botón verde)
3. Nombra el repositorio exactamente así:
   ```
   TU-USUARIO.github.io
   ```
   *(Reemplaza `TU-USUARIO` con tu nombre de usuario de GitHub)*
4. Marca **"Public"**
5. Haz clic en **"Create repository"**

---

### Paso 2 — Sube los archivos

#### Opción A — Desde el navegador (más fácil):
1. En tu repositorio recién creado, haz clic en **"uploading an existing file"**
2. Arrastra TODA la carpeta `portfolio-blog` (o selecciona todos los archivos)
3. Escribe un mensaje de commit: `Initial portfolio`
4. Haz clic en **"Commit changes"**

#### Opción B — Desde la terminal (recomendado):
```bash
# Clona el repositorio
git clone https://github.com/TU-USUARIO/TU-USUARIO.github.io.git

# Copia todos los archivos del portafolio dentro
cp -r portfolio-blog/* TU-USUARIO.github.io/

# Entra a la carpeta
cd TU-USUARIO.github.io

# Agrega todos los archivos
git add .

# Primer commit
git commit -m "🎓 Initial portfolio"

# Sube al repositorio
git push origin main
```

---

### Paso 3 — Activa GitHub Pages

1. Ve a tu repositorio en GitHub
2. Haz clic en **"Settings"** (pestaña superior)
3. En el menú izquierdo, haz clic en **"Pages"**
4. En **"Source"**, selecciona **"Deploy from a branch"**
5. En **"Branch"**, selecciona **"main"** y carpeta **"/ (root)"**
6. Haz clic en **"Save"**

---

### Paso 4 — ¡Listo! 🎉

Después de 1-2 minutos, tu blog estará disponible en:
```
https://TU-USUARIO.github.io
```

---

## ✏️ Cómo agregar nuevas entradas

### Para agregar un nuevo blog a una materia:

1. Crea un nuevo archivo HTML en la carpeta de la materia, por ejemplo:
   ```
   ingenieria-software/blog-ciclo-de-vida.html
   ```

2. Usa como base la estructura de `blog-requisitos.html`

3. En el `index.html` de la materia, agrega una nueva tarjeta:
   ```html
   <a href="blog-ciclo-de-vida.html" class="entry-card">
     <div class="entry-left">
       <span class="entry-index">02</span>
       <div class="entry-info">
         <h3>Modelos de Ciclo de Vida del Software</h3>
         <span>Blog · Proceso de Software · 2025</span>
       </div>
     </div>
     <span class="entry-arrow">→</span>
   </a>
   ```

4. Guarda, sube los cambios con git y GitHub Pages se actualiza automáticamente.

---

## 🎨 Personalización

- **Tu nombre:** Edita `index.html` y reemplaza "Portafolio Académico" por tu nombre
- **Colores por materia:** Cada `index.html` de materia tiene `--c: #COLOR` en el `<style>`
- **Descripción del hero:** Edita el párrafo `<p>` en cada página de materia

---

## 🌐 Dominio personalizado (opcional)

Si quieres usar `tunombre.dev` en lugar de `TU-USUARIO.github.io`:
1. Compra un dominio en [Namecheap](https://namecheap.com) (~$12/año para `.dev` o `.tech`)
2. En GitHub Pages Settings → Custom domain, escribe tu dominio
3. Configura los DNS de tu dominio apuntando a GitHub según la [documentación oficial](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
