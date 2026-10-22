# FRONT MATTER — the About page at `/about/`

Built 2026-10-21. Updated 2026-10-22: the drawing-set hub became the main page at the root
domain, so the About page moved to a project page at
<https://ethanantoineli.github.io/about/>. The hub now carries an **About me** button that opens
it. This repo was renamed `EthanAntoineLi.github.io` → `about`; the hub repo (`personal-page`)
took the user-site name.

## Why

A bare `https://ethanantoineli.github.io/` used to be a 404. It is now the real front door — the
hub — and the About page sits one path over. The About page is written for admissions readers:
the first screen answers school, year, location, A-level subjects and predictions, intended
course, shows a portrait, and the record carries the CV's content directly.

## What shipped

- `site/index.html` — self-contained page, same design language as the drawing set (paper `#f6f6f4`,
  ink `#101214`, signal rust `#b23e22`, Inter Tight + Instrument Serif, mono labels). Asset paths
  are relative, so it works under `/about/`.
- `site/img/portrait.jpg` — studio headshot from `~/Desktop/PHOTOS/`, 4:5 crop, 720 × 900.
- `site/img/og-about.png` — 1200 × 630 social card.
- `README.md` — rewritten for the `/about/` project site.
- **No CV on the site, and no CV buttons.** The PDF was published for a few hours, then removed
  on 2026-10-22 at Ethan's request ("don't publish the CV, don't make it downloadable"), then the
  two request-by-email buttons were dropped too ("don't keep either of them — put the information
  on the page"): `site/cv/` is gone, `/cv/Ethan-Antoine-Li-CV.pdf` returns 404, and the CV's
  content now sits directly in the page — education dates, every competition and award, and the
  toolkit line in the Record section, with the experience covered by the about sections. A cleaned
  copy (no mobile number, no street address) is kept outside the repo at `_qa/private/`.
- Contact on the page is the professional **Outlook** address (`ethan.li.1@outlook.com`), the same
  one the hub uses.

## Page structure

1. Running head: brand + `Front matter · rev 2026.10`, nav (About, Record, The set ↗ → `/`).
2. Masthead: name (serif italic middle name), one-line lede with intended course, contact email,
   portrait plate (`Fig. 000`, 4:5).
3. Facts strip: **School** (The British School of Guangzhou · Guangzhou, China), **Year**
   (Year 13 · A-levels 2025–2027), **A-levels · predicted** (Mathematics A*, Further Mathematics
   A*, Physics A, Chemistry A · EPQ rescue arm, 2026), **Course** (Engineering · 2027 entry).
4. Four short first-person sections — The short version / Why rescue / How I build / Off the bench.
5. Record, as the CV's on-page equivalent: The British School of Guangzhou (IGCSE & A-levels,
   2019–), EPQ, Senior Physics Challenge (Bronze), Senior Mathematical Challenge (Silver),
   Australian Mathematics Challenge (Credit), Intermediate Physics Challenge final (Bronze, ASDAN)
   and Silver, plus a **Toolkit** line (Python, C++, Shapr3D, STM32F407, Bambu Lab A1 mini,
   three.js).
6. The door, after the content: `THE DRAWING SET — The work, arm, drone, Nora — OPEN THE SET →`,
   links to the hub at `/`. Hover/focus fills ink.
7. Footer, no trackers, no cookies.

On screens ≤ 900 px the order is copy → facts → portrait, so the admissions facts stay in the
first screen instead of being pushed down by the photo.

## Content sources

- School, location, EPQ, summer schools, battery lab, competitions, tennis, charity, languages:
  the CV.
- A-level subjects, Year 13, intended course (Engineering, 2027 entry): confirmed facts from the
  workspace profile (`memory/ABOUT_ME.md`), not on the CV.
- **Predicted grades supplied by Ethan on 2026-10-22: `A*A*AA`, in the order Mathematics A*,
  Further Mathematics A*, Physics A, Chemistry A.**
- EPQ grade, IGCSE/AS results: still not known, so not stated.

## QA (2026-10-22, Chrome 1440×900 / 1024×768 / 390×844 / 320×800)

- No horizontal scroll at 320 / 360 / 480 / 560 / 700 / 860 / 1024 / 1100 / 1280 / 1440.
- At 1440 × 900 the first screen holds name, portrait, the facts strip (with predictions) and the
  start of the About.
- Zero console errors, zero failed requests, zero external requests; the three self-hosted fonts
  load; the portrait decodes 720 × 900.
- No-JS: name, portrait, facts and door all render. Reduced motion: entrance animation off.
- Door click lands on the hub at `/` (hub title, cat canvas, three sheet rows).
- CV: no button or link in the page source, no PDF in `site/`; `/cv/Ethan-Antoine-Li-CV.pdf` is
  a 404. The record carries the CV's education, competitions and toolkit.

## Deployment

- This repo is `EthanAntoineLi/about` (renamed from `EthanAntoineLi/EthanAntoineLi.github.io` on
  2026-10-22). Its Pages workflow uploads `site/` and serves it at `/about/`.
- The `personal-page` repo was renamed `EthanAntoineLi.github.io` and now deploys the hub at the
  root. Its Pages workflow no longer sets `BASE=/personal-page/`.
- The old root-domain 404 page was removed; the hub's `public/404.html` now handles 404s.
- The CV file is still inside the old root repo's git history (it was the cleaned copy — no phone
  or street address). The live site no longer serves it. If the history must be purged as well,
  that needs a force-push history rewrite.

## Open

1. A specific course name (Engineering Science / Mechanical) can replace the generic "Engineering".
2. EPQ grade / IGCSE results would complete the academic picture if wanted.
3. The Social Impact Award has no year in the source CV, so it stays in the prose ("Off the
   bench") rather than in the dated record.
