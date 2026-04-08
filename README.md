# AZGU (Stitch AI export) — single page build

This repo contains a **single-page** HTML build assembled from multiple Stitch AI exports.

## Run locally

Open `index.html` in a browser.

Optional (recommended) local server:

```bash
python -m http.server 5173
```

Then open `http://localhost:5173/`.

## Navigation

The app uses hash routes:

- `#home`
- `#menu`
- `#meal`
- `#cart`

## Deploy on GitHub Pages

1. Create a new GitHub repository (empty).
2. Push this folder to GitHub.
3. In GitHub: **Settings → Pages**:
   - Source: `Deploy from a branch`
   - Branch: `main` / `(root)`

Because the entrypoint is `index.html` in the repository root, Pages will work without extra config.
