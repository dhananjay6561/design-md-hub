# Hasura Design System

## Brand Overview
Hasura is the GraphQL data-access company — instant, secure GraphQL APIs on your data (and now PromptQL for AI data access). The current identity is confident and technical: a deep **navy-black** canvas, a vivid **lime** accent that signals speed, a strong **electric blue** for actions, and monospace GraphQL everywhere. It reads like a high-performance developer control plane.

> **Rebrand note (verify against live):** the older stub's teal `#1EB4D4` is superseded — the live palette is navy `#000615` + lime `#B6FC34` + blue `#3970FD` / `#1E56E3`.

## Color Palette

### Primary
- Blue (brand action): `#3970FD` — primary buttons, links
- Blue deep: `#1E56E3` / `#0D41C6`
- Blue light: `#80A3FF` (accents on dark)
- Lime (accent): `#B6FC34` — highlights, speed, run states

### Backgrounds — Dark (default)
- Base: `#000615` — navy-black page
- Surface: `#0A1120`
- Elevated: `#121A2E`
- Code well: `#00030D`
- Border: `rgba(255,255,255,.09)`

### Backgrounds — Light
- Base: `#F0F4FF` — cool blue-white
- Surface: `#FFFFFF`
- Tint: `#DFE8FF` / `#C6D6FF`
- Border: `#E5E7EB`

### Text
- Primary (dark): `#F5F5F5` / (light): `#0B0E1C`
- Secondary: `#9DA4AE` / `#697394`
- Muted: `#6C737F`

### Accent tints
- Purple: `#DBC6FF`
- Cream: `#FFE4B0`

### GraphQL syntax
- Keyword (`query`/`mutation`): `#DBC6FF`
- Field: `#80A3FF`
- String: `#B6FC34`
- Number / enum: `#FFE4B0`
- Punctuation: `#6C737F`

### Semantic
- Success: `#3DD68C`
- Warning: `#FFB020`
- Error: `#FF5A5F`
- Info: `#3970FD`

## Typography

### Font Stack (real Hasura fonts)
- Display / UI: **Archivo** (Google Fonts, self-hosted by Hasura) — headings, body, buttons.
- Code / mono: **JetBrains Mono** (Google Fonts, real Hasura font) — GraphQL, JSON, keys.

### Scale
- xs 11 / sm 13 / base 15 / md 18 / lg 22 / xl 30 / 2xl 46

### Weights
Regular 400 · Medium 500 · Semibold 600 · Bold 700

## Components

### Buttons
- Primary: blue `#3970FD`, white text, radius 8px — "Get started"
- Lime CTA: `#B6FC34` fill, navy text (`#000615`) — high-emphasis moments
- Secondary: transparent, 1px border — "Contact Us"

### GraphQL editor
Dark code well, JetBrains Mono, GraphQL-highlighted (keyword / field / string / number). Operation tabs above; a lime **Run** (▶) triggers execution.

### Response viewer
JSON pane keyed with syntax colors; status line shows time + row count.

## Signature Component — GraphQL API Explorer
Hasura's core value is **instant GraphQL on your data**. The signature is the Console **API Explorer** (GraphiQL): a query editor with GraphQL syntax highlighting, operation tabs (`users`, `orders + relationship`, `insert (mutation)`), and a lime **Run** button. Executing an operation returns realistic JSON in the response pane with a `200 · N rows · Xms` status line. Each operation maps to a deterministic result. This is the single UI most associated with Hasura.

## Guardrails

**DO**
- Use navy `#000615` as the dark canvas and blue `#3970FD` for actions.
- Reserve lime `#B6FC34` for the Run state, highlights, and speed cues.
- Render all GraphQL, JSON and keys in JetBrains Mono.
- Use Archivo for UI; keep GraphQL syntax colors consistent.

**DON'T**
- Don't use the legacy teal `#1EB4D4` as the brand color.
- Don't put lime on a light background as text (too low contrast) — flip to blue.
- Don't render GraphQL/JSON in a proportional font.
- Don't overuse lime — it's an accent, not a surface.
