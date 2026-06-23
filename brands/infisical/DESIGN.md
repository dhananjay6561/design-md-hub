# Infisical Design System

> The modern security platform — light-first, volt-accented, geometric-grotesque type on near-white surfaces with a distinctive neon-yellow highlight motif.

## Overview

Infisical is **light-first** — the primary experience is white (`#ffffff`) and light gray (`#f3f4f6`) with pure black text. The brand accent is **volt** (`#f5f841`), a neon yellow used as a text-highlight marker on headings and as the primary CTA background. The display and UI font is **AllianceNo2** (geometric grotesque, loaded from Infisical CDN). Code, keys, and secret values use **JetBrains Mono**. The aesthetic is confident and editorial — large type, clean surfaces, and a memorable neon-on-white contrast that stands out in a sea of blue dev tools.

## Colors

### Light (Primary)

| Token | Value | Usage |
|-------|-------|-------|
| `--v2-color-bg` | `#ffffff` | Component / card background |
| `--v2-color-bg-page` | `#f3f4f6` | Page background |
| `--v2-color-border` | `#eaeaea` | Borders, dividers |
| `--v2-color-frame` | `#d1d1d1` | Input borders, strong dividers |
| `--v2-color-text` | `#000000` | Primary text |
| `--v2-color-text-muted` | `rgba(38,38,38,0.32)` | Secondary / supporting text |
| `--v2-color-text-subtle` | `#737373` | Placeholders, metadata |
| `--v2-color-volt` | `#f5f841` | Brand accent — CTA bg, H1 highlight marker |
| `--v2-color-void` | `#000000` | CTA bg (dark buttons), text on volt |
| `--v2-color-accent-green` | `#56a600` | Secrets product color (lime green) |
| `--v2-color-accent-deep-green` | `#23776a` | Deep green hover/active |
| `--v2-color-accent-lime` | `#dbf530` | Lime variant |
| `--v2-color-tint` | `#c3c3c3` | Subtle fills |
| `--v2-color-shade` | `#111111` | Near-black for contrast |

### Dark (`[data-v2-theme=dark]`)

| Token | Value | Usage |
|-------|-------|-------|
| `--v2-color-bg` | `#131316` | Surface / card background |
| `--v2-color-bg-page` | `#0e0e11` | Page background |
| `--v2-color-border` | `#1d1d22` | Borders |
| `--v2-color-frame` | `#2a2a30` | Input borders |
| `--v2-color-text` | `#e4e4e7` | Primary text |
| `--v2-color-text-muted` | `rgba(228,228,231,0.5)` | Supporting text |
| `--v2-color-text-subtle` | `#a1a1aa` | Muted / metadata |
| `--v2-color-volt` | `#c2d72a` | Dark-mode volt — same highlight, muted |
| `--v2-color-shade` | `#131316` | Same as bg in dark |
| `--v2-color-border-dark` | `#1d1d22` | Strong borders |

### Product Colors

| Product | Ink | Accent |
|---------|-----|--------|
| Secrets Management | `#56a600` (lime green) | `#f5f841` (volt) |
| Certificate Management (PKI) | `#a16207` (amber) | `#ffe601` |
| PAM (Privileged Access) | `#dc2626` (red) | `#ffc299` |

## Typography

All fonts loaded via `@font-face` from Infisical CDN + Google Fonts.

- **Display + UI**: `AllianceNo2` — geometric grotesque, loaded from Infisical CDN as OTF
- **Mono**: `JetBrains Mono` — Google Fonts, used for secret keys, values, code, commands

