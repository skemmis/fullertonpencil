# Fullerton Pencil website

Static site, no build step. Open `index.html` through any static host (Netlify, GitHub Pages, Cloudflare Pages, S3).
The logo is applied as a CSS mask, so it must be served over http(s), not opened as a local file.

- `index.html` — Home, About, Contact, Order (Coming soon) views (switch via #home, #about, #contact, #order)
- `assets/logo-green.png` — transparent wordmark, recolored by CSS for light/dark
- `assets/logo-cream.png` — cream wordmark for other uses
- `assets/photos/` — product photos generated with Gemini

The contact form validates input but does not send anything. Wire it to a form service (Formspree, Netlify Forms) to make it real.

## Hosting on Railway

Railway's builder (Railpack) detects this as a static site because of `index.html` and the `Staticfile`, and serves it with Caddy. No build or start command is needed. See the "Host Fullerton site on Railway" guide for the custom domain and GoDaddy DNS steps.
