# Neon DESIGN.md

> Serverless Postgres with a dark, developer-focused interface and a signature green glow.

## Overview

Neon's design is dark-first, minimal, and technical. It signals modern infrastructure — the deep dark backgrounds, subtle green accent, and monospace-heavy UI communicate that this is a tool built for engineers. The aesthetic references terminal culture without being retro — clean, precise, and fast-feeling.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#00E599` | CTAs, active states, brand accent |
| `primary-hover` | `#00CC88` | Hover on primary |
| `background` | `#0C0C0C` | App background |
| `surface` | `#141414` | Cards, panels |
| `surface-raised` | `#1C1C1C` | Elevated surfaces, dropdowns |
| `surface-overlay` | `#242424` | Modals, tooltips |
| `text-primary` | `#EDEDED` | Primary text |
| `text-secondary` | `#8C8C8C` | Supporting text, metadata |
| `text-muted` | `#555555` | Placeholders, disabled |
| `border` | `#282828` | Dividers, subtle borders |
| `border-strong` | `#333333` | Input borders, emphasis |
| `error` | `#F04747` | Errors |
| `warning` | `#F5A623` | Warnings |
| `success` | `#00E599` | Success (same as primary) |
| `green-dim` | `rgba(0,229,153,0.10)` | Subtle primary backgrounds |
| `green-glow` | `rgba(0,229,153,0.15)` | Glow effects on focus |

## Typography

- **Font family**: `Inter`, `ui-sans-serif`, `system-ui`, `sans-serif`
- **Mono font**: `JetBrains Mono`, `ui-monospace`, `Menlo`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `heading-lg` | 24px | 600 | 1.3 |
| `heading-md` | 18px | 600 | 1.4 |
| `heading-sm` | 14px | 600 | 1.4 |
| `body` | 14px | 400 | 1.5 |
| `body-sm` | 13px | 400 | 1.5 |
| `caption` | 12px | 400 | 1.4 |
| `code` | 13px | 400 | 1.6 |

Mono font used heavily — SQL editors, connection strings, branch names, metrics.

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
| `radius-sm` | 3px | Tags, small chips |
| `radius-md` | 6px | Buttons, inputs, cards |
| `radius-lg` | 8px | Modals, larger panels |
| `radius-full` | 9999px | Avatars, status dots |

## Shadows

Elevation via background layering, not shadows. Dark UI only.

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 4px rgba(0,0,0,0.5)` | Subtle |
| `shadow-md` | `0 4px 16px rgba(0,0,0,0.6)` | Dropdowns |
| `glow-primary` | `0 0 16px rgba(0,229,153,0.2)` | Focus glow |

## Components

### Button

- **Primary**: `primary` (#00E599) background, `#0C0C0C` text, `6px` radius, `8px 16px` padding, 500 weight
- **Secondary**: `surface-raised` background, `border-strong` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover fills `surface-raised`
- **Danger**: `#F04747` background, white text
- All: `13px`, `100ms ease`

### Input / SQL Editor

- Background: `surface-raised`
- Border: `1px solid border` → `border-strong` hover → `primary` focus with `glow-primary`
- Radius: `radius-md`
- Font: monospace for SQL/connection strings, sans-serif for labels
- Height: `36px` standard inputs

### Project / Branch Card

- Background: `surface`
- Border: `1px solid border`
- Radius: `radius-lg`
- Padding: `space-4 space-5`
- Hover: `border-strong` border + `surface-raised` background
- Branch indicator: green dot + monospace branch name

### Metrics / Stats

- Numbers in monospace, large weight 600
- Green for positive values, red for errors
- Subtle sparkline charts using `primary` color

### Badge

- Padding: `2px 6px`
- Radius: `radius-sm`
- Font: `caption`, 500 weight
- Status variants: active (green-dim), idle (surface-raised), error (red)

## Layout

- **Sidebar**: `240px` fixed, dark background
- **Main**: scrollable content area
- **Max content width**: `960px` for dashboards
- **SQL editor**: full-width, resizable panel
- **Metrics grid**: 2–4 column responsive grid

## Responsive

- Desktop-first developer tool
- Sidebar collapses on mobile
- SQL editor simplified on small screens

## Tone & Guardrails

- DO: Use green accent only for CTAs, active states, and success
- DO: Prefer monospace for all technical values (IDs, branches, SQL)
- DO: Keep backgrounds layered — depth via color steps not shadows
- DO: Make metrics and numbers the visual hero on dashboard screens
- DON'T: Use the green glow decoratively — only on interactive focus
- DON'T: Add rounded corners above `8px` — keep the UI sharp
- DON'T: Use light mode as the primary experience
- DON'T: Add illustrations or marketing visuals inside the dashboard
- DON'T: Show loading spinners where skeleton screens work better
