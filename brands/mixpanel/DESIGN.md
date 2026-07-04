# Mixpanel Design System

## Brand Overview

Mixpanel is the product-analytics platform — event-based tracking, funnels, retention, and
insights. The rebranded identity leads with a confident **purple `#7856FF`** and a playful warm
**chart spectrum** (coral, yellow, teal, blue, green) for segments and series, on a clean canvas.
The product is chart-first — the funnel is its signature. Light-first.

> "The product intelligence system for the AI era."

## Typography

- **DM Sans** — display / UI / body (real Mixpanel brand font, Google Fonts).
- **Inter** — secondary UI (real, Google Fonts).
- **Mono** — counts, event names, distinct_ids (here: **JetBrains Mono**).

## Color Palette

### Primary
- Purple: `#7856FF` — brand, CTAs, primary series
- Purple Deep: `#472BA0`
- Purple Light: `#9074FF`
- Ink: `#15003F` — deep purple, dark page

### Chart Spectrum (segments & series)
- Coral: `#FF7557` · Yellow: `#F9C85F` · Teal: `#7FE1D8`
- Blue: `#72BEF4` · Green: `#3BA974` · Peach: `#FFB27A`

### Surfaces — Light
- Page: `#F7F5FF`
- Card: `#FFFFFF`
- Sunken: `#F1EEFB`
- Border: `#E8E4F5`

### Surfaces — Dark (deep purple, real tokens)
- Page: `#15003F`
- Surface: `#1E0B4D`
- Elevated: `#2E1670`
- Border: `rgba(255,255,255,.10)`

### Text
- Primary (light `#1F2023` / dark `#F1ECFF`)
- Secondary: `#6B6680`
- Muted: `#9A94B0`

### Semantic
- Success: `#3BA974` · Warning: `#F9C85F` · Error / dropoff: `#FF7557`

## Logo

The **Mixpanel mark** — the `><` chevron pair (viewBox `0 0 24 24`, single path), rendered in
purple `#7856FF`. Pairs with the "Mixpanel" wordmark set in DM Sans.

## Signature Component — Funnel

A conversion funnel: ordered steps (Viewed → Trial → Activated → Invited → Upgraded), each a
bar sized by count with overall and step-to-step conversion %, and the dropoff between steps in
coral. A **segment** switch (All / Mobile / Web) reslices every step's counts and the bars
re-animate. This is the defining Mixpanel analysis.

## Guardrails

**DO**
- Lead with purple `#7856FF`; use the warm spectrum for segments/series.
- Give funnel steps both overall and step-to-step conversion %.
- Show dropoff explicitly (coral) between steps.
- Set counts, event names, and IDs in the mono stack.
- Keep the canvas light so the chart colors carry meaning.

**DON'T**
- Don't reassign spectrum colors between segments within one view.
- Don't invent dark surfaces; anchor on the real deep purple `#15003F`.
- Don't use coral for anything but dropoff / negative in analysis views.
- Don't set metric counts in a proportional font.
- Don't show a funnel step without its conversion rate.
