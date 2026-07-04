# Weights & Biases Design System

## Brand Overview
Weights & Biases (W&B) is the AI developer platform — experiment tracking, model management, and evaluations for the world's leading AI teams. The identity is data-rich and confident: dark **slate** surfaces, the signature **gold** dot-gauge mark, and a bright multi-hue chart palette (teal / magenta / orange / mint) that maps to overlaid run curves. It reads like a high-density research dashboard.

> **Palette note (verify against live):** the real signature gold is `#FFCC33` (not `#FFCC00`), the dark surface is warm **slate `#2B3038`** (not pure `#0F0F0F`), and the brand carries a full run-chart spectrum (teal `#00AFC2`, magenta `#FF0E65`, orange `#FFAD33`, mint `#5EEAD4`).

## Color Palette

### Primary
- Brand Gold: `#FFCC33` — mark, signature accent, primary run
- Gold Orange: `#FFAD33` / `#FCBC32`
- Teal: `#00AFC2` — secondary brand, chart line
- Magenta: `#FF0E65` — accent, chart line

### Chart / run spectrum
- Run 1 (gold): `#FFCC33`
- Run 2 (teal): `#00AFC2`
- Run 3 (magenta): `#FF0E65`
- Run 4 (orange): `#FFAD33`
- Run 5 (mint): `#5EEAD4`
- Peach: `#FFB666` · Lavender: `#EDE8FF`

### Backgrounds — Dark (default)
- Base: `#1A1C1F`
- Surface: `#212429`
- Elevated: `#2B3038`
- Hairline: `#34373C`
- Border: `rgba(255,255,255,.09)`

### Backgrounds — Light
- Base: `#FBFBFC`
- Surface: `#FFFFFF`
- Border: `#E5E7EB`

### Text
- Primary (dark): `#FBFBFC` / (light): `#1A1C1F`
- Secondary: `#C5C7CC` / `#5B6069`
- Muted: `#8A8F98`

### Run state / semantic
- Running: `#FFCC33` (gold, pulsing)
- Finished: `#5EEAD4` (mint)
- Crashed / error: `#FF0E65`
- Success: `#34D399`

## Typography

### Font Stack (real W&B fonts, all Google Fonts)
- UI / body: **Source Sans 3** (Source Sans Pro) — headings, body, buttons.
- Serif accent: **Source Serif 4** (Source Serif Pro) — editorial headlines.
- Code / mono: **Inconsolata** — run names, metrics, config, code.

### Scale
- xs 11 / sm 13 / base 15 / md 18 / lg 22 / xl 30 / 2xl 46

### Weights
Light 300 · Regular 400 · Semibold 600 · Bold 700

## Components

### Buttons
- Primary: gold `#FFCC33`, ink text (`#1A1C1F`) — "Sign up"
- Secondary: transparent, 1px border — "Contact sales"
- Ghost / link: teal `#00AFC2`

### Run legend row
Colored line-swatch + run name (Inconsolata) + state dot + final metric value. Toggling hides/shows the run's line in the chart.

### Metric chart
SVG line chart with gridlines; each run is a polyline in its fixed run color; axis labels in Inconsolata.

## Signature Component — Experiment Runs
W&B's core value is **experiment tracking**: overlaying metric curves across runs. The signature is a **Runs panel**: a project header with a metric selector (`train/loss`, `val/accuracy`, `lr`), an SVG line chart overlaying multiple run curves in the run-color spectrum, and a legend of runs (name, state, final value). Toggling a run shows/hides its curve; switching the metric reslices every curve. This is the single UI most associated with Weights & Biases.

## Guardrails

**DO**
- Use gold `#FFCC33` as the signature; keep the dot-gauge mark gold.
- Keep dark surfaces warm slate `#2B3038` / `#1A1C1F` (not pure black).
- Assign each run a fixed color from the spectrum and keep it consistent across chart + legend.
- Render run names, metrics, and config in Inconsolata.

**DON'T**
- Don't flatten the gold to `#FFCC00` or the dark to pure `#0F0F0F`.
- Don't recolor a run between the chart and its legend row.
- Don't render metrics or run ids in a proportional font.
- Don't overload the hero with the full spectrum — gold leads, others support charts.
