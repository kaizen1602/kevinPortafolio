# Portafolio — Kevin Uribe

Currículum / portafolio web de **Kevin Uribe — Desarrollador Full-Stack**.
Una sola página (`index.html`) con efectos, animaciones y transiciones. **Sin build, sin dependencias.** Solo HTML + CSS + JS vanilla.

## Estructura

```
portfolio/
├── index.html          ← el sitio completo (todo embebido)
├── assets/img/         ← foto + capturas de proyectos
├── netlify.toml        ← config para Netlify
├── vercel.json         ← config para Vercel
└── README.md
```

## Ver localmente

Abre `index.html` directo en el navegador (doble clic), **o** sirve la carpeta para que carguen bien las imágenes:

```powershell
# Opción A — Python
python -m http.server 8080
# Opción B — Node
npx serve .
```
Luego abre http://localhost:8080

## Desplegar (3 opciones, todas gratis)

### 1. Netlify (más rápido — arrastrar y soltar)
1. Entra a https://app.netlify.com/drop
2. Arrastra **toda la carpeta `portfolio/`**.
3. Listo. Te da una URL pública al instante. Conecta tu dominio en *Site settings → Domain*.

### 2. Vercel
```powershell
npm i -g vercel
vercel        # dentro de la carpeta portfolio/
```
Sigue el prompt. `vercel --prod` para producción.

### 3. GitHub Pages
1. Sube el contenido de `portfolio/` a un repo.
2. *Settings → Pages → Branch: main / root*.
3. Tu sitio queda en `https://<usuario>.github.io/<repo>/`.

## Personalizar

| Qué | Dónde |
|-----|-------|
| Email / WhatsApp / GitHub | bloque `.socials` y sección `#contacto` en `index.html` |
| Textos de proyectos | `<article class="proj">` dentro de `#proyectos` |
| Capturas | reemplaza archivos en `assets/img/` (mismo nombre) |
| Colores de acento por proyecto | atributo `style="--c:...;--c2:..."` en cada `.proj` |
| Roles del efecto typing | array `roles` en el `<script>` |

## Notas
- Los proyectos internos (AppVisitas, Altius, SuperEdu) están marcados como *Red interna corporativa* — sin enlace público. Si tienes demo pública, cambia el `<a class="proj-link muted">` por un enlace real.
- Las capturas de SuperEdu llevan blur en nombres de empleados y marca del cliente (datos personales / cliente anonimizado en el portafolio).
