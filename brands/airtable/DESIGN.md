# Airtable Design System

## Brand Overview
Airtable is the app-building platform on top of a database–spreadsheet hybrid. The current identity (post-2023 refresh) is confident and editorial: a **light-first** white canvas, a **monochrome ink** wordmark and mark (the old tricolor record logo is retired), and deep, saturated **navy-blue** for interactive chrome. Color still matters — but it's concentrated in the *product*, where field types and single-select options carry a bright, semantic spectrum. Marketing pages layer warm editorial section washes (cream, terracotta, forest) over the neutral base.

## Color Palette

### Primary
- **Ink** `#181D26` — wordmark, mark, primary text, headings
- **Deep navy** `#040E20` — darkest brand ink / near-black surfaces
- **Blue (brand)** `#254FAD` — primary buttons, brand blue
- **Blue (deep)** `#002D98` — pressed / high-emphasis
- **Blue (bright)** `#2684FF` — links, focus, interactive accents
- **Blue (light)** `#458FFF` — dark-mode lift for blue (deep blue reads too dark on dark)

### Text & Neutrals
- **Text primary** `#181D26`
- **Text secondary** `#333840`
- **Text muted** `#9297A0`
- **Border** `#C0C6D1` — hairlines, grid lines
- **Surface soft** `#F4F6F8` — secondary panels, row hover

### Field & single-select spectrum (product core)
Airtable's select options and field types draw from a fixed bright palette. Each option gets a distinct color — never reuse a hue for two options in the same field.
- **blue** `#2D7FF9`   · **cyan** `#18BFFF`   · **teal** `#20D9D2`
- **green** `#20C933`  · **yellow** `#FCB400`  · **orange** `#FF6F2C`
- **red** `#F82B60`    · **pink** `#FF08C2`    · **purple** `#8B46FF`
- **gray** `#676B74`

### Marketing section washes (editorial only — never product UI)
- **Cream** `#FAF5E8`  · **Sky** `#C7E5F2`  · **Mint** `#B6E995`
- **Terracotta** `#912E1F`  · **Forest** `#0A2E0E` / `#214224`  · **Peach** `#FCAB79`

### Semantic
- **Success** `#20C933`  · **Warning** `#FCB400`  · **Error** `#F82B60`

## Typography
Airtable ships **Neue Haas Grotesk** as its brand type (self-hosted, CORS-open — used directly here).
- **Display** — `Haas Grot Disp (Roman 55)` — hero H1, large marketing headings
- **UI / Body** — `Neue Haas Grotesk Text Round` — Roman 400, Medium 500, Bold 700 — all app text, labels, buttons, table cells
- **Mono** — `JetBrains Mono` — field IDs, dates, record IDs, formulas (Airtable ships no branded mono)

## Spacing
4px base — 4, 8, 12, 16, 20, 24, 32, 48.

## Border Radius
- Buttons: 8px  ·  Cards / panels: 12px  ·  Grid cells: 0 (flush)
- Single-select chips: 9999px (pill)  ·  Field-type badges: 4px  ·  Avatars: 50%

## Components

### Grid (Table view)
The signature surface. Sticky header row of typed field columns (icon + name), a leftmost row-number gutter with a hover expand affordance, and flush cells. Row hover raises to `--surface-soft`. At least 20 rows visible without scroll.

### Single-select chip
A colored pill from the spectrum above. Text is dark or white chosen for contrast against the chip color — never a fixed color.

### Field-type badge
Icon + type name, color-coded by field type, used in the field-config menu and column headers.

### Collaborator cell
Circular initial avatar (spectrum color) + name. Used for Collaborator and Created-by fields.

### Button
Deep-navy `#254FAD` primary with white text; `rounded-8`. Secondary is a hairline outline on white.

## Guardrails

**DO**
- Keep the mark and wordmark monochrome ink `#181D26` — the tricolor logo is legacy.
- Reserve the bright field spectrum for the *product* (select options, field types) — keep marketing chrome neutral + editorial washes.
- Give every single-select option a distinct color; compute chip text color for contrast.
- Use deep navy `#254FAD` for primary actions; bright blue `#2684FF` for links/focus.
- Use monospace for field IDs, record IDs, and dates.

**DON'T**
- Don't resurrect the classic `#2D7FF9` tricolor logo or use it as the corporate brand blue.
- Don't use marketing wash colors (terracotta, forest, cream) inside product UI.
- Don't put two identical colors on different options of one select field.
- Don't rely on color alone for field type — always pair with the type icon.
- Don't exceed 20 rows in the demo grid without scroll containment.
