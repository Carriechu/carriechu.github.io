# AGENTS.md

## Cursor Cloud specific instructions

This is a static Jekyll site (academic homepage) served via GitHub Pages.

### Project structure
- `index.html` — single-page site with inline CSS/JS
- `_config.yml` — Jekyll config; only plugin is `jekyll-sitemap`
- `robots.txt`, `photo.jpg`, and one PDF in the repo root

### Running locally
```bash
jekyll serve --host 0.0.0.0 --port 4000
```
This builds to `_site/` and starts a dev server with auto-regeneration. The `--detach` flag can be added for background mode.

### Lint / validation
No linter or test framework is configured in the repo. For ad-hoc HTML checks:
```bash
npx htmlhint index.html
```

### Notes
- `_site/` is the build output directory; it is regenerated on each `jekyll build` / `jekyll serve`.
- The `jekyll-sitemap` plugin auto-generates `sitemap.xml` in `_site/`.
- There are no environment variables, secrets, or external services required.
- System dependency: Ruby + `jekyll` and `jekyll-sitemap` gems must be installed (handled by the VM update script).
