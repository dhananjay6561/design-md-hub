# Fly.io DESIGN.md

> Deploy apps close to your users — a developer platform with a bold, dark aesthetic and a distinctive purple accent.

## Overview

Fly.io's design is dark, confident, and developer-native. It doesn't shy away from strong contrast — deep near-blacks, bright purple highlights, and a deliberate use of gradient accents. The aesthetic is modern infrastructure: technical, fast, and direct. Marketing pages use rich gradients and glows; the dashboard is cleaner and more restrained.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#8B5CF6` | CTAs, active states, links |
| `primary-hover` | `#7C3AED` | Hover on primary |
| `background` | `#0E0E10` | App background |
| `surface` | `#18181B` | Cards, panels |
| `surface-raised` | `#27272A` | Elevated surfaces, dropdowns |
| `surface-overlay` | `#3F3F46` | Modals, tooltips |
| `text-primary` | `#FAFAFA` | Primary text |
| `text-secondary` | `#A1A1AA` | Supporting text, metadata |
| `text-muted` | `#71717A` | Placeholders, disabled |
| `border` | `#27272A` | Dividers, subtle borders |
| `border-strong` | `#3F3F46` | Input borders, emphasis |
| `error` | `#F87171` | Errors |
| `warning` | `#FCD34D` | Warnings |
| `success` | `#34D399` | Success, running |
| `purple-dim` | `rgba(139,92,246,0.15)` | Subtle primary backgrounds |
| `purple-glow` | `rgba(139,92,246,0.25)` | Glow on focus/hover |

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
| `radius-lg` | 10px | Cards, panels |
| `radius-full` | 9999px | Pills, avatars |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 4px rgba(0,0,0,0.5)` | Subtle |
| `shadow-md` | `0 4px 16px rgba(0,0,0,0.6)` | Dropdowns |
| `shadow-lg` | `0 8px 32px rgba(0,0,0,0.7)` | Modals |
| `glow-purple` | `0 0 20px rgba(139,92,246,0.3)` | Focus glow |

## Components

### Button

- **Primary**: `primary` background, white text, `6px` radius, `8px 18px` padding, 500 weight
- **Secondary**: `surface-raised` background, `border-strong` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover fills `surface-raised`
- **Danger**: `error` color background, white text
- All: `13px`, `120ms ease`

### App Card

- Background: `surface`
- Border: `1px solid border`
- Radius: `radius-lg`
- Padding: `space-4 space-5`
- Status dot: green (running), yellow (starting), red (stopped)
- Hover: `purple-glow` box-shadow
- Region tag: monospace, `caption` size

### Input

- Background: `surface-raised`
- Border: `1px solid border-strong` → `primary` focus with `glow-purple`
- Radius: `radius-md`, height: `36px`
- Padding: `8px 12px`
- Font: `body-sm`

### Log Output

- Background: `background`
- Font: monospace, `12px`, `line-height: 1.6`
- Green for stdout, red for stderr, muted for timestamps
- Scrollable with fixed height panel

### Badge

- Padding: `3px 8px`
- Radius: `radius-full`
- Font: `caption`, 500 weight
- Running: green-dim; Stopped: gray; Error: red-dim; Starting: yellow-dim

## Layout

- **Sidebar**: `220px` fixed left
- **Main content**: scrollable, fills remaining width
- **Max content width**: `1000px`
- **Top bar**: `48px`, app name + region + actions

## Responsive

- Desktop-first developer tool
- Sidebar collapses to icons on narrow viewports
- Log panels scroll horizontally on mobile

## Tone & Guardrails

- DO: Use purple accent for all interactive states
- DO: Use status colors consistently — green=running, red=stopped, yellow=starting
- DO: Show region/location data — proximity is a core product value
- DO: Use monospace for all machine-generated output
- DON'T: Use light backgrounds in the dashboard — dark only
- DON'T: Use more than one glow effect per view
- DON'T: Round corners above `10px`
- DON'T: Hide errors — surface them clearly with actionable messages
