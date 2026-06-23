# Resend Design System

> Email for developers — a stark dark-first platform with near-monochrome aesthetics and green status signals.

## Overview

Resend is **dark-first** — pure black (`#000`) background, near-white `#f0f0f0` text, and near-zero decorative color. Status signals (delivered, bounced, opened) carry the only meaningful color. The display font is **ABC Favorit** (geometric grotesque), body is **Inter** variable, code/addresses use **Commit Mono**, and editorial moments use **Domaine Display** serif. The aesthetic is confident, minimal, and dev-native — no gradients, no illustrations, just clean type and subtle borders.

## Colors

### Dark (Primary)

| Token | Hex | Usage |
|-------|-----|-------|
| `background` | `#000000` | Page / app background |
| `canvas` | `#141517` | Slightly lifted surface (cards, panels) |
| `gray-2` | `#1b1b1b` | Input backgrounds, subtle fills |
| `gray-3` | `#2a2a2a` | Borders, dividers |
| `gray-4` | `#313131` | Hover states |
| `gray-9` | `#6e7679` | Very muted text |
| `gray-10` | `#878d8f` | Muted text, placeholders |
| `gray-11` | `#a1a4a5` | Secondary / supporting text |
| `gray-12` | `#f0f0f0` | Primary text (near white) |
| `green-bright` | `#62FFB3` | Brand green — opened/active indicator |
| `green-solid` | `#00c758` | Delivered status, success |
| `red` | `#fb2c36` | Bounced, errors |
| `amber` | `#f99c00` | Pending / warning |
| `blue` | `#3080ff` | Links, info |
| `violet` | `#8d54ff` | Hover accents |

### Light

| Token | Hex |
|-------|-----|
| `background` | `#fdfdfd` |
| `canvas` | `#f3f4f6` |
| `gray-3` | `#e5e5e5` |
| `gray-11` | `#333333` |
| `gray-12` | `#191919` |

## Typography

All fonts loaded from Resend's own CDN via `@font-face`.

- **Display**: `ABC Favorit` (Book 400, Medium 500) — geometric grotesque, used for headings and marketing
- **Sans**: `Inter` (variable, wght 100–900) — UI body, labels, inputs
- **Mono**: `Commit Mono` (Regular 400, Italic) — code, API keys, email addresses, IDs
- **Editorial**: `Domaine Display` (Regular 400, Medium 500, Bold 700) — serif for editorial moments

| Scale | Size | Weight | Font | Line Height |
|-------|------|--------|------|-------------|
| `display` | 56px | 400 | ABC Favorit | 1.05 |
| `heading-lg` | 32px | 400 | ABC Favorit | 1.15 |
| `heading-md` | 20px | 500 | ABC Favorit | 1.3 |
| `heading-sm` | 16px | 500 | Inter | 1.4 |
| `body` | 14px | 400 | Inter | 1.5 |
| `body-sm` | 13px | 400 | Inter | 1.5 |
| `caption` | 12px | 400 | Inter | 1.4 |
| `editorial` | 24px | 400 | Domaine Display | 1.5 |
| `code` | 13px | 400 | Commit Mono | 1.6 |

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
| `radius-sm` | 4px | Badges, tags |
| `radius-md` | 6px | Buttons, inputs |
| `radius-lg` | 8px | Cards, panels |
| `radius-full` | 9999px | Pills, avatars |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 3px rgba(0,0,0,.5)` | Subtle card lift |
| `shadow-md` | `0 4px 12px rgba(0,0,0,.6)` | Dropdowns |
| `shadow-lg` | `0 8px 24px rgba(0,0,0,.7)` | Modals |

## Components

### Button

- **Primary**: `gray-12` (#f0f0f0) bg, `#000` text, `6px` radius, `8px 16px` padding, 500 weight
- **Secondary**: transparent, `1px solid gray-3` border, `gray-12` text, hover fills `gray-2`
- **Ghost**: transparent, `gray-11` text, hover `gray-2` bg
- **Danger**: `red` bg, white text
- All: Inter, `13px`, `120ms ease`

### Input

- Background: `gray-2` (#1b1b1b)
- Border: `1px solid gray-3` → `gray-12` ring on focus
- Radius: `radius-md`, height: `36px`
- Font: `body-sm` Inter; API keys use Commit Mono

### Email Log Row

- Height: `44px`
- Layout: status dot + recipient (Commit Mono) + subject + timestamp + open count
- Hover: `gray-2` background
- Border-bottom: `1px solid gray-3`
- Status: green dot (delivered), red (bounced), amber (pending)

### Metric Card

- Background: `canvas` (#141517)
- Border: `1px solid gray-3`
- Radius: `radius-lg`
- Large number: 28px ABC Favorit, `gray-12`
- Label: `caption` Inter, `gray-11`
- Delta indicator: green (up) or red (down)

### Badge

- Padding: `2px 8px`; Radius: `radius-full`; Font: `caption` 500
- Delivered: `rgba(0,199,88,.15)` bg / `#00c758` text
- Bounced: `rgba(251,44,54,.15)` bg / `#fb2c36` text
- Pending: `rgba(249,156,0,.15)` bg / `#f99c00` text
- Opened: `rgba(98,255,179,.15)` bg / `#62FFB3` text

## Layout

- **Sidebar**: `216px` fixed left — logo + nav only
- **Main**: fills remaining, max `960px` content width
- **Dashboard**: metric cards grid (3–4 col) + email log table
- **API docs**: two-column — prose left, live code right

## Tone & Guardrails

- DO: Keep the UI near-monochrome — color only for status signals and the brand green
- DO: Use Commit Mono for all email addresses, API keys, IDs, and code
- DO: Use ABC Favorit for all headings and display text
- DO: Prioritize email delivery status — it's the core product metric
- DON'T: Add decorative gradients, background images, or illustrations
- DON'T: Use more than 3 accent colors on a single screen
- DON'T: Default to light mode — dark is the primary Resend experience
- DON'T: Round corners above `8px` (except pills)
- DON'T: Show raw SMTP errors — translate to human-readable delivery messages
