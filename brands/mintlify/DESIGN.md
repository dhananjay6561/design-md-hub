# Mintlify Design System

## Overview
Mintlify is a documentation platform that makes it easy to build beautiful, interactive docs. The design language is clean, bright, and modern — it signals that documentation can be a first-class product experience. The mint/emerald green anchors a refined dark aesthetic.

**Brand personality:** Clean, polished, product-quality docs, developer-delight.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--mint-green` | `#0EA47A` | Primary brand, CTAs, links |
| `--mint-green-light` | `#34D399` | Hover states, highlights |
| `--mint-emerald` | `#10B981` | Secondary accent |
| `--mint-white` | `#F8FAFC` | Primary text on dark |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0D1117` | Main background |
| `--bg-surface` | `#161C24` | Cards, sidebar, panels |
| `--bg-elevated` | `#1E2633` | Dropdowns, modals |
| `--border` | `#2A3441` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#F8FAFC` | Headings, body |
| `--text-secondary` | `#94A3B8` | Labels, captions |
| `--text-muted` | `#546882` | Placeholders, disabled |
| `--text-green` | `#34D399` | Links, accent text |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#0EA47A` | Deploy success |
| `--warning` | `#F59E0B` | Deprecation notice |
| `--danger` | `#EF4444` | Breaking change, error |
| `--info` | `#3B82F6` | Informational callout |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 40px | 700 | Hero, landing |
| Heading 1 | 30px | 600 | Page titles |
| Heading 2 | 22px | 600 | Section headers |
| Heading 3 | 17px | 600 | Subsections |
| Body | 15px | 400 | Prose content |
| Small | 13px | 400 | Captions, metadata |
| Mono | 13px | 400 | Code, API paths |

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Icon gaps |
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
| `--radius-sm` | `4px` | Badges, tags |
| `--radius-md` | `8px` | Buttons, inputs |
| `--radius-lg` | `12px` | Cards, callout boxes |
| `--radius-xl` | `16px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.4);
--shadow-md: 0 4px 16px rgba(0,0,0,0.5);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.6);
--shadow-green: 0 0 0 3px rgba(14,164,122,0.25);
```

---

## Components

### Buttons
```
Primary:  bg #0EA47A, text white, hover #0C9470, radius 8px, height 38px, font-weight 500
Ghost:    bg transparent, border #2A3441, text #94A3B8, hover border #0EA47A
```

### Inputs
```
Background: #161C24
Border:     #2A3441 default, #0EA47A focused
Text:       #F8FAFC
Placeholder: #546882
Radius:     8px, height: 38px
```

### Callout Boxes
```
Note:    border-left 3px solid #3B82F6, bg rgba(59,130,246,0.08)
Warning: border-left 3px solid #F59E0B, bg rgba(245,158,11,0.08)
Danger:  border-left 3px solid #EF4444, bg rgba(239,68,68,0.08)
Tip:     border-left 3px solid #0EA47A, bg rgba(14,164,122,0.08)
```

### API Method Badges
```
GET:    bg rgba(34,197,94,0.12), text #22C55E
POST:   bg rgba(59,130,246,0.12), text #3B82F6
PUT:    bg rgba(245,158,11,0.12), text #F59E0B
DELETE: bg rgba(239,68,68,0.12), text #EF4444
PATCH:  bg rgba(139,92,246,0.12), text #8B5CF6
```

---

## Layout

- Docs max-width: 1280px
- Left sidebar: 260px (navigation)
- Right sidebar: 220px (on-page TOC)
- Content width: 720px max
- Search bar: centered, prominent at top

---

## Responsive Breakpoints

| Name | Width |
|------|-------|
| Mobile | < 768px |
| Tablet | 768px – 1024px |
| Desktop | > 1024px |

---

## Tone & Guardrails

### DO
- Use API method badges (GET/POST/PUT/DELETE) consistently in reference docs
- Use callout boxes generously — they guide readers to important information
- Show inline code with a subtle background and green tint for types
- Keep the left sidebar navigation clean and hierarchical — max 2 nesting levels
- Use the search bar as a first-class navigation element — not an afterthought

### DON'T
- Don't use more than 4 heading levels in a single page — docs need clarity
- Don't overload the right sidebar TOC — if it's too long, the page is too long
- Don't use the green for warning or danger callouts — semantic color consistency matters
- Don't make code blocks feel like afterthoughts — they're the product in dev docs
- Don't use passive voice in documentation copy — "Run this command", not "This command can be run"
