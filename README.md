# Atelier Index

A self-contained, static catalogue site — 31 houses, 270 catalogue images.

Pure static files: `index.html` plus a small runtime (`support.js`); React 18 and
Babel are served locally from `vendor/` (no CDN, works offline). The brand index
lives in `brands-data.global.js` / `brands-data.js`, and catalogue imagery under
`public/brands/`.

## Run locally

```bash
python3 -m http.server 8090
# then open http://127.0.0.1:8090/  (double-clicking index.html also works)
```

## Deploy

Any static host; no build command, no server, no database. Publish directory:
**repository root** (already encoded in `netlify.toml`).

- **Netlify (connected):** New site → Import from Git → pick this repo → leave the
  build command empty → publish directory `.`
- **Netlify (drag & drop):** drop this folder onto https://app.netlify.com/drop

Note: `robots.txt` currently disallows all crawlers — remove it when you want the
site indexed by search engines.

The original packaging notes are in `HOSTING-README.txt`.
