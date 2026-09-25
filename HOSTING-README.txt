ATELIER INDEX — complete website package
=========================================

This folder IS the website. Everything needed to host it live is here.

WHAT'S INSIDE
  index.html            the site (open it by double-clicking — works offline)
  vendor/               fonts + runtime (React, Babel) — makes it self-contained
  public/brands/        31 brands, all catalogue images
  support.js            page runtime
  brands-data.global.js brand/product index (01 MISRAA ... 31 NO CAP)
  brands-data.js        same index, module version (fallback)
  robots.txt            keeps search engines out

HOW TO HOST IT
  Any static host works — no server or database needed.

  Netlify (used for the current live site):
    * Easiest: open https://app.netlify.com/drop and drag this whole folder
      onto the page. Done — you get a live URL in ~1 minute.
    * Or via CLI (if you have Node):
        cd into this folder
        npx --yes netlify-cli deploy --prod --dir .

  Other options: Vercel, Cloudflare Pages, GitHub Pages, or your own hosting
  (upload/extract the CONTENTS of this folder into the web root, e.g. public_html).

UPDATING THE SITE
  Current live site: https://atelier-index.netlify.app
  The full working project (with sources) lives in the private GitHub repo
  CocaineJesus322/fashion-catalog. To publish an update:
      python3 scripts/make_netlify_site.py
      npx --yes netlify-cli deploy --prod --dir netlify-site

NOTES
  * Fully self-contained: no CDN, no internet required to run.
  * Images are 135 original brand assets + 135 added later (JPEG, native resolution).
  * This site is viewable by anyone with the link; robots.txt blocks search engines.
