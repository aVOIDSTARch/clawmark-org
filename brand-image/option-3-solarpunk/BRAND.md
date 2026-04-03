# Option 3: SOLARPUNK

**Tagline:** "Fair exchange between all things."
**Mood:** Optimistic futurism rooted in the natural world. If Option 1 is cosmic and Option 2 is monastic, this one is alive. It takes the "relationship between digital and physical entities" literally — the visual language borrows from biology, growth patterns, and symbiosis. But it's not hippie or soft. The execution is precise, technical, and unmistakably engineered. Think: a circuit board that grew like a vine.

---

## Personality

Confident warmth. This brand believes the future is bright — not in a naive way, but because it's building the infrastructure to make it bright. It speaks plainly, avoids jargon where possible, and treats its audience as partners in something worth building. There's an undercurrent of rebellion: this is not how finance usually looks, and that's intentional.

**If this brand were a person:** A systems biologist who left academia to build cooperative infrastructure. Wears earth tones but carries a laptop covered in stickers for obscure programming languages.

**If this brand were architecture:** Bjarke Ingels' CopenHill — a waste-to-energy plant with a ski slope on the roof. Infrastructure that is also beautiful, also public, also fun.

---

## Color Palette

### Primary Colors

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| **Deep Soil** | Rich near-black with green undertone | `#0C1210` | Background, primary surface |
| **Photon Green** | Vivid bright green | `#22C55E` | Primary accent, CTAs, logo, growth |
| **Parchment** | Warm off-white with yellow tint | `#F5F0E8` | Body text, headings |

### Secondary Colors

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| **Copper** | Warm metallic orange | `#D4782F` | Secondary accent, human-side references |
| **Sky** | Clear light blue | `#38BDF8` | Tertiary accent, digital-side references |
| **Moss** | Dark muted green | `#1A3A2A` | Cards, elevated surfaces |
| **Bark** | Medium brown-gray | `#6B6358` | Secondary text, borders |

### Dual Accent System

Photon Green is the primary brand color. But the dual accent of **Copper** (physical/human) and **Sky** (digital/agent) can be used to visually represent the two realms when they appear together. This is the visual language for the core concept: physical entities and digital entities meeting as equals.

### Gradient

Subtle gradient from Copper through Photon Green to Sky — used only on the logo or as a rare divider. Represents the spectrum from physical to digital with growth (green) at the center.

---

## Typography

| Role | Font | Weight | Size Range |
|------|------|--------|------------|
| **Display/Logo** | **Outfit** | Bold (700) | 48-72px |
| **Headings** | **Outfit** | SemiBold (600) | 24-40px |
| **Body** | **Source Sans 3** | Regular (400) | 16-18px |
| **Code/Technical** | **Source Code Pro** | Regular (400) | 14-16px |
| **Captions/Labels** | **Outfit** | Medium (500) | 12-14px |

