# Railway DESIGN.md

> Ship software peacefully — the all-in-one intelligent cloud provider for deploying apps, databases, and everything in between.

## Overview

Railway's design stands out in the dev tools space by being warm and approachable rather than cold and technical. It uses a deep dark background with a distinctive violet/purple accent, smooth animations, and a layout that feels more like a creative tool than an ops dashboard. The hero uses IBM Plex Serif with tight negative tracking for an editorial, premium feel. The brand balances developer seriousness with a sense of delight.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#853bce` | Purple accent, glow effects, active states (`--pink-500`) |
| `primary-hover` | `#6D31A9` | Hover on primary — darker, not lighter (`--pink-600`) |
| `background` | `#13111C` | App background (dark oatmeal) |
| `background-light` | `#F9F3E9` | Light mode background (oatmeal) |
| `surface` | `#181622` | Cards, panels |
| `surface-raised` | `#1F1C2B` | Elevated surfaces |
| `surface-overlay` | `#27243A` | Dropdowns, modals |
| `text-primary` | `#F1F0EF` | Primary text |
| `text-secondary` | `#868593` | Supporting text |
| `text-muted` | `#59497A` | Placeholders, disabled |
| `border` | `#2C2A3E` | Dividers, borders |
| `border-strong` | `#3D3A55` | Inputs, emphasis |
| `error` | `#D85B59` | Errors, destructive (`--red-600: hsl(1, 62%, 60%)`) |
| `warning` | `#DFAE2A` | Warnings, building (`--yellow-500: hsl(44, 74%, 52%)`) |
| `success` | `#72BF9B` | Success, deployed (`--green-600: hsl(152, 38%, 60%)`) |
| `purple-dim` | `rgba(133,59,206,0.12)` | Subtle primary backgrounds |
| `purple-glow` | `rgba(133,59,206,0.20)` | Hover glow on cards |
| `hero-gradient` | `linear-gradient(327deg, rgba(33,0,75,0.24), transparent), linear-gradient(246deg, rgba(209,21,111,0.16), transparent), #13111C` | Landing page hero background |

## Typography

**Font variables (declared in `<style>` on every page):**
- `--font-inter`: `'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`
- `--font-inter-tight`: `'Inter Tight', var(--font-inter)` — condensed, used for UI headings
- `--font-jetbrains-mono`: `'JetBrains Mono', ui-monospace, SFMono-Regular, monospace`
- `--font-ibm-plex-serif`: `'IBM Plex Serif', Georgia, Cambria, 'Times New Roman', serif` — editorial display only

**Font usage:**
- **App body**: `--font-inter` (default `<body>` font)
- **App headings**: `--font-inter-tight` (tighter letterspacing)
- **Marketing display headings**: `--font-ibm-plex-serif` (landing page only)
- **Code / logs / env vars**: `--font-jetbrains-mono`

### Landing page type scale

Railway uses responsive fluid type (`clamp()`) on the marketing site. All display sizes use IBM Plex Serif.

| Class | Size | Line Height | Usage |
|-------|------|-------------|-------|
| `text-huge` | `clamp(48px, 6vw, 64px)` | 1.25 | Largest display hero |
| `text-jumbo` | `clamp(40px, 5vw, 48px)` | 1.25 | Hero subheadings |
| `text-large` | `clamp(32px, 4vw, 40px)` | 1.25 | Section intro headings |
| `text-h1` | `clamp(28px, 2.5vw, 32px)` | 1.375 | Page headings |
| `text-h2` | `clamp(24px, 3vw, 28px)` | 1.375 | Section headings |
| `text-h3` | `clamp(22px, 2.5vw, 24px)` | 1.375 | Card/panel headings |
| `text-h4` | `20px` | 1.375 | Minor headings |
| `text-base` | `16px` | 1.5 | Body copy |
| `text-sm` | `14px` | 1.5 | Labels, metadata |
| `text-xs` | `12px` | 1.4 | Captions |

**Hero headline** — IBM Plex Serif, `40px`, `font-weight: 500`, `letter-spacing: -1.96px`, `line-height: 1.12`

**Section headings** — IBM Plex Serif, `36px`, `font-weight: 400`, `letter-spacing: -0.72px`, `line-height: 48px`

### App type scale

| Scale | Font | Size | Weight | Line Height |
|-------|------|------|--------|-------------|
| `heading-display` | IBM Plex Serif | 36px | 400 | 48px |
| `heading-lg` | Inter Tight | 22px | 600 | 1.3 |
| `heading-md` | Inter Tight | 16px | 600 | 1.4 |
| `heading-sm` | Inter | 14px | 600 | 1.4 |
| `body` | Inter | 14px | 400 | 1.5 |
| `body-sm` | Inter | 13px | 400 | 1.5 |
| `caption` | Inter | 12px | 400 | 1.4 |
| `code` | JetBrains Mono | 12px | 400 | 1.6 |

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

- Background: `#13111C` (same as background)
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
