# Marcela Macedo — Portfolio

Rebuild of Marcela's product design portfolio. Plain HTML/CSS, no build step —
open `site/index.html` in a browser, or just view it live once GitHub Pages
is switched on (see **Deploying**, below).

## Status

- ✅ **Screen 1 — hero ("Above the Fold")** committed. Direction: near-monochrome,
  huge single-typeface headline, looping brand strip, scattered rotated photo
  collage (inspired by the [Millls Readymag template](https://readymag.com/designs/5648674/4/)).
- ⏳ **Screen 2 onward** — case study previews, About, footer. Not built yet.

## Structure

```
site/
  index.html      real page markup
  styles.css      all styles
  assets/         drop project PNGs here
cv-master.md       source-of-truth CV / experience bank
Moodboard/          reference images Marcela collected
```

## Adding project images

The hero has four dashed placeholder slots tagged with the filenames it's
expecting: `moodys-01.png`, `chanel-02.png`, `mb-chatbot.png`, `chloe-03.png`.
Drop matching files into `site/assets/`, then in `site/index.html` swap the
placeholder `<span class="tag">` line for an `<img>`, e.g.:

```html
<div class="ph ph1">
  <img src="assets/moodys-01.png" alt="Moody's design system screenshot">
</div>
```

(Different filenames are fine — just say so and they'll get wired in.)

## Deploying (so it's live, no local server needed)

Once this is pushed to GitHub:

1. Repo → **Settings → Pages**
2. Source: **Deploy from a branch** → Branch: **main**, folder **/site**
   *(or move `site/`'s contents to the repo root and pick `/root` — either works)*
3. Save. GitHub gives you a live URL at `https://<username>.github.io/<repo>/`
   within a minute or two, and it redeploys automatically on every push.

## Next session

- Screen 2: case study preview cards
- About section
- Footer / contact
- Swap in real project images once available
