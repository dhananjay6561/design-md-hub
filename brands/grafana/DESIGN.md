# Grafana — Design System

> Dashboard anything. Observe everything.

Grafana is the open, composable observability platform — it unifies metrics, logs, traces, profiles, and business data into dashboards you can query, visualize, and alert on. Grafana Labs' identity has two faces that share one accent: the **marketing brand** (Poppins headlines, bold orange on light) and the **product** (the iconic dark dashboard, dense panels, a specific categorical color palette for time-series). Both are anchored by the unmistakable **orange → yellow** logomark.

Design principles: **the data is the hero** (chrome recedes, panels dominate), **dark-first but theme-aware**, and **a fixed categorical palette** so the same series is the same color everywhere.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| Grafana orange | `#FF671D` | Primary brand, logomark, CTAs, key accents |
| Grafana yellow | `#FBE136` | Logomark gradient end, highlights |
| Logo gradient | `#FF671D → #FBE136` | The orb mark; reserve for logo + marquee moments |

### Surfaces
| Token | Dark | Light | Usage |
|---|---|---|---|
| canvas | `#0B0C0E` | `#FFFFFF` | App / page background |
| panel | `#181B1F` | `#FFFFFF` | Dashboard panels, cards |
| raised | `#22252B` | `#F4F5F5` | Inputs, hover, headers |
| border | `#2B2D32` | `#E4E5E7` | Panel & control borders |

### Text
| Token | Dark | Light |
|---|---|---|
| primary | `#E4E5E9` | `#101010` |
| secondary | `#9FA1A6` | `#5A5A5A` |
| faint | `#6E7178` | `#8A8A8A` |

### Visualization palette (categorical — fixed order)
Grafana's classic series colors. A series keeps its color across every panel.
| Color | Hex | | Color | Hex |
|---|---|---|---|---|
| green | `#73BF69` | | red | `#F2495C` |
| yellow | `#FADE2A` | | blue | `#5794F2` |
| orange | `#FF9830` | | purple | `#B877D9` |
| | | | cyan | `#3FC6EB` |

### Thresholds (state semantics)
| State | Hex | Meaning |
|---|---|---|
| ok | `#73BF69` | within threshold |
| warning | `#FADE2A` | approaching limit |
| critical | `#F2495C` | breached / alerting |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / headings | **Poppins** (`500 / 600 / 700`) | `--font-heading` on grafana.com — marketing headlines. |
| UI / body | **Inter** (`400 / 500 / 600`) | `--font-sans` — the product UI, body copy, panel titles, legends. |
| Metrics / queries | **Roboto Mono** (`400 / 500`) | Big stat values, axis ticks, PromQL/LogQL, timestamps. |

Scale: hero 52–60px (Poppins), section 22px, panel title 13px `600`, stat value 32–40px (Roboto Mono, tabular), body 14px, legend/axis 11–12px mono.

---

## Shape, spacing & motion

- **Radius:** panels `4px`, cards `8px`, buttons `2px`, pills `9999px`. Grafana is deliberately *square* — small radii signal a dense, technical tool.
- **Spacing:** 8px grid; panels sit in a tight gap (`8px`) grid. Information density is a feature, not a bug.
- **Elevation:** panels are flat with `1px` borders (`#2B2D32` dark). No drop shadows inside the dashboard — depth comes from the border and the canvas contrast.
- **Motion:** minimal and functional — panels refresh on an interval (crosshair follows the cursor, tooltips track live values). No decorative animation; the movement is the data updating.

---

## Components

- **Panel** — the atom of Grafana. Header (title + menu) over a viz body: time-series, stat, gauge, table, bar, heatmap, logs.
- **Time-series** — multi-series line/area chart, shared crosshair, hover tooltip listing every series value at that timestamp, legend below with min/max/last.
- **Stat panel** — a large Roboto-Mono value with unit, a background sparkline, and a threshold color.
- **Gauge** — radial or bar gauge with green/yellow/red threshold bands.
- **Time range picker** — `Last 5m / 1h / 6h / 24h`, plus a refresh interval (`10s`, `30s`, `1m`).

---

## Guardrails

**Do**
- Keep panel chrome quiet and let the data dominate — the visualization is the hero.
- Use the fixed categorical palette so a given series is the same color in every panel.
- Color by threshold for state (green ok → yellow warning → red critical).
- Reserve the orange→yellow gradient for the logomark and one marquee moment.
- Use Roboto Mono for numbers, timestamps, and queries; keep panel titles in Inter.

**Don't**
- Recolor series arbitrarily or reuse a color for two series in one view.
- Flood a dashboard with orange — it's the brand accent, not a data color (use `#FF9830` from the viz palette for orange series).
- Add heavy shadows or large radii — Grafana is dense, square, and flat.
- Let decoration compete with the metrics; every pixel of a panel should carry signal.
