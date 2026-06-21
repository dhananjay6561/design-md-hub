# Sentry Design System

## Overview
Sentry is an error monitoring and performance platform for developers. The visual language is dark, dense, and technical — built for engineers who live in dashboards. The brand balances urgency (errors need fixing) with calm professionalism (don't panic, here's the data).

**Brand personality:** Technical, reliable, urgent-but-calm, developer-first.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--sentry-purple` | `#6C5FC7` | Primary actions, links, highlights |
| `--sentry-pink` | `#F55C47` | Critical errors, destructive actions |
| `--sentry-orange` | `#F0A858` | Warnings, degraded performance |
| `--sentry-green` | `#2BA22B` | Resolved issues, success states |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#1A1625` | Main app background |
| `--bg-surface` | `#241C35` | Cards, panels, sidebars |
| `--bg-elevated` | `#2E2541` | Modals, dropdowns, tooltips |
| `--border` | `#3A2F50` | Dividers, input borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#EBE6F5` | Body, headings |
| `--text-secondary` | `#9B8EC4` | Labels, metadata |
| `--text-muted` | `#6A5E8A` | Placeholders, disabled |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--error` | `#F55C47` | Error level events |
| `--warning` | `#F0A858` | Warning level events |
| `--info` | `#6C5FC7` | Info level events |
| `--success` | `#2BA22B` | Resolved, healthy |

---

## Typography

**Primary Font:** `Rubik` (Google Fonts)
**Monospace Font:** `Roboto Mono` (for stack traces, code, hashes)

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 32px | 700 | Page titles |
| Heading 1 | 24px | 600 | Section headers |
| Heading 2 | 18px | 600 | Card titles |
| Body | 14px | 400 | Default content |
| Small | 12px | 400 | Metadata, timestamps |
| Mono | 13px | 400 | Stack traces, event IDs |

Line height: 1.5 for body, 1.2 for headings.

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Icon gaps, tight inline |
| `--space-2` | `8px` | List item padding |
| `--space-3` | `12px` | Inner card padding |
| `--space-4` | `16px` | Standard component gap |
| `--space-6` | `24px` | Section padding |
| `--space-8` | `32px` | Large section gaps |
| `--space-12` | `48px` | Page section spacing |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `4px` | Badges, tags, chips |
| `--radius-md` | `6px` | Buttons, inputs |
| `--radius-lg` | `8px` | Cards, panels |
| `--radius-xl` | `12px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.4);
--shadow-md: 0 4px 12px rgba(0,0,0,0.5);
--shadow-lg: 0 8px 24px rgba(0,0,0,0.6);
--shadow-purple: 0 0 0 3px rgba(108,95,199,0.3);
```

---

## Components

### Buttons
```
Primary:    bg #6C5FC7, text white, hover #7B6DD6, radius 6px, height 36px
Danger:     bg #F55C47, text white, hover #F76B57
Ghost:      bg transparent, border #3A2F50, text #9B8EC4, hover border #6C5FC7
```

### Inputs
```
Background: #241C35
Border:     #3A2F50 default, #6C5FC7 focused
Text:       #EBE6F5
Placeholder: #6A5E8A
Radius:     6px, height: 36px
```

### Event Level Badges
```
error:    bg rgba(245,92,71,0.15), text #F55C47, border rgba(245,92,71,0.3)
warning:  bg rgba(240,168,88,0.15), text #F0A858, border rgba(240,168,88,0.3)
info:     bg rgba(108,95,199,0.15), text #6C5FC7, border rgba(108,95,199,0.3)
resolved: bg rgba(43,162,43,0.15), text #2BA22B, border rgba(43,162,43,0.3)
```

### Issue Row
```
Left accent bar: 3px solid (level color)
Background: --bg-surface
Title: --text-primary 14px 500
Metadata: --text-secondary 12px
Count pill: --bg-elevated, monospace
```

---

## Layout

- App max-width: 1280px
- Sidebar width: 220px (collapsed 60px)
- Content padding: 24px
- Grid: 12-column, 16px gap

---

## Responsive Breakpoints

| Name | Width |
|------|-------|
| Mobile | < 768px |
| Tablet | 768px – 1024px |
| Desktop | > 1024px |

On mobile, sidebar collapses to bottom nav.

---

## Tone & Guardrails

### DO
- Use monospace for all event IDs, hashes, stack traces
- Color-code severity consistently across the entire UI
- Show timestamps in relative time ("2 hours ago") with absolute on hover
- Keep error messages technical and precise — developers prefer accuracy over hand-holding
- Use `--sentry-pink` (#F55C47) only for actual errors; don't repurpose for branding

### DON'T
- Don't use bright colors on large surface areas — they're reserved for status indicators
- Don't round corners more than 8px — Sentry's aesthetic is sharp, not soft
- Don't use light backgrounds for the main dashboard — dark is non-negotiable for readability in dimly lit offices
- Don't mix multiple accent colors in a single component
- Don't use animations on data tables — performance and focus matter more than delight
