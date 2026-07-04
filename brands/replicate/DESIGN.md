# Replicate Design System

## Brand Overview

Replicate lets you run and fine-tune AI models with one line of code. The identity is minimal and
code-forward: **monochrome black/white** with a neutral gray scale and a vivid **orange-red
`#EA2804`** accent (plus a playful spectrum for model tags). Everything is in service of the
model page and the prediction. Light-first.

> "Run and fine-tune models. Deploy custom models. All with one line of code."

## Typography

- **Basier Square** — Replicate's brand typeface (proprietary). **Inter** is used here as the
  ≈ fallback for display and UI.
- **Mono** — model slugs, prediction IDs, logs, code (here: **JetBrains Mono**).

## Color Palette

### Primary
- Black: `#000000` — text, primary buttons
- White: `#FFFFFF`
- Orange-Red: `#EA2804` — brand accent, Run
- Blue: `#2563EB` — links

### Accent Spectrum (model tags)
- Yellow: `#FFE629` · Pink: `#FF6BFC` · Magenta: `#E54FE2` · Salmon: `#F97E82`

### Surfaces — Light
- Page: `#FFFFFF`
- Surface: `#F9FAFB`
- Sunken (logs/code): `#111827`
- Border: `#E5E7EB`

### Surfaces — Dark (neutral near-black)
- Page: `#0F1115`
- Surface: `#17191E`
- Elevated: `#1F232B`
- Border: `#2A2E37`

### Text
- Primary (light `#111827` / dark `#E6E9EF`)
- Secondary: `#6B7280`
- Muted: `#9CA3AF`

### Prediction Status
- Starting: `#9CA3AF` · Processing: `#2563EB` · Succeeded: `#16A34A` · Failed: `#EA2804`

## Logo

The **Replicate mark** — the three nested staircase brackets (viewBox `0 0 24 24`, single path),
rendered in black (or `#EA2804`). Pairs with the "Replicate" wordmark in Basier Square.

## Signature Component — Prediction

The model page run: a header (owner/model slug, visibility, run count), a prompt input, and a
**Run** action that drives the prediction lifecycle — starting → processing (with streaming
setup + inference **logs**) → succeeded — then streams the output and shows predict time and
prediction ID. This is the core Replicate moment: a model, a run, an output.

## Guardrails

**DO**
- Keep the canvas monochrome; use `#EA2804` for the Run/brand accent.
- Show the full prediction lifecycle and streaming logs, not just the output.
- Set model slugs, prediction IDs, and logs in the mono stack.
- Show predict time and prediction ID on every completed run.
- Use the spectrum only for model tags/badges, not core UI.

**DON'T**
- Don't make the brand blue — Replicate is monochrome with an orange-red accent.
- Don't invent dark surfaces; anchor on a neutral near-black `#0F1115`.
- Don't hide logs — they're how developers debug a prediction.
- Don't set slugs or IDs in a proportional font.
- Don't skip the status — a prediction always has a state.
