# Sacred Devotional Embroidery Collection — Landing Page

Static landing page (English) for the **+100 Catholic Designs** embroidery collection.

## Stack
- Single-file `index.html` styled with **pre-compiled Tailwind CSS** (`tailwind.min.css`) — no runtime CDN, fast load on desktop and mobile.
- Optimized **WebP** images with JPEG fallback via `<picture>`.
- Meta Pixel + UTMify tracking, Hotmart checkout.

## Files
| File | Purpose |
|------|---------|
| `index.html` | The landing page |
| `tailwind.min.css` | Pre-compiled Tailwind utilities used by the page |
| `hero-mockup.webp` / `.jpg` | Hero image (LCP, preloaded) |
| `pack-completo.webp` / `.jpg` | Offer-card product image |
| `imagens/` | Gallery images (`.webp` + `.jpg` fallback) |

## Performance notes
- Images are resized + WebP-encoded (hero ~166 KB vs ~2.4 MB original).
- `width`/`height` set on all images to avoid layout shift.
- Hero is preloaded with `fetchpriority="high"`.

> If you add **new Tailwind classes** to `index.html`, recompile `tailwind.min.css`
> (the file only contains classes present at build time).

## Run locally
Just open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
```
