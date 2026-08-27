# Personal Academic Site — Multi-Page Edition

A four-page personal site for an astrophysicist with an editorial /
observatory aesthetic. Plain HTML and CSS — no build tools, no JavaScript
required (just CSS animations and Google Fonts).

## Pages

- `index.html` — Home: hero with animated orbital diagram, recent news, about
- `research.html` — Five research projects with descriptions and links
- `publications.html` — Publications grouped by year, with stats bar
- `contact.html` — Contact info, links, and CV download

All four pages share `style.css` and a top navigation bar.

## Design notes

- **Typography**: Fraunces (variable display serif) + Newsreader (body serif)
  + IBM Plex Sans (UI) + IBM Plex Mono (dates and metadata).
- **Color palette**: warm parchment background, deep ink, prussian blue
  accent, amber star accent. Edit `:root` at the top of `style.css` to
  recolor the entire site.
- **Decoration**: Custom inline-SVG orbital diagram on the home page with
  three slowly-rotating orbits at different rates. Subtle paper grain texture
  via SVG noise.
- **Responsive** at 880px and 620px breakpoints. Respects `prefers-reduced-motion`.

## Customizing

1. Replace every "Your Name" / "University of Somewhere" placeholder.
2. Update the news feed on `index.html` with real recent items.
3. Replace the placeholder research projects on `research.html`. Each one
   takes a `tags` line, `h3` title, paragraph, and links list — copy/paste
   `<article class="research-entry">` to add more.
4. Fill in real publications on `publications.html`. Wrap your name in
   `<span class="me">Your Name</span>` so it gets the accent color.
   Group by year with the existing `.pub-year` sections.
5. Update institution and ORCID/ADS/GitHub links on `contact.html`.
6. Drop your CV PDF into the folder as `cv.pdf` (referenced from contact page).
7. Add a headshot to `images/` if you want to use one (not used by default).

## Color customization

Edit these variables at the top of `style.css`:

```css
--bg: #f5efe1;          /* page background — warm parchment */
--ink: #181613;         /* primary text */
--accent: #2c4763;      /* link & highlight color (prussian blue) */
--accent-warm: #a8521e; /* "star" color (amber) */
```

Try other accent colors:
- Forest (#2d5a3d) + warm gold accent
- Burgundy (#5e2e3a) + cream
- Slate (#3a4a5c) + copper

## Previewing locally

Open the folder in VS Code, install the "Live Server" extension, then
right-click `index.html` → "Open with Live Server". Each save auto-refreshes.

## Deploying to GitHub Pages

1. Create a GitHub repo named exactly `yourusername.github.io`.
2. Push these files to the `main` branch.
3. Settings → Pages → confirm serving from `main` branch root.
4. Live at `https://yourusername.github.io` within ~1 minute of push.

## File tree

```
astro-site-pro/
├── index.html
├── research.html
├── publications.html
├── contact.html
├── style.css
├── images/
└── README.md
```
