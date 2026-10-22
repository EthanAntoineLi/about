# ethan-about — the About page at `/about/`

The main site is the drawing-set hub at <https://ethanantoineli.github.io/>
(repo `EthanAntoineLi.github.io` — the old `personal-page` repo).

This repo deploys the **About page** as a GitHub Pages project site:
<https://ethanantoineli.github.io/about/>.

| Path | What it is |
| --- | --- |
| `site/index.html` | The About page — school, year, location, A-level subjects and predictions, intended course, portrait, record and toolkit. |
| `site/img/portrait.jpg` | Portrait used on the page (4:5, 720 × 900). |
| `site/img/og-about.png` | 1200 × 630 social card. |
| `site/fonts/` | Self-hosted Inter Tight 300/400 and Instrument Serif italic. |

## Deploy

`.github/workflows/deploy.yml` uploads `site/` as a Pages artifact on every push to `main`;
GitHub Pages serves it at `/about/`. No build step, no npm.

Asset paths are **relative** on purpose (`fonts/…`, `img/…`) so the page works under the
project path. Links back into the site (`/`, `/work/nora/`) are root-absolute.

## Notes

- The hub at `/` carries the "About me" button that opens this page.
- **The CV is not published and not linked** (Ethan's call, 2026-10-22). Its content —
  education, competitions, toolkit — lives directly on the About page.
- The old root-domain 404 page was removed with the move; the hub now owns the 404.
- Build record: `ABOUT-PAGE.md`.
