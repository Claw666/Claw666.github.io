# csongorkocsis.com

One static page, no build step, no dependencies, no third-party requests.

## Files
- `index.html` — the whole site: markup, CSS and ~15 lines of JS in one file.
- `favicon.svg` — monogram favicon.
- `robots.txt`, `sitemap.xml`
- `CNAME` — the custom domain.
- `cv.pdf` — not linked yet. The contact row shows a "CV — under construction" chip; when the file is ready, swap that `<span class="soon">` for `<a href="cv.pdf">CV</a>`.

## Editing
Everything lives in `index.html`.

- **Colours** — the `:root` block at the top of `<style>`. Light values first; the
  two blocks below it hold the dark values (one for the system preference, one for
  the manual override). Change a colour in all three places if it applies to both themes.
- **Adding a job or project** — copy one `.row` block. Nothing else to touch; the
  last row in a `.list` gets its closing rule automatically.
- **Removing a section** — delete the whole `<section>`.
- **Theme** — the page follows the visitor's system setting. The button in the header
  cycles Auto → Light → Dark and remembers the choice in `localStorage`.

## Deploying
Push to the repo's default branch and enable GitHub Pages from the root. Keep the
`CNAME` file so the custom domain survives redeploys.

## Weight
~9 KB of HTML on the wire before compression, one request for the page and one for
the favicon. No webfonts: type is the system UI face (SF on Apple, Segoe on Windows,
Roboto on Android).
