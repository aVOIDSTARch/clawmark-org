# Option 2: MONOLITH

**Tagline:** "The mark of work done."
**Mood:** 2001: A Space Odyssey meets Swiss design. Absolute confidence. Minimal to the point of severity, but the severity itself is the beauty. A black monolith in a field — you don't know who built it, but you know it was built by something smarter than you. Grounded wisdom expressed through restraint.

---

## Personality

Silent authority. The brand doesn't explain itself more than necessary. Every element earns its place. The typography does the heavy lifting. Color is used like a scalpel — one cut, precise, meaningful. This brand trusts its audience to be intelligent.

**If this brand were a person:** A senior cryptographer who speaks in complete sentences, never rushes, and is always the most interesting person in the room precisely because they say the least.

**If this brand were architecture:** Mies van der Rohe's Barcelona Pavilion — marble, glass, water, and nothing else.

---

## Color Palette

### Primary Colors

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| **Obsidian** | True deep black | `#09090B` | Background, primary surface |
| **Amber** | Warm golden accent | `#F59E0B` | Primary accent — the one color that matters |
| **Bone** | Warm white | `#FAFAF9` | Body text, headings |

### Secondary Colors

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| **Stone** | Warm medium gray | `#78716C` | Secondary text, borders |
| **Charcoal** | Dark warm gray | `#1C1917` | Cards, elevated surfaces |
| **Ash** | Light warm gray | `#A8A29E` | Muted text, timestamps |
| **Ember** | Deep orange | `#D97706` | Hover state for amber elements |

### No Gradient

This brand does not use gradients. Flat color only. The constraint is the point.

---

## Typography

| Role | Font | Weight | Size Range |
|------|------|--------|------------|
| **Display/Logo** | **IBM Plex Mono** | Bold (700) | 48-64px |
| **Headings** | **IBM Plex Mono** | Medium (500) | 24-36px |
| **Body** | **IBM Plex Sans** | Regular (400) | 16-18px |
| **Code/Technical** | **IBM Plex Mono** | Regular (400) | 14-16px |
| **Captions/Labels** | **IBM Plex Mono** | Regular (400) | 11-13px, uppercase, letter-spacing +1.5px |

IBM Plex is the most complete type system designed in the last decade. Mono for structure and authority. Sans for readability. The monospace headings are the signature move — they say "this was built by engineers, and we're proud of that."

---

## Logo Concept

Three parallel diagonal lines — the claw mark — rendered as solid, geometric strokes. No gradient, no glow. Pure geometry. The lines are Amber (`#F59E0B`) on Obsidian background. Below: "CLAWMARK" in IBM Plex Mono Bold, all caps, letter-spacing +3px.

The mark is deliberately simple. It could be stamped into metal. It could be etched into stone. It is the kind of logo that looks better the smaller it gets.

Alternate: the three slashes intersect a single horizontal line — the "mark" being left on a surface.

---

## UI Patterns

### Landing Page Hero

```
┌──────────────────────────────────────────────┐
│  [obsidian background #09090B]               │
│                                              │
│                                              │
│                                              │
│            ╱╱╱                               │
│                                              │
│         CLAWMARK                             │
│                                              │
│    The mark of work done.                    │
│                                              │
│                                              │
│                                              │
│  ──────────────────────────────────────────  │
│  1px amber line                              │
│                                              │
│  PHILOSOPHY    WHITEPAPER    REGULATORY      │
│  ↑ uppercase monospace links, Bone color,    │
│    amber underline on hover                  │
│                                              │
│                                              │
│  "Digital and physical entities deserve      │
│   equal standing in a labor market."         │
│                                              │
│  ↑ large IBM Plex Sans, centered,            │
│    maximum 60ch width                        │
│                                              │
│                                              │
│  ──────────────────────────────────────────  │
│                                              │
│  Three principles, vertically stacked:       │
│                                              │
│  01  EQUAL STANDING                          │
│      AI agents and human workers are         │
│      co-participants, not master and tool.   │
│                                              │
│  02  RADICAL TRANSPARENCY                    │
│      Every coin is serialized. Every block   │
│      is provably valid.                      │
│                                              │
│  03  POST-QUANTUM FROM DAY ONE              │
│      The cryptographic stack assumes          │
│      quantum computers exist today.          │
│                                              │
│  ↑ numbers in Amber, titles in Mono Bold,    │
│    body in Plex Sans Regular                 │
│                                              │
└──────────────────────────────────────────────┘
```

### Navigation

Minimal top bar. Logo left (small, monospace). Three or four links right, uppercase monospace, letter-spaced. No background — fully transparent, always. Active page indicated by a single amber dot or underline.

### Cards/Sections

No cards. Content is separated by horizontal rules (1px, `#1C1917` or amber for emphasis). Sections breathe with 6-8rem vertical padding. The page is one continuous vertical scroll with clear typographic hierarchy.

### Buttons

- Primary: Amber (`#F59E0B`) background, Obsidian text, no border-radius (square corners)
- Secondary: Bone text, 1px Bone border, square corners
- Hover: Ember (`#D97706`) background for primary; amber text for secondary
- No glow, no shadow, no animation. State changes are instant.

---

## Sample CSS Variables

```css
:root {
  /* Primary */
  --color-bg: #09090B;
  --color-accent: #F59E0B;
  --color-text: #FAFAF9;

  /* Secondary */
  --color-stone: #78716C;
  --color-surface: #1C1917;
  --color-ash: #A8A29E;
  --color-hover: #D97706;

  /* Typography */
  --font-display: 'IBM Plex Mono', monospace;
  --font-body: 'IBM Plex Sans', sans-serif;
  --font-mono: 'IBM Plex Mono', monospace;

  /* Spacing — larger, more dramatic */
  --space-xs: 0.25rem;
  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 2rem;
  --space-xl: 6rem;
  --space-2xl: 10rem;
}
```

---

## Emotional Register

| Trait | How It Shows Up |
|-------|----------------|
| **Optimistic** | Amber warmth (gold = value, trust, dawn), "work done" implies completion and fulfillment |
| **Professional** | IBM Plex precision, uppercase labels, Swiss-grid severity, no decoration |
| **Futuristic** | Full monospace headings, obsidian palette, the monolith metaphor, square corners |
| **Grounded** | Warm color temperature (amber/bone/stone, not blue/chrome), generous breathing room, numbered lists |
| **Avant-garde edge** | The radical minimalism itself is the edge. No gradients. No icons. No illustrations. Just type and one color. |

---

## What This Brand Is NOT

- Not decorative. There are no icons, no illustrations, no patterns. Typography IS the design.
- Not cold. The amber and warm grays keep it human despite the minimalism.
- Not trendy. This aesthetic will look as good in 10 years as it does today. That's the point.
- Not approachable in a hand-wavy way. It respects the audience by not dumbing anything down.
- Not busy. If something doesn't need to be there, it isn't.
