# Eastern Shore Heating & Air Conditioning — Website

A fast, single-file static site for Eastern Shore Heating & Air Conditioning Inc.
(Brick Township, NJ · family-owned since 1979).

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire site (HTML + CSS + JS inline, only external dep is Google Fonts) |
| `favicon.svg` | Site icon (thermometer mark) |
| `site.webmanifest` | PWA / add-to-homescreen metadata |
| `robots.txt`, `sitemap.xml` | SEO crawler files |
| `netlify.toml` | Deploy + security headers config |
| `og-image.jpg` | **TODO:** add a 1200×630 social-share image (referenced by Open Graph tags) |

## Before going live — checklist

1. **Wire up the contact form.** Open `index.html`, find `const FORM_ENDPOINT = ''`
   near the bottom `<script>`. Create a free form at [formspree.io](https://formspree.io)
   (or similar) and paste the endpoint URL. Until then the form falls back to
   opening the visitor's email client to `info@easternshorehvac.com`.
2. **Add `og-image.jpg`** (1200×630) for link previews on Facebook/iMessage/etc.
3. **Confirm the real review count** — currently shown as "4.9★ from 600+ reviews"
   (sourced from Birdeye/HomeAdvisor, July 2026). Update if it changes.
4. **Verify the geo coordinates** in the JSON-LD schema match the Mantoloking Rd address.
5. **Replace testimonials** with more if desired — three verified quotes are included
   now (HomeAdvisor + Facebook). Google reviews can be embedded via a widget later.

## Local preview

```bash
python3 -m http.server 8429
# then open http://localhost:8429
```

## Deploy

**Netlify (easiest):** drag this folder onto [app.netlify.com/drop](https://app.netlify.com/drop),
or run `netlify deploy --prod`. Then point the `easternshorehvac.com` DNS at Netlify.

Any static host works too (Cloudflare Pages, GitHub Pages, Vercel, S3) — it's just static files.
