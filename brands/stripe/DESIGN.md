# Stripe DESIGN.md

> Financial infrastructure for the internet — polished, precise, and built to make complexity feel effortless.

## Overview

Stripe's design philosophy is rooted in trustworthiness and technical elegance. The system communicates financial authority without coldness — clean white surfaces, a deep navy for authoritative text, and a signature indigo accent that feels energetic without being aggressive. Typography runs light and airy (weight 300–400), leveraging negative letter-spacing on display text to create a confident editorial density. The overall effect is deliberate restraint: every element earns its place, whitespace is generous to a fault, and decoration is replaced by information architecture.

Core principles:
- **Clarity over cleverness** — interfaces must be immediately legible to non-technical operators
- **Generous space** — breathing room signals precision and trust in a financial context
- **Restrained color** — indigo accent is used sparingly to guide attention, not saturate it
- **Accessible by default** — WCAG AA contrast on all text; color is never the sole signal

---

## Colors

### Light Mode

| Token | Hex | Usage |
|-------|-----|-------|
| `brand-indigo` | `#635BFF` | Primary CTAs, active nav, focus rings |
| `brand-indigo-alt` | `#533AFD` | Accent borders, interactive highlights |
| `brand-lavender` | `#7F7DFC` | Hover states on brand elements |
| `brand-indigo-dim` | `rgba(99,91,255,0.10)` | Focus ring shadow, subtle tints |
| `brand-orange` | `#FF6118` | Secondary accent, warm highlights |
| `text-primary` | `#0A2540` | Headings, primary body text |
| `text-body` | `#273951` | Body paragraphs, form labels |
| `text-secondary` | `#50617A` | Subheadings, supporting text |
| `text-subdued` | `#64748D` | Captions, metadata, placeholders |
| `background` | `#FFFFFF` | Page background, card surfaces |
| `background-offset` | `#F6F9FC` | Alternate rows, sidebar fills, page washes |
| `background-mist` | `#F8FAFD` | Input backgrounds, subtle containers |
| `border-quiet` | `#E5EDF5` | Dividers, input borders at rest |
| `border-neutral` | `#C9D5E0` | Emphasized borders, selected states |
| `border-accent` | `#533AFD` | Focused inputs, active component rings |
| `success-text` | `#3EAE20` | Success badge text |
| `success-bg` | `#EEFAE9` | Success badge fill |
| `success-border` | `#BFEDAA` | Success badge border |
| `warning-text` | `#F27400` | Warning badge text |
| `warning-bg` | `#FFF3E0` | Warning badge fill |
| `warning-border` | `#FFCB7A` | Warning badge border |
| `danger-text` | `#DF1B41` | Error badge text, destructive actions |
| `danger-bg` | `#FDE8ED` | Error badge fill |
| `danger-border` | `#F9ADBF` | Error badge border |
| `neutral-badge-bg` | `#EEF2F7` | Neutral/info badge fill |
| `neutral-badge-text` | `#50617A` | Neutral badge text |

### Dark Mode

| Token | Hex | Usage |
|-------|-----|-------|
| `brand-primary` | `#0085FF` | Primary CTAs in dark contexts |
| `text-primary` | `#C9CED8` | Primary body text |
| `text-secondary` | `#8C99AD` | Supporting, metadata |
| `background` | `#14171D` | App background |
| `background-offset` | `#1B1E25` | Cards, sidebar, form fields |
| `border` | `#2B3039` | Dividers, input borders |
| `danger` | `#F23154` | Errors, destructive |
| `success-text` | `#3EAE20` | Success state text |
| `success-bg` | `#152207` | Success badge fill |
| `success-border` | `#20360C` | Success badge border |
| `warning-text` | `#F27400` | Warning state text |
| `warning-bg` | `#400A00` | Warning badge fill |
| `warning-border` | `#5F1400` | Warning badge border |
| `danger-text` | `#F46B7D` | Danger state text |
| `danger-bg` | `#420320` | Danger badge fill |
| `danger-border` | `#61092D` | Danger badge border |
| `neutral-badge-bg` | `#1B1E25` | Neutral badge fill |
| `neutral-badge-border` | `#2B3039` | Neutral badge border |
| `neutral-badge-text` | `#8C99AD` | Neutral badge text |

---

## Typography

**Primary font**: `sohne-var`, `Söhne`, `SF Pro Display`, `system-ui`, `sans-serif`
**Monospace font**: `Source Code Pro`, `ui-monospace`, `monospace`

Stripe uses Söhne (a geometric sans-serif from Klim Type Foundry) set as a variable font. Display and headline text runs at weight 300 with negative letter-spacing for editorial density — one of Stripe's most distinctive typographic signatures. Body and UI text steps up to 400 for legibility.

