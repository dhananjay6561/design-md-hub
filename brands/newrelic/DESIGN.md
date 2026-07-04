# New Relic Design System

## Brand Overview

New Relic is the intelligent observability platform — APM, infrastructure, logs, and alerts in
one. The rebranded identity is editorial and high-contrast: a near-black **`#080F11`** (with a
faint green cast) paired with a warm **cream `#E5E4D8`**, lit by a teal/green data-viz accent.
The product is chart-dense — golden signals, dashboards, and traces. Dark-first.

> "AI-powered Observability."

## Typography

- **Mona Sans** — display / UI (New Relic self-hosts the open Mona Sans; loaded here from the
  GitHub CDN, CORS ✅ — used directly).
- **Inter** — secondary UI (real, Google Fonts).
- **Geist Mono** — metrics, queries (NRQL), IDs (real, Google Fonts).

## Color Palette

### Primary
- Ink: `#080F11` — page, deep surfaces
- Cream: `#E5E4D8` — paper, primary text on dark
- Teal: `#008C99` — accent, latency series
- Green: `#00AC69` — healthy, throughput (light `#00D188`)

### Surfaces — Dark (real near-black)
- Page: `#080F11`
- Surface: `#141A20`
- Elevated: `#1D252C`
- Border: `#293338`

### Surfaces — Light
- Page: `#F1F0E4` (warm)
- Card: `#FFFFFF`
- Border: `#D8D7CA`

### Text
- Primary (dark `#E5E4D8` / light `#080F11`)
- Secondary: `#9AA4A6`
- Muted: `#6B7578`

### Data-viz & Semantic
- Throughput: `#00AC69` · Latency: `#17B8C4` · Errors: `#F5544E`
- Warning: `#F0B400` · Apdex: `#8B7BF0`

## Logo

The **New Relic mark** — the isometric cube/hexagon glyph (viewBox `0 0 24 24`, single path),
rendered in cream `#E5E4D8` on dark (or `currentColor`). Pairs with the "New Relic" wordmark in
Mona Sans.

## Signature Component — Golden Signals

A service-health view: a service header with health status over four **golden-signal** tiles —
Throughput, Error rate, Latency (p95), and Apdex — each a live sparkline with a big current
value and delta. A time-range switch (30m / 3h / 24h) reslices every series; the throughput
tile streams a new point live. This is the core New Relic observability moment.

## Guardrails

**DO**
- Pair near-black `#080F11` with the warm cream `#E5E4D8` — that contrast is the brand.
- Use green for throughput/healthy, teal for latency, red for errors — consistently.
- Set metrics, NRQL, and IDs in Geist Mono.
- Give every chart a current value, unit, and delta.
- Show the time range on any time-series view.

**DON'T**
- Don't cool the cream to plain white — the warmth is the identity.
- Don't invent dark surfaces; anchor on the real near-black `#080F11`.
- Don't reuse a data-viz color for an unrelated signal.
- Don't set metric values in a proportional font.
- Don't show a sparkline without its scale/current value.
