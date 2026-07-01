# MongoDB Design System

## Overview

MongoDB is the leading document database platform. "One data platform. Unlimited AI potential." — the design language pairs a deep dark navy with a vivid leafy green, balancing enterprise credibility with developer approachability. Dark-first.

**Brand positioning:** Developer-first, scalable, AI-native data platform. Atlas is the flagship cloud product.

---

## Colors

### Green Scale (Primary Brand)
| Token | Hex | Usage |
|-------|-----|-------|
| `--brand` | `#00ED64` | Primary CTA buttons, active states, brand accent |
| `--brand-hover` | `#00AA57` | Hover on green elements |
| `--brand-dark` | `#00684A` | Dark green — success text on light bg, secondary fills |
| `--brand-deepest` | `#014E3D` | Deepest green for section bgs |
| `--brand-tint` | `rgba(0,237,100,0.08)` | Connected status bg, active nav tint |

### Navy Scale (Backgrounds)
| Token | Hex | Usage |
|-------|-----|-------|
| `--navy-deepest` | `#061621` | Hero gradient, very deep bg |
| `--navy-primary` | `#001E2B` | **Main dark bg — the single most identifiable MongoDB color** |
| `--navy-surface` | `#21313C` | Cards, sidebar panels |
| `--navy-raised` | `#3D4F58` | Raised elements, hover states, popovers |

### Slate Scale (Neutral)
| Token | Hex | Usage |
|-------|-----|-------|
| `--slate-500` | `#5D6C74` | Muted text, disabled, placeholders |
| `--slate-400` | `#B8C4C2` | Secondary text on dark bg, light borders |
| `--slate-200` | `#E7EEEC` | Light mode borders, light bg dividers |
| `--slate-100` | `#F5F7FA` | Light mode subtle surface |

### Blue (Informational)
| Token | Hex | Usage |
|-------|-----|-------|
| `--blue` | `#006CFA` | Links, info states, secondary CTA |

### Semantic Tokens
| Token | Light | Dark |
|-------|-------|------|
| `--bg` | `#ffffff` | `#001E2B` |
| `--bg2` | `#F5F7FA` | `#061621` |
| `--surface` | `#ffffff` | `#21313C` |
| `--raised` | `#E7EEEC` | `#3D4F58` |
| `--border` | `#E7EEEC` | `#3D4F58` |
| `--text` | `#001E2B` | `#ffffff` |
| `--text2` | `#3D4F58` | `#B8C4C2` |
| `--text3` | `#5D6C74` | `#5D6C74` |
| `--brand` | `#00684A` | `#00ED64` |
| `--logo-text` | `#001E2B` | `#ffffff` |

---

## Typography

### Font Stack
| Role | Family | CDN |
|------|--------|-----|
| Display / Marketing | MongoDBValueSerif | `https://static.mongodb.com/com/fonts/MongoDBValueSerif-Regular.woff2` |
| Display Bold | MongoDBValueSerif Bold | `https://static.mongodb.com/com/fonts/MongoDBValueSerif-Bold.woff2` |
| UI / Body | EuclidCircularA Regular | `https://static.mongodb.com/com/fonts/EuclidCircularA-Regular-WebXL.woff2` |
| UI Medium | EuclidCircularA Medium | `https://static.mongodb.com/com/fonts/EuclidCircularA-Medium-WebXL.woff2` |
| Alternate Display | AkzidenzGroteskBQ Light | `https://static.mongodb.com/com/fonts/akzidenzgroteskbq_light-webfont.woff2` |
| Code / Queries | Source Code Pro | `https://static.mongodb.com/com/fonts/SourceCodePro-Regular.ttf` |

All fonts are served from `static.mongodb.com` with `Access-Control-Allow-Origin: *`.

### Type Scale
| Role | Font | Size | Weight | Line Height |
|------|------|------|--------|-------------|
| Hero / Display | MongoDBValueSerif | 52px | 700 | 1.05 |
| H1 | MongoDBValueSerif | 32px | 400 | 1.2 |
| H2 | EuclidCircularA | 20px | 500 | 1.3 |
| H3 | EuclidCircularA | 16px | 500 | 1.4 |
| Body | EuclidCircularA | 15px | 400 | 1.65 |
| Small / Label | EuclidCircularA | 13px | 400 | 1.5 |
| Code / Query | Source Code Pro | 13px | 400 | 1.6 |

