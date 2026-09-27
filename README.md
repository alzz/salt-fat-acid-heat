# Salt Fat Acid Heat

Find which salt, fat, acid and aromatics each cuisine cooks with.

**Live page → [alzz.github.io/salt-fat-acid-heat](https://alzz.github.io/salt-fat-acid-heat/)**

A single self-contained HTML page, in Spanish. No build step and no
dependencies; the only network request is for the Google Fonts. Open
`index.html` in a browser and it works.

## Usage

Use the [hosted page](https://alzz.github.io/salt-fat-acid-heat/), or run it
locally:

```
git clone git@github.com:alzz/salt-fat-acid-heat.git
cd salt-fat-acid-heat
xdg-open index.html      # or open, or just double-click it
```

## What it does

- **Buscar** — search an ingredient or a region.
- **Explorar** — browse by category, ingredient or region. An ingredient page
  lists the regions that use it; a region page lists its ingredients.
- **Ruedas** — one wheel per category, from the inside out: continent, region
  and ingredient. Tap any segment to open its page.

Every view has its own URL fragment (`#/explorar/regiones`, `#/ruedas/sabor`),
so links and the back button work.

## Hosting

Served by GitHub Pages straight from `main`, no build and no workflow: the whole
app is one file at the repository root, so pushing to `main` is the deploy.

Settings → Pages → Source **Deploy from a branch**, branch `main`, folder
`/ (root)`.

`.nojekyll` turns off the Jekyll build. Nothing here needs it, and without the
file a `{{` or `{%` inside the page's JavaScript would one day be read as a
Liquid tag and quietly mangled.

## License

MIT — see [LICENSE](LICENSE).
