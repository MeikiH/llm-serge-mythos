# CLAUDE.md — Serge Mythos

## Project

Satirical AI landing page. Two static HTML pages (EN + FR) for **Serge Mythos**, a fake frontier LLM by **HotTropic Labs**. Parodies real AI product launches.

No build system. Pure HTML + CDN libraries. Open the HTML files directly in a browser.

## File map

| File | Role |
|------|------|
| `index.html` | Landing page EN — source of reference for code organization |
| `fr/index.html` | Landing page FR — must stay structurally identical to `index.html` |
| `img/` | Avatar images for Serge Dupont-Machin |

## Stack

- **Tailwind CSS 4** via `@tailwindcss/browser@4` CDN — styles go inside `<style type="text/tailwindcss">` with `@theme {}` for custom tokens. The linter warning "Unknown at rule @theme" is a false positive; ignore it.
- **daisyUI 5** — used for `<dialog>` modals only
- **AOS 2.3.4** — scroll animations via `data-aos` attributes
- **Font Awesome 6.7.2** — `<i class="fa-solid fa-...">` icons
- **Google Fonts** — Playfair Display (serif), DM Sans (sans), Space Mono (mono)

## Design tokens

```css
--color-bleu:       #002395
--color-rouge:      #ED2939
--color-or:         #C9A84C
--color-blanc:      #EDECE8   /* page background */
--color-gris:       #1a1a1a
--color-gris-clair: #f2f1ed   /* section backgrounds */
```

## Code conventions

- Indentation: 4 spaces everywhere
- Section comments: `<!-- ═══ SECTION NAME ═══ -->`
- Section headers: `<h3>` eyebrow (font-mono, tracked, colored) + `<h2>` title (font-serif, text-5xl md:text-6xl) + `<p>` subtitle
- Timeline entries: `flex gap-2` with year in `font-mono text-xl text-black/35 pt-0.5 pr-6`
- Modals: daisyUI `<dialog>`, `rounded-none`, `bg-blanc`, tricolor bar at top, `font-mono` labels, `font-serif` title

## Modals

Both pages have two modals:

- `#modal_dangerous` — "too dangerous" parody statement; triggered by all access/demo CTAs
- `#modal_legal` — legal notice; triggered by footer link

Modal pattern:
```html
<dialog id="modal_NAME" class="modal">
  <div class="modal-box max-w-2xl bg-blanc p-0 rounded-none overflow-hidden">
    <div class="h-1.5 w-full" style="background: linear-gradient(...)"></div>
    <div class="p-8 md:p-10">...</div>
  </div>
  <form method="dialog" class="modal-backdrop"><button>close</button></form>
</dialog>
```

## Editorial tone

Straight-faced official communications with jokes buried in the specifics. Serge Dupont-Machin is the founder/CMO. He always knows the investors personally. He always says things are going very well.

## When editing both pages

Always update both `index.html` and `fr/index.html` together. Check that the structural HTML is identical; only content and color classes should differ.
