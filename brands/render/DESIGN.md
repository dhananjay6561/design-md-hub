# Render Design System

## Overview
Render is a unified cloud platform for deploying apps and databases. The design language blends a dark navy base with a vibrant teal/mint accent — it communicates speed, reliability, and a modern Heroku alternative. The palette is distinctive and instantly recognizable.

**Brand personality:** Fast, modern, reliable, developer-friendly, no-ops.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--render-teal` | `#46E3B7` | Primary brand, CTAs, highlights |
| `--render-teal-hover` | `#30C9A0` | Hover on teal elements |
| `--render-navy` | `#10162F` | Deep background, hero |
| `--render-purple` | `#7C3AED` | Secondary accent, deploy logs |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#10162F` | Main background |
| `--bg-surface` | `#171E3C` | Cards, panels |
| `--bg-elevated` | `#1F2850` | Dropdowns, modals |
| `--border` | `#2C3560` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#EEF0FF` | Headings, body |
| `--text-secondary` | `#8E9AC8` | Labels, captions |
| `--text-muted` | `#5A6494` | Placeholders, disabled |
| `--text-teal` | `#46E3B7` | Links, accent text |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#46E3B7` | Deploy succeeded, live |
| `--warning` | `#F5A623` | Degraded, slow build |
| `--danger` | `#EF4444` | Failed deploy, crash |
| `--info` | `#60A5FA` | Informational |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 40px | 700 | Hero, marketing |
| Heading 1 | 28px | 600 | Page titles |
| Heading 2 | 20px | 600 | Section headers |
| Body | 14px | 400 | Default content |
| Small | 12px | 400 | Metadata, table rows |
| Mono | 13px | 400 | Deploy logs, env vars |

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Icon gaps |
| `--space-2` | `8px` | Compact spacing |
| `--space-3` | `12px` | Inline padding |
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
--shadow-teal: 0 0 0 3px rgba(70,227,183,0.25);
--shadow-teal-glow: 0 4px 24px rgba(70,227,183,0.12);
```

---

## Components

### Buttons
```
Primary:  bg #46E3B7, text #10162F, hover bg #30C9A0, radius 6px, height 38px, font-weight 600
Ghost:    bg transparent, border #2C3560, text #8E9AC8, hover border #46E3B7
Height:   38px, padding 0 18px
```

### Inputs
```
Background: #171E3C
Border:     #2C3560 default, #46E3B7 focused
Text:       #EEF0FF
Placeholder: #5A6494
Radius:     6px, height: 38px
Font:       JetBrains Mono for env vars, keys
```

### Service Status Badges
```
Live:      bg rgba(70,227,183,0.12), text #46E3B7, border rgba(70,227,183,0.3)
Building:  bg rgba(96,165,250,0.12), text #60A5FA, border rgba(96,165,250,0.3)
Failed:    bg rgba(239,68,68,0.12), text #EF4444, border rgba(239,68,68,0.3)
Suspended: bg rgba(90,100,148,0.12), text #8E9AC8, border rgba(90,100,148,0.3)
```

### Deploy Log
```
Background:  #0C1226 (darker than page)
Font:        JetBrains Mono 12px
Line height: 1.6
Success line: color #46E3B7
Error line:   color #EF4444
Timestamp:    color #5A6494
Border:       1px solid #2C3560
Radius:       6px
```

---

## Layout

- Dashboard max-width: 1200px
- Content padding: 24px
- Service list: table layout, not cards — density matters
- Build logs: full-width, collapsible

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
- Use dark navy as the background — it differentiates Render from the grey-dark crowd
- Use teal on deploy status indicators — it's the "all green" of Render's world
- Use monospace for all deploy logs, env var keys, and service URLs
- Show deploy timestamps in relative time with absolute on hover
- Dark text on teal buttons — the navy ensures readability at full contrast

### DON'T
- Don't use the teal on backgrounds larger than a button — it's an accent, not a fill
- Don't use a grey dark background — the navy blue is what makes Render instantly recognizable
- Don't mix the purple accent with teal on the same component
- Don't animate deploy log lines scrolling — it can make incidents feel more chaotic
- Don't use rounded corners beyond 10px — Render is polished, not bubbly
