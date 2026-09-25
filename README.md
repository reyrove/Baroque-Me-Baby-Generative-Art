# Baroque Me Baby

**A seed-based generative system for baroque-style geometric ornament.**

A catalogue of computational textile compositions for fashion, textile and surface design — algorithmically drawn, seed-documented, and ready for production.

---

## Overview

Baroque Me Baby is a generative design system rather than a single artwork. Each composition is built from a baroque-style frame that wraps a layered geometric interior — concentric, radial, polygonal, or organic — and is fully reproducible from a single numeric seed.

The system is designed for:

- **Fashion houses** adapting ornament for apparel and accessories
- **Textile studios** developing repeat patterns and yardage
- **Surface designers** working across print, wallpaper, and interior applications

Every composition can be licensed, adapted, or commissioned to a brief.

---

## Concept

Ornament, when it is *generated* rather than drawn, becomes a language — infinite, precise, and quietly reproducible.

The baroque frame has always been a computational structure: symmetrical, decorative, endlessly repeatable. Baroque Me Baby translates that structure into code. Each composition begins with a frame and unfolds inward through layers of ornament, until the interior becomes its own small architecture.

The palette, the number of layers, the style of the interior, and the density of decoration are all derived from a single numeric seed.

---

## Features

- **Seed-based generation** — every composition is defined by a numeric seed and can be regenerated exactly
- **Deterministic output** — the same seed always produces the same composition
- **Four interior styles** — Concentric, Radial, Polygonal, Organic
- **Adaptive surfaces** — one seed applied across print, scarf, textile, and wall formats
- **Archive** — eight curated seeds available for immediate loading
- **Download** — export any composition as a high-resolution PNG
- **Keyboard shortcuts** — `R` for new seed, `S` to save

---

## Project Structure

```
.
├── index.html          # Main catalogue page
├── images/
│   ├── fav.svg         # Favicon
│   ├── tote.png        # Mockup: tote bag
│   ├── tee.png         # Mockup: t-shirt
│   └── cushion.png     # Mockup: cushion
└── README.md
```

---

## How It Works

### The Seed

A numeric seed (a large integer) initializes a deterministic pseudo-random generator. From this seed, the system derives:

- Background and frame palette
- Number of layers (typically 5–15)
- Interior style (Concentric, Radial, Polygonal, Organic)
- Decoration count (typically 8–16)
- Rotation offsets and per-layer variation

Because the generator is deterministic, the same seed always produces the same composition — on any device, at any time.

### The Frame

A baroque border is drawn first, with:

- A rounded rectangular main frame in one of three rotating colour schemes
- An inner white field
- Decorative elements placed radially around the frame edge
- Ornamented corners with petal-like rosettes

### The Interior

Layered geometric marks are drawn inside the frame. Each layer rotates slightly relative to the previous one, creating a moiré-like interference that gives the composition its sense of depth.

The interior style is chosen per seed:

| Style       | Description                                              |
|-------------|----------------------------------------------------------|
| Concentric  | Nested circles contracting toward the center             |
| Radial      | Lines radiating outward from a partially random inner ring |
| Polygonal   | N-sided polygons, one per layer                          |
| Organic     | Irregular closed curves with variable radius             |

### The Surfaces

The same seed is rendered across four surface formats:

| Surface  | Aspect | Material          |
|----------|--------|-------------------|
| Print    | 1 : 1  | Cotton rag        |
| Scarf    | 3 : 1  | Twill silk        |
| Textile  | 4 : 3  | Fabric yardage    |
| Wall     | 2 : 3  | Wallpaper         |

Each surface uses the same underlying seed and structural logic — only the repeat, orientation, and scale change.

---

## Usage

### In the browser

1. Open `index.html` in any modern browser.
2. Click **New Seed** to generate a new composition.
3. Click **Download** to save the current plate as a PNG.
4. Scroll to the **Archive** section and click any plate to load it into Plate 001.

### Keyboard shortcuts

| Key | Action          |
|-----|-----------------|
| `R` | New seed        |
| `S` | Save as PNG     |

### Reproducing a composition

Each composition is identified by an 8-digit seed label displayed in the metadata panel. To reproduce a specific composition, note the seed and regenerate it programmatically:

```js
const rng = new RandomGenerator(seed);
renderComposition(canvas, { rng });
```

---

## Technical Notes

- **No build step.** The system is a single HTML file with inline CSS and JavaScript.
- **No dependencies.** All drawing is done with the native Canvas 2D API.
- **Deterministic.** The `RandomGenerator` class uses a xorshift-based PRNG seeded by an integer, so identical seeds produce identical outputs.
- **Responsive.** The layout adapts from large desktop down to very small mobile devices (tested at 360px viewport width).
- **Accessible.** Supports `prefers-reduced-motion`. Pinch-zoom is enabled.

### Browser support

Tested in current versions of:

- Chrome / Edge
- Firefox
- Safari (desktop and iOS)

---

## Licensing

All Baroque Me Baby compositions are **seed-documented** and available for licensing across textile, surface, and print applications.

- **Standard licenses** cover single-product production runs.
- **Commercial use, custom editions, or exclusive rights** are available on request.

Each license is issued against a specific seed ID. Regeneration of the same seed produces the identical composition — ensuring reproducibility between artist, studio, and manufacturer.

For licensing enquiries: [reyhanehdaneshdoost@gmail.com](mailto:reyhanehdaneshdoost@gmail.com)

---

## Commission

Baroque Me Baby is a generative design system, not a fixed artwork. It can be adapted for specific briefs:

| Service     | Description                                                       |
|-------------|-------------------------------------------------------------------|
| Licensing   | Existing seeds from the archive, licensed for production use      |
| Commission  | New compositions designed to your palette, repeat, and product    |
| Systems     | A private generative tool built for your studio's ongoing use     |

To begin a conversation: [reyhanehdaneshdoost@gmail.com](mailto:reyhanehdaneshdoost@gmail.com)

---

## Credits

- **Design & Generative System** — Reyhaneh Daneshdoost
- **Typefaces** — Cormorant Garamond · DM Mono
- **Platform** — Reyrove Studio
- **Edition** — Baroque Me Baby, Autumn 2026

### On AI tools

Where technical obstacles were encountered, AI tools were used for debugging and code optimization. Every structural, aesthetic, and conceptual decision remained the artist's own.

---

## Links

- Website — [reyrove.github.io](https://reyrove.github.io/)
- Instagram — [@rey._.rove](https://www.instagram.com/rey._.rove/)
- LinkedIn — [Reyhaneh Daneshdoost](https://www.linkedin.com/in/reyhaneh-daneshdoost-730481160/)
- X — [@reyrove](https://x.com/reyrove)

---

© Baroque Me Baby · All compositions reproducible by seed · Computational Textile Design