Outfit is geometric but friendly — it has the precision of a grotesque without the coldness. Source Sans 3 (Adobe's open-source workhorse) is supremely readable and pairs perfectly. Source Code Pro for technical content keeps the family consistent.

---

## Logo Concept

Three diagonal claw marks that transition from organic (rough, natural edges on the left) to geometric (clean, precise edges on the right) — a single visual that captures the physical-to-digital bridge. The strokes are Photon Green. Below: "CLAWMARK" in Outfit Bold.

Alternate version: the three slashes emerge from a circle (representing wholeness/exchange), with the left half of each stroke textured and the right half smooth.

The logo should feel like it was designed by nature and refined by an engineer.

---

## UI Patterns

### Landing Page Hero

```
┌──────────────────────────────────────────────┐
│  [deep soil background #0C1210]              │
│                                              │
│  ╱╱╱  ← claw mark, organic-to-geometric     │
│        left strokes slightly rough,          │
│        right strokes sharp                   │
│                                              │
│  CLAWMARK                                    │
│  Fair exchange between all things.           │
│                                              │
│  ──────────────────────────────────────────  │
│  thin photon green divider                   │
│                                              │
│  Two columns, representing the two realms:   │
│                                              │
│  ┌── PHYSICAL ──────┐ ┌── DIGITAL ──────┐   │
│  │                  │ │                  │   │
│  │  Human workers   │ │  AI agents       │   │
│  │  craft skill     │ │  compute power   │   │
│  │  judgment        │ │  speed           │   │
│  │  presence        │ │  scale           │   │
│  │                  │ │                  │   │
│  │  [copper accent] │ │  [sky accent]    │   │
│  └──────────────────┘ └──────────────────┘   │
│                                              │
│         ↓ photon green arrow ↓               │
│                                              │
│  ┌── CLAWMARK ──────────────────────────┐    │
│  │                                      │    │
│  │  One coin. One dollar. One serial    │    │
│  │  number. The trustworthy medium      │    │
│  │  of exchange between both realms.    │    │
│  │                                      │    │
│  │  [Read the Whitepaper →]             │    │
│  │                                      │    │
│  └──────────────────────────────────────┘    │
│  ↑ moss card with photon green accent        │
│                                              │
│  ──────────────────────────────────────────  │
│                                              │
│  Principles section:                         │
│  Cards in a 2x3 grid, each with a           │
│  small green dot + principle title + one     │
│  sentence. Moss background, parchment text.  │
│                                              │
└──────────────────────────────────────────────┘
```

### Navigation

Top bar with subtle `#0C1210` → `#1A3A2A` depth. Logo left. Links right in Parchment, with Photon Green underline on hover. Active page has a small green dot before the link text.

### Cards/Sections

Moss (`#1A3A2A`) cards with 1px `#2D4A3A` border, 6px border-radius (slightly rounded — organic, not sharp, not bubbly). Content sections alternate between full-bleed Deep Soil and Moss-card layouts.

### Buttons

- Primary: Photon Green (`#22C55E`) background, Deep Soil text, 4px border-radius
- Secondary: Transparent, 1px Photon Green border, Photon Green text
- Copper variant: Copper background for physical-realm CTAs
- Sky variant: Sky background for digital-realm CTAs
- Hover: lighten 10%, subtle lift (transform: translateY(-1px))

---

## Sample CSS Variables

```css
:root {
  /* Primary */
  --color-bg: #0C1210;
  --color-accent: #22C55E;
  --color-text: #F5F0E8;

  /* Secondary */
  --color-copper: #D4782F;
  --color-sky: #38BDF8;
  --color-surface: #1A3A2A;
  --color-border: #2D4A3A;
  --color-muted: #6B6358;

  /* Gradient */
  --gradient-bridge: linear-gradient(135deg, #D4782F, #22C55E, #38BDF8);

  /* Typography */
  --font-display: 'Outfit', sans-serif;
  --font-body: 'Source Sans 3', sans-serif;
  --font-mono: 'Source Code Pro', monospace;

  /* Spacing */
  --space-xs: 0.25rem;
  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 2rem;
  --space-xl: 4rem;
  --space-2xl: 8rem;

  /* Borders */
  --radius: 6px;
}
```

---

## The Dual-Realm Visual Language

This is the unique feature of this brand option. Whenever the site discusses the relationship between physical and digital entities, the visual system supports it:

- **Copper** = physical realm (humans, craft, judgment, presence)
- **Photon Green** = the bridge (CLAWMARK, the exchange, the protocol)
- **Sky** = digital realm (agents, compute, speed, scale)

This can be used in:
- The landing page two-column layout
- Icons or badges next to job types on the marketplace
- The explorer, showing which transactions involve agent vs human wallets
- Charts on the dashboard, showing agent vs human activity

---

## Emotional Register

| Trait | How It Shows Up |
|-------|----------------|
| **Optimistic** | Green as primary (growth, life, go), "fair exchange" language, the symbiosis metaphor |
| **Professional** | Outfit's geometric precision, Source Sans readability, structured grid layouts |
| **Futuristic** | Dark palette, the organic-to-geometric logo, the dual-realm system, post-quantum language |
| **Grounded** | Earth tones (soil, copper, bark, moss), the word "parchment" in the palette, the nature metaphors |
| **Avant-garde edge** | The organic-to-geometric transition, the copper/sky duality, calling the marketplace a place where "all things" exchange |

---

## What This Brand Is NOT

- Not hippie or soft. The execution is precise and technical. "Solarpunk" is the mood, not the aesthetic.
- Not green-washed. The green accent is about growth and the future, not environmentalism (though that's a fine association).
- Not childish. The color palette is rich and deep, not bright and cartoonish.
- Not complex on the surface. The dual-realm system is powerful but only appears when relevant — most pages are just Deep Soil + Photon Green + Parchment.
- Not a gardening website. The natural metaphors are subtle. The site looks like a technology company, not a seed catalog.
