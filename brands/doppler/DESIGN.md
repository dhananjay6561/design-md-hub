# Doppler DESIGN.md

> Secrets management platform — a dark-first, high-contrast design system built around security, trust, and developer experience. Typographically distinct with a custom proprietary typeface and a vivid purple-to-orange-to-pink gradient identity.

## Overview

Doppler's design is dark-first (deep purple-near-black backgrounds), uses a proprietary custom typeface (DopplerRepro), and leans into a vivid brand gradient — purple `#6B13F5` to orange `#F55C15` to pink `#FF9EFA`. The aesthetic is authoritative and modern, positioned for both security-conscious enterprises and developer teams. Light mode inverts to warm cream (`#F1F0EC`) on near-white, maintaining the same typographic weight and structure.

## Colors

All colors extracted from live doppler.com HTML and CSS bundle (`ec074c50093238e3.css`).

### Core Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `purple-brand` | `#6B13F5` | Primary brand, CTAs, active states |
| `purple-light` | `#B997FF` | Hover, secondary purple |
| `orange-brand` | `#F55C15` | Gradient accent, warnings |
| `pink-brand` | `#FF9EFA` | Gradient accent, highlights |
| `green-brand` | `#00F575` | Success, synced states |
| `green-dark` | `#00BF5B` | Success hover |

### Dark Mode (default)

| Token | Hex | Usage |
|-------|-----|-------|
| `bg` | `#1C1624` | Page background |
| `surface` | `#2D2734` | Cards, panels |
| `surface-raised` | `#302C37` | Elevated surfaces |
| `surface-subtle` | `#241E2C` | Inset areas |
| `text-primary` | `#F1F0EC` | Body text, headings |
| `text-secondary` | `#8B877D` | Supporting text |
| `text-muted` | `#45403D` | Placeholders, disabled |
| `border` | `#44443C` | Dividers, input borders |
| `border-subtle` | `#3E384B` | Subtle dividers |

### Light Mode

| Token | Hex | Usage |
|-------|-----|-------|
| `bg` | `#FCFAF6` | Page background (warm cream) |
| `surface` | `#F1F0EC` | Cards, panels |
| `surface-raised` | `#FFFFFF` | Elevated, modals |
| `text-primary` | `#0C0404` | Body text, headings |
| `text-secondary` | `#44443C` | Supporting text |
| `text-muted` | `#84847C` | Placeholders |
| `border` | `#BCBCBC` | Dividers |

### Brand Gradient

The Doppler mark uses a layered gradient sequence:

```
Primary: linear-gradient(from #FF9EFA → #F55C15@42% → #6B13F5)
Overlay 1: radial from #F55C15 fading to transparent
Overlay 2: radial from #FF9EFA fading to transparent
```

## Typography

- **Primary font**: `DopplerRepro` — custom proprietary variable typeface loaded from `/_next/static/media/*.woff2`. Fallback: `Arial`, `sans-serif`
- **Mono font**: `DopplerReproMono` — custom mono variant. Fallback: `Arial`, `monospace`
- **Secondary font**: `Inter` — used for UI elements and body prose

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| `display` | 56–72px | 400 (regular) | Hero H1 |
| `heading-xl` | 40px | 400 | Section headers |
| `heading-lg` | 28px | 400 | Card titles |
| `heading-md` | 20px | 400 | Sub-section titles |
| `body` | 16px | 400 | Body text |
| `body-sm` | 14px | 400 | Supporting text |
| `label` | 12px | 400 | Labels, captions |
| `mono` | 13px | 400 | Secret keys, code |

**Note**: DopplerRepro is used at regular weight (400) for most headings — the brand deliberately avoids heavy bold weights. Type appears slightly condensed and geometric.

## Spacing

Base unit: `8px`

| Token | Value |
|-------|-------|
| `space-1` | 4px |
| `space-2` | 8px |
| `space-3` | 12px |
| `space-4` | 16px |
| `space-6` | 24px |
| `space-8` | 32px |
| `space-12` | 48px |
| `space-16` | 64px |
| `space-32` | 128px |

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-sm` | 4px | Inputs, small badges |
| `radius-md` | 8px | Cards, dropdowns |
| `radius-lg` | 12px | Panels, modals |
| `radius-xl` | 16px | Large cards |
| `radius-full` | 9999px | Pills, avatars |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 2px rgba(0,0,0,0.3)` | Subtle card lift |
| `shadow-md` | `0 4px 16px rgba(0,0,0,0.4)` | Panels, dropdowns |
| `shadow-lg` | `0 8px 32px rgba(0,0,0,0.5)` | Modals, toasts |

## Animation

```css
--global-ease: cubic-bezier(0.9, 0.1, 0.1, 0.9);
--global-transition: 350ms var(--global-ease);
```

A sharp, fast-in / fast-out easing curve — confident and snappy.

## Components

### Button — Primary
- Background: `#6B13F5`
- Text: `#F1F0EC`
- Border-radius: 6px
- Padding: `10px 20px`
- Hover: `#B997FF` text on `#6B13F5`, slight scale up
- No shadow by default — flat and confident

### Button — Secondary / Ghost
- Border: `1px solid #44443C`
- Text: `#F1F0EC`
- Background: transparent
- Hover: `surface` background fill

### Input / Secret Field
- Background: `#2D2734`
- Border: `1px solid #44443C`
- Text: `DopplerReproMono`, `#F1F0EC`
- Focus ring: `#6B13F5` with 2px offset

### Secret Row
- Layout: grid with `key | value | environment` columns
- Key: mono font, `#B997FF`
- Value: mono font, masked by default (dots), reveal on hover/click
- Row hover: `surface-raised` background

### Environment Badge
- Pill shape, `radius-full`
- `dev`: `#6B13F5` bg, light text
- `staging`: orange tint
- `production`: green `#00F575` tint (high-visibility)

### Project Sidebar
- Dark left rail, `bg` color
- Active item: `surface` highlight + left `#6B13F5` border
- Icon + label layout

## Guardrails

1. **Never use Inter for display/hero text** — DopplerRepro only at display sizes
2. **Never use white `#FFFFFF` as the primary background** in dark mode — `#1C1624` is canonical
3. **Cream, not white**: light mode background is `#FCFAF6` (warm), not pure white
4. **The brand gradient** (purple→orange→pink) is only for the logo mark — do not apply it to buttons or UI chrome
5. **Regular weight headings** — DopplerRepro reads as strong at 400 weight; do not bold headings
6. **Production environment** always uses green emphasis — never red (red = error only)
7. **Secret values** must be masked by default; never display plaintext on load
8. **`#6B13F5` purple** is the only valid primary CTA color — do not substitute indigo or violet
9. **Mono font for all secret keys and values** — never display secrets in a proportional font
10. **Gradient must be the layered 3-stop sequence** — single-stop purple or orange alone reads as off-brand
