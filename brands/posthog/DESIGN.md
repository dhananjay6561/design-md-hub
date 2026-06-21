# PostHog Design System

## Overview
PostHog is an open-source product analytics platform. The design language is bold, playful but data-dense — it blends the scrappiness of an open-source project with professional analytics tooling. The brand's mascot (the hedgehog) sets a friendly tone that distinguishes it from enterprise analytics tools.

**Brand personality:** Open, bold, data-first, friendly, opinionated.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--ph-blue` | `#1D4AFF` | Primary actions, links, CTAs |
| `--ph-yellow` | `#F9BD2B` | Highlights, hover states, accents |
| `--ph-red` | `#F54E00` | Danger, negative trends |
| `--ph-green` | `#36AE7C` | Positive metrics, success |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#151515` | Main background |
| `--bg-surface` | `#1D1D1D` | Cards, panels |
| `--bg-elevated` | `#282828` | Dropdowns, modals |
| `--border` | `#3A3A3A` | Dividers, input borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#FFFFFFDE` | Headlines, body |
| `--text-secondary` | `#FFFFFF99` | Labels, captions |
| `--text-muted` | `#FFFFFF60` | Placeholders, disabled |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#36AE7C` | Positive change, events firing |
| `--warning` | `#F9BD2B` | Degraded, partial |
| `--danger` | `#F54E00` | Error, negative |
| `--info` | `#1D4AFF` | Informational |

---

## Typography

**Primary Font:** `Matter` (fallback: `Inter`, `system-ui`)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 36px | 800 | Hero/landing |
| Heading 1 | 28px | 700 | Page titles |
| Heading 2 | 20px | 600 | Section headers |
| Body | 15px | 400 | Default content |
| Small | 13px | 400 | Captions, metadata |
| Mono | 13px | 400 | Code, event names |

PostHog uses slightly heavier font weights than most analytics tools — it reads as confident.

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Micro gaps |
| `--space-2` | `8px` | Inline spacing |
| `--space-3` | `12px` | Tight padding |
| `--space-4` | `16px` | Standard gap |
| `--space-6` | `24px` | Card padding |
| `--space-8` | `32px` | Section gap |
| `--space-12` | `48px` | Page sections |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `4px` | Tags, chips |
| `--radius-md` | `8px` | Buttons, inputs |
| `--radius-lg` | `12px` | Cards |
| `--radius-xl` | `16px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 4px rgba(0,0,0,0.5);
--shadow-md: 0 4px 16px rgba(0,0,0,0.6);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.7);
--shadow-blue: 0 0 0 3px rgba(29,74,255,0.35);
```

---

## Components

### Buttons
```
Primary:  bg #1D4AFF, text white, hover #1038E0, radius 8px, height 38px, font-weight 600
Yellow:   bg #F9BD2B, text #151515, hover #E0AA20 — for featured CTAs only
Ghost:    bg transparent, border #3A3A3A, text #FFFFFF99, hover border #1D4AFF
```

### Inputs
```
Background: #1D1D1D
Border:     #3A3A3A default, #1D4AFF focused
Text:       #FFFFFFDE
Placeholder: #FFFFFF60
Radius:     8px, height: 38px
```

### Metric Cards
```
Background:  #1D1D1D
Value:       32px 700 --text-primary
Change pill: green bg for positive, red bg for negative
Border:      1px solid #3A3A3A
Radius:      12px
```

### Event Badges
```
Capture:  bg rgba(29,74,255,0.15), text #1D4AFF
Warning:  bg rgba(249,189,43,0.15), text #F9BD2B
Error:    bg rgba(245,78,0,0.15), text #F54E00
```

---

## Layout

- Max content width: 1280px
- Sidebar: 240px (collapsible)
- Content padding: 24px horizontal, 32px vertical
- Dashboard grid: configurable, default 3 columns

---

## Responsive Breakpoints

| Name | Width |
|------|-------|
| Mobile | < 768px |
| Tablet | 768px – 1200px |
| Desktop | > 1200px |

---

## Tone & Guardrails

### DO
- Use bold font weights liberally — PostHog reads as confident, not timid
- Use `--ph-yellow` for interactive hover states and highlights, not decorative accents
- Show absolute numbers alongside percentages — data scientists hate ambiguity
- Use the hedgehog mascot for empty states and onboarding — it's a differentiator, not cringe
- Keep dark backgrounds — PostHog users work in terminals and prefer low-glare

### DON'T
- Don't use `--ph-yellow` as a background for large sections — it's an accent, not a fill
- Don't tone down colors to be "safer" — PostHog's boldness is intentional branding
- Don't use thin font weights (300, 200) — they disappear on dark backgrounds
- Don't use pie charts — PostHog's design system explicitly discourages them for analytics
- Don't add heavy drop shadows to chart elements — keep data visualizations clean
