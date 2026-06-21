# Lemon Squeezy Design System

## Overview
Lemon Squeezy is a payments and subscription platform built for indie developers and software creators. The design language is bright, playful, and confident — it feels like the fun alternative to Stripe for solo founders and small teams. The lemon yellow is central to the identity.

**Brand personality:** Playful, indie-friendly, bright, approachable, modern.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--ls-yellow` | `#FDE047` | Primary brand color, CTAs, highlights |
| `--ls-yellow-dark` | `#EAC800` | Hover on yellow elements |
| `--ls-black` | `#0F0F0F` | Text on yellow, high-contrast surfaces |
| `--ls-purple` | `#7C3AED` | Secondary actions, links on dark |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0C0C0C` | Main background |
| `--bg-surface` | `#161616` | Cards, panels |
| `--bg-elevated` | `#202020` | Dropdowns, modals |
| `--border` | `#2E2E2E` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#F5F5F5` | Headings, body |
| `--text-secondary` | `#888888` | Labels, captions |
| `--text-muted` | `#555555` | Placeholders, disabled |
| `--text-on-yellow` | `#0F0F0F` | Text placed on yellow backgrounds |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#22C55E` | Payment successful, active subscriptions |
| `--warning` | `#F59E0B` | Trial ending, expiring card |
| `--danger` | `#EF4444` | Failed charge, cancellation |
| `--info` | `#7C3AED` | Plan upgrade suggestions |

---

## Typography

**Primary Font:** `Plus Jakarta Sans` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 48px | 800 | Hero, marketing |
| Heading 1 | 32px | 700 | Page titles |
| Heading 2 | 22px | 600 | Section headers |
| Body | 15px | 400 | Content |
| Small | 13px | 400 | Metadata, labels |
| Mono | 13px | 400 | API keys, amounts |

Plus Jakarta Sans reads as friendly but professional — distinct from the Inter monoculture.

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
| `--space-20` | `80px` | Hero sections |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `6px` | Small badges |
| `--radius-md` | `10px` | Buttons, inputs |
| `--radius-lg` | `16px` | Cards, panels |
| `--radius-xl` | `20px` | Modals |
| `--radius-full` | `9999px` | Pills, tags |

Lemon Squeezy uses rounder corners than typical dev tools — it's intentionally approachable.

---

## Shadows

```css
--shadow-sm: 0 1px 4px rgba(0,0,0,0.5);
--shadow-md: 0 4px 20px rgba(0,0,0,0.6);
--shadow-lg: 0 8px 40px rgba(0,0,0,0.7);
--shadow-yellow: 0 0 0 3px rgba(253,224,71,0.3);
--shadow-yellow-glow: 0 4px 24px rgba(253,224,71,0.15);
```

---

## Components

### Buttons
```
Primary:  bg #FDE047, text #0F0F0F, hover bg #EAC800, radius 10px, height 42px, font-weight 700
Purple:   bg #7C3AED, text white, hover #6D28D9
Ghost:    bg transparent, border #2E2E2E, text #888888, hover border #FDE047
Sizes:    sm 34px, md 42px, lg 50px
```

### Inputs
```
Background: #161616
Border:     #2E2E2E default, #FDE047 focused
Text:       #F5F5F5
Placeholder: #555555
Radius:     10px, height: 42px
```

### Pricing Card
```
Background:  #161616
Border:      1px solid #2E2E2E
Highlighted: border #FDE047, shadow --shadow-yellow-glow
Price:       48px 800 --text-primary
Period:      14px --text-secondary
CTA:         full-width primary button
Radius:      16px
```

### Revenue Badge
```
Background: rgba(34,197,94,0.12)
Text:       #22C55E
Font:       monospace, 13px 600
Radius:     9999px
Padding:    4px 12px
```

---

## Layout

- Max-width: 1200px
- Content padding: 24px horizontal
- Dashboard uses card grid (3-col desktop, 1-col mobile)
- Marketing pages use full-bleed sections

---

## Responsive Breakpoints

| Name | Width |
|------|-------|
| Mobile | < 640px |
| Tablet | 640px – 1024px |
| Desktop | > 1024px |

---

## Tone & Guardrails

### DO
- Lead with the yellow — it's what makes Lemon Squeezy instantly recognizable
- Use large, bold numbers for revenue metrics — indie founders obsess over MRR
- Use rounded corners and friendly typography — it signals approachability
- Show success states enthusiastically — payments completing is cause for a small celebration
- Use `Plus Jakarta Sans` at heavy weights for CTAs — it reads as energetic

### DON'T
- Don't use muted or desaturated palettes — Lemon Squeezy is vibrant by design
- Don't overuse purple; it's secondary to the yellow brand anchor
- Don't use thin fonts — they feel too corporate for the indie-dev audience
- Don't use yellow text on white/light backgrounds — it's illegible; use black text on yellow instead
- Don't use aggressive/corporate copy — "Get started free" beats "Request a demo"
