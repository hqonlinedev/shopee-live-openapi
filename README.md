# PIM API Docs

API documentation rendered with [Redoc](https://github.com/Redocly/redoc) and hosted on **GitHub Pages**.

## Live docs

Once GitHub Pages is enabled, the docs will be available at:

<https://hqonlinedev.github.io/pim-openapi/>

## Files

- [`swagger.pim.yaml`](swagger.pim.yaml) — PIM service OpenAPI specification
- [`index.html`](index.html) — Redoc renderer (entry point for GitHub Pages)

## Enable GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, choose the branch (e.g. `main`) and the `/ (root)` folder.
4. Save. GitHub Pages will publish `index.html` and serve `swagger.pim.yaml` alongside it.

## Local preview

Serve the folder with any static file server, e.g.:

```bash
npx http-server .
# or
python3 -m http.server 8080
```

Then open <http://localhost:8080>.

## Switching which spec is rendered

[`index.html`](index.html) loads `swagger.pim.yaml`. To render a different spec, change the `spec-url` attribute:

```html
<redoc spec-url="your-spec.yaml"></redoc>
```
