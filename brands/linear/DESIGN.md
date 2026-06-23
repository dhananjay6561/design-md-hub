# Linear DESIGN.md

> The product development system for teams and agents.

## Overview

Linear's design is dark-first, dense, and precise. It prioritizes information density over whitespace, speed over decoration, and keyboard-first workflows. The aesthetic is technical and minimal — almost brutalist in its restraint — with a deep purple accent as the only color statement.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#5E6AD2` | Active states, CTAs, links |
| `primary-hover` | `#4F5BBF` | Hover on primary |
| `background` | `#08090A` | App background |
| `surface` | `#191D20` | Panels, sidebars |
| `surface-raised` | `#222529` | Cards, dropdowns |
| `surface-overlay` | `#2E3033` | Modals, popovers |
| `text-primary` | `#F2F2F3` | Primary text |
| `text-secondary` | `#8A8A9A` | Supporting text, metadata |
| `text-muted` | `#5A5A6A` | Placeholders, disabled |
| `border` | `#2A2A2E` | Dividers, subtle borders |
| `border-strong` | `#3A3A40` | Input borders, emphasized |
| `error` | `#E5484D` | Errors, destructive |
| `warning` | `#FFB224` | Warnings |
| `success` | `#46A758` | Success, completed |
| `purple-dim` | `rgba(94,106,210,0.15)` | Subtle primary backgrounds |

## Typography

- **Font family**: `Inter`, `ui-sans-serif`, `system-ui`, `sans-serif`
- **Mono font**: `JetBrains Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `heading-lg` | 20px | 600 | 1.3 |
| `heading-md` | 16px | 600 | 1.4 |
| `heading-sm` | 13px | 600 | 1.4 |
| `body` | 14px | 400 | 1.5 |
| `body-sm` | 13px | 400 | 1.5 |
| `caption` | 12px | 400 | 1.4 |
| `label` | 12px | 500 | 1.3 |
| `code` | 12px | 400 | 1.6 |

Letter spacing: `-0.01em` on all text, `-0.02em` on headings.

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

Linear is intentionally dense — prefer `space-2` and `space-3` inside components.

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-sm` | 3px | Tags, badges, small chips |
| `radius-md` | 6px | Buttons, inputs, cards |
| `radius-lg` | 8px | Modals, larger panels |
| `radius-full` | 9999px | Avatars, status dots |

Linear uses tight radii — nothing feels overly rounded.

## Shadows

Linear avoids decorative shadows. Elevation is communicated through background color differences, not shadows.

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.4)` | Subtle separation |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.5)` | Dropdowns, tooltips |
| `shadow-lg` | `0 8px 32px rgba(0,0,0,0.6)` | Modals |

## Components

### Button

- **Primary**: `primary` background, white text, `6px` radius, `7px 14px` padding, 500 weight
- **Secondary**: `surface-raised` background, `border-strong` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover shows `surface-raised`
- **Danger**: `error` background or `error` text with transparent bg
- All buttons: `13px`, `font-weight: 500`, no uppercase, transition `100ms`
- Hover states feel instant — Linear is fast

### Issue Row (List Item)

- Height: `36px`
- Padding: `space-2 space-3`
- Layout: icon + title + metadata in a horizontal row
- Status icon: `16px`, colored dot or icon
- Priority icon: `14px`, left of status
- Title: `body` size, `text-primary`
- Metadata (assignee, label, due): `text-secondary`, right-aligned
- Hover: `surface-raised` background
- Selected: `purple-dim` background + `primary` left border `2px`

### Sidebar / Navigation

- Background: `surface` (`#191D20`)
- Width: `220px`, collapsible
- Section headers: `label` scale, `text-muted`, uppercase, `space-2` padding
- Nav item: `32px` height, `space-2 space-3` padding, `body-sm`
- Active: `surface-raised` background, `text-primary`
- Icon: `16px`, `text-secondary` default, `text-primary` on active

### Command Palette (Cmd+K)

- Background: `surface-overlay`
- Border: `1px solid border-strong`
- Radius: `radius-lg`
- Shadow: `shadow-lg`
- Input: borderless, `16px`, `text-primary`
- Result item: `36px` height, icon + label + shortcut hint
- Active result: `surface-raised` background

### Input / Select

- Background: `surface-raised`
- Border: `1px solid border` → `border-strong` on hover → `primary` on focus
- Radius: `radius-md`
- Padding: `6px 10px`
- Font: `body-sm`
- Height: `32px` for single-line inputs

### Badge / Label

- Padding: `2px 6px`
- Radius: `radius-sm`
- Font: `label` (12px, 500)
- Dot + text layout for status badges
- Colors are muted/pastel variants of status colors on dark backgrounds

## Layout

- **Sidebar**: fixed `220px` left, collapsible
- **Main**: full remaining width, with its own inner layout (list, board, etc.)
- **Toolbar**: `48px` height, sits above content
- **No max-width**: Linear fills the viewport — it's a dense app
- **Board view**: Kanban columns, fixed width `280px`, horizontal scroll

## Responsive

Linear is desktop-first. Mobile is minimal — sidebar collapses, most features remain available but density reduces.

## Tone & Guardrails

- DO: Default to dark theme — it's the primary experience
- DO: Keep UI dense; whitespace is earned, not default
- DO: Use the purple accent only for selection, focus, and active state
- DO: Make interactions feel instant — `100ms` max for hover transitions
- DO: Use keyboard shortcuts everywhere; surface them in tooltips
- DON'T: Use rounded corners larger than `8px`
- DON'T: Add decorative gradients, illustrations, or hero images
- DON'T: Use color for anything other than status, priority, and labels
- DON'T: Add loading spinners where optimistic UI is possible
- DON'T: Use modals for simple confirmations — prefer inline or toast
