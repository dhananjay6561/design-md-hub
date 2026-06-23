# Sentry Design System

## Overview

Sentry is an application performance monitoring and error tracking platform for developers. The visual language is dense and technical — built for engineers who live in dashboards. The brand combines urgency (errors need fixing) with calm professionalism (here's the data, here's the fix).

**Headline (live):** "Code breaks, fix it faster"
**Meta description:** "Application performance monitoring for developers & software teams to see errors clearer, solve issues faster & continue learning continuously."
**Brand personality:** Developer first. Always.

---

## Colors

All values extracted directly from `sentry.io` CSS bundle (`/_astro/Layout.CTuWOC2S.css`).

### Brand Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--color-blurple` | `#6a5fc1` | Primary CTA, info events, focused inputs |
| `--color-dk-blurple` | `#4e2a9a` | Hover states, gradient endpoints |
| `--color-alt-dk-blurple` | `#422082` | Deep purple gradient |
| `--color-hot-pink` | `#fd44b0` | Marketing accents, neon highlights |
| `--color-lt-pink` | `#fa7faa` | Light pink gradient step |
| `--color-lt-orange` | `#ffb287` | Gradient warm endpoint |
| `--color-lt-yellow` | `#ffdb4a` | Gradient gold end |
| `--color-md-pink` | `#e1567c` | Mid-range pink |
| `--color-dk-pink` | `#c73852` | Error semantic color |

### Dark Mode Surfaces
Defined in `.dark { ... }` class in the CSS bundle.

| Variable | Hex | Usage |
|----------|-----|-------|
| `--bg-primary` | `#1f1633` | App background (`--color-rich-black`) |
| `--bg-secondary` | `#181225` | Sidebar, secondary panels (`--color-utility-black`) |
| `--border-color` | `#362d59` | All borders, dividers (`--color-dk-violet`) |
| `--text-primary` | `#ffffff` | Headings, body text |
| `--text-secondary` | `#ececf1` | Secondary text (`--color-gray-2`) |

### Light Mode Surfaces
Defined in `:root { ... }` in the CSS bundle.

| Variable | Hex | Usage |
|----------|-----|-------|
| `--bg-primary` | `#ffffff` | App background |
| `--bg-secondary` | `#f6f6f8` | Secondary panels |
| `--border-color` | `#ececf1` | All borders (`--color-gray-2`) |
| `--text-primary` | `#362d59` | Headings, body text (`--color-dk-violet`) |
| `--text-secondary` | `#9093c1` | Secondary text |

### Semantic / Status
| State | Hex | Usage |
|-------|-----|-------|
| Error | `#c73852` (`--color-dk-pink`) | Error-level events, destructive actions |
| Warning | `#f2b712` (`--color-md-yellow`) | Warning-level events, degraded states |
| Info | `#6a5fc1` (`--color-blurple`) | Info-level events, neutral actions |
| Resolved | `#2ba22b` | Resolved issues, success states |

### Notable Gradients
```css
/* CTA gradient (primary-dark button) */
background: linear-gradient(120deg, #c83852 0%, #b44092 25%, #6a5fc1 50%, transparent 55%);

/* Gold gradient */
background: linear-gradient(45deg, #ffb287 0%, #ffc36a 50%, #fedb4b 100%);

/* Purple descent (dark sections) */
background: linear-gradient(149deg, #36166b 18%, #422082 57%, #4e2a9a 96%);
```

---

## Typography

**Primary font:** `Rubik` — loaded via `@font-face` from `/astro-assets/fonts/rubik-latin-*.woff2`. Weights: 400, 500, 700; italic 400, 500.
**Display font:** `Dammit Sans` — custom bold-only font loaded from `/astro-assets/fonts/dammitsansv0.3-bold.otf`. Weight 700 only.
**Monospace:** `IBM Plex Mono` (referenced in CSS as `SF Mono`, `Monaco`, `IBM Plex Mono` fallback chain). Use for stack traces, event IDs, hashes, code snippets.

For external use (Google Fonts import):
```css
@import url('https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,400;0,500;0,700;1,400&family=IBM+Plex+Mono:wght@400;500&display=swap');
```

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 34px+ | 700 | Page hero titles (e.g. "Code breaks, fix it faster") |
| Heading 1 | 24px | 700 | Section headers |
| Heading 2 | 18px | 600 | Card titles, subsections |
| Body | 14px | 400 | Default content |
| Small | 12px | 400 | Metadata, timestamps, captions |
| Mono | 13px | 400 | Stack traces, event IDs, code |
| Label | 11px | 600 uppercase | Table headers, section labels (letter-spacing: 0.1em) |

Line height: 1.5 for body, 1.15–1.2 for headings.

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `space-1` | 4px | Icon gaps, tight inline spacing |
| `space-2` | 8px | List item padding, badge margins |
| `space-3` | 12px | Inner card padding |
| `space-4` | 16px | Standard component gap |
| `space-6` | 24px | Section internal padding |
| `space-8` | 32px | Large section separators |
| `space-12` | 48px | Page section spacing |

