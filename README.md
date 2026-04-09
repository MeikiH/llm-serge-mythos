# Serge Mythos

Parody landing page for **Serge Mythos** — the French LLM with maximum confidence, published by **HotTropic Labs**.

[www.serge-mythos.tech](https://www.serge-mythos.tech)

Serge Mythos is not a real product. Probably.

---

## Structure

```
serge-mythos/
├── index.html          # Landing page EN (root)
├── fr/
│   └── index.html      # Landing page FR
├── img/
│   ├── serge-dupont-machin-avatar.png
│   └── serge-dupont-machin.png
```

## Stack

No build step. Everything runs in the browser.

| Library | Version | Usage |
|---------|---------|-------|
| [Tailwind CSS Browser](https://tailwindcss.com/blog/tailwindcss-v4) | 4 (CDN) | Utility classes + `@theme {}` custom tokens |
| [daisyUI](https://daisyui.com) | 5 (CDN) | Modal component (`<dialog>`) |
| [AOS](https://michalsnik.github.io/aos/) | 2.3.4 | Scroll animations |
| [Font Awesome](https://fontawesome.com) | 6.7.2 | Icons in use case cards |
| Google Fonts | — | Playfair Display · DM Sans · Space Mono |

## Design tokens (Tailwind `@theme`)

```
--color-bleu:       #002395   (French flag blue)
--color-rouge:      #ED2939   (French flag red)
--color-or:         #C9A84C   (gold accent)
--color-blanc:      #EDECE8   (off-white background)
--color-gris:       #1a1a1a   (near-black text)
--color-gris-clair: #f2f1ed   (light grey sections)
```

## Local development

Open `index.html` or `fr/index.html` directly in a browser. No build step, no server required.

## Modals

Two daisyUI modals on each page:

- `modal_dangerous` — triggered by all "Request Early Access" / "Request Demo" CTAs. Parody statement suspending early access due to Serge's unsafe behavior.
- `modal_legal` — triggered by "Legal Notice" in the footer.

## Brand hierarchy

```
HotTropic Labs  (company — "Makers of Serge")
    └── Serge           (base LLM)
            └── Serge Mythos    (frontier model — this site)
```

Mirrors the Anthropic → Claude → Claude Mythos structure. Serge personally knows the investors. The leak was an agentic GTM strategy.
