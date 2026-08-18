# Marcela Macedo — Portfolio

Rebuild of Marcela's product design portfolio. Plain HTML/CSS, no build step —
open `index.html` in a browser, or view it live via GitHub Pages (see
**Deploying**, below).

Live: https://marcelamcm.github.io/portfoliomarcela/

## Status

- ✅ **Screen 1 — hero ("Above the Fold")** committed. Direction: near-monochrome,
  huge single-typeface headline, looping brand strip, scattered rotated photo
  collage (inspired by the [Millls Readymag template](https://readymag.com/designs/5648674/4/)).
- ⏳ **Screen 2 onward** — case study previews, About, footer. Not built yet.

## Structure

```
index.html          real page markup
styles.css           all styles
assets/               drop project PNGs here
cv-master.md          source-of-truth CV / experience bank
Moodboard/             reference images Marcela collected
```

## Adding project images

The hero has four dashed placeholder slots tagged with the filenames it's
expecting: `moodys-01.png`, `chanel-02.png`, `mb-chatbot.png`, `chloe-03.png`.
Drop matching files into `assets/`, then in `index.html` swap the placeholder
`<span class="tag">` line for an `<img>`, e.g.:

```html
<div class="ph ph1">
  <img src="assets/moodys-01.png" alt="Moody's design system screenshot">
</div>
```

(Different filenames are fine — just say so and they'll get wired in.)

## Deploying

Already wired up: GitHub Pages serves straight from the repo root on `main`,
and redeploys automatically a minute or two after every push. Nothing to run
locally — push, then refresh the live URL above.

## Next session

- Screen 2: case study preview cards
- About section
- Footer / contact
- Swap in real project images once available
