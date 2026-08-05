# jamiendreaj.com

My personal portfolio — the things I've designed, built, and shipped.

Built as a static site with no framework and no build step: two files, plain HTML
and CSS, and a small amount of vanilla JavaScript. That was a deliberate choice.
The site is fast, has no dependencies to age or break, and can be hosted anywhere.

## Running it locally

No install step. From this folder:

```bash
python3 -m http.server 4321
```

Then open <http://localhost:4321>.

## What's in here

| File | Purpose |
| --- | --- |
| `index.html` | The whole page — content and structure |
| `styles.css` | Design system, layout, animation |
| `assets/screenshots/` | App screenshots and icons |

## Design notes

The look is "liquid glass": a drifting aurora background built from blurred
radial gradients, a wave horizon, thin metallic rings that intersect as they
move, and frosted-glass cards that let the light through from behind.

A few constraints I held to:

- **System fonts only** (`-apple-system` / SF Pro) — no web font downloads
- **Only `transform` and `opacity` animate**, so everything stays on the GPU
- **Full `prefers-reduced-motion` support** — motion freezes rather than degrades
- **`prefers-reduced-transparency`** swaps frosted panels for solid ones
- Hover effects gated behind `@media (hover: hover)` so they don't misfire on touch
- Visible `:focus-visible` rings for keyboard navigation

## Stack

HTML, CSS, vanilla JavaScript. No framework, no bundler, no dependencies.

---

Jamie X. Ndreaj
