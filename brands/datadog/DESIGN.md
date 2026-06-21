# Datadog Design System

## Overview
Datadog is a monitoring and analytics platform for cloud-scale infrastructure. The design language is data-dense, professional, and dark — built for engineers who live in dashboards. The purple brand anchors a UI that needs to surface massive amounts of telemetry data clearly.

**Brand personality:** Powerful, data-dense, always-on, engineering-focused.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--dd-purple` | `#632CA6` | Primary brand, CTAs, links |
| `--dd-purple-light` | `#8B5CF6` | Hover states, highlights |
| `--dd-pink` | `#D000E5` | Secondary accent, graphs |
| `--dd-dog` | `#774AA4` | Mid-tone purple fills |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#13111A` | Main background |
| `--bg-surface` | `#1C1829` | Cards, panels |
| `--bg-elevated` | `#26213A` | Dropdowns, modals |
| `--border` | `#352F4D` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#EEE9FF` | Headings, body |
| `--text-secondary` | `#A899CC` | Labels, captions |
| `--text-muted` | `#6B5F94` | Placeholders, disabled |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#1AAB79` | OK status, resolved |
| `--warning` | `#F5A623` | Alert, degraded |
| `--danger` | `#E84040` | Critical alert, error |
| `--info` | `#3B82F6` | Informational |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 32px | 700 | Page titles |
| Heading 1 | 24px | 600 | Section headers |
| Heading 2 | 18px | 600 | Card titles |
| Body | 14px | 400 | Default content |
| Small | 12px | 400 | Metadata, table rows |
| Mono | 13px | 400 | Metrics, queries, logs |

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
| `--space-12` | `48px` | Page sections |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `3px` | Tags, small badges |
| `--radius-md` | `6px` | Buttons, inputs |
| `--radius-lg` | `8px` | Cards, panels |
| `--radius-xl` | `12px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.5);
--shadow-md: 0 4px 16px rgba(0,0,0,0.6);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.7);
--shadow-purple: 0 0 0 3px rgba(99,44,166,0.35);
```

---

## Components

### Buttons
```
Primary:  bg #632CA6, text white, hover #7B3DC8, radius 6px, height 36px
Ghost:    bg transparent, border #352F4D, text #A899CC, hover border #632CA6
Danger:   bg #E84040, text white
```

### Inputs
```
Background: #1C1829
Border:     #352F4D default, #632CA6 focused
Text:       #EEE9FF
Placeholder: #6B5F94
Radius:     6px, height: 36px
```

### Monitor Status Badges
```
OK:        bg rgba(26,171,121,0.15), text #1AAB79
Warning:   bg rgba(245,166,35,0.15), text #F5A623
Critical:  bg rgba(232,64,64,0.15), text #E84040
No Data:   bg rgba(107,95,148,0.15), text #A899CC
```

### Metric Widget
```
Background: #1C1829
Value:      28px 700 --text-primary, monospace
Unit:       14px --text-secondary
Sparkline:  1px solid --dd-purple-light
Border:     1px solid --border
Radius:     8px
```

---

## Layout

- Dashboard max-width: unconstrained (fills viewport)
- Sidebar: 220px fixed
- Widget grid: configurable columns, 8px gap
- Content padding: 16px

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
- Use monospace for all metrics, query results, and log lines
- Color-code monitor status consistently (OK/Warn/Critical/No Data)
- Show relative time ("5 minutes ago") with absolute on hover
- Keep widget backgrounds slightly lighter than the page — depth matters for dashboards
- Use the purple sparingly — reserve it for primary actions and navigation

### DON'T
- Don't use a light theme for monitoring dashboards — dark reduces eye strain during incidents
- Don't use more than 3 colors per chart — clarity beats completeness
- Don't animate metric values on every update — flickering is distracting during incidents
- Don't round corners beyond 8px — Datadog is enterprise, not consumer
- Don't use the pink accent on alerts — it's for graphs, not status indicators
