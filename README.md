# mimikai-site

Sitio estático de Mimikai: landing, política de privacidad y soporte. Pensado para desplegarse con **GitHub Pages** (igual que `ayre-site`).

## Estructura

| Archivo | Descripción |
|---------|-------------|
| `index.html` | Landing del juego (hero, features, modos de juego). |
| `privacy.html` | Política de privacidad (la página que pide App Store / Play Store). |
| `terms.html` | Términos y condiciones / EULA. |
| `support.html` | Página de soporte con preguntas frecuentes y contacto. |

Sin build ni dependencias: HTML + CSS inline. Se sirve tal cual.

## Deploy en GitHub Pages

> En el plan **free** de la organización, GitHub Pages solo funciona en repos **públicos**. Una política de privacidad debe ser pública de todos modos, así que el repo se crea público.

1. Crear el repo en GitHub (público):

   ```bash
   gh repo create TheBTeamCol/mimikai-site --public --source=. --remote=origin --push
   ```

   O manualmente: crear `TheBTeamCol/mimikai-site` en GitHub y luego:

   ```bash
   git remote add origin https://github.com/TheBTeamCol/mimikai-site.git
   git push -u origin main
   ```

2. En GitHub: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** / carpeta **/ (root)** → **Save**

3. El sitio queda disponible en:
   - `https://thebteamcol.github.io/mimikai-site/`
   - Privacidad: `https://thebteamcol.github.io/mimikai-site/privacy.html`
   - Términos: `https://thebteamcol.github.io/mimikai-site/terms.html`
   - Soporte: `https://thebteamcol.github.io/mimikai-site/support.html`

## Pendientes

- Reemplazar los enlaces `#` de los badges de tiendas en `index.html` cuando la app esté publicada.
- Si la app móvil añade analítica, crash reporting (p. ej. Firebase Crashlytics) o suscripciones, actualizar `privacy.html` y `support.html`.
