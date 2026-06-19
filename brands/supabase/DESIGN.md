# Supabase DESIGN.md

> Open-source Firebase alternative — a developer-first backend platform with a dark-native dashboard built around a signature emerald green.

## Overview

Supabase's design is dark-native, technical, and intentionally restrained. The aesthetic draws from terminal and code-editor conventions — deep near-black backgrounds, tight borders, and a single chromatic statement in brand green (`#3ECF8E`). The design system is built on Radix UI color primitives, TailwindCSS utility classes, and a Figma-to-CSS pipeline that exports semantic tokens as CSS custom properties.

The core philosophy is "less is more" (explicitly rooted in Dieter Rams). Hierarchy is created through size and color value, not weight or decoration. No bold (700) weights appear in the type system — `400` is default, `500` reserved for interactive labels. Shadows are almost never used; depth is communicated through background layering — `surface-100` → `surface-200` → `surface-300` as surfaces stack. The brand green appears only where it counts: CTAs, active navigation states, and brand identity. Using it anywhere else dilutes its signal.

Dark mode is the primary experience. Light mode exists but is secondary.

## Colors

### Brand

| Token | Hex | Usage |
|-------|-----|-------|
| `brand-green` | `#3ECF8E` | Primary CTA, logo, active nav indicators, focus rings |
| `brand-green-dark` | `#249361` | Pressed/hover state on brand-green elements |
| `brand-link` | `#00C573` | Interactive text links, inline code links |
| `brand-border` | `rgba(62, 207, 142, 0.30)` | Subtle green border highlight, focus outlines |

### Dark Mode (primary experience)

| Token | Hex | Usage |
|-------|-----|-------|
| `background` | `#171717` | App canvas, page background |
| `background-deep` | `#0F0F0F` | Deepest surfaces, button fills, canvas behind sidebar |
| `surface-100` | `#1C1C1C` | Panels, sidebar background, card surfaces |
| `surface-200` | `#242424` | Elevated cards, table row hover, form backgrounds |
| `surface-300` | `#2A2A2A` | Stacked surfaces, active dropdown backgrounds |
| `overlay` | `rgba(41, 41, 41, 0.84)` | Modals, sheet overlays, glass panels |
| `border` | `#2E2E2E` | Default card and panel borders |
| `border-strong` | `#363636` | Button borders, input borders, emphasized dividers |
| `border-stronger` | `#434343` | Hover borders, focus-adjacent borders |
| `text-primary` | `#FAFAFA` | Primary text, headings |
| `text-secondary` | `#B4B4B4` | Secondary labels, metadata |
| `text-muted` | `#898989` | Placeholder text, disabled labels, footnotes |
| `text-faint` | `#4D4D4D` | Least-emphasis text, decorative copy |

### Light Mode

| Token | Hex | Usage |
|-------|-----|-------|
| `background` | `#FFFFFF` | App canvas |
| `surface-100` | `#F9FAFB` | Panel backgrounds (Radix Slate 1) |
| `surface-200` | `#F1F3F5` | Elevated cards (Radix Slate 2) |
| `surface-300` | `#E8EAED` | Deep stacking (Radix Slate 3) |
| `border` | `#DDE1E5` | Default borders (Radix Slate 5) |
| `border-strong` | `#C8CDD2` | Emphasized borders (Radix Slate 6) |
| `text-primary` | `#11181C` | Primary text (Radix Slate 12) |
| `text-secondary` | `#687076` | Secondary text (Radix Slate 10) |
| `text-muted` | `#889096` | Muted text (Radix Slate 9) |

### Semantic / Status

| Token | Hex | Usage |
|-------|-----|-------|
| `success` | `#3ECF8E` | Success states (shares brand-green) |
| `success-subtle` | `rgba(62, 207, 142, 0.12)` | Success badge backgrounds |
| `warning` | `#F5A623` | Warning states, degraded indicators |
| `warning-subtle` | `rgba(245, 166, 35, 0.12)` | Warning badge backgrounds |
| `destructive` | `#E5484D` | Errors, delete actions, destructive CTAs |
| `destructive-subtle` | `rgba(229, 72, 77, 0.12)` | Error badge backgrounds |

## Typography