| Scale | Size | Weight | Line Height | Letter Spacing | Usage |
|-------|------|--------|-------------|----------------|-------|
| `display` | 48px | 300 | 1.03 | −0.030em | Hero headings |
| `heading-xl` | 44px | 300 | 1.05 | −0.025em | Page titles |
| `heading-lg` | 32px | 300 | 1.10 | −0.020em | Section headings |
| `heading-md` | 26px | 300 | 1.15 | −0.018em | Sub-section headings |
| `heading-sm` | 22px | 300 | 1.20 | −0.015em | Card headings |
| `heading-xs` | 18px | 400 | 1.25 | −0.010em | Sidebar headings |
| `body-lg` | 18px | 300 | 1.60 | 0em | Lead paragraphs |
| `body` | 16px | 400 | 1.60 | 0em | Default body text |
| `body-sm` | 15px | 400 | 1.55 | 0em | Compact body, form copy |
| `label` | 14px | 400 | 1.45 | 0em | Form labels, UI labels |
| `caption` | 12px | 300 | 1.40 | 0.005em | Metadata, helper text |
| `micro` | 11px | 400 | 1.35 | 0.010em | Badges, timestamps |
| `code` | 13px | 400 | 1.60 | 0em | Inline code, API keys |

> On mobile, display and heading scales step down one level (e.g., `display` 48px → 32px, `heading-xl` 44px → 28px).

---

## Spacing

Base unit: `4px`. All spacing values are multiples of 4.

| Token | Value | Usage |
|-------|-------|-------|
| `space-0` | 0px | Reset |
| `space-1` | 2px | Micro nudge, icon gaps |
| `space-2` | 4px | Tight inline spacing |
| `space-3` | 6px | Badge padding, chip gaps |
| `space-4` | 8px | Input vertical padding, icon margin |
| `space-5` | 10px | Compact element padding |
| `space-6` | 12px | Button vertical padding, list item gaps |
| `space-7` | 16px | Default horizontal padding, card gap |
| `space-8` | 20px | Form row gaps |
| `space-9` | 24px | Section internal padding, card padding |
| `space-10` | 32px | Section gaps, page padding |
| `space-11` | 40px | Large layout gaps |
| `space-12` | 44px | Hero padding |
| `space-13` | 64px | Section vertical spacing |
| `space-14` | 96px | Hero vertical margins |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-none` | 0px | Tables, full-bleed elements |
| `radius-xs` | 1px | Subtle rounding on minimal components |
| `radius-sm` | 4px | Buttons, inputs, tabs, chips |
| `radius-md` | 6px | Compact cards, dropdowns |
| `radius-lg` | 8px | Standard cards, modals |
| `radius-xl` | 16px | Featured cards, large containers |
| `radius-full` | 9999px | Pill badges, avatar circles |

> Interactive elements (buttons, inputs, selects) use `radius-sm` (4px). Content containers use `radius-lg` (8px). Decorative and featured surfaces use `radius-xl` (16px).

---

## Shadows

Stripe's elevation system is deliberately subtle — shadows are cool-tinted and diffuse, never heavy or warm.

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-xs` | `0 1px 3px rgba(10,37,64,0.06)` | Subtle lift, hovered rows |
| `shadow-sm` | `0 2px 5px rgba(10,37,64,0.08), 0 1px 2px rgba(10,37,64,0.04)` | Default cards, inputs at rest |
| `shadow-md` | `0 3px 6px rgba(10,37,64,0.08), 0 2px 4px rgba(10,37,64,0.06)` | Raised cards, dropdowns |
| `shadow-lg` | `0 8px 24px rgba(10,37,64,0.10), 0 2px 8px rgba(10,37,64,0.06)` | Modals, popovers |
| `shadow-xl` | `0 20px 40px rgba(10,37,64,0.12), 0 4px 16px rgba(10,37,64,0.08)` | Floating panels, command palette |
| `shadow-focus` | `0 0 0 3px rgba(99,91,255,0.10)` | Focus ring on all interactive elements |
| `shadow-focus-danger` | `0 0 0 3px rgba(223,27,65,0.12)` | Focus ring on error-state inputs |

---

## Components

### Button

Stripe buttons are compact, low-radius, and typeset at weight 400. Primary uses the brand indigo fill; secondary is a ghost/outline style.