MongoDBValueSerif is a proprietary serif used exclusively for marketing headings and hero copy. EuclidCircularA handles all UI and body text. Source Code Pro is mandatory for all query, JSON, and `_id` fields.

---

## Logo

The MongoDB wordmark SVG (`viewBox="0 0 1102 278"`) has two distinct parts:

**Leaf mark (first `<path>`):**
A tall teardrop/leaf shape with an internal spine. Color is always `#00ED64` (bright green) — fixed regardless of theme. This is the most protected brand element.

**Wordmark letters:**
Six letter-path groups for "MongoDB". Use `fill="var(--logo-text)"` so the text adapts to dark/light automatically.

**Theming rule:** Leaf = always `#00ED64`. Text = `var(--logo-text)`.

---

## Spacing & Shape

| Property | Value |
|----------|-------|
| Border radius — buttons, inputs | 6px |
| Border radius — cards, panels | 10px |
| Border radius — badges, chips | 4px |
| Border radius — modals | 14px |
| Elevation | Subtle — `0 1px 4px rgba(0,0,0,0.4)` on dark surfaces |

---

## Components

### Buttons
- **Primary:** `background: var(--brand)`, `color: #001E2B` (always dark text — even on dark-mode green), radius 6px, padding `10px 20px`, weight 500, EuclidCircularA.
- **Ghost:** transparent, `border: 1px solid var(--border)`, hover border switches to `var(--brand)`.
- **Danger:** `#FF6960` bg, white text.

CTAs on site: "Try Free", "Talk to an Expert", "Get started for free", "Explore Atlas".

### Connection Status Badges
- **Connected:** `#00ED64` text on `rgba(0,237,100,0.08)` bg — pulsing green dot
- **Disconnected:** `#FF6960` text on red-tinted bg — static red dot
- **Connecting:** `#006CFA` text on blue-tinted bg — animated dot

### Collection Chips
Small uppercase label, EuclidCircularA 11px/500, radius 4px:
- Document: navy/slate bg
- Index: blue tint
- Schema: green tint

### Document Cards
`background: var(--surface)`, `border: 1px solid var(--border)`, radius 10px:
- Header: `background: var(--raised)`, field names in Source Code Pro, green-tinted
- Values: Source Code Pro, white text on dark
- `_id` field: `color: var(--brand)`, always monospace

---

## Signature Component — Atlas Data Explorer

The most recognizable MongoDB UI: the Atlas Data Explorer showing a cluster's databases, collections, and live document data with MQL filter support.

**Layout:** Left sidebar (240px) + main content area.

**Sidebar:**
- Cluster name at top with connection status badge (Connected — green)
- Database tree: collapsed → click to expand → reveals collections
- Collections listed with doc count in slate text
- Active collection: green left-border + brand-tint bg

**Main content:**
- Breadcrumb: `Cluster0 / sample_mflix / movies`
- Filter bar: Source Code Pro query input with `{ }` placeholder, "Find" CTA button
- Document count display: "Displaying documents 1–20 of 21,349"
- Table view: columns for `_id`, `title`, `year`, `genre`, `runtime`
- Row hover: `background: var(--raised)`
- Click row → expandable inline JSON panel with full document

**JSON document panel:**
```
{
  "_id": ObjectId("573a1390f29313caabcd4135"),
  "title": "The Perils of Pauline",
  "year": 1914,
  "genres": ["Action", "Adventure", "Romance"],
  "runtime": 199,
  "cast": ["Pearl White", "Crane Wilbur", ...]
}
```

---

## Guardrails

### DO
- Use `#001E2B` (dark navy) as the primary dark background — it is MongoDB's visual identity
- Keep the leaf mark always `#00ED64` — it is invariant across themes
- Use Source Code Pro for ALL query fields, JSON values, collection names, and `_id` display
- Put dark text (`#001E2B`) on the primary green CTA button — the contrast is intentional
- Reserve `#00ED64` for brand and success/connected states — it is not a decorative color

### DON'T
- Use generic black or gray as the dark background — `#001E2B` navy IS the brand signal
- Display `_id` fields in a proportional font — always monospace
- Use `#00ED64` for warning or danger states — semantic colors must stay distinct
- Use green decoratively (gradients, borders, non-interactive highlights)
- Exceed 10px border-radius on product UI elements — MongoDB is enterprise-grade, not playful
