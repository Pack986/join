# Pack 986 — Join Page

Recruitment landing page for Cub Scout Pack 986. Single-file HTML/CSS/JS — no build step, no dependencies.

**Live site:** https://pack986.github.io/join/

---

## Deployment

This repo is hosted via **GitHub Pages** under the Pack986 GitHub Organization.

- Source: `main` branch, `/ (root)` folder
- Pushing to `main` automatically updates the live site within ~60 seconds

---

## Making changes

1. Edit `index.html` (everything — HTML, CSS, JS — is in one file)
2. Commit and push:
   ```
   git add index.html
   git commit -m "describe your change"
   git push
   ```
3. Live in ~1 minute.

---

## Updating photos

All photos live in the `images/` folder. There are two gallery areas on the page:

- **Featured gallery** — 10 hero tiles near the top of the Adventures section (the big visual showcase)
- **Full photo grid** — 32 thumbnail tiles with category filters (Camping, Hiking, Pack Life, etc.)

---

### Swap out a featured gallery tile

1. Copy your new photo into `images/` (compress to under 500KB first — see tip below)
2. In `index.html`, find the `<!-- ========= GALLERY ========= -->` section
3. Locate the `<div class="photo-tile ...">` for the tile you want to replace
4. Update the `src` attribute on the `<img>` tag and the label text in `<span class="ph-label">`
5. Commit and push

**Tile types** — add the right class to the `<div>`:
- `photo-tile` — standard square tile
- `photo-tile wide` — spans 2 columns (landscape/banner)
- `photo-tile tall` — taller aspect ratio (portrait)

Current featured tiles:

| File | Label | Type |
|---|---|---|
| `images/river-rafting.jpg` | River Rafting | Wide |
| `images/popcorn-sales.jpg` | Popcorn Sales | Standard |
| `images/service-project.jpg` | Community Service | Standard |
| `images/snow-day.jpg` | Snow Day | Tall |
| `images/pinewood-derby.jpg` | Pinewood Derby | Standard |
| `images/parade.jpg` | St. Patrick's Day Parade | Standard |
| `images/uss-hornet.jpg` | USS Hornet Overnight | Standard |
| `images/gallery-campfire-smores.jpg` | Camping & Outdoors | Wide |
| `images/gallery-hiking-hills.jpg` | Hiking | Standard |
| `images/gallery-archery.jpg` | Archery | Standard |

---

### Add a photo to the full grid

1. Copy your photo into `images/` as `gallery-your-name.jpg`
2. In `index.html`, find the `<!-- ========= FULL PHOTO GRID ========= -->` section
3. Add a new `<button>` block inside `.fg-grid`, following this pattern:
   ```html
   <button class="fg-item reveal" data-cat="CATEGORY" data-src="images/gallery-your-name.jpg" data-label="Your Label">
     <img src="images/gallery-your-name.jpg" alt="Description of the photo" loading="lazy">
     <span class="fg-label-hover">Your Label</span>
   </button>
   ```
4. Set `data-cat` to one of the existing categories:
   - `camping` — campouts, campfires, fishing, camp activities
   - `hiking` — trail hikes, nature walks
   - `pack-life` — pack meetings, den activities, ceremonies
   - `derby` — Pinewood Derby
   - `service` — community service, fire station visits, parades
   - `fundraising` — popcorn sales
5. Update the filter pill count for that category in the `<div class="fg-filters">` block (find `data-filter="CATEGORY"` and increment the number in `<span class="fg-count">`)
6. Also increment the **All Photos** count
7. Commit and push

---

### Remove a photo from the full grid

1. Delete the file from `images/`
2. In `index.html`, delete the matching `<button class="fg-item ...">` block
3. Decrement the count for its category pill and the All Photos count
4. Commit and push

---

### Compress photos before adding

Keep images under ~500KB. The fastest way on Mac:

```bash
sips -Z 1200 ~/Downloads/your-photo.jpg --out images/gallery-your-name.jpg
```

Or use [squoosh.app](https://squoosh.app) in the browser.

---

## Custom domain (optional)

To use a domain like `pack986.org` instead of the `github.io` URL:

1. Buy a domain (~$10–15/yr via Porkbun, Namecheap, or Cloudflare Registrar)
2. In **Settings → Pages → Custom domain**, enter your domain
3. Add the DNS records GitHub provides at your registrar (usually 4 A records + 1 CNAME)
4. Enable "Enforce HTTPS" once the domain verifies (~24 hrs for DNS)

---

## File structure

```
.
├── README.md           ← you are here
├── index.html          ← the entire site (HTML + CSS + JS in one file)
└── images/
    ├── river-rafting.jpg       ← featured gallery tiles
    ├── popcorn-sales.jpg
    ├── service-project.jpg
    ├── snow-day.jpg
    ├── pinewood-derby.jpg
    ├── parade.jpg
    ├── uss-hornet.jpg
    └── gallery-*.jpg           ← full photo grid (32 photos)
```

---

Questions? Contact the Pack 986 Membership team at joinpack986@gmail.com
