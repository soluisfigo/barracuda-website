# Barracuda Advertising — Landing Page

Sitio web estático de Barracuda Advertising, listo para deploy en GitHub Pages.

## Deploy en GitHub Pages

1. Crea un repositorio en GitHub (ej. `barracuda-website`)
2. Sube estos archivos al repositorio:
   ```bash
   git init
   git add .
   git commit -m "Initial commit - landing page"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/barracuda-website.git
   git push -u origin main
   ```
3. Ve a **Settings → Pages** en tu repositorio
4. En **Source**, selecciona `main` branch y carpeta `/ (root)`
5. Guarda y espera ~1 minuto. Tu sitio estará en `https://TU_USUARIO.github.io/barracuda-website/`

## Dominio personalizado

Para usar `www.barracudaadvertising.com`:

1. En GitHub → Settings → Pages → Custom domain, escribe `www.barracudaadvertising.com`
2. En tu proveedor de DNS, agrega un registro CNAME:
   - **Host:** `www`
   - **Valor:** `TU_USUARIO.github.io`
3. Para el dominio raíz (`barracudaadvertising.com`), agrega registros A apuntando a las IPs de GitHub Pages:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

## Agregar el video de IA (4to video)

En `index.html`, busca el comentario `VIDEO 4` y:
1. Elimina el `<div class="video-placeholder">...</div>`
2. Descomenta la línea del iframe
3. Reemplaza `VIDEO_ID_AQUI` con el ID del video de YouTube

## Hacer cambios con GitHub + Claude

Una vez que el repo esté configurado, puedes pedirle a Claude que haga cambios directamente en el código del repositorio. Los cambios se desplegarán automáticamente en GitHub Pages.

## Estructura del proyecto

```
/
├── index.html    ← Landing page completa (HTML + CSS + JS en un solo archivo)
├── CNAME         ← Dominio personalizado para GitHub Pages
└── README.md     ← Este archivo
```

## Tecnologías

- HTML5 semántico
- CSS3 (variables, grid, flexbox, animaciones)
- JavaScript vanilla (scroll reveal, navbar, mobile menu)
- Google Fonts (Roboto)
- Sin dependencias ni frameworks — carga ultra rápida
