# Webflow Design System

## Brand Overview

Webflow is the agentic web platform — design, build, and launch sites visually, then scale them
with a real CMS and code-quality output. The 2024 rebrand pairs a confident **Webflow blue**
`#146EF5` and near-black `#080808` with an editorial set of **pastels** (peach, mint, lavender,
cream) used as section backgrounds. Marketing is light and expressive; the **Designer** product
is a dark-chrome cockpit wrapped around a live canvas. Light-first.

> "Make your website a growth engine."

## Typography

- **WF Visual Sans** — Webflow's proprietary brand typeface (display / UI). Proprietary sans;
  **Inter** is used here as the ≈ fallback.
- **WF Visual Sans Mono** — the real brand mono, self-hosted (CloudFront, CORS ✅) — **used
  directly** for Designer labels, CSS values, class names, and breakpoints.

## Color Palette

### Primary
- Webflow Blue: `#146EF5` — brand, CTAs, Designer selection
- Blue Deep: `#002A6A`
- Ink: `#080808`
- Page: `#FAFCFF`

### Pastels (section backgrounds — 2024 rebrand)
- Lavender: `#CDBCF0`
- Mint: `#A6DABF`
- Peach: `#FFCA97`
- Cream: `#FAFFE7`
- Purple accent: `#7A3DFF`

### Designer Chrome (product UI — always dark)
- Panel: `#2E2E2E`
- Panel Deep: `#1E1E1E`
- Input: `#383838`
- Border: `#404040`
- Selection: `#146EF5`

### Surfaces — Dark (near-black, stepped from real `#080808`)
- Page: `#080808`
- Surface: `#141414`
- Elevated: `#1E1E1E`
- Border: `#2A2A2A`

### Text
- Primary (light `#080808` / dark `#F2F2F2`)
- Secondary: `#575757`
- Muted: `#8A8A8A`

### Semantic
- Success: `#00560D` · Warning: `#FFCA97` · Error: `#DD9A93`

## Logo

The **Webflow mark** — the interlocking-strokes glyph (viewBox `0 0 24 24`, single path),
rendered in Webflow blue `#146EF5` (or `currentColor` in monochrome contexts). Pairs with the
"Webflow" wordmark set in WF Visual Sans.

## Signature Component — Designer

The Webflow Designer: a dark-chrome workspace with a **breakpoint switcher** (desktop / tablet /
mobile), a live **canvas** rendering a flex layout, and a right-hand **Style panel**. Adjusting
Layout (flex direction, justify, align, gap) and Background repaints the selected element on the
canvas in real time — the defining Webflow interaction of designing visually and seeing CSS
apply instantly.

## Guardrails

**DO**
- Use Webflow blue `#146EF5` for brand, CTAs, and canvas selection.
- Keep the Designer chrome dark regardless of the surrounding theme.
- Use WF Visual Sans Mono for CSS values, class names, and breakpoints.
- Use pastels as section backgrounds, not as UI control colors.
- Show the selected element and its style values together (visual + code).

**DON'T**
- Don't use the pre-rebrand indigo `#4353FF` — the current brand blue is `#146EF5`.
- Don't recolor the Webflow mark outside blue or a single flat color.
- Don't put pastel fills on interactive controls (buttons, inputs).
- Don't set CSS values or class names in a proportional font.
- Don't invent dark surfaces; step within the real near-black `#080808`.
