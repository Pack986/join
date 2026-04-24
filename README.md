# Pack 986 Landing Page

Recruitment landing page for Cub Scout Pack 986. Single-file HTML, mobile-first, no build step required.

## What's here

- `pack986-landing.html` — the full landing page (HTML + CSS + a tiny bit of JS, all in one file)

That's it. No dependencies to install, no framework to build. Open it in a browser and it just works.

## Deploying

### Option 1: Netlify (easiest)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Rename `pack986-landing.html` to `index.html`
3. Drag the file onto the page
4. You'll get a live URL immediately (something like `https://random-name-12345.netlify.app`)
5. In Netlify's site settings, you can rename the subdomain to something friendlier like `pack986.netlify.app`

**To update later:** drag the new file to the same site's "Deploys" tab, or connect this GitHub repo to Netlify for automatic deploys on every commit.

### Option 2: GitHub Pages

1. Make sure this repo is public
2. Rename `pack986-landing.html` to `index.html`
3. Go to **Settings → Pages**
4. Under "Source," select `Deploy from a branch`, choose `main` branch and `/ (root)` folder
5. Save. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute

## Customizing before publishing

A few things to swap out before going live:

### 1. Replace photo placeholders with real photos

In the gallery section, find the `<div class="photo-tile ...">` blocks. Each one looks like this:

```html
<div class="photo-tile ph-1 wide reveal">
  <svg class="ph-icon" ...></svg>
  <span class="ph-label">Campouts & Hikes</span>
</div>
```

Replace each with an actual image:

```html
<img src="images/campout.jpg" alt="Scouts at a campout" class="photo-tile wide reveal">
```

Keep the class names (`wide`, `tall`, `reveal`) on the `<img>` tag — they control the grid layout.

Create an `images/` folder in the repo and put your photos there. Keep them under ~500KB each for fast mobile loading (use [squoosh.app](https://squoosh.app) to compress).

### 2. Update the contact email

Search for `pack986@example.com` and replace it with the real address. Appears in one place in the "Join" section.

### 3. Optional tweaks

- **Hero stats** — update "12+ Events / Year" or other numbers in the hero section if you want different ones
- **Committee chair names** — James & Shashi are mentioned in the Join section and footer; update if leadership changes
- **Pack number** — appears as "986" in multiple places; easy to find-and-replace if this gets forked for another pack

## Custom domain (optional)

Both Netlify and GitHub Pages support custom domains. If you want something like `pack986.org` or `joinpack986.com`:

1. Buy a domain (Namecheap, Porkbun, or Cloudflare — ~$10-15/year)
2. In your host's settings (Netlify or GitHub Pages), add the custom domain
3. Update DNS records at your registrar as instructed by the host

## File structure

```
.
├── README.md                    <- you are here
├── pack986-landing.html         <- the landing page
└── images/                      <- (add this) your photos
    ├── campout.jpg
    ├── pinewood-derby.jpg
    └── ...
```

## Tech notes

- No build step, no npm install, no framework. Just HTML.
- Uses Google Fonts (Alfa Slab One, Fraunces, Work Sans) loaded via CDN.
- Mobile-first responsive: tested from 320px width up.
- Scroll-triggered reveal animations via IntersectionObserver.
- The SVG badge in the hero animates (rotating ring) via CSS keyframes.

## Maintenance

Edit the HTML file directly. No rebuild needed — just save and redeploy (drag-and-drop to Netlify, or `git push` if using GitHub Pages).

---

Questions? Contact James or Shashi, Pack 986 Committee Chairs.
