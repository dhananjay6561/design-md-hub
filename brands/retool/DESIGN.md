# Retool DESIGN.md

> Build internal software better, with AI — a low-code platform for building powerful internal tools fast.

## Overview

Retool's design is unapologetically utilitarian. It's a canvas-and-components tool where maximum information density is the goal. After a major brand refresh, the palette moved away from enterprise blue toward a warm neutral system — dark charcoal, off-white cream, and muted accent colors. Light-mode-first, tight spacing, data tables, form-heavy layouts. It doesn't try to be beautiful; it tries to be fast and powerful.

## Colors

**Brand palette (post-2024 rebrand):**

| Token | Hex | Usage |
|-------|-----|-------|
| `color-dark` | `#151515` | Primary CTA background, dark text (light mode) |
| `color-dark-hover` | `#2E2F2D` | Hover on primary button |
| `cream` | `#E9EBDF` | Primary button text, page bg (dark mode) |
| `background` | `#F7F8F4` | App background (light) |
| `surface` | `#FFFFFF` | Panels, cards, canvas items |
| `surface-secondary` | `#EDEDEA` | Hover states, table headers |
| `text-primary` | `#151515` | Body text, headings |
| `text-secondary` | `#59554E` | Supporting text, labels |
| `text-muted` | `#8B8780` | Placeholders, disabled |
| `border` | `#D8D5CC` | Dividers, input borders |
| `border-strong` | `#C0BBB1` | Emphasized borders |
| `blue` | `#518DD2` | Secondary CTAs, focus rings, selection |
| `blue-light` | `#D8E6F3` | Selected row bg, blue tint surfaces |
| `blue-hover` | `#B0CCEA` | Hover on blue outlined actions |
| `orange` | `#E8765E` | Accent highlights, data viz |
| `green` | `#4D9987` | Success, confirmation |
| `error` | `#EF4444` | Errors (`--raw-red-primary`) |
| `success` | `#4D9987` | Success states (green-primary) |
| `warning` | `#ECA438` | Warnings (`--raw-yellow-primary`) |

## Typography

**Font variables (declared as Next.js font vars):**
- `--font-saans` / `saansFont`: custom variable font — display & marketing headings
- `--font-px-grotesk` / `pxGroteskFont`: `Px Grotesk, sans-serif` — UI body font (approximated by DM Sans)
- **Mono**: `JetBrains Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `hero` | `72px` | 300 | 76px |
| `display` | `40px` | 300 | 1.2 |
| `heading-lg` | 18px | 600 | 1.3 |
| `heading-md` | 15px | 600 | 1.4 |
| `heading-sm` | 13px | 600 | 1.4 |
| `body` | 13px | 400 | 1.5 |
| `body-sm` | 12px | 400 | 1.5 |
| `caption` | 11px | 400 | 1.4 |
| `label` | 11px | 500 | 1.3 |
| `code` | 12px | 400 | 1.6 |

Retool uses small type throughout — information density over readability comfort.

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

Retool defaults to tight spacing. Use `space-2` and `space-3` inside components.

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-sm` | 3px | Tags, small badges |
| `radius-md` | 4px | Buttons, inputs, most components |
| `radius-lg` | 6px | Cards, modals |
| `radius-full` | 9999px | Avatars, pills |

Retool uses very tight radii — enterprise-feels intentional.

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 2px rgba(0,0,0,0.06)` | Subtle card lift |
| `shadow-md` | `0 2px 8px rgba(0,0,0,0.08)` | Dropdowns, popovers |
| `shadow-lg` | `0 4px 16px rgba(0,0,0,0.10)` | Modals |

## Components

### Button

- **Primary**: `color-dark` (#151515) background, `cream` text, `4px` radius, `6px 14px` padding, 500 weight
- **Primary hover**: `color-dark-hover` (#2E2F2D) background
- **Secondary outline**: `surface` background, `border-strong` border, `text-primary`
- **Blue outline**: transparent, `1px solid blue`, `blue` text — for secondary actions
- **Ghost**: transparent, `text-secondary`, hover fills `surface-secondary`
- **Danger**: `error` background, white text
- All: `12px`, `100ms ease`, compact

### Data Table

- Row height: `32px`
- Header: `surface-secondary` background, `label` font, `text-secondary`
- Cell: `body-sm`, `text-primary`, `space-2 space-3` padding
- Selected row: `blue-light` background
- Hover: `surface-secondary`
- Border: `1px solid border` on all cells
- Pagination: compact, bottom-right

### Input / Form Field

- Background: `surface`
- Border: `1px solid border` → `blue` on focus
- Radius: `radius-md`
- Padding: `5px 10px`
- Height: `30px` (compact)
- Label: `label` scale, above field, `text-secondary`

### Left Panel / Component Tree

- Background: `surface`
- Border-right: `1px solid border`
- Width: `240px`
- Item: `28px` height, `space-2 space-3` padding
- Active: `blue-light` background, `blue` text
- Font: `body-sm`

### Canvas Component

- Background: `surface`
- Border: `1px solid border`
- Radius: `radius-md`
- Selected: `2px solid blue` border
- Hover: `blue-light` border tint

### Badge

- Padding: `1px 6px`
- Radius: `radius-sm`
- Font: `caption`, 500 weight
- Variants: success, error, warning, neutral

## Layout

- **Three-panel layout**: left component panel + canvas + right property panel
- **Left panel**: `240px`, component tree + query list
- **Right panel**: `280px`, selected component properties
- **Canvas**: fills remaining width, scrollable
- **Top bar**: `44px`, tool controls + app name + deploy button
- **No max-width**: fills the viewport

## Responsive

- Desktop-only app — no mobile layout
- Panels can be collapsed to expand canvas
- Minimum viewport: `1280px`

## Tone & Guardrails

- DO: Maximize information density — small text and tight spacing are features
- DO: Use black (#151515) for the primary CTA — never the blue
- DO: Use the blue accent only for selection, focus, and secondary outlined actions
- DO: Keep forms compact — Retool users are power users
- DO: Use data tables as the default pattern for list data
- DON'T: Add rounded corners above `6px` — enterprise convention
- DON'T: Use decorative visuals, illustrations, or gradients
- DON'T: Animate canvas interactions — performance over delight
- DON'T: Use dark mode — Retool is light-first
- DON'T: Add whitespace that doesn't serve information hierarchy