| Scale | Size | Weight | Font | Line Height |
|-------|------|--------|------|-------------|
| `h1` | 3.5rem (56px) | 700 | AllianceNo2 | 1.1 |
| `h2` | 2.25rem (36px) | 700 | AllianceNo2 | 1.1 |
| `h3` | 1.125rem (18px) | 600 | AllianceNo2 | 1.3 |
| `body-lg` | 1.125rem (18px) | 400 | AllianceNo2 | 1.5 |
| `body` | 1rem (16px) | 400 | AllianceNo2 | 1.5 |
| `body-sm` | 0.875rem (14px) | 400 | AllianceNo2 | 1.5 |
| `caption` | 0.75rem (12px) | 400 | AllianceNo2 | 1.4 |
| `code` | 13px | 400 | JetBrains Mono | 1.6 |

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

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-sm` | 4px | Tags, badges |
| `radius-md` | 6px | Buttons, inputs |
| `radius-lg` | 8px | Cards, panels |
| `radius-full` | 9999px | Pills |

## Shadows

Light bg — shadows are subtle gray:

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 3px rgba(0,0,0,.08)` | Subtle card lift |
| `shadow-md` | `0 4px 12px rgba(0,0,0,.10)` | Dropdowns |
| `shadow-lg` | `0 8px 32px rgba(0,0,0,.12)` | Modals |

## Components

### Button

- **Primary (dark)**: `#000000` bg, `#f5f841` (volt) text, `6px` radius, `8px 16px` padding, 600 weight
- **Primary (volt)**: `#f5f841` bg, `#000000` text — for inline CTAs
- **Secondary**: `#ffffff` bg, `#eaeaea` border, `#000000` text, hover: `#f3f4f6` bg
- **Ghost**: transparent, `#737373` text, hover: `#f3f4f6` bg
- All: AllianceNo2, `14px`, `120ms ease`

### Secret Row

- Height: `40px`
- Layout: key name (JetBrains Mono 13px) + masked value (`•••••••••`) + copy + reveal + delete
- Default state: value fully masked
- Revealed state: value visible for 3s then auto-masks
- Hover: `#f3f4f6` bg
- Border-bottom: `1px solid #eaeaea`

### Environment Tabs

- Tabs: Development / Staging / Production
- Active: `#000000` bottom border 2px, `#000000` text, 600 weight
- Inactive: `#737373` text, 400 weight
- Tab font: AllianceNo2 14px

### Input

- Background: `#ffffff`
- Border: `1px solid #d1d1d1` → `#000000` on focus
- Radius: `6px`, height: `36px`
- Font: AllianceNo2 14px; secret values use JetBrains Mono
- Placeholder: `#c3c3c3`

### Badge

- Padding: `2px 8px`; Radius: `9999px`; Font: 12px 500
- Active / Synced: `rgba(86,166,0,.12)` bg / `#56a600` text
- Error: `rgba(220,38,38,.12)` bg / `#dc2626` text
- Pending: `rgba(245,248,65,.25)` bg / `#56a600` text (volt tint)

### H1 Highlight Motif

The signature typography element: key words in the H1 get a volt-yellow background marker effect. Words like "Secrets", "Certificates", "AI Agents" are wrapped with `background: var(--v2-color-volt)` and `color: #000000`. This is Infisical's most recognizable visual signature.

## Layout

- **Navbar**: full-width, `56px` height, white bg, logo left + nav center + CTAs right
- **Hero**: centered, max `1200px`, large H1 with volt marker, subtitle below, dual CTAs
- **Secrets dashboard**: left sidebar (project tree) + main panel (toolbar + table)
- **Table toolbar**: search left + filter + "Add Secret" button right

## Tone & Guardrails

- DO: Light-first — white surfaces are the primary experience
- DO: Use volt (`#f5f841`) for CTAs and highlighted H1 words — it's the brand signature
- DO: Use JetBrains Mono for ALL secret keys, values, paths, and IDs
- DO: Mask all secret values by default — reveal is always an explicit user action
- DO: Keep the UI clean and structured — security tools must feel trustworthy, not cluttered
- DON'T: Default to dark mode — the primary Infisical experience is light
- DON'T: Use volt for error/warning states — it's a brand accent, not a semantic color
- DON'T: Use Inter or other fonts — AllianceNo2 is the brand font
- DON'T: Round corners above `8px` on cards; buttons use `6px`, not pills
- DON'T: Show unmasked secret values in any list or log view
