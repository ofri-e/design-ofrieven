# design.ofrieven.com — Ofri Even, Brand & Motion

Static site (Claude Design runtime). No build step: GitHub Pages serves these files as they are.

## Files
- `index.html` — entry point; loads `BrandWeb.dc.html` (one responsive site: web / tablet / mobile).
- `BrandWeb.dc.html` — all pages: home, Work (grid + list), About, 8 project pages.
- `StretchHero.dc.html`, `BrandFeatureCard.dc.html` (home cards), `BrandProjectCard.dc.html` (Work cards) — components.
- `support.js`, `image-slot.js` — runtime.
- `assets/` — images and videos. `CNAME` — custom domain.

Design tokens (colors, fonts, type sizes, radii) live in the `:root` block at the top of `BrandWeb.dc.html`.
Project pages are deep-linkable: `/#expoza`, `/#t42`, `/#ladies-first`, `/#fi-bo`, `/#beatles-2030`,
`/#best-new-artist`, `/#both-and-nation`, `/#taltalim`, plus `/#projects` and `/#about`.

## Deploy
1. Create a new GitHub repo (e.g. `design-ofrieven`) and push this folder's contents to `main`.
2. Repo → Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. Custom domain: `design.ofrieven.com` (already in `CNAME`). Tick "Enforce HTTPS" once it's available.
4. DNS (Cloudflare): add `CNAME` record — Name `design`, Target `<your-github-username>.github.io`, Proxy **off** (DNS only).
