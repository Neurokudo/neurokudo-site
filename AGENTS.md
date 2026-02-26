# AGENTS.md

## Cursor Cloud specific instructions

This is a static HTML/CSS/JS landing page with no build system, package manager, or backend. There are no dependencies to install.

### Running the site locally

```
python3 -m http.server 8000
```

Then open `http://localhost:8000/` in a browser.

### Project structure

- `index.html` — single-page landing (all HTML, CSS, and JS inline)
- `photo/` — static image assets (JPGs)
- `.github/workflows/deploy.yml` — CI/CD: deploys to Selectel S3 via `rclone` on push to `main`

### Notes

- No linter, test framework, or build step exists in this project. Validation is visual (open in browser).
- Deployment requires `S3_ACCESS_KEY_ID`, `S3_SECRET_ACCESS_KEY`, and `S3_BUCKET` GitHub secrets (not needed for local dev).
- Google Fonts are loaded from CDN; the page works offline but falls back to system fonts.
