# Claude (Anthropic) DESIGN.md

> Warm, minimal, and human — an AI interface that feels thoughtful rather than mechanical.

## Overview

Claude's design language prioritizes legibility, warmth, and calm focus. It avoids the cold blues common in enterprise software, instead leaning into creamy off-whites, deep charcoals, and a distinctive coral-orange accent. The aesthetic is editorial — generous whitespace, clear hierarchy, no visual clutter.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#D97757` | CTAs, active states, highlights |
| `primary-hover` | `#C4633F` | Button hover |
| `background` | `#FAF9F7` | Page background (warm white) |
| `surface` | `#FFFFFF` | Cards, panels |
| `surface-secondary` | `#F3F2EF` | Subtle section backgrounds |
| `text-primary` | `#1A1A1A` | Body text, headings |
| `text-secondary` | `#6B6B6B` | Supporting text, metadata |
| `text-muted` | `#9E9E9E` | Placeholders, disabled |
| `border` | `#E5E4E0` | Dividers, input borders |
| `border-strong` | `#CCCBC7` | Emphasized borders |
| `error` | `#E53935` | Error states |
| `success` | `#43A047` | Success states |

### Dark Mode

| Token | Hex |
|-------|-----|
| `background` | `#1A1A1A` |
| `surface` | `#242424` |
| `surface-secondary` | `#2E2E2E` |
| `text-primary` | `#F0EFE9` |
| `border` | `#3A3A3A` |

## Typography

- **Font family**: `Söhne`, `ui-sans-serif`, `system-ui`, `-apple-system`, `sans-serif`
- **Mono font**: `Söhne Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `display` | 32px | 600 | 1.2 |
| `heading-lg` | 24px | 600 | 1.3 |
| `heading-md` | 18px | 600 | 1.4 |
| `body` | 15px | 400 | 1.6 |
| `body-sm` | 13px | 400 | 1.5 |
| `caption` | 12px | 400 | 1.4 |
| `code` | 13px | 400 | 1.6 |

Letter spacing: tighter on headings (`-0.01em`), normal on body.

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
| `space-12` | 48px |

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-sm` | 4px | Tags, badges |
| `radius-md` | 8px | Inputs, small cards |
| `radius-lg` | 12px | Cards, modals |
| `radius-xl` | 16px | Large panels |
| `radius-full` | 9999px | Pills, avatars |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 2px rgba(0,0,0,0.05)` | Subtle lift |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.08)` | Cards, dropdowns |
| `shadow-lg` | `0 8px 24px rgba(0,0,0,0.12)` | Modals, popovers |

## Components

### Button

- **Primary**: coral background (`#D97757`), white text, `8px` radius, `10px 18px` padding, 500 weight
- **Secondary**: transparent, `1px solid border-strong`, hover fills `surface-secondary`
- **Ghost**: no border, `text-secondary`, hover fills `surface-secondary`
- **Danger**: `#E53935` background, white text
- All buttons: `14px`, transition `150ms ease`, no harsh box-shadows

### Input / Textarea

- Border: `1px solid border` → `border-strong` on hover → `primary` on focus
- Background: `surface`
- Padding: `10px 14px`
- Radius: `radius-md`
- Placeholder: `text-muted`
- Font: `body` scale

### Message Bubble (Chat)

- **User**: `surface-secondary` background, `radius-lg` with top-left `4px` (tail), right-aligned, max-width `70%`
- **Assistant**: `surface` background, `1px solid border`, `radius-lg` with top-right `4px`, left-aligned, max-width `80%`
- Padding: `space-4 space-5`
- Code blocks inside: `surface-secondary`, `radius-md`, monospace font

### Sidebar / Navigation

- Background: `surface-secondary`
- Width: `260px`
- Item padding: `space-2 space-3`
- Active item: `primary` left border `2px`, `surface` background
- Item text: `text-secondary` default, `text-primary` on active/hover
- Font: `body-sm`, 500 weight on active

### Card

- Background: `surface`
- Border: `1px solid border`
- Radius: `radius-lg`
- Padding: `space-6`
- Shadow: `shadow-sm` default, `shadow-md` on hover
- Transition: `150ms ease`

### Badge / Tag

- Padding: `2px 8px`
- Radius: `radius-sm`
- Font: `caption`, 500 weight
- Variants: neutral (`surface-secondary`), primary (coral, low opacity bg), success, error

## Layout

- **Max content width**: `768px` for prose/chat, `1200px` for dashboards
- **Sidebar layout**: fixed left sidebar `260px` + scrollable main content
- **Chat layout**: centered column, input pinned to bottom
- **Grid**: 12-column, `24px` gutter
- **Section padding**: `space-8` vertical, `space-6` horizontal on mobile

## Responsive

- Sidebar collapses to bottom nav or hamburger on mobile (`< 768px`)
- Typography scales down ~10% on mobile
- Cards go full-width on mobile
- Chat bubbles max-width expands to `90%` on mobile

## Tone & Guardrails

- DO: Use generous whitespace — crowded UI feels anxious
- DO: Prefer warm neutrals over pure white/black
- DO: Use the coral accent sparingly — one CTA per view
- DO: Animate with `ease` curves, keep transitions under `200ms`
- DON'T: Use harsh drop shadows or heavy borders
- DON'T: Use blue as a primary color — it conflicts with the brand
- DON'T: Use all-caps headings
- DON'T: Use more than 2 font weights on a single screen
- DON'T: Add decorative gradients or glass-morphism effects
