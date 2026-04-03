# Option 1: AURORA

**Tagline:** "Where realms converge."
**Mood:** Luminous optimism meets deep technical confidence. The aurora borealis as metaphor — something ancient, natural, and awe-inspiring that is also a product of physics most people don't understand. Grounded in science, beautiful in expression.

---

## Personality

Warm but precise. The brand feels like a brilliant professor who also happens to be a poet. It doesn't shout "FUTURE!" — it radiates it quietly. There's a sense of dawn, of something arriving that was always inevitable. Not cold, not corporate, not crypto-bro. Wise, luminous, and slightly otherworldly.

**If this brand were a person:** A calm, articulate futurist who quotes both Satoshi and Ursula K. Le Guin. Wears all black but with one piece of iridescent jewelry.

**If this brand were architecture:** A Tadao Ando concrete pavilion with a glass ceiling that reveals the northern lights.

---

## Color Palette

### Primary Colors

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| **Deep Space** | Near-black with blue undertone | `#0B0E17` | Background, primary surface |
| **Aurora Cyan** | Electric teal-cyan | `#00E5CC` | Primary accent, CTAs, links, logo glow |
| **Signal White** | Warm off-white | `#EAEDF3` | Body text, headings |

### Secondary Colors

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| **Aurora Violet** | Soft purple | `#7B61FF` | Secondary accent, hover states, charts |
| **Aurora Green** | Muted emerald | `#34D399` | Success states, positive indicators |
| **Frost** | Cool gray | `#6B7A99` | Secondary text, borders, muted elements |
| **Midnight** | Dark navy | `#141B2D` | Cards, elevated surfaces |

### Gradient

The signature gradient runs from Aurora Cyan (`#00E5CC`) through Aurora Violet (`#7B61FF`) — used sparingly on the logo, key dividers, or a subtle top-of-page border. Never as a background fill.

---

## Typography

| Role | Font | Weight | Size Range |
|------|------|--------|------------|
| **Display/Logo** | **Space Grotesk** | Bold (700) | 48-72px |
| **Headings** | **Space Grotesk** | Medium (500) | 24-40px |
| **Body** | **Inter** | Regular (400) | 16-18px |
| **Code/Technical** | **JetBrains Mono** | Regular (400) | 14-16px |
| **Captions/Labels** | **Inter** | Medium (500) | 12-14px, letter-spacing +0.5px |

Space Grotesk bridges geometric precision with humanist warmth. It says "engineered" without saying "cold." Inter is the most readable screen font ever made. JetBrains Mono signals technical seriousness.

---

## Logo Concept

A stylized **claw mark** — three diagonal slashes — rendered as light trails, like aurora streaks across a dark sky. The slashes have a subtle gradient (cyan → violet). Below or beside them, "CLAWMARK" in Space Grotesk Bold, letter-spaced +2px.

The mark works at any size: as a favicon (just the slashes), as a header logo (slashes + wordmark), and as a full lockup (slashes + wordmark + ".org" in Frost gray).

---

## UI Patterns

### Landing Page Hero

```
┌──────────────────────────────────────────────┐
│  [dark background #0B0E17]                   │
│                                              │
│  ╱╱╱  ← three aurora-gradient slash marks    │
│                                              │
│  CLAWMARK                                    │
│  Where realms converge.                      │
│                                              │
│  Furthering the relationship between         │
│  digital and physical entities through       │
│  fair market labor exchange.                 │
│                                              │
│  [Read the Whitepaper]  [Our Philosophy]     │
│   ↑ aurora cyan button   ↑ ghost button      │
│                                              │
│  ─────── subtle gradient divider ──────────  │
│                                              │
│  Three cards in a row:                       │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐        │
│  │ Equal   │ │ Radical │ │ Post-   │        │
│  │ Standing│ │Transpar-│ │ Quantum │        │
│  │         │ │  ency   │ │         │        │
│  │ [icon]  │ │ [icon]  │ │ [icon]  │        │
│  └─────────┘ └─────────┘ └─────────┘        │
│   #141B2D cards with #00E5CC icon accents    │
│                                              │
└──────────────────────────────────────────────┘
```

### Navigation

Top bar, fixed. Logo left, links right. No hamburger on desktop. Background goes from transparent to `#0B0E17` on scroll. Links in Signal White, active link underlined in Aurora Cyan.

### Cards/Sections

Dark elevated surfaces (`#141B2D`) with 1px border in `#1E293B`. Subtle box-shadow downward. No rounded corners larger than 4px — sharp is futuristic.

### Buttons

- Primary: Aurora Cyan (`#00E5CC`) background, `#0B0E17` text, 2px border-radius
- Secondary: Transparent, 1px Aurora Cyan border, Aurora Cyan text
- Hover: Subtle glow effect (box-shadow: 0 0 20px rgba(0, 229, 204, 0.3))

---

## Sample CSS Variables

```css
:root {
  /* Primary */
  --color-bg: #0B0E17;
  --color-accent: #00E5CC;
  --color-text: #EAEDF3;

  /* Secondary */
  --color-violet: #7B61FF;
  --color-green: #34D399;
  --color-muted: #6B7A99;
  --color-surface: #141B2D;
  --color-border: #1E293B;

  /* Gradient */
  --gradient-aurora: linear-gradient(135deg, #00E5CC, #7B61FF);

  /* Typography */
  --font-display: 'Space Grotesk', sans-serif;
  --font-body: 'Inter', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;

  /* Spacing */
  --space-xs: 0.25rem;
  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 2rem;
  --space-xl: 4rem;
  --space-2xl: 8rem;
}
```

---

## Emotional Register

| Trait | How It Shows Up |
|-------|----------------|
| **Optimistic** | Warm accent colors (cyan/green), "converge" language, upward visual motion |
| **Professional** | Space Grotesk precision, restrained use of color, no gradients on text |
| **Futuristic** | Dark palette, aurora gradient, monospace in technical contexts, post-quantum language |
| **Grounded** | Inter for body text (familiar, readable), generous whitespace, plain language in body copy |
| **Avant-garde edge** | The three-slash logo, gradient as a signature element, the word "realms" |

---

## What This Brand Is NOT

- Not neon-everything. The accent is restrained — one or two elements per page.
- Not a trading platform aesthetic. No green/red candles, no dashboard-first design.
- Not sterile. There's warmth in the typography and the aurora metaphor.
- Not playful or casual. This is serious infrastructure with beautiful execution.
