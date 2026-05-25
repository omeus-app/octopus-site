# octopus-site — Marketing Site

## Role in Octopus

The site is the **public-facing marketing presence** for octopus. Hosted at octopus.you via GitHub Pages. It communicates the product vision, demonstrates the reading experience, and drives waitlist signups.

## What This Repository Contains

- `index.html` — Landing page (hero, problem statement, pitch, subscribe CTA)
- `demo.html` — Interactive demo wrapper (intro overlay → reading engine iframe)
- `engine/reading-engine.html` — Full reading engine prototype (tap-to-explore, pull gestures, Bento Grid sidecar)
- `css/style.css` — Design system stylesheet (CSS variables, typography, palette)
- Static assets (logo, OG image, fonts)

## Dual Purpose

### 1. Marketing
Communicates the octopus thesis to potential users:
- The Buffet Problem / Intellectual Diabetes
- The 10-Kilometer Rule / Gym metaphor
- The reading experience (live demo)
- Waitlist signup → Substack (`omeus.substack.com/subscribe`)

### 2. UX Source of Truth
The `engine/reading-engine.html` file is the **definitive interaction prototype** for the reading experience. It defines:
- Tap-to-explore gesture behavior
- Bento Grid sidecar layout (3-column: entities, words, idioms)
- Pull-down (story context) and pull-up (reflective synthesis) panels
- Long-press annotation flow
- Zero-UI reading surface behavior
- Design system: CSS variables, Cormorant Garamond serif, Inter sans-serif, warm palette

This prototype is the reference that octopus-spencer will implement natively.

## Design System (CSS Variables)

```css
--bg:          #FDFAF6;       /* Warm off-white background */
--ink:         #1C1917;       /* Primary text */
--ink-soft:    #57534E;       /* Secondary text */
--ink-ghost:   #A8A29E;       /* Tertiary/hint text */
--brand:       #E06C2B;       /* Brand orange */
--brand-deep:  #9B3D12;       /* Deep brand (buttons, emphasis) */
--brand-glow:  rgba(224, 108, 43, 0.12);  /* Subtle brand highlight */
--serif:       'Cormorant Garamond', Georgia, serif;
--sans:        'Inter', -apple-system, sans-serif;
```

## Boundary — What This Repository Does NOT Do

- Does NOT serve the actual product (that's octopus-spencer)
- Does NOT process books or serve dynamic content
- Does NOT handle authentication or user state
- Does NOT contain architecture design or PoCs (that's octopus-racoon-city)
- Is NOT a web app — it is a static marketing site

## Tech Stack

- Static HTML + CSS + vanilla JavaScript
- No build system, no framework
- GitHub Pages hosting
- Zero dependencies

## Status

Polished and live. Updated when marketing messaging or the demo experience evolves.

## Adjacent Repositories

| Repository | Relationship |
|-----------|-------------|
| **octopus-spencer** | Spencer implements the native version of what reading-engine.html prototypes |
| **octopus-alice** | UX mockups in alice informed the site's demo design |
| **octopus-racoon-city** | No direct dependency — separate concerns (marketing vs. architecture) |
| **octopus-hive** | The demo uses sample content that the hive pipeline would produce at scale |
