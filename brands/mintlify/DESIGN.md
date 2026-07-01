# Mintlify Design System

## Overview

Mintlify is the knowledge infrastructure platform for the agent web. The design language is warm, precise, and paperlike — distinguishing itself from the cold white/black of most dev tools through a distinctive warm off-white background and two-tone emerald green brand mark. Light-mode-first.

**Brand positioning:** "The knowledge infrastructure agents build on" — self-updating documentation for startups, enterprises, and agents.

---

## Colors

### Brand Green
| Token | Hex | Usage |
|-------|-----|-------|
| `--color-brand-base` (dark) | `#18e299` | Primary brand — dark mode CTAs, links, accents |
| `--color-brand-base` (light) | `#0c8c5e` | Primary brand — light mode CTAs, links, accents |
| `--color-brand-vivid` | `#1fa77a` | Hover, emphasis |
| `--color-mint-dark` | `#17cf85` | Accent on dark backgrounds |

The leaf mark uses exactly two tones: `#18E299` (bright mint, top shape) and `#0C8C5E` (dark green, bottom two shapes). These are fixed and must not be altered.

### Light Mode Backgrounds
| Token | Hex | Usage |
|-------|-----|-------|
| `--color-background-primary` | `#fefdfb` | Page background — warm off-white, never pure white |
| `--color-background-secondary` | `#faf8f5` | Cards, sidebars, secondary surfaces |
| `--color-background-tertiary` | `#ebe9e6` | Raised chips, badges, hover states |
| `--color-background-main` | `#ffffff` | Doc content area only |
| `--color-background-gray-subtle` | `#f9f8f7` | Subtle fills |
| `--color-border-line` | `#f1f0ee` | Primary border — very subtle warm gray |

### Dark Mode Backgrounds
| Token | Hex | Usage |
|-------|-----|-------|
| `--color-background-primary` | `#0a0b0f` | Page background |
| `--color-background-secondary` | `#121715` | Cards, sidebars |
| `--color-background-tertiary` | `#485450` | Raised elements |
| `--color-background-gray-subtle` | `#110a03` | Subtle dark fill |
| `--color-border-line` | `#1e1f21` | Primary border |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--color-text-main` (light) | `#08090a` | Primary text |
| `--color-text-main` (dark) | `#ffffff` | Primary text |

---

## Typography

### Font Stack
| Role | Family | Source |
|------|--------|--------|
| Display / H1 | ABCArizonaFlare Regular | `https://www.mintlify.com/_next/static/media/ABCArizonaFlare_Regular-s.p.957a285d.otf` |
| UI / Body | Inter Variable | `https://www.mintlify.com/_next/static/media/InterVariable-s.p.494bb210.ttf` |
| Code / Mono | PaperMono | `https://www.mintlify.com/_next/static/media/PaperMono-s.p.9e1cd850.woff2` |

All three font files are served with `Access-Control-Allow-Origin: *` from `www.mintlify.com`.

### Type Scale
| Role | Font | Size | Weight | Line Height |
|------|------|------|--------|-------------|
| Display | ABCArizonaFlare | 48–52px | 400 | 1.1 |
| H1 (docs) | ABCArizonaFlare | 28px | 400 | 1.2 |
| H2 | Inter Variable | 20px | 600 | 1.3 |
| H3 | Inter Variable | 16px | 600 | 1.4 |
| Body | Inter Variable | 15px | 400 | 1.7 |
| Small / label | Inter Variable | 13px | 500 | 1.5 |
| Caption | Inter Variable | 12px | 400 | 1.5 |
| Code | PaperMono | 13px | 400 | 1.6 |
| Nav label | PaperMono | 10px | 600 | — |

ABCArizonaFlare is a proprietary serif (Commercial Type). It is used exclusively for marketing display text and doc page headings — never for UI labels or body copy.

---

## Logo

The wordmark SVG (`viewBox="0 0 104 24"`) has two parts:

**Leaf mark (3 paths):**
- Top shape: `fill="#18E299"` (bright mint)
- Bottom-left shape: `fill="#0C8C5E"` (dark green)
- Bottom-right shape: `fill="#0C8C5E"` (dark green)

**Wordmark text paths:** `fill="var(--color-text-main)"` — automatically inherits the CSS variable, making it adapt to dark/light mode without JS.

The leaf mark colors are invariant across themes. Only the text portion adapts.

---

## Spacing & Shape

| Property | Value |
|----------|-------|
| Border radius — buttons, inputs | 4px |
| Border radius — cards, callouts | 8px |
| Border radius — modals | 12px |
| Border radius — badges | 100px (pill) |
| Elevation | None — Mintlify uses borders, not shadows |
| Grid gutter | 7 (Tailwind custom grid-layout) |

---

## Components

### Buttons
- **Primary:** `background: var(--color-text-main)` (inverted — dark bg on light mode, white bg on dark mode), `color: var(--color-background-primary)`, radius 4px, padding `10px 20px`, weight 500, size 14px.
- **Ghost / Outline:** transparent bg, `border: 1px solid var(--color-border-line)`, hover `border-color: var(--color-brand-base)`.
- No `border-radius` above 4px for interactive controls.

CTA labels used: "Get started", "Contact sales", "Read customer stories", "For enterprises", "For startups".

### Badges
Pill-shaped (100px radius), PaperMono font, 11px/500. Color families:
- Brand: bg `color-mix(in srgb, brand 12%, transparent)`, text `var(--color-brand-base)`
- Gray: bg `var(--color-background-tertiary)`, text secondary
- Warning: amber tones
- Danger: red tones

### Callouts
`border-radius: 8px`, `border: 1px solid`, filled with 5% brand tint. Types: tip (brand/green), warning (amber), note (gray).

### Code Blocks
Background `var(--color-background-gray-subtle)`, PaperMono 13px, brand-colored command prefixes (`$`, JSON keys).

---

## Signature Component — Docs Viewer

The most iconic Mintlify UI pattern: the documentation viewer with sidebar navigation and content area, combined with CMD+K search.

**Layout:** Two-panel — 220px fixed sidebar + fluid content area.

**Sidebar:**
- Search bar with ⌘K shortcut hint
- Grouped navigation: section group labels in PaperMono 10px uppercase
- Nav items: 13px Inter, active state uses brand left-border + tinted background

**Content area:**
- ABCArizonaFlare h1 for page title
- Inter body text at 15px/1.7
- PaperMono code blocks with brand-colored keywords
- Brand-tinted callout boxes

**CMD+K modal:**
- Full-width input at top
- Filterable page results with icon + title + path
- Keyboard navigation (↑↓ navigate, ↵ open, Esc close)

---

## Guardrails

### DO
- Use `#fefdfb` (warm off-white) as the light mode page background — it is the single most distinctive visual element
- Use ABCArizonaFlare exclusively for display and doc headings; never for UI labels or body text
- Use `#18e299` for dark mode brand; `#0c8c5e` for light mode — they are not interchangeable
- Use PaperMono for all code, metadata labels, and section identifiers
- Keep border-radius at 4px for interactive elements; elevation via borders not shadows

### DON'T
- Use pure white (`#ffffff`) as the main page background in light mode
- Use `#18e299` directly on light mode backgrounds — it fails contrast
- Add drop shadows to cards — use subtle borders instead
- Use font-weight above 600 for Inter in UI contexts
- Alter the two-tone green of the leaf mark
- Use the brand green for decorative elements — reserve it for interactive and semantic use
