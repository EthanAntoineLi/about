# EthanAntoineLi.github.io

Root-domain 404 for <https://ethanantoineli.github.io/>.

The portfolio itself is a project page at
<https://ethanantoineli.github.io/personal-page/> (`personal-page` repo).
GitHub Pages only serves a custom 404 from a site's own root, so this tiny
user-site repo exists solely to replace the default "Site not found" page
with the site's own wrong-address page, pointing at the portfolio.

- `site/404.html` — the page (self-contained, site fonts copied in)
- `.github/workflows/deploy.yml` — uploads `site/` and deploys to Pages

There is intentionally no `index.html`: typing the bare domain gives the 404,
which is where the portfolio link lives.
