# Pack 986 — Join Page

Recruitment landing page for Cub Scout Pack 986. Single-file HTML/CSS/JS — no build step, no dependencies.

**Live site:** https://pack986.github.io/join/

---

## How it's deployed

This repo lives under the **Pack986 GitHub Organization** and is served via **GitHub Pages**.

- Source: `main` branch, `/ (root)` folder
- Any `git push` to `main` automatically updates the live site within ~60 seconds
- No manual deploy step needed

To verify or change the Pages configuration: **GitHub → Pack986/join → Settings → Pages**

---

## Managing the site

### Making a change

1. Edit `index.html` directly (everything — HTML, CSS, JS — is in one file)
2. Commit and push to `main`:
   ```
   git add index.html
   git commit -m "your change description"
   git push
   ```
3. GitHub Pages will rebuild automatically. Check the live URL in ~1 minute.

### Things you'll want to update before launch

| What | Where in `index.html` | Notes |
|---|---|---|
| Contact email | Search `pack986@example.com` | One occurrence, in the Join section |
| Committee chair names | Search `James` and `Shashi` | Footer + Join section copy |
| Hero stats | `<div class="hero-stats">` block | "12+ Events / Year", etc. |
| Photo tiles | `<div class="gallery">` section | See instructions below |

### Swapping in real photos

The gallery currently shows placeholder tiles with gradient backgrounds. To replace with real photos:

Find each `<div class="photo-tile ...">` block in the gallery section and replace it with an `<img>` tag:

```html
<!-- Before (placeholder) -->
<div class="photo-tile ph-1 wide reveal">
  <svg class="ph-icon" ...></svg>
  <span class="ph-label">Campouts &amp; Hikes</span>
</div>

<!-- After (real photo) -->
<img src="images/campout.jpg" alt="Scouts on a campout" class="photo-tile wide reveal">
```

Keep the layout class names (`wide`, `tall`, `reveal`) on the `<img>` — they control the grid.

Add your photos to an `images/` folder in the repo. Keep files under ~500KB each for fast mobile loading — [squoosh.app](https://squoosh.app) is a free compressor.

---

## Custom domain (optional)

To use a domain like `pack986.org` or `joinpack986.com` instead of the `github.io` URL:

1. Buy a domain (~$10–15/yr via Porkbun, Namecheap, or Cloudflare Registrar)
2. In **Settings → Pages → Custom domain**, enter your domain
3. At your registrar, add the DNS records GitHub instructs you to add (usually 4 A records + 1 CNAME)
4. Check "Enforce HTTPS" once the domain verifies (takes up to 24 hrs for DNS to propagate)

---

## File structure

```
.
├── README.md       ← you are here
├── index.html      ← the entire site (HTML + CSS + JS, one file)
└── images/         ← add this folder when you have real photos
    ├── campout.jpg
    └── ...
```

---

## Tech notes

- No npm, no framework, no build step — just HTML
- Google Fonts (Alfa Slab One, Fraunces, Work Sans) loaded via CDN
- Mobile-first responsive, tested from 320px up
- Scroll-triggered reveal animations via `IntersectionObserver`
- Hero badge SVG animates via CSS `@keyframes`

---

Questions? Contact James or Shashi, Pack 986 Committee Chairs.
