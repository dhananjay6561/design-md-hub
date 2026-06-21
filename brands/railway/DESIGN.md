# Railway DESIGN.md

> Deploy in seconds — a deployment platform that makes infrastructure feel effortless and almost playful.

## Overview

Railway's design stands out in the dev tools space by being warm and approachable rather than cold and technical. It uses a deep dark background with a distinctive violet/purple accent, smooth animations, and a layout that feels more like a creative tool than an ops dashboard. The brand balances developer seriousness with a sense of delight.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#7B61FF` | CTAs, active states, links |
| `primary-hover` | `#6B50EF` | Hover on primary |
| `background` | `#0B0D0E` | App background |
| `surface` | `#161819` | Cards, panels |
| `surface-raised` | `#1E2022` | Elevated surfaces |
| `surface-overlay` | `#26292B` | Dropdowns, modals |
| `text-primary` | `#F1F0EF` | Primary text |
| `text-secondary` | `#8A8886` | Supporting text |
| `text-muted` | `#555250` | Placeholders, disabled |
| `border` | `#2A2D30` | Dividers, borders |
| `border-strong` | `#383B3E` | Inputs, emphasis |
| `error` | `#FF4444` | Errors, destructive |
| `warning` | `#FFB224` | Warnings |
| `success` | `#23C45E` | Success, deployed |
| `purple-dim` | `rgba(123,97,255,0.12)` | Subtle primary backgrounds |
| `purple-glow` | `rgba(123,97,255,0.20)` | Hover glow on cards |

## Typography

- **Font family**: `Inter`, `ui-sans-serif`, `system-ui`, `sans-serif`
- **Mono font**: `JetBrains Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `heading-lg` | 22px | 600 | 1.3 |
| `heading-md` | 16px | 600 | 1.4 |
| `heading-sm` | 14px | 600 | 1.4 |
| `body` | 14px | 400 | 1.5 |
| `body-sm` | 13px | 400 | 1.5 |
| `caption` | 12px | 400 | 1.4 |
| `code` | 12px | 400 | 1.6 |

## Spacing

Base unit: `4px`

| Token | Value |
|-------|-------|
| `space-1` | 4px |
| `space-2` | 8px |
| `space-3` | 12px |
| `space-4` | 16px |
| `space-5` | 20px |
| `space-6` | 24px |
| `space-8` | 32px |
| `space-10` | 40px |

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-sm` | 4px | Tags, chips |
| `radius-md` | 6px | Buttons, inputs |
| `radius-lg` | 10px | Cards, panels |
| `radius-xl` | 14px | Large modals |
| `radius-full` | 9999px | Pills, avatars |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 4px rgba(0,0,0,0.5)` | Subtle |
| `shadow-md` | `0 4px 20px rgba(0,0,0,0.6)` | Cards, dropdowns |
| `shadow-lg` | `0 8px 40px rgba(0,0,0,0.7)` | Modals |
| `glow-purple` | `0 0 20px rgba(123,97,255,0.25)` | Accent glow |

## Components

### Button

- **Primary**: `primary` background, white text, `6px` radius, `8px 18px` padding, 500 weight
- **Secondary**: `surface-raised` background, `border-strong` border
- **Ghost**: transparent, `text-secondary`, hover shows `surface-raised`
- **Danger**: `error` background, white text
- All: `13px`, `120ms ease`

### Service Card (Canvas)

- Background: `surface`
- Border: `1px solid border`
- Radius: `radius-lg`
- Padding: `space-4`
- Hover: `purple-glow` box-shadow + `border-strong` border
- Status dot: colored circle (success/error/building/idle)
- Railway uses a **canvas layout** for services — cards float on a grid

### Deploy Log

- Background: `#0B0D0E` (same as background)
- Font: monospace, `12px`
- Color-coded: green for success lines, red for errors, muted for info
- Scrollable panel, fixed height

### Input

- Background: `surface-raised`
- Border: `1px solid border` → `primary` on focus with subtle `glow-purple`
- Radius: `radius-md`, height: `36px`
- Font: `body-sm`

### Badge / Status

- Padding: `3px 8px`
- Radius: `radius-full` (pill)
- Font: `caption`, 500 weight
- Deployed: green-dim; Building: orange-dim; Failed: red-dim; Sleeping: gray

## Layout

- **Canvas view**: infinite canvas with draggable service cards
- **List view**: traditional sidebar + content layout
- **Sidebar**: `220px`, collapsible
- **Max content width**: `1100px`
- **Deploy panel**: slides in from right, `440px` wide

## Responsive

- Canvas view disables on mobile, falls back to list
- Sidebar collapses to bottom nav
- Desktop-first, but functional on tablet

## Tone & Guardrails

- DO: Use violet/purple accent for all interactive highlights
- DO: Keep the canvas view clean — services are the content
- DO: Use status colors consistently: green=live, yellow=building, red=error
- DO: Animate deployments — motion communicates progress
- DON'T: Use harsh drop shadows — glow effects instead
- DON'T: Clutter the canvas with too much metadata per card
- DON'T: Use light backgrounds inside the app — dark only
- DON'T: Use more than one glow effect per screen
- DON'T: Show raw stack traces inline — collapse behind "show details"