Supabase uses **Circular** as its primary typeface — a geometric sans-serif with rounded terminals that softens the technical edge without sacrificing density. **Source Code Pro** (with fallback to **Office Code Pro**, **Menlo**) serves all monospace contexts.

- **Primary stack**: `"Circular", "Helvetica Neue", Helvetica, Arial, sans-serif`
- **Mono stack**: `"Source Code Pro", "Office Code Pro", Menlo, monospace`

| Scale | Size | Weight | Line Height | Letter Spacing | Usage |
|-------|------|--------|-------------|----------------|-------|
| `display` | 72px | 400 | 1.00 | normal | Marketing hero headings |
| `heading-xl` | 48px | 400 | 1.10 | -0.02em | Section heroes |
| `heading-lg` | 36px | 400 | 1.25 | normal | Section headings |
| `heading-md` | 24px | 400 | 1.33 | -0.01em | Card titles, dialog headings |
| `heading-sm` | 18px | 400 | 1.56 | normal | Sub-headings, panel titles |
| `body-lg` | 16px | 400 | 1.50 | normal | Primary body copy |
| `body` | 14px | 400 | 1.57 | normal | Default UI text, form labels |
| `nav-link` | 14px | 500 | 1.43 | normal | Navigation links, menu items |
| `button` | 14px | 500 | 1.14 | normal | Button labels |
| `caption` | 12px | 400 | 1.33 | normal | Helper text, metadata |
| `code-label` | 12px | 400 | 1.33 | 0.075em | Uppercase technical labels (mono) |

Notes:
- Hierarchy is driven by **size and color value**, not font weight
- No `700` (bold) weight exists in the standard UI scale
- `code-label` is always uppercase with `letter-spacing: 0.075em` (1.2px at 16px base)
- Inline code uses mono stack at `0.875em` relative to surrounding text

## Spacing

Base unit: **8px**

| Token | Value | Usage |
|-------|-------|-------|
| `space-px` | 1px | Hairline borders, dividers |
| `space-0.5` | 2px | Micro gaps, icon offsets |
| `space-1` | 4px | Tight internal gaps, badge padding |
| `space-1.5` | 6px | Small padding, icon-to-label gaps |
| `space-2` | 8px | Default internal padding (compact) |
| `space-3` | 12px | Comfortable internal padding |
| `space-4` | 16px | Standard component padding, form fields |
| `space-5` | 20px | Card internal padding |
| `space-6` | 24px | Card padding, section gaps |
| `space-8` | 32px | Large internal spacing |
| `space-10` | 40px | Component separation |
| `space-12` | 48px | Section spacing (mobile) |
| `space-16` | 64px | Section spacing (tablet) |
| `space-24` | 96px | Section spacing (desktop) |
| `space-32` | 128px | Hero section padding |

Dashboard components favor `space-2` through `space-4`. Marketing sections use `space-24` and `space-32`.

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-none` | 0px | Tables, data grids, full-bleed elements |
| `radius-xs` | 3px | Tags, tiny chips |
| `radius-sm` | 4px | Badges, small status pills (non-pill style) |
| `radius-md` | 6px | Inputs, selects, ghost buttons, tooltips |
| `radius-lg` | 8px | Cards, dropdowns, sheet panels |
| `radius-xl` | 12px | Feature cards, larger panels |
| `radius-2xl` | 16px | Marketing feature cards |
| `radius-full` | 9999px | Primary pill buttons, tabs, avatar chips |

Supabase mixes radii intentionally — pill buttons (`9999px`) alongside `6px` inputs creates visual contrast between interactive and container elements.

## Shadows

Supabase uses elevation sparingly. Depth is primarily communicated through background color differences. Shadows appear only for floating elements.

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-none` | none | Default; all flat surfaces |
| `shadow-sm` | `0 1px 2px rgba(0,0,0,0.40)` | Subtle separation, input focus rings |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.40)` | Dropdowns, tooltips, popovers |
| `shadow-lg` | `0 8px 32px rgba(0,0,0,0.50)` | Modals, command palettes |
| `shadow-brand` | `0 4px 12px rgba(62,207,142,0.20)` | Focused brand CTAs (use sparingly) |

In dark mode, shadows are heavier (`rgba(0,0,0,0.5–0.6)`) because the low-contrast backgrounds require more shadow depth to register. Avoid decorative box shadows on cards — use border color instead.

## Components

### Button

Supabase uses two distinct button shapes: **pill** (primary CTAs) and **rounded** (interface actions). Mix intentionally — pills for calls-to-action, rounded for in-context actions.

**Primary (Pill)**
- Background: `#3ECF8E` (brand-green)
- Text: `#0F0F0F`
- Padding: `8px 20px`
- Radius: `9999px`
- Font: `14px / 500`
- Hover: background `#249361`
- Focus: `shadow-brand` + `2px` offset ring in `brand-green`

