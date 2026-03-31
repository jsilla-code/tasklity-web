# Tasklity — Web de apps para el día a día

Repositorio oficial de **Tasklity**, página web que aloja herramientas gratuitas e instalables.

## Estructura del repositorio

```
tasklity-web/
├── index.html          ← Página principal (diseño y buscador)
├── _redirects          ← Reglas de enrutamiento para Netlify
├── netlify.toml        ← Configuración de Netlify (cabeceras, caché)
├── README.md           ← Este archivo
│
│   ── Las apps se añaden como subcarpetas ──
├── mis-vacaciones/     ← (añadir cuando esté lista)
│   ├── index.html
│   ├── manifest.json
│   ├── sw.js
│   └── icons/
└── taskflow/           ← (añadir cuando esté lista)
    ├── index.html
    ├── manifest.json
    ├── sw.js
    └── icons/
```

## Cómo añadir una nueva app

1. Crea una carpeta con el nombre de la app dentro del repo
2. Añade su `index.html`, `manifest.json`, `sw.js` e `icons/`
3. Descomenta (o añade) su ruta en `_redirects`
4. Añade su tarjeta en `index.html` (sección `#app-grid`)
5. Haz commit y push → Netlify despliega automáticamente

## Despliegue en Netlify

1. Conecta este repositorio en [app.netlify.com](https://app.netlify.com)
2. Build command: *(vacío)*
3. Publish directory: `.`
4. Para el dominio propio: **Site settings → Domain management → Add custom domain**

## Dominio propio

Desde el panel de tu proveedor de dominio, apunta los DNS a Netlify:

| Tipo  | Nombre | Valor                  |
|-------|--------|------------------------|
| A     | @      | 75.2.60.5              |
| CNAME | www    | [tu-sitio].netlify.app |

El SSL (HTTPS) lo gestiona Netlify automáticamente gratis.
