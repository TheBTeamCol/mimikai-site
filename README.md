# mimikai-site

Sitio estático de Mimikai: landing, política de privacidad y soporte. Pensado para desplegarse con **GitHub Pages** (igual que `ayre-site`).

## Estructura

| Archivo | Descripción |
|---------|-------------|
| `index.html` | Landing del juego (hero, features, modos de juego). |
| `privacy.html` | Política de privacidad (la página que pide App Store / Play Store). |
| `support.html` | Página de soporte con preguntas frecuentes y contacto. |

Sin build ni dependencias: HTML + CSS inline. Se sirve tal cual.

## Deploy en GitHub Pages

1. Crear el repo en GitHub (público):

   ```bash
   gh repo create jssilva93/mimikai-site --public --source=. --remote=origin --push
   ```

   O manualmente: crear `jssilva93/mimikai-site` en GitHub y luego:

   ```bash
   git remote add origin https://github.com/jssilva93/mimikai-site.git
   git push -u origin main
   ```

2. En GitHub: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** / carpeta **/ (root)** → **Save**

3. El sitio queda disponible en:
   - `https://jssilva93.github.io/mimikai-site/`
   - Privacidad: `https://jssilva93.github.io/mimikai-site/privacy.html`
   - Soporte: `https://jssilva93.github.io/mimikai-site/support.html`

## Pendientes

- Confirmar si la app móvil usa analítica / reporte de crashes (Firebase Analytics, Crashlytics, etc.) y declararlo en `privacy.html` (hay un comentario `PENDIENTE DE CONFIRMAR` en el archivo).
- Reemplazar los enlaces `#` de los badges de tiendas en `index.html` cuando la app esté publicada.
