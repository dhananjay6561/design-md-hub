# Snowflake Design System

## Brand Overview

Snowflake is the **AI Data Cloud** — one platform to mobilize data, build apps, and run AI
across clouds. The identity is crisp and arctic: a white, airy marketing canvas, deep midnight
navy for depth, and the unmistakable arctic-blue snowflake mark. The product surface (Snowsight)
is a data-worker's cockpit — worksheets, warehouses, and result grids. Light-first.

> "Mobilize the world's data."

## Typography

- **Texta** — display, headings, nav, UI (real Snowflake brand font, weights 400/800/900,
  self-hosted at `snowflake.com/fonts/`, CORS ✅ — used directly here).
- **Lato** — body / long-form (real, 400/600/900, same CDN).
- **Source Code Pro** — SQL, code, warehouse names, metrics (real, same CDN).

Roles are strict: Texta for anything headline/interface, Lato for running prose, Source Code
Pro for anything a query engine would read.

## Color Palette

### Primary
- Arctic Blue (brand): `#29B5E8` — the snowflake mark, highlights, links
- Blue Hover: `#249EDC`
- Action Blue (CTA): `#126FE7` — primary buttons (white text)
- Midnight Navy: `#042130` — dark page, deep sections, ink

### Surfaces — Light
- Page: `#FFFFFF`
- Surface: `#F6F9FA`
- Elevated: `#ECEEF1`
- Light Blue Tint: `#D4F0FA` (callouts, selected)
- Border: `#D2D1D4`

### Surfaces — Dark (anchored on real `#042130`, stepped within the navy hue)
- Page: `#042130`
- Surface: `#08293A`
- Elevated: `#0E3348`
- Border: `rgba(255,255,255,.10)`

### Text
- Primary (light `#042130` / dark `#EAF6FB`)
- Secondary: `#535862`
- Muted: `#B9C2C5`

### SQL Syntax
- Keyword: `#126FE7` (dark: `#5AA8FF`)
- Function: `#8B5CF6`
- String: `#12A150`
- Number: `#C2410C`
- Comment: `#B9C2C5`

### Semantic
- Success: `#12A150`
- Warning: `#F59E0B`
- Error: `#EF4444`

## Logo

The **snowflake mark** — a six-point flake built from interlocking arrows around a central
gem, viewBox `0 0 28 28`, single `currentColor` path — rendered in arctic blue `#29B5E8`.
It carries the brand with or without the "Snowflake" wordmark set in Texta.

## Signature Component — SQL Worksheet (Snowsight)

A worksheet mirroring Snowsight: role + warehouse chips (`ACCOUNTADMIN`, `COMPUTE_WH`), a
syntax-highlighted SQL editor, and a blue **Run** button that executes a query against
`snowflake_sample_data.tpch_sf1` and streams a **results grid** — typed columns, monospace
cells, and a `N rows · Xs` status. The result grid is the core Snowflake work moment.

## Guardrails

**DO**
- Render the snowflake mark in arctic blue `#29B5E8`; keep its geometry intact.
- Keep the marketing canvas white and airy; use navy for depth, not as the default.
- Use Source Code Pro for all SQL, warehouse names, and result cells.
- Reserve action blue `#126FE7` for primary buttons; arctic blue for brand/links.
- Show query metrics (rows, duration, warehouse) — data workers expect them.

**DON'T**
- Don't recolor or distort the snowflake mark.
- Don't invent a saturated dark palette; anchor on real `#042130` within the navy hue.
- Don't set SQL or metrics in a proportional font.
- Don't put white text on arctic blue `#29B5E8` (low contrast) — use navy or action blue.
- Don't crowd the worksheet — the editor and result grid are the product.
