# S.M Bag Centre — Website

A redesigned, static website for S.M Bag Centre (bag & luggage repair, Bangalore, since 1969). No frameworks, no build step — plain HTML/CSS/JS, ready to publish on GitHub Pages.

## Design direction

Instead of a generic template, the site borrows its visual language from the shop's own world: **repair tickets and hang tags**. Service cards, the hero visual and testimonials are styled as stitched, hole-punched tags with stamped ink labels — a nod to how a repair actually gets logged and handed back to you.

- **Palette:** aged canvas background, saddle-leather brown, waxed-thread mustard, stamp-ink red.
- **Type:** Roboto Slab (headings), Special Elite (stamp/ticket labels), Work Sans (body).
- **Motion:** intentionally minimal — hover states only, no scroll animations, gradients, or auto-playing effects. Respects `prefers-reduced-motion`.
- Fully responsive (mobile, tablet, desktop) and keyboard-accessible (visible focus states).

## Files

```
├── index.html    # all page content/sections
├── style.css     # design tokens + all styling
├── script.js     # one line: sets the footer's copyright year
└── README.md
```

Update phone numbers, branch addresses, or copy directly in `index.html`. Colors, fonts, and spacing are all controlled by CSS custom properties at the top of `style.css` (`:root`) — change the design in one place.

## Publish to GitHub Pages

1. **Create a new repository** on GitHub (e.g. `sm-bag-centre`), and don't initialize it with a README (you already have one here).

2. **Push these files** to it:
   ```bash
   cd sm-bag-centre
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/sm-bag-centre.git
   git push -u origin main
   ```

3. **Turn on Pages:**
   - Go to your repo → **Settings** → **Pages**.
   - Under "Build and deployment", set **Source** to `Deploy from a branch`.
   - Set **Branch** to `main` and folder to `/ (root)`, then **Save**.

4. Wait a minute, then your site is live at:
   ```
   https://<your-username>.github.io/sm-bag-centre/
   ```

### Using a custom domain (optional)
In the same **Settings → Pages** screen, enter your domain under "Custom domain" (e.g. `smbagcentre.com`), then add a `CNAME` record at your domain registrar pointing to `<your-username>.github.io`. GitHub will add a `CNAME` file to the repo automatically.

## Local preview
No build tools needed — just open `index.html` in a browser, or run a tiny local server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```
