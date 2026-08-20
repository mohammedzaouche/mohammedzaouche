# Mohammed Zaouche — Portfolio

Senior Graphic Designer. Brand systems, campaign design and motion across
banking, healthcare, hospitality, luxury and tech.

## What this is

A single static page. No build step, no dependencies, no framework.

```
index.html                 the whole site — markup, CSS, JS and project data
img/                       optimised WebP artwork (project frames + mockups)
fonts/                     self-hosted Outfit + Inter (woff2)
Mohammed-Zaouche-CV.pdf    downloadable CV
vercel.json                caching + security headers
```

## Editing

Everything lives in `index.html`.

- **Projects** — the `PROJECTS` array near the bottom of the file. Each entry
  has `title`, `client`, `sector`, `cat`, `loc`, `year`, `blurb`, `tags`,
  `cover` and `images`. Add an image by dropping the file in `img/` and adding
  `{src, w, h}` to that project's `images`. **Always set the real `w` and `h`** —
  they keep the browser from ever distorting the frame.
- **Clients marquee** — the `CLIENTS` array. Row one scrolls right-to-left,
  row two left-to-right; the list is split in half automatically.
- **Filters** — the `CATS` array. A category only appears if a project uses its
  `cat` id.
- **Colours** — the `:root` block at the top of the stylesheet.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploying

Pushing to the default branch deploys to production on Vercel.