| Variant | Background | Text | Border | Radius | Padding | Font |
|---------|-----------|------|--------|--------|---------|------|
| Primary | `#635BFF` | `#FFFFFF` | none | 4px | 8px 16px | 14px / 400 |
| Primary hover | `#533AFD` | `#FFFFFF` | none | 4px | 8px 16px | 14px / 400 |
| Secondary | `#FFFFFF` | `#0A2540` | 1px `#C9D5E0` | 4px | 8px 16px | 14px / 400 |
| Secondary hover | `#F6F9FC` | `#0A2540` | 1px `#C9D5E0` | 4px | 8px 16px | 14px / 400 |
| Danger | `#DF1B41` | `#FFFFFF` | none | 4px | 8px 16px | 14px / 400 |
| Ghost/Link | transparent | `#635BFF` | none | 4px | 8px 12px | 14px / 400 |
| Disabled | `#F6F9FC` | `#8C99AD` | 1px `#E5EDF5` | 4px | 8px 16px | 14px / 400 |

Focus state: `box-shadow: 0 0 0 3px rgba(99,91,255,0.10)`.

---

### Input

| State | Background | Border | Text | Placeholder | Radius |
|-------|-----------|--------|------|-------------|--------|
| Default | `#FFFFFF` | 1px `#C9D5E0` | `#0A2540` | `#64748D` | 4px |
| Hover | `#FFFFFF` | 1px `#50617A` | `#0A2540` | `#64748D` | 4px |
| Focus | `#FFFFFF` | 1px `#533AFD` | `#0A2540` | `#64748D` | 4px |
| Error | `#FFFFFF` | 1px `#DF1B41` | `#0A2540` | `#64748D` | 4px |
| Disabled | `#F8FAFD` | 1px `#E5EDF5` | `#8C99AD` | `#8C99AD` | 4px |

Padding: `10px 12px`. Font: 14px / 400. Focus ring: `box-shadow: 0 0 0 3px rgba(99,91,255,0.10)`. Error ring: `box-shadow: 0 0 0 3px rgba(223,27,65,0.12)`.

Labels sit above the input (`margin-bottom: 6px`), 14px / 400, color `#273951`.

---

### Card

| Property | Value |
|----------|-------|
| Background | `#FFFFFF` |
| Border | 1px `#E5EDF5` |
| Border radius | 8px |
| Padding | 24px |
| Shadow | `0 2px 5px rgba(10,37,64,0.08), 0 1px 2px rgba(10,37,64,0.04)` |
| Hover shadow | `0 3px 6px rgba(10,37,64,0.08), 0 2px 4px rgba(10,37,64,0.06)` |
| Gap between cards | 16px or 24px |

Featured/hero cards use `border-radius: 16px`. Nested inner cards or stat tiles use `background: #F6F9FC`, `border: 1px #E5EDF5`, `radius: 8px`, `padding: 16px`.

---

### Navigation

Stripe's primary navigation is a top bar on the marketing site and a left sidebar in the dashboard.

**Top navigation (stripe.com):**

| Property | Value |
|----------|-------|
| Background | `#FFFFFF` with `border-bottom: 1px #E5EDF5` |
| Height | 64px |
| Logo color | `#0A2540` (dark mark) |
| Nav link color | `#273951` |
| Nav link hover | `#635BFF` |
| CTA button | Primary style (indigo fill) |
| Font | 15px / 400, `sohne-var` |

**Dashboard sidebar:**

| Property | Value |
|----------|-------|
| Background | `#0A2540` (deep navy) |
| Width | 220px |
| Text color | `#C9CED8` |
| Active item bg | `rgba(99,91,255,0.15)` |
| Active item text | `#FFFFFF` |
| Icon color | `#8C99AD` |
| Active icon | `#635BFF` |
| Section label | 11px / 400 uppercase, `#64748D` |
| Item padding | 8px 12px |
| Item radius | 4px |
| Border right | 1px `#1A2D42` |

---

### Badge

Stripe uses small, high-contrast status pills. No icons unless strictly necessary.

| Variant | Background | Text | Border | Radius | Padding |
|---------|-----------|------|--------|--------|---------|
| Success | `#EEFAE9` | `#3EAE20` | 1px `#BFEDAA` | 9999px | 2px 8px |
| Warning | `#FFF3E0` | `#F27400` | 1px `#FFCB7A` | 9999px | 2px 8px |
| Danger | `#FDE8ED` | `#DF1B41` | 1px `#F9ADBF` | 9999px | 2px 8px |
| Neutral | `#EEF2F7` | `#50617A` | 1px `#C9D5E0` | 9999px | 2px 8px |
| Info | `#EEF4FF` | `#635BFF` | 1px `#C5BFFE` | 9999px | 2px 8px |

Font: 11px / 400, uppercase, `letter-spacing: 0.03em`.

