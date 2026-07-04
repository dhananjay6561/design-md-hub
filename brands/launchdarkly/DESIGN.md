# LaunchDarkly Design System

## Brand Overview

LaunchDarkly is runtime control for AI-era software — feature flags, experimentation, and AI
agent control that let teams ship fast while staying in control. The identity is high-contrast
and confident: near-black surfaces, an **electric lime `#EBFF38`** as the signature accent, and
a supporting **blue `#405BFF`** for interactive state. Dark-first.

> "Move at AI speed. Stay in control."

## Typography

- **Body / UI / Headings** — LaunchDarkly's proprietary brand faces (Next.js-obfuscated as
  `bodyFont` / `headingFont`). **Inter** is used here as the ≈ fallback.
- **Mono** — flag keys, variation values, targeting rules (here: **JetBrains Mono**).

## Color Palette

### Primary
- Electric Lime: `#EBFF38` — brand accent, primary CTAs, highlights
- Lime Alt: `#DDFF46`
- Blue: `#405BFF` — interactive, flag targeting, links
- Blue Hover: `#3048E8`

### Accent
- Periwinkle: `#7581EE` · Pink: `#E75FA4` · Orange: `#FF9D29`

### Surfaces — Dark (real near-black neutrals)
- Page: `#191919`
- Surface: `#212121`
- Deepest: `#101010`
- Border: `#2E2E2E`

### Surfaces — Light
- Page: `#F8F8F8`
- Card: `#FFFFFF`
- Border: `#E5E5E5`

### Text
- Primary (dark `#F8F8F8` / light `#191919`)
- Secondary: `#A0A0A0`
- Muted (dark `#707070` / light `#6B6B6B`)

### Flag State
- Targeting On: `#405BFF` (toggle) · Off: neutral gray
- Serving `true`: `#00C48C` · `false`: `#707070`

### Semantic
- Success: `#00C48C` · Warning: `#FF9D29` · Error: `#E75FA4`

## Logo

The **LaunchDarkly wordmark** (viewBox `0 0 156 24`) ending in the signature arrow/star mark,
rendered in `currentColor` — near-white on dark, near-black on light. The lime is never used to
fill the wordmark; it stays an accent.

## Signature Component — Feature Flags Dashboard

The flags dashboard: an environment switcher (**Production / Staging**) over a list of feature
flags. Each row has a flag key (mono), a description, a **toggle** (blue when targeting is on),
and — for percentage rollouts — a split variation bar. Toggling a flag flips its targeting state
live; switching environments shows that environment's independent flag states. This is the core
LaunchDarkly control moment.

## Guardrails

**DO**
- Use electric lime `#EBFF38` for brand accent and primary CTAs.
- Use blue `#405BFF` for the "targeting on" toggle and interactive state.
- Keep flag keys, variation values, and targeting rules in the mono stack.
- Show each environment's flag state independently (Production ≠ Staging).
- Keep surfaces near-black neutral so lime and blue lead.

**DON'T**
- Don't fill the wordmark with lime — it stays an accent, not a logo color.
- Don't invent navy dark surfaces; LaunchDarkly's dark is neutral near-black.
- Don't use lime for destructive or error states (it reads as positive/brand).
- Don't set flag keys or variation values in a proportional font.
- Don't imply a flag is global — always scope it to an environment.
