# Infisical DESIGN.md

> Open-source secrets management — a security-first platform with a dark, trust-communicating UI and a yellow accent.

## Overview

Infisical's design communicates security and reliability above all. The dark theme conveys seriousness; the yellow accent is distinctive and memorable in a space dominated by blues and greens. The UI is clean and structured, prioritizing clarity for sensitive operations — viewing, editing, and rotating secrets.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#FFDE00` | CTAs, active states, brand accent |
| `primary-hover` | `#F5D000` | Hover on primary |
| `background` | `#0D0D0F` | App background |
| `surface` | `#18181B` | Cards, panels |
| `surface-raised` | `#232326` | Elevated surfaces |
| `surface-overlay` | `#2C2C30` | Dropdowns, modals |
| `text-primary` | `#F4F4F5` | Primary text |
| `text-secondary` | `#A1A1AA` | Supporting text |
| `text-muted` | `#71717A` | Placeholders, disabled |
| `border` | `#27272A` | Dividers |
| `border-strong` | `#3F3F46` | Input borders |
| `error` | `#F87171` | Errors, critical |
| `success` | `#4ADE80` | Success, synced |
| `warning` | `#FB923C` | Warnings |
| `yellow-dim` | `rgba(255,222,0,0.10)` | Subtle primary backgrounds |

### Light Mode

| Token | Hex |
|-------|-----|
| `background` | `#FFFFFF` |
| `surface` | `#FAFAFA` |
| `surface-raised` | `#F4F4F5` |
| `text-primary` | `#09090B` |
| `text-secondary` | `#71717A` |
| `border` | `#E4E4E7` |
| `primary` | `#D4B800` |

## Typography

- **Font family**: `Inter`, `ui-sans-serif`, `system-ui`, `sans-serif`
- **Mono font**: `JetBrains Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `heading-lg` | 20px | 600 | 1.3 |
| `heading-md` | 16px | 600 | 1.4 |
| `body` | 14px | 400 | 1.5 |
| `body-sm` | 13px | 400 | 1.5 |
| `caption` | 12px | 400 | 1.4 |
| `code` | 13px | 400 | 1.6 |

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
| `radius-full` | 9999px | Pills, avatars |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 4px rgba(0,0,0,0.5)` | Subtle |
| `shadow-md` | `0 4px 16px rgba(0,0,0,0.6)` | Dropdowns |
| `shadow-lg` | `0 8px 32px rgba(0,0,0,0.7)` | Modals |

## Components

### Button

- **Primary**: `primary` (#FFDE00) background, `#0D0D0F` text, `6px` radius, `8px 16px` padding, 600 weight
- **Secondary**: `surface-raised` background, `border-strong` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover fills `surface-raised`
- **Danger**: `error` background, white text
- All: `13px`, `120ms ease`

### Secret Row

- Height: `40px`
- Layout: key name (monospace, `body-sm`) + masked value (`••••••••`) + env tag + actions
- Reveal button: eye icon, `text-muted` → `text-primary` on hover
- Copy button: copy icon, appears on row hover
- Border-bottom: `1px solid border`
- Hover: `surface-raised` background

### Environment Selector

- Tabs: Development / Staging / Production
- Active tab: `primary` bottom border, `text-primary`
- Tab font: `body-sm`, 500 weight

### Input

- Background: `surface-raised`
- Border: `1px solid border-strong` → `primary` on focus
- Radius: `radius-md`, height: `36px`
- Secret value inputs: monospace font
- Masked by default with toggle

### Badge

- Padding: `2px 8px`
- Radius: `radius-sm`
- Font: `caption`, 500 weight
- Synced: green-dim; Out of sync: yellow-dim; Error: red-dim

## Layout

- **Sidebar**: `220px` fixed — project tree + environment nav
- **Main**: secrets table fills remaining width
- **Max content width**: none — table is full-width
- **Toolbar**: above table — search + filter + add secret button

## Responsive

- Desktop-first security tool
- Sidebar collapses on mobile
- Secret rows simplify (hide actions, show on tap) on mobile

## Tone & Guardrails

- DO: Yellow accent is the brand — use it confidently for CTAs
- DO: Mask all secret values by default — reveal is an explicit action
- DO: Use monospace for all secret keys and values
- DO: Show environment context always — Dev/Staging/Prod must be unambiguous
- DON'T: Show unmasked secrets in logs or error messages
- DON'T: Use yellow for warning states — it's a brand color here
- DON'T: Use decorative animations near secret operations
- DON'T: Round corners above `8px`
- DON'T: Use light mode as default
