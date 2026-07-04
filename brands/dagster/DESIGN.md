# Dagster Design System

## Brand Overview
Dagster is the data orchestration platform — the operational layer that structures how data is built, observed and delivered, "so both teams and AI agents can rely on it." The identity is a deep near-black **navy** canvas, a confident **indigo** brand color, a fresh **lime** highlight, and an asset-lineage graph as the central metaphor. It reads like a serious, modern control plane for data platforms.

> **Rebrand note (verify against live):** the older stub's purple `#7B61FF` is superseded — the current brand is **indigo `#4F43DD`** with a blue-violet range (`#2D40EA` / `#4D65FF`) and a lime accent `#EAFFBB`.

## Color Palette

### Primary
- Indigo (brand): `#4F43DD` — primary actions, materializing, links
- Blue-violet: `#2D40EA` / `#4D65FF`
- Indigo light: `#A7A0F8` / `#B9B4F1`
- Lime accent: `#EAFFBB` — highlights, freshness

### Backgrounds — Dark (default)
- Base: `#0A0D12` — near-black navy page
- Deep: `#040615` / `#030615` — deepest wells
- Purple-black: `#1B0130`
- Surface: `#101828`
- Elevated: `#151D2E`
- Border: `rgba(255,255,255,.09)`

### Backgrounds — Light
- Base: `#F7F7FF` — cool near-white
- Surface: `#FFFFFF`
- Alt: `#FAFAFA`
- Border: `#E3E8EF`

### Text
- Primary (dark): `#F7F7FF` / (light): `#101828`
- Secondary: `#CDD5DF` / `#475467`
- Muted: `#758696`

### Asset / run status
- Materialized (success): `#22C55E`
- Materializing / in progress: `#4F43DD` (indigo)
- Stale (warning): `#F59E0B`
- Failed: `#EF4444`
- Queued: `#4D65FF`
- Missing / skipped: `#758696`

## Typography

### Font Stack (real Dagster fonts)
- Display: **Aspekta** (proprietary geometric sans) — approximated in this reference by **Geist**, which Dagster also ships. `Geist, Aspekta, system-ui, sans-serif`.
- UI / body: **Geist** (Google Fonts, real Dagster font).
- Code / mono: **Geist Mono** (Google Fonts, real Dagster font) — asset keys, run IDs, code.

### Scale
- xs 11 / sm 13 / base 15 / md 18 / lg 22 / xl 30 / 2xl 46

### Weights
Regular 400 · Medium 500 · Semibold 600 · Bold 700

## Components

### Buttons
- Primary: indigo `#4F43DD`, white text, radius 8px — "Get started for free"
- Secondary: transparent, 1px border — "Talk to sales"
- Ghost / link: indigo text — "Read the docs"

### Asset node
A rounded card in the lineage graph: asset key (Geist Mono), a status dot, and metadata (last materialized, row count). Status color drives the left border / dot.

### Status pill
Rounded pill with a leading dot; colors map to the asset/run status table above.

## Signature Component — Asset Lineage Graph
Dagster's core concept is **software-defined assets** and their lineage. The signature is the **Asset Graph**: a DAG of assets (`raw_orders` → `stg_orders` → `orders` → `order_metrics` / `customer_ltv` → `daily_report`) with dependency edges and per-asset status. Pressing **Materialize all** runs the DAG in topological order — each asset flips to `Materializing` (indigo pulse) then `Materialized` (green), edges light up, and a run-status footer updates. This is the single UI most associated with Dagster.

## Guardrails

**DO**
- Use indigo `#4F43DD` as the brand color; reserve lime `#EAFFBB` for highlights.
- Keep the page a deep navy `#0A0D12` in dark mode (the default).
- Use Geist for UI and Geist Mono for asset keys, run IDs, and code.
- Map asset/run status to their fixed colors consistently.
- Make lineage the hero metaphor — assets and edges, not generic dashboards.

**DON'T**
- Don't use the legacy purple `#7B61FF` as the primary brand.
- Don't render asset keys or run IDs in a proportional font — always mono.
- Don't invent status colors; use the materialized/materializing/stale/failed set.
- Don't overuse lime — it's an accent, not a surface.