---

### Table

Stripe tables are clean and scannable with minimal visual noise.

| Property | Value |
|----------|-------|
| Background | `#FFFFFF` |
| Border | `border-collapse: collapse`; outer: 1px `#E5EDF5` |
| Header background | `#F6F9FC` |
| Header text | 12px / 400, `#50617A`, uppercase, `letter-spacing: 0.04em` |
| Header padding | 10px 16px |
| Row border | `border-bottom: 1px #E5EDF5` |
| Row text | 14px / 400, `#0A2540` |
| Row padding | 14px 16px |
| Row hover bg | `#F6F9FC` |
| Selected row bg | `rgba(99,91,255,0.05)` |
| Numeric columns | Tabular figures (`font-variant-numeric: tabular-nums`), right-aligned |
| Radius (container) | 8px |
| Shadow | `0 2px 5px rgba(10,37,64,0.08)` |

---

## Layout Principles

- **12-column grid** with a max content width of **1280px**, 24px gutters at large viewports, collapsing to 16px at tablet.
- **Section vertical rhythm**: 64px–96px between major page sections on marketing pages; 24px–32px between dashboard panels.
- **Page horizontal padding**: 32px at desktop, 24px at tablet, 16px at mobile.
- **Sidebar + main**: Dashboard uses a fixed 220px sidebar with a fluid main area. On tablet, sidebar collapses to icon-only (48px). On mobile, sidebar becomes a drawer.
- **Bento layouts**: Marketing pages use asymmetric 2–3 column CSS Grid layouts (`grid-template-columns: repeat(12, 1fr)`) with feature cards spanning 7/5 or 8/4 column splits.
- **Content over chrome**: Navigation and structural UI are kept minimal so data and product information dominate.
- **Z-index layers**: background (0) → cards (1) → sticky nav (100) → dropdowns (200) → modals (300) → toasts (400).

---

## Responsive Behavior

| Breakpoint | Width | Changes |
|------------|-------|---------|
| `xs` | < 480px | Single column, stacked navigation drawer, reduced padding (16px), display type drops one step |
| `sm` | 480–767px | Single column, 16px gutters, cards go full-width |
| `md` | 768–1023px | Two-column grid, sidebar collapses to icon rail (48px), 24px gutters |
| `lg` | 1024–1279px | Full layout, 24px gutters, sidebar fully expanded |
| `xl` | 1280px+ | Max-width container centered, generous margins, multi-column bento grids |

Typography responsive rules:
- `display` (48px) → 36px on `sm`, 28px on `xs`
- `heading-xl` (44px) → 32px on `sm`, 24px on `xs`
- `heading-lg` (32px) → 26px on `sm`, 22px on `xs`
- Body and label sizes remain constant across breakpoints.

---

## Tone & Guardrails

### DO

- Use `#0A2540` (deep navy) for all primary text — never pure `#000000`.
- Apply the brand indigo `#635BFF` to exactly one primary action per view.
- Use weight 300 for display headlines; weight 400 for all UI text.
- Set negative letter-spacing (`−0.015em` to `−0.030em`) on all display and heading text.
- Keep cards on `#FFFFFF` against `#F6F9FC` backgrounds to create clear elevation.
- Use `font-variant-numeric: tabular-nums` for all monetary and numeric data.
- Maintain `3px focus ring` (`rgba(99,91,255,0.10)`) on every interactive element for accessibility.
- Use badges as pill shapes (`border-radius: 9999px`) with color + border (never fill-only).
- Allow generous vertical whitespace — 24px minimum between dashboard components.
- Use `Source Code Pro` for API keys, code samples, and terminal output.

### DON'T

- Don't use the indigo accent for decorative purposes; reserve it for interactive and brand focal points.
- Don't apply bold (600+) weights — Stripe's voice is authoritative through restraint, not heaviness.
- Don't use warm shadows (no `rgba(0,0,0,0.x)` with warm tints); always use `rgba(10,37,64,...)` cool-toned shadows.
- Don't collapse padding below `8px` on interactive elements — financial interfaces demand precision tap targets.
- Don't use more than two semantic colors on a single card or panel (e.g., success + neutral is fine; success + warning + danger is not).
- Don't stack indigo CTAs; one primary action per surface, all others secondary or ghost.
- Don't use border-radius above `16px` on data-heavy containers — large radii signal marketing, not precision UI.
- Don't rely on color alone to communicate status — always pair badge color with a text label.
- Don't use full-black (`#000000`) text, backgrounds, or borders anywhere in the system.
- Don't apply drop shadows to inline elements, text, or icons — shadows are structural, not decorative.
