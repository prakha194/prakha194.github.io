# Melzo at the root of prakha194.github.io

Why this exists: Google shows **one favicon and one site name per hostname**.
A project site like `prakha194.github.io/Melzo/` is a *subdirectory*, so Google
ignores its favicon and site name and uses the hostname's (currently the generic
"GitHub Pages documentation" + GitHub's icon). Claiming the hostname root fixes
both for every page under it, including `/Melzo/`.

## Steps (5 minutes, all in the browser)

1. Create a new **public** repo named exactly `prakha194.github.io`
   (github.com/new -> Repository name: `prakha194.github.io` -> Public -> Create).
2. Upload every file in this folder to the repo root (Add file -> Upload files).
   Keep the names exactly: `index.html`, `favicon.ico`, `favicon.png`,
   `icon-192.png`, `apple-touch-icon.png`, `robots.txt`, `sitemap.xml`.
3. Repo -> Settings -> Pages -> Source: "Deploy from a branch", Branch: `main`,
   folder `/ (root)` -> Save.
4. Wait ~1 minute, then open https://prakha194.github.io/ — you should see the
   Melzo landing page instead of a 404.
5. In Search Console, add a **new property**: URL prefix `https://prakha194.github.io/`
   and verify it with the HTML tag method (paste the meta tag into `index.html`
   of this repo, in the `<head>`), then submit `sitemap.xml`.
6. Then URL Inspection -> `https://prakha194.github.io/` -> Request Indexing.

Google re-reads favicons and site names on recrawl: expect a few days to a
couple of weeks before the icon and the name "Melzo" replace the GitHub Pages
defaults in search results.
