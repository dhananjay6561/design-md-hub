# Cloudflare Design System

## Overview
Cloudflare is the Internet's connectivity cloud — CDN, security, DNS, edge compute. The design language is bold and enterprise-grade, with the iconic orange as its only accent color. It's professional without being sterile, and technical without being inaccessible.

**Brand personality:** Trustworthy, fast, global, no-nonsense enterprise.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--cf-orange` | `#F38020` | Primary brand, CTAs, links |
| `--cf-orange-light` | `#FBAD41` | Hover states, highlights |
| `--cf-blue` | `#0051C3` | Secondary actions (light mode) |
| `--cf-yellow` | `#FBAD41` | Warning, attention |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#111111` | App background |
| `--bg-surface` | `#1A1A1A` | Cards, panels |
| `--bg-elevated` | `#242424` | Dropdowns, modals |
| `--border` | `#333333` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#F2F2F2` | Headings, body |
| `--text-secondary` | `#AAAAAA` | Labels, metadata |
| `--text-muted` | `#666666` | Placeholders, disabled |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#00B050` | Requests served, active zones |
| `--warning` | `#FBAD41` | Partial failure, degraded |
| `--danger` | `#D60000` | Attack detected, error |
| `--info` | `#0051C3` | Informational |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `Source Code Pro`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 40px | 700 | Hero, landing pages |
| Heading 1 | 28px | 600 | Page titles |
| Heading 2 | 20px | 600 | Section headers |
| Body | 14px | 400 | Default content |
| Small | 12px | 400 | Metadata, table rows |
| Mono | 13px | 400 | IPs, hostnames, code |

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Icon gaps |
| `--space-2` | `8px` | Compact row padding |
| `--space-3` | `12px` | Inline padding |
| `--space-4` | `16px` | Standard component gap |
| `--space-6` | `24px` | Card padding |
| `--space-8` | `32px` | Section gaps |
| `--space-16` | `64px` | Page section spacing |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `3px` | Tags, inline badges |
| `--radius-md` | `6px` | Buttons, inputs |
| `--radius-lg` | `8px` | Cards, panels |
| `--radius-xl` | `12px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.5);
--shadow-md: 0 4px 12px rgba(0,0,0,0.6);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.7);
--shadow-orange: 0 0 0 3px rgba(243,128,32,0.3);
```

---

## Components

### Buttons
```
Primary:  bg #F38020, text white, hover #FBAD41 — text becomes #111 on hover
Ghost:    bg transparent, border #333, text #AAAAAA, hover border #F38020
Danger:   bg #D60000, text white
Height:   36px, radius 6px, font-weight 500
```

### Inputs
```
Background: #1A1A1A
Border:     #333333 default, #F38020 focused
Text:       #F2F2F2
Placeholder: #666666
Radius:     6px, height: 36px
```

### Status Badges
```
Active:    bg rgba(0,176,80,0.15), text #00B050
Warning:   bg rgba(251,173,65,0.15), text #FBAD41
Blocked:   bg rgba(214,0,0,0.15), text #D60000
Inactive:  bg rgba(102,102,102,0.15), text #AAAAAA
```

### Data Table
```
Header:     bg #242424, text #AAAAAA uppercase 11px
Row hover:  bg #1F1F1F
Border:     bottom 1px solid #2A2A2A
Numbers:    monospace right-aligned
```

---

## Layout

- Dashboard max-width: 1400px
- Left nav: 224px fixed
- Content area padding: 24px
- Data-dense tables preferred over cards for lists

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
- Use `--cf-orange` sparingly — it's the only accent and must retain prominence
- Use monospace for all IPs, hostnames, DNS records, and numeric data
- Display global metrics with large numbers front-and-center — Cloudflare users care about scale
- Use flat, minimal shadows — the UI should feel grounded and fast-loading
- Prefer tabular data over cards when listing zones, routes, or rules

### DON'T
- Don't use multiple accent colors — Cloudflare's entire identity rests on the single orange
- Don't use rounded corners beyond 8px — the UI is professional, not bubbly
- Don't use animations on table rows or data updates — it adds cognitive load
- Don't use gradients on backgrounds — Cloudflare is flat and solid
- Don't make the orange glow or pulse — it's a color, not a notification system
