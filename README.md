# Marcela Macedo — Portfolio

Rebuild of Marcela's product design portfolio. Plain HTML/CSS, no build step —
open `index.html` in a browser, or view it live via GitHub Pages (see
**Deploying**, below).

Live: https://marcelamcm.github.io/portfoliomarcela/

## Status

- ✅ **Home page** rebuilt to match the direction from the Framer draft
  (dark theme, huge Archivo display type, cream-on-black, indigo accent).
  Nav (name / work / about me) → hero (`marcela macedo` + tagline) →
  "companies I have worked with" marquee → **selected work** grid with
  filter pills (all / enterprise saas / luxury fashion / e-commerce) →
  **about** section (bio, real photobooth strip, why-work-with-me,
  beyond-the-screen) → footer (contact, pages, socials, big wordmark).
  Work grid order: Moody's, Chloé, Chanel, Richemont.
- ✅ **Case study pages** for **Moody's** ([moodys.html](moodys.html)) and
  **Chloé** ([chloe.html](chloe.html)), sourced from `cv-master.md`. Chanel
  and Richemont cards on the home page are marked "Case study coming soon"
  until their pages are written.
- ✅ **About photo** — real photobooth strip at
  `assets/about/photobooth.png`, right-aligned next to the intro paragraph.
- ✅ **Tag pills** — Moody's card/case-study uses an `AI` tag instead of
  `Figma` (the Nagarro engagement's AI-driven work). Apply the same to any
  future Mercedes-Benz card. Chanel/Chloé/Richemont keep `Figma`.
- ⏳ **"Download resume" button removed** for now — no resume PDF in the
  repo yet. Re-add once `resume.pdf` exists (see `.btn` in `index.html`'s
  about section).
- ⏳ Chanel and Richemont case study pages — not built yet.
- ⏳ Off-White and Foursource have no imagery yet — add project cards for
  them once assets exist.

### Note on project imagery (2026-08-19)

The original flat `assets/projects/*.jpg` files (moodys/chanel/chloé/
richemont hero + card shots) disappeared from disk outside of any edit made
in this repo — not deleted via any command run here, and they were never
committed to git, so there was no local history to restore from. Marcela
re-supplied one image per brand, organized into per-brand subfolders. The
site now points at those:

```
assets/projects/moodys/moodys-card.png
assets/projects/chloe/chloe-app-mockup.png
assets/projects/chanel/chanel-card.png
assets/projects/richemont/richemont-card.png
```

Each case study page (`moodys.html`, `chloe.html`) now reuses that single
brand image for both the hero banner and the in-body media — there's only
one image per brand at the moment, so the earlier "second image" spot in
each case study was removed rather than left broken. Add a second image per
brand and reintroduce a `.case-media` block in the case study page whenever
more imagery exists.

**Going forward:** keep new project images inside `assets/projects/<brand>/`
(one folder per brand) rather than flat in `assets/projects/` — matches how
Marcela's been adding them.

## Structure

```
index.html                 home page
moodys.html                 Moody's case study
chloe.html                   Chloé case study
styles.css                     all styles (dark theme, Archivo + Inter)
assets/projects/<brand>/          one folder per brand, project imagery
assets/about/                       photobooth strip photo
cv-master.md                          source-of-truth CV / experience bank
Moodboard/                              reference images Marcela collected
```

## Adding project images

Work cards (`.proj-media img`) read from `assets/projects/<brand>/`. To swap
or add imagery, drop a file in the brand's folder (create one if it doesn't
exist yet) and point the relevant `<img src="...">` at it.

## Deploying

Already wired up: GitHub Pages serves straight from the repo root on `main`,
and redeploys automatically a minute or two after every push. Nothing to run
locally — push, then refresh the live URL above.

## Next session

- Resume PDF + re-add the "download resume" button
- Chanel and Richemont case study pages
- A second image per brand, to restore the `.case-media` section in each
  case study page
- Add Off-White and Foursource cards once assets are in Figma
