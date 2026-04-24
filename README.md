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

Photos live in the `images/` folder. To swap one out, replace the file and update the `src` in the matching `<img>` tag in the gallery section of `index.html`. Keep images under ~500KB — use [squoosh.app](https://squoosh.app) to compress if needed.

Current featured gallery images (7 tiles):

| File | Tile |
|---|---|
| `images/river-rafting.jpg` | Wide — Annual River Rafting |
| `images/popcorn-sales.jpg` | Popcorn Sales |
| `images/service-project.jpg` | Community Service |
| `images/snow-day.jpg` | Tall — Snow Day |
| `images/pinewood-derby.jpg` | Pinewood Derby |
| `images/parade.jpg` | St. Patrick's Day Parade |
| `images/uss-hornet.jpg` | USS Hornet Overnight |

Full photo grid images (33 tiles in `images/gallery-*.jpg`)

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
├── README.md       ← you are here
├── index.html      ← the entire site
└── images/
    ├── river-rafting.jpg
    ├── popcorn-sales.jpg
    ├── service-project.jpg
    ├── snow-day.jpg
    ├── pinewood-derby.jpg
    ├── parade.jpg
    └── uss-hornet.jpg
```

---

Questions? Contact the Pack 986 Membership team at joinpack986@gmail.com
