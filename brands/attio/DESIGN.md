# Attio — Design System

The CRM for agentic revenue. A clean, data-first CRM built on a flexible object model — Companies, People, Deals, Lists, Workflows. The design language is quiet: near-white paper, near-black ink, a single electric blue, and typed data cells that read like a well-built database.

Tokens below are lifted from the live site (`attio.com`) — the `--color-black-*` / `--color-white-*` scales and their semantic mappings.

---

## Colors

Attio runs on two neutral ramps — a **black** scale and a **white** scale — plus one saturated **blue** accent and three semantic hues. Light is the primary surface; dark is a faithful inversion of the same ramps.

### Neutral ramps (theme-invariant source)

| Black | Hex | | White | Hex |
|---|---|---|---|---|
| black-50 | `#101010` | | white-100 | `#ffffff` |
| black-100 | `#1c1d1f` | | white-200 | `#fafafb` |
| black-200 | `#202124` | | white-300 | `#f3f4f6` |
| black-300 | `#232529` | | white-400 | `#edeff3` |
| black-400 | `#2e3238` | | white-500 | `#e4e7ec` |
| black-500 | `#383e47` | | white-600 | `#dee2e7` |
| black-600 | `#505967` | | white-700 | `#d3d8df` |
| black-700 | `#6f7988` | | white-800 | `#cad0d9` |
| black-800 | `#8f99a8` | | white-900 | `#b5bdc9` |
| black-900 | `#a4adba` | | | |

### Accent + semantic

| Token | Hex | Use |
|---|---|---|
| blue-500 | `#266df0` | Accent / links (light) |
| blue-400 | `#709ff5` | Accent / links (dark) |
| blue-100 | `#e8f0ff` | Accent tint / selection |
| green-500 | `#0fc27b` | Positive · won · connected |
| red-500 | `#ff5b59` | Negative · lost · error |
| yellow-500 | `#f5b900` | Warning · pending |

### Semantic mapping (live `--internal-color-*`)

| Role | Light | Dark |
|---|---|---|
| primary-background | white-100 `#fff` | black-50 `#101010` |
| secondary-background | white-200 `#fafafb` | black-100 `#1c1d1f` |
| surface | white-400 `#edeff3` | black-400 `#2e3238` |
| surface-subtle | white-300 `#f3f4f6` | black-300 `#232529` |
| primary-foreground (text) | black-100 `#1c1d1f` | white-100 `#fff` |
| caption / tertiary | black-600 `#505967` | black-900 `#a4adba` |
| weak-stroke | white-400 `#edeff3` | black-300 `#232529` |
| default-stroke | white-700 `#d3d8df` | black-700 `#6f7988` |
| link-foreground | blue-500 `#266df0` | blue-400 `#709ff5` |
| focus-ring | `#266df04d` | `#709ff599` |

---

## Typography

Two families, three optical roles. Attio ships **Inter Display** (headings) and **Inter** (body/UI) — the same superfamily at different optical sizes — plus **Tiempos Text** as a rare editorial serif. No brand monospace exists; metadata falls back to the system mono stack.

| Role | Family | Notes |
|---|---|---|
| Display / headings | Inter Display | Semibold, tight tracking (`-0.02em`), optical size high |
| Body / UI / cells | Inter | 400–600; the workhorse for every label, cell, and button |
| Editorial serif | Tiempos Text | Regular + italic; sparing — pull-quotes only |
| Metadata / hex | system mono | `ui-monospace, SFMono-Regular, Menlo` — Attio ships no brand mono |

> In this preview Inter is loaded from Google Fonts as a variable font (opsz axis) so it serves both the Display and text cuts; Tiempos Text is self-hosted from `attio.com` (CORS-open), Georgia-backed.

---

## Type scale

| Step | Size | Weight | Tracking |
|---|---|---|---|
| Display | 64–80px (`clamp`) | 600 | -0.02em |
| Heading-lg | 40px | 600 | -0.02em |
| Heading-md | 28px | 600 | -0.015em |
| Title | 18px | 600 | -0.01em |
| Body | 14px | 400 | 0 |
| Caption / cell-meta | 12px | 400–500 | 0 |

---

## Radius, spacing, elevation

- **Radius:** 6px (chips / cells) · 9px (buttons / inputs) · 12px (cards) · 16px (panels).
- **Borders:** 1px, `weak-stroke` for internal grid lines, `default-stroke` for container edges. The table reads through hairlines, not shadows.
- **Elevation:** shadows are subtle and only on floating surfaces (popovers, the record card). Surfaces sit on borders, not drop shadows.
- **Density:** the CRM is dense — cell height `~44px`, generous only in the hero.

---

## Components

- **Buttons:** primary = ink (`#1c1d1f` on light, inverts to white on dark) with `--btn-text`; secondary = surface with a hairline border. Accent blue is reserved for links and selection, *not* primary buttons.
- **Records table:** the core surface. Typed attribute columns — text, domain, **connection strength**, **status/stage pill**, currency, owner avatar, relative time. Column headers sort; status pills click to cycle.
- **Status / stage pills:** rounded, low-saturation fills keyed to semantic hue (green won, blue active, grey lead, red lost).
- **Connection strength:** Attio's signature attribute — a 4-segment strength meter derived from a team's email/calendar activity.
- **Inputs:** surface fill, hairline border, blue focus ring (`focus-ring` token).

---

## Guardrails

**Do**
- Keep the canvas near-white `#fff` / near-black `#101010`; let the data be the color.
- Reserve blue `#266df0` for links, selection, and focus — never a primary button.
- Make primary buttons ink; invert `--btn-text` per theme so they never lose contrast.
- Build UI as typed cells on hairline grids — Attio is a database you can see.
- Color status by meaning: green won, red lost, yellow pending, grey lead.

**Don't**
- Don't turn the accent blue into a button fill or a background wash.
- Don't lean on drop shadows for structure — use 1px strokes.
- Don't set body, cells, or labels in a serif — Tiempos is a rare editorial accent only.
- Don't invent dark-mode tints; step through the real `black-*` ramp.
- Don't crowd the palette with a second saturated hue beyond the semantic three.
