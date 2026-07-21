# Beautified Esthetics

Static website for [Beautified Esthetics](https://beautifiedesthetics.com/) — an all-natural skincare clinic in Cary, NC — built as a single, dependency-free HTML page and hosted for free on GitHub Pages.

## What's here

- `index.html` — the entire site (HTML + CSS in one file, no build step, no JavaScript required)
- `.nojekyll` — tells GitHub Pages to serve files as-is

The only external dependency is Google Fonts (Fraunces + Outfit).

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `beautified-esthetics`).
2. Push this folder to it:

   ```sh
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/beautified-esthetics.git
   git push -u origin main
   ```

3. On GitHub, go to **Settings → Pages**, set **Source** to "Deploy from a branch", pick the `main` branch and `/ (root)` folder, and save.
4. After a minute the site is live at `https://<your-username>.github.io/beautified-esthetics/`.

### Using the custom domain (beautifiedesthetics.com)

1. In **Settings → Pages → Custom domain**, enter `beautifiedesthetics.com` and save (this creates a `CNAME` file).
2. At the domain registrar, point the domain at GitHub Pages:
   - `A` records for the apex domain: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` → `<your-username>.github.io`
3. Back in the Pages settings, enable **Enforce HTTPS** once the certificate is issued.

## Updating content

Everything lives in `index.html`:

- **Prices / services** — edit the cards in the `<!-- Facials -->` section and the rows in the `<!-- Waxing & Body -->` section.
- **Hours or contact info** — edit the `<!-- Contact -->` section.
- **Booking link** — search for `squareup.com/appointments` and replace all occurrences if the Square link ever changes.
- **Photo** — the About section uses `nicole.jpeg`. To swap it, replace that file (keeping the name) or update the `<img>` tag's `src` in the About section.

Commit and push — GitHub Pages redeploys automatically.