**Default (Outline)**
- Background: `#0F0F0F`
- Text: `#FAFAFA`
- Border: `1px solid #FAFAFA`
- Padding: `8px 16px`
- Radius: `9999px`
- Font: `14px / 500`
- Hover: border `rgba(255,255,255,0.7)`

**Secondary (Interface)**
- Background: `surface-200` (`#242424`)
- Text: `#FAFAFA`
- Border: `1px solid #2E2E2E`
- Padding: `6px 12px`
- Radius: `6px`
- Font: `14px / 500`
- Hover: border `#363636`, background `surface-300`

**Ghost**
- Background: transparent
- Text: `#FAFAFA`
- Border: `1px solid transparent`
- Padding: `6px 12px`
- Radius: `6px`
- Hover: background `surface-200`, border `border`

**Destructive**
- Background: `#E5484D`
- Text: `#FAFAFA`
- Padding: `6px 12px`
- Radius: `6px`

All buttons: `transition: 150ms`, no uppercase, no letter-spacing expansion.

### Input

- Background: `surface-200` (`#242424`) in dark; `#FFFFFF` in light
- Border: `1px solid #2E2E2E` (default) → `#363636` (hover) → `#3ECF8E` (focus)
- Radius: `6px`
- Padding: `8px 12px`
- Font: `14px / 400`, `text-primary`
- Placeholder: `text-muted` (`#898989`)
- Height: `36px` (default), `32px` (compact), `40px` (large)
- Focus ring: `0 0 0 2px rgba(62, 207, 142, 0.25)`
- Error state: border `#E5484D`, focus ring `rgba(229,72,77,0.25)`
- Disabled: `opacity: 0.5`, `cursor: not-allowed`
- Helper/error text: `12px`, `text-muted` or `destructive`, `4px` margin-top

### Card

- Background: `surface-100` (`#1C1C1C`)
- Border: `1px solid #2E2E2E`
- Radius: `8px`
- Padding: `16px` (compact) or `24px` (default)
- Hover (interactive cards): border `#363636`
- Header: `14px / 500`, `text-primary`, `border-bottom: 1px solid border`
- Body: `14px / 400`, `text-secondary`
- Marketing feature cards: radius `16px`, padding `24–32px`, gradient border accent optional

### Navigation (Sidebar)

- Background: `#0F0F0F` (deepest) or `surface-100` (`#1C1C1C`)
- Width: `256px` (desktop), `288px` (mobile drawer)
- Top nav height: `48px`
- Section labels: `11px / 500`, uppercase, `text-muted`, `letter-spacing: 0.075em`, padding `8px 12px`
- Nav item height: `32px`
- Nav item padding: `6px 12px`
- Nav item font: `14px / 400`, `text-secondary`
- Active nav item: background `surface-200`, text `text-primary`, left border `2px solid #3ECF8E`
- Hover nav item: background `surface-200`, text `text-primary`
- Icon size: `16px`, `text-muted` default, `text-primary` on active
- Separator: `1px solid border`, `margin: 4px 0`
- Collapsible: icon-only mode collapses to `48px` wide

### Badge

| Variant | Background | Text | Border |
|---------|------------|------|--------|
| Default | `surface-200` (`#242424`) | `text-secondary` | `1px solid border` |
| Success | `rgba(62,207,142,0.12)` | `#3ECF8E` | `1px solid rgba(62,207,142,0.25)` |
| Warning | `rgba(245,166,35,0.12)` | `#F5A623` | `1px solid rgba(245,166,35,0.25)` |
| Destructive | `rgba(229,72,77,0.12)` | `#E5484D` | `1px solid rgba(229,72,77,0.25)` |
| Brand | `rgba(62,207,142,0.12)` | `#3ECF8E` | none |

