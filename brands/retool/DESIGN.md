# Retool DESIGN.md

> Build internal tools fast — a dense, functional UI builder that prioritizes utility over aesthetics.

## Overview

Retool's design is unapologetically utilitarian. It's a canvas-and-components tool where maximum information density is the goal. The aesthetic is light-mode-first, uses a classic blue accent, and borrows heavily from enterprise SaaS conventions — tight spacing, data tables, form-heavy layouts. It doesn't try to be beautiful; it tries to be fast and powerful.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#3C5DD6` | CTAs, active states, selected |
| `primary-hover` | `#3251C2` | Hover on primary |
| `primary-light` | `#EEF1FC` | Selected backgrounds, highlights |
| `background` | `#F7F8FA` | App background |
| `surface` | `#FFFFFF` | Panels, cards, canvas items |
| `surface-secondary` | `#F2F3F5` | Hover states, subtle fills |
| `text-primary` | `#1A1A2E` | Body text, headings |
| `text-secondary` | `#5C5F7A` | Supporting text, labels |
| `text-muted` | `#9699B3` | Placeholders, disabled |
| `border` | `#E0E2EA` | Dividers, input borders |
| `border-strong` | `#C8CADB` | Emphasized borders |
| `error` | `#D93025` | Errors |
| `success` | `#1E8A4C` | Success states |
| `warning` | `#F59E0B` | Warnings |

## Typography

- **Font family**: `Inter`, `ui-sans-serif`, `system-ui`, `sans-serif`
- **Mono font**: `JetBrains Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
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

- **Primary**: `primary` background, white text, `4px` radius, `6px 14px` padding, 500 weight
- **Secondary**: `surface` background, `border` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover fills `surface-secondary`
- **Danger**: `error` background, white text
- All: `12px`, `100ms ease`, compact

### Data Table

- Row height: `32px`
- Header: `surface-secondary` background, `label` font, `text-secondary`
- Cell: `body-sm`, `text-primary`, `space-2 space-3` padding
- Selected row: `primary-light` background
- Hover: `surface-secondary`
- Border: `1px solid border` on all cells
- Pagination: compact, bottom-right

### Input / Form Field

- Background: `surface`
- Border: `1px solid border` → `primary` on focus
- Radius: `radius-md`
- Padding: `5px 10px`
- Height: `30px` (compact)
- Label: `label` scale, above field, `text-secondary`

### Left Panel / Component Tree

- Background: `surface`
- Border-right: `1px solid border`
- Width: `240px`
- Item: `28px` height, `space-2 space-3` padding
- Active: `primary-light` background, `primary` text
- Font: `body-sm`

### Canvas Component

- Background: `surface`
- Border: `1px solid border`
- Radius: `radius-md`
- Selected: `2px solid primary` border
- Hover: `primary-light` border tint

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
- DO: Use the blue accent only for selection, focus, and the primary CTA
- DO: Keep forms compact — Retool users are power users
- DO: Use data tables as the default pattern for list data
- DON'T: Add rounded corners above `6px` — enterprise convention
- DON'T: Use decorative visuals, illustrations, or gradients
- DON'T: Animate canvas interactions — performance over delight
- DON'T: Use dark mode — Retool is light-first
- DON'T: Add whitespace that doesn't serve information hierarchy
