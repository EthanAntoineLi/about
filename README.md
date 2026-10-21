# EthanAntoineLi.github.io

Root-domain site for <https://ethanantoineli.github.io/>.

## What is here

| Path | What it is |
| --- | --- |
| `site/index.html` | **The About page** — the front door of the site: who Ethan is, the admissions facts (school, year, A-level subjects, intended course), a portrait, a one-page CV, and the door into the drawing set. |
| `site/404.html` | Wrong-address page. Brand and "back to the front page" links go to `/`; the sheet list links into the portfolio. |
| `site/cv/Ethan-Antoine-Li-CV.pdf` | The public CV. Same content as the source DOCX, with the mobile number and home street address removed; one page. |
| `site/img/portrait.jpg` | Portrait used on the About page (900 × 900, from a studio headshot). |
| `site/img/og-about.png` | 1200 × 630 social card for the About page. |
| `site/fonts/` | Self-hosted Inter Tight 300/400 and Instrument Serif italic. No external requests. |

The portfolio itself is a project page at `/personal-page/` (`EthanAntoineLi/personal-page`).
GitHub Pages only serves a custom 404 from a site's own root, so this user-site repo exists to
host both the root front matter and that 404.

## Deploy

`.github/workflows/deploy.yml` uploads `site/` as a Pages artifact on every push to `main`.
No build step, no npm. Everything is one self-contained HTML file per page plus local assets.

## Notes

- `/` and `/personal-page/` are two independent Pages deployments. After touching either one,
  check the other still serves.
- Do not add third-party fonts, analytics or CDN requests — the site is deliberately self-hosted
  and cookie-free.
- Build record for the About page: `ABOUT-PAGE.md`.