- Padding: `2px 8px`
- Radius: `4px`
- Font: `12px / 500`
- Optional leading dot: `6px` circle, same color as text

### Table

- Container: `Card` wrapper, `radius-lg`, `border`
- Header row: background `surface-200`, height `36px`, padding `0 12px`
- Header text: `12px / 500`, `text-muted`, uppercase, `letter-spacing: 0.075em`
- Header border-bottom: `1px solid border-strong`
- Data row: height `44px`, padding `0 12px`
- Data row font: `14px / 400`, `text-primary` (primary col), `text-secondary` (supporting cols)
- Row separator: `1px solid border`
- Hover row: background `surface-200`
- Selected row: background `rgba(62,207,142,0.08)`, left border `2px solid brand-green`
- Empty state: `text-muted`, `14px`, centered, `48px` vertical padding
- Pagination: `32px` height nav controls, `text-secondary`, border-separated from table body

## Layout

Supabase's dashboard uses a two-panel shell — a fixed left sidebar and a scrollable main content area.

- **Shell**: sidebar `256px` fixed left + main fills remaining width
- **Content max-width**: `1280px` centered within main (wider for full-bleed tables/grids)
- **Page header**: `48px` height, `border-bottom: 1px solid border`, contains breadcrumb + actions
- **Content padding**: `24px` horizontal (desktop), `16px` (mobile)
- **Section spacing**: `32px` between page sections
- **Form layouts**: max-width `640px` for single-column forms; two-column at `768px+`
- **Grid**: 12-column, `24px` gap (desktop), 4-column `16px` gap (mobile)
- **Empty canvas (SQL editor, etc.)**: `bg-alternative` — a deeper variant than the standard background
- **Toasts/notifications**: fixed bottom-right, `320px` wide, `shadow-lg`, `radius-lg`

## Responsive Behavior

| Breakpoint | Width | Behavior |
|------------|-------|----------|
| Mobile | < 640px | Sidebar collapses to bottom nav or drawer; single-column layout; reduced content density |
| Tablet | 640px – 1024px | Sidebar collapses to icon-only (48px); main content full-width |
| Desktop | 1024px – 1280px | Full two-panel layout; sidebar 256px; standard density |
| Wide | > 1280px | Content max-width caps at 1280px, centered; data grids expand freely |

- Dashboard tables use `hidden md:table-cell` to hide description columns on narrow viewports
- Marketing site sections use full-viewport-width layouts with 96–128px top/bottom padding on desktop, 48px on mobile
- Navigation on mobile: bottom navigation bar or slide-out drawer (288px)
- Font sizes do not scale with viewport — `14px` body holds at all sizes

## Tone & Guardrails

**DO:**
- Default to dark theme — it is the native, primary experience
- Use `#3ECF8E` only for primary CTAs, active nav states, and brand identity
- Communicate depth through background layering (`surface-100` → `surface-200` → `surface-300`), not shadows
- Keep borders thin (`1px`) and use border-color variation to express hierarchy
- Use `400` weight for body text and `500` for interactive labels only — no `700` in UI
- Apply `9999px` radius to marketing pill buttons, `6px` to interface buttons
- Reserve mono font for code, technical labels, and numeric data that demands alignment
- Use the destructive red only for irreversible or high-consequence actions
- Apply `transition: 150ms` to all interactive states — crisp, not slow

**DON'T:**
- Use brand green as a decorative color, background fill, or general highlight
- Add drop shadows to flat card surfaces — use border color differences instead
- Use `font-weight: 700` or heavier in UI copy
- Add decorative gradients or illustration in the dashboard (marketing site only)
- Round dashboard card corners beyond `8px` — reserve `16px` for marketing cards
- Make the sidebar wider than `256px` without a specific layout need
- Use color alone to convey status — always pair with text or icon
- Use modals for confirmations that can be inline or handled with a toast
- Override `text-muted` for body copy — if text needs to be readable, use `text-secondary` or `text-primary`
- Apply `shadow-brand` (green glow) to more than one element per page
