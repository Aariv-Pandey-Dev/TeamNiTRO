# Team N!TRO — official website

A dependency-free, single-page website built with semantic HTML, CSS and JavaScript.
No build step, no external services: extract the folder and open `index.html`.

## Run it

- Double-click `index.html`, or
- serve the folder for the full experience:

```bash
python3 -m http.server 8000
```

then open <http://localhost:8000>.

## Structure

```
index.html        entry point
css/styles.css    design system and layout
js/app.js         boot sequence, atom, tabs, filters, fortune cookie
assets/           transparent logos, icon set, motion marks, badge, colour tiles, favicon, OG image
fonts/            Glacial Indifference (bundled woff2, SIL Open Font License)
hq/               the N!TRO Activity Monitor (team-only HQ) — see hq/README.md
.nojekyll         tells GitHub Pages to publish the files exactly as they are
```

## Publishing on GitHub Pages

The click-by-click guide, including the Firebase setup for the Activity
Monitor, is in **DEPLOY.md**.

Upload this whole folder to a repository, then Settings → Pages → Deploy from a
branch (main, root). The site is at `https://<user>.github.io/<repo>/` and the
Activity Monitor at `https://<user>.github.io/<repo>/hq/`. The emblem in the
hero and the link in the footer both point to `hq/index.html`, so they keep
working wherever the site is hosted.

## Notes

- The contact form intentionally runs in localhost demonstration mode: it
  validates the submission in the browser and does not transmit any data.
- The boot sequence plays once per session; click, press a key, or add
  `?skipIntro` to the URL to skip it. It never plays for visitors who prefer
  reduced motion.
- "Reduce effects" in the footer disables all animation and is remembered
  between visits.
- `assets/team-nitro-logo-pack.png` is the untouched official logo pack. Every
  other mark (lockups, emblem, badge, icon set, motion marks, colour tiles) is
  an optimized copy extracted from it for this site.
