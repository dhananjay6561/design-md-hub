# Prisma Design System

## Overview
Prisma is a next-generation ORM for Node.js and TypeScript. The design language is clean, minimal, and developer-focused — heavy on documentation clarity and code readability. The aesthetic is calm and confident, matching the reliability Prisma promises at the database layer.

**Brand personality:** Precise, minimal, trustworthy, documentation-first.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--prisma-teal` | `#16A394` | Primary brand, CTAs, links |
| `--prisma-indigo` | `#5A67D8` | Secondary actions, hover |
| `--prisma-white` | `#F8F9FC` | Primary text (dark mode) |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0F1117` | App background |
| `--bg-surface` | `#161B27` | Cards, panels |
| `--bg-elevated` | `#1E2533` | Dropdowns, modals |
| `--border` | `#2A3141` | Dividers, input borders |
| `--code-bg` | `#0D1117` | Code block backgrounds |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#F8F9FC` | Headings, body |
| `--text-secondary` | `#9BA3BF` | Labels, captions |
| `--text-muted` | `#5C677D` | Placeholders, disabled |
| `--text-code` | `#7DD3C8` | Inline code text |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#16A394` | Migration applied, success |
| `--warning` | `#F59E0B` | Breaking change, deprecation |
| `--danger` | `#EF4444` | Error, failed migration |
| `--info` | `#5A67D8` | Informational notes |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 40px | 700 | Hero, docs landing |
| Heading 1 | 30px | 600 | Page titles |
| Heading 2 | 22px | 600 | Section headers |
| Body | 15px | 400 | Default content |
| Small | 13px | 400 | Captions, metadata |
| Code | 13px/14px | 400 | Code blocks, inline |

Code blocks use `JetBrains Mono`. Inline code uses teal text on a subtle dark background.

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Icon gaps |
| `--space-2` | `8px` | Inline padding |
| `--space-3` | `12px` | Compact elements |
| `--space-4` | `16px` | Standard gap |
| `--space-6` | `24px` | Card padding |
| `--space-8` | `32px` | Section gap |
| `--space-12` | `48px` | Page sections |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `4px` | Badges, chips |
| `--radius-md` | `6px` | Buttons, inputs |
| `--radius-lg` | `10px` | Cards, panels |
| `--radius-xl` | `14px` | Modals |
| `--radius-code` | `6px` | Code blocks |

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.4);
--shadow-md: 0 4px 16px rgba(0,0,0,0.5);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.6);
--shadow-teal: 0 0 0 3px rgba(22,163,148,0.25);
```

---

## Components

### Buttons
```
Primary:  bg #16A394, text white, hover #12907F, radius 6px, height 38px
Secondary: bg transparent, border #2A3141, text #9BA3BF, hover border #16A394
Height:   38px, padding 0 18px, font-weight 500
```

### Inputs
```
Background: #161B27
Border:     #2A3141 default, #16A394 focused
Text:       #F8F9FC
Placeholder: #5C677D
Radius:     6px, height: 38px, font-family: JetBrains Mono for schema fields
```

### Code Block
```
Background: #0D1117
Border:     1px solid #2A3141
Radius:     6px
Padding:    16px
Font:       JetBrains Mono 13px
Keyword:    #F472B6 (pink)
String:     #86EFAC (green)
Type:       #7DD3C8 (teal)
Comment:    #5C677D
```

### Badges
```
Migration: bg rgba(22,163,148,0.15), text #16A394
Warning:   bg rgba(245,158,11,0.15), text #F59E0B
Error:     bg rgba(239,68,68,0.15), text #EF4444
```

---

## Layout

- Docs max-width: 1200px
- Sidebar (docs): 260px
- Content area: 720px max-width, centered
- Code-to-prose ratio: aim for ~40% code in technical docs

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
- Lead with code examples — Prisma's users learn by reading schemas and queries
- Use teal `#16A394` for syntax highlighting on types and field names in Prisma Schema
- Keep line lengths short in prose (70–80 chars) — matches how developers read docs
- Show before/after comparisons for migration guides
- Use `JetBrains Mono` consistently for anything schema, query, or terminal related

### DON'T
- Don't use indigo as a primary CTA — it's a secondary color, not the brand anchor
- Don't use colorful backgrounds on large areas — Prisma's dark is almost black, not purple
- Don't clutter the layout — whitespace signals precision and confidence
- Don't use emoji in error messages or console output — keep it professional
- Don't mix `--prisma-teal` and `--prisma-indigo` in the same component
