# FRONT MATTER — the About page at the root domain

Built 2026-10-21. This replaces the earlier cover-sheet plan that lived in this folder
(`PLAN-front-matter.md`): that plan deliberately left out school, city, subjects, photo and CV,
which the user has now asked for explicitly.

## Why

A bare `https://ethanantoineli.github.io/` used to be a 404. The root domain is now the real
front door, and the front door is an **About page for admissions readers**: the first screen has
to answer school, year, location, A-level subjects, intended course, show a portrait, offer the CV,
and give one obvious way into the work.

The work itself stays where it is: the drawing set at `/personal-page/`.

## What shipped

- `site/index.html` — self-contained page, same design language as the drawing set (paper `#f6f6f4`,
  ink `#101214`, signal rust `#b23e22`, Inter Tight + Instrument Serif, mono labels).
- `site/cv/Ethan-Antoine-Li-CV.pdf` — public CV, generated from `~/Desktop/CV_Ethan 0821.docx`
  with only two changes: the mobile number and the home street address are removed; the line
  becomes `Email: ethan2027@126.com · Guangzhou, China`. One page, no other edits.
- `site/img/portrait.jpg` — studio headshot from `~/Desktop/PHOTOS/`, 4:5 crop, 720 × 900.
- `site/img/og-about.png` — 1200 × 630 social card.
- Contact on the page is the professional **Outlook** address (`ethan.li.1@outlook.com`),
  the same one the hub uses. The CV keeps the application address from the source DOCX
  (`ethan2027@126.com`) — confirm if that should change too.
- `site/404.html` — brand and "back to the front page" now go to `/`; sub-copy explains the root is
  the about page and the drawing set is at `/personal-page/`.
- `README.md` — rewritten for the new root site.

## Page structure

1. Running head: brand + `Front matter · rev 2026.10`, nav (About, Record, The set ↗).
2. Masthead: name (serif italic middle name), one-line lede with intended course, CV button,
   email, portrait plate (`Fig. 000`, 4:5).
3. Facts strip: **School** (The British School of Guangzhou · Guangzhou, China), **Year**
   (Year 13 · A-levels 2025–2027), **A-levels & EPQ** (Mathematics, Further Mathematics, Physics,
   Chemistry · EPQ rescue arm, 2026), **Course** (Engineering · 2027 entry).
4. Four short first-person sections — The short version / Why rescue / How I build / Off the bench.
5. Record: EPQ, Senior Physics Challenge (Bronze), Senior Mathematical Challenge (Silver),
   Intermediate Physics Challenge final (Bronze, ASDAN) + Full CV button.
6. The door, after the content: `THE DRAWING SET — The work, arm, drone, Nora — OPEN THE SET →`,
   links to `/personal-page/`. Hover/focus fills ink.
7. Footer, no trackers, no cookies.

On screens ≤ 900 px the order is copy → facts → portrait, so the admissions facts stay in the
first screen instead of being pushed down by the photo.

## Content sources

- School, location, EPQ, summer schools, battery lab, competitions, tennis, charity, languages:
  the CV.
- A-level subjects, Year 13, intended course (Engineering, 2027 entry): confirmed facts from the
  workspace profile (`memory/ABOUT_ME.md`), **not** on the CV — the CV has no subject list or
  intended course, which is why the page carries them.
- No predicted grades, IGCSE/AS results or EPQ grade: not known, so not stated. These are the
  strongest missing pieces of academic evidence — add them when Ethan supplies them.

## QA (2026-10-21, local build, Chrome 1440×900 / 1024×768 / 390×844 / 320×800)

- No horizontal scroll at 320 / 360 / 480 / 560 / 700 / 860 / 1024 / 1100 / 1280 / 1440.
- At 1440 × 900 the first screen holds name, portrait, facts strip and the start of the About;
  the door sits after the content, per review.
- Zero console errors, zero failed requests, zero external requests; the three self-hosted fonts
  load; the portrait decodes 720 × 900.
- No-JS: name, portrait, facts, door and CV link all render. Reduced motion: entrance animation off.
- Tab order: skip → brand → About → Record → The set → CV → email → Nora → Full CV → door links.
- Door click lands on `/personal-page/` (hub title, cat canvas, three sheet rows).
- Tap targets: CV button ≥ 44 px; nav links padded (≥ 30 px); door is a full-width target.
- CV PDF: 1 page, text layer contains no mobile number and no street address.
- 404: brand and home link point at `/`.

## Open before going public

1. **Confirm the portrait may be public** (it is a real headshot) and that the cleaned CV is
   acceptable as published.
2. **Confirm the wording**: Year 13, A-levels 2025–2027, “Engineering · 2027 entry”. A specific
   course name (Engineering Science / Mechanical) can replace the generic one.
3. **Academic evidence**: predicted grades, IGCSE/AS results and the EPQ grade are the missing
   pieces an admissions reader looks for. Supply the numbers and they go into the facts strip and
   the CV.
4. The hub has **no link back to `/`** yet — the door is one-way for now.
5. Deployment: pushed to `main` on 2026-10-22; the Pages workflow deploys `site/` to
   `https://ethanantoineli.github.io/`.
