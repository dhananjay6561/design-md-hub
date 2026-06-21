# MongoDB Design System

## Overview
MongoDB is the world's most popular NoSQL database. The design language pairs a deep dark navy with a vivid leafy green — professional, modern, and instantly recognizable. The brand balances enterprise credibility with developer approachability.

**Brand personality:** Scalable, powerful, developer-friendly, data-first.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--mdb-green` | `#00ED64` | Primary brand, CTAs, highlights |
| `--mdb-green-dark` | `#00684A` | Hover states, secondary fills |
| `--mdb-navy` | `#001E2B` | Primary background, hero sections |
| `--mdb-forest` | `#023430` | Deep surface color |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#001E2B` | Main background |
| `--bg-surface` | `#0C2336` | Cards, panels |
| `--bg-elevated` | `#112B40` | Dropdowns, modals |
| `--border` | `#1C3D54` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#FFFFFF` | Headings, body |
| `--text-secondary` | `#89A0B1` | Labels, captions |
| `--text-muted` | `#4E6C7D` | Placeholders, disabled |
| `--text-green` | `#00ED64` | Links, accent text |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#00ED64` | Connected, operation OK |
| `--warning` | `#FFC010` | Index missing, slow query |
| `--danger` | `#FF6960` | Error, connection failed |
| `--info` | `#0498EC` | Informational |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 40px | 700 | Hero, marketing |
| Heading 1 | 28px | 600 | Page titles |
| Heading 2 | 20px | 600 | Section headers |
| Body | 15px | 400 | Default content |
| Small | 13px | 400 | Labels, metadata |
| Mono | 13px | 400 | Queries, JSON, shell |

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Micro gaps |
| `--space-2` | `8px` | Inline spacing |
| `--space-3` | `12px` | Compact padding |
| `--space-4` | `16px` | Standard gap |
| `--space-6` | `24px` | Card padding |
| `--space-8` | `32px` | Section gap |
| `--space-12` | `48px` | Page sections |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `4px` | Tags, badges |
| `--radius-md` | `6px` | Buttons, inputs |
| `--radius-lg` | `10px` | Cards, panels |
| `--radius-xl` | `14px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 4px rgba(0,0,0,0.5);
--shadow-md: 0 4px 20px rgba(0,0,0,0.6);
--shadow-lg: 0 8px 40px rgba(0,0,0,0.7);
--shadow-green: 0 0 0 3px rgba(0,237,100,0.25);
```

---

## Components

### Buttons
```
Primary:  bg #00ED64, text #001E2B, hover #00C84F, radius 6px, height 40px, font-weight 600
Ghost:    bg transparent, border #1C3D54, text #89A0B1, hover border #00ED64
Danger:   bg #FF6960, text white
```

### Inputs
```
Background: #0C2336
Border:     #1C3D54 default, #00ED64 focused
Text:       #FFFFFF
Placeholder: #4E6C7D
Radius:     6px, height: 40px
Font:       JetBrains Mono for query fields
```

### Connection Status
```
Connected:    bg rgba(0,237,100,0.12), text #00ED64, dot #00ED64
Disconnected: bg rgba(255,105,96,0.12), text #FF6960, dot #FF6960
Connecting:   bg rgba(4,152,236,0.12), text #0498EC, dot #0498EC (pulse)
```

### Query Result Card
```
Background:  #0C2336
Border:      1px solid #1C3D54
Header:      bg #112B40, monospace field names, text #00ED64
Value:       white, monospace
Radius:      10px
```

---

## Layout

- Dashboard max-width: 1280px
- Sidebar: 240px
- Content padding: 24px
- Collections list: table, not cards

---

## Responsive Breakpoints

| Name | Width |
|------|-------|
| Mobile | < 768px |
| Tablet | 768px – 1280px |
| Desktop | > 1280px |

---

## Tone & Guardrails

### DO
- Dark navy on ALL surfaces — the deep background is MongoDB's identity
- Use monospace for all query fields, JSON output, and collection names
- Use the bright green sparingly — button CTAs and status indicators only
- Dark text on green buttons — the navy contrast demands it
- Show document counts and query times in monospace

### DON'T
- Don't use a grey or black background — the navy blue is the brand signal
- Don't use green for errors or warnings — semantic colors must stay distinct
- Don't round corners more than 10px — MongoDB is enterprise, not playful
- Don't use thin font weights — navy backgrounds require weight 400+
- Don't omit connection status — it's critical context in a database UI