Container: `max-width: 1152px` (`--breakpoint-xl`). Responsive breakpoints: 576px, 768px, 992px, 1152px.

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | 4px | Badges, chips, small tags |
| `--radius-md` | 6px | Buttons, inputs, issue rows |
| `--radius-lg` | 8px | Cards, panels, modals |
| `--radius-btn` | `2em` | Pill buttons (marketing CTAs) |
| `--radius-btn-new` | `0.5rem` | New-style buttons |

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.4);
--shadow-md: 0 4px 12px rgba(31,22,51,0.25);   /* uses rich-black tint */
--shadow-lg: 0 8px 24px rgba(31,22,51,0.3);
--shadow-card: 0px 8px 24px 0px rgba(31,22,51,0.15);
--shadow-focus: 0 0 0 3px rgba(106,95,193,0.25);  /* blurple focus ring */
```

---

## Components

### Buttons (`.btn` / `.btn-new`)

```
Height:       2.5em (34–40px)
Border-radius: 0.5rem (btn-new) / 2em (pill)
Font:         Rubik, 0.875rem, weight 700, UPPERCASE
Letter-spacing: 0.2px
Transition:   color, border-color, background-color, box-shadow 0.2s
```

Button variants:
- **Primary (dark bg):** gradient `#c83852 → #b44092 → #6a5fc1`, text `#1f1633`
- **Primary (light bg):** gradient `#fa7faa → #ff9691 → #ffb287`, text `#1f1633`
- **Secondary light:** border-only with gradient hover
- **Gold:** `linear-gradient(45deg, #ffb287, #ffc36a, #fedb4b)`, text `#1f1633`
- **Ghost:** transparent background, border `--border-color`, text `--text-secondary`

### Inputs

```
Height:          34–36px
Background:      --bg-primary
Border:          1px solid --border-color
Focus border:    --color-blurple (#6a5fc1)
Focus shadow:    0 0 0 3px rgba(106,95,193,0.2)
Border-radius:   6px
Font:            Rubik 13px
Placeholder:     --text-secondary (muted)
```

### Event Level Badges

```
error:    bg rgba(199,56,82,0.18),   text #fa7faa,   border rgba(199,56,82,0.4)
warning:  bg rgba(242,183,18,0.15),  text #f2b712,   border rgba(242,183,18,0.35)
info:     bg rgba(106,95,193,0.2),   text #a99de0,   border rgba(106,95,193,0.4)
resolved: bg rgba(43,162,43,0.15),   text #4ec94e,   border rgba(43,162,43,0.35)
```

Font: 11px, weight 600, UPPERCASE, letter-spacing 0.04em, border-radius 4px.

### Issue Row (Issues List)

```
Grid:         checkbox | title+culprit | level | project | assignee | events | last-seen
Row height:   ~44px with 10px padding
Hover bg:     --elevated
Border-left:  none (level dot used instead)
Title:        13px weight 500 --text-primary, truncated
Culprit:      11px --text-4, truncated
Level dot:    8px circle, colored + glow ring
Event count:  IBM Plex Mono 12px, background --elevated
```

---

## Layout

- App max-width: `1152px`
- Sidebar width: ~220px (app UI)
- Content padding: `24px`
- Grid: 12-column, gap `16px`

Responsive breakpoints from CSS:
| Name | Var | Width |
|------|-----|-------|
| xs | `--breakpoint-xs` | 0px |
| sm | `--breakpoint-sm` | 576px |
| md | `--breakpoint-md` | 768px |
| lg | `--breakpoint-lg` | 992px |
| xl | `--breakpoint-xl` | 1152px |

---

## Tone & Guardrails

### DO
- Use IBM Plex Mono for all event IDs, hashes, stack traces, and code references
- Color-code severity consistently — level dots, badges, and row indicators must always align
- Show timestamps as relative ("2 hours ago") with the absolute datetime visible on hover
- Keep error messages technically accurate — developers prefer precision over softened language
- Use blurple (`#6a5fc1`) as the primary action color and for info-level status indicators
- Reserve hot-pink / lt-pink gradients for marketing surfaces only — not in the product UI

### DON'T
- Don't apply bright brand colors (`#fd44b0`, `#fa7faa`) to large surface areas in the product — they're status and marketing signals
- Don't exceed `8px` border-radius on data tables, issue rows, or dashboards — Sentry's product aesthetic is sharp and dense
- Don't repurpose the error color (`#c73852`) for non-error states — semantic color is strict
- Don't add animations to issue rows or data tables — performance and information density take priority
- Don't override the dark primary surface (`#1f1633`) for the main dashboard — dark mode is non-negotiable for dev tooling
- Don't stack multiple accent colors in a single component
