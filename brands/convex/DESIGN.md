# Convex Design System

## Brand Overview
Convex is the reactive backend platform — a real-time database, serverless functions, file storage, scheduling, search and auth in one, positioned as **"the backend building blocks for your agents."** The current identity is warm and editorial: a distinctive **antique-white cream** canvas, near-black type, a serif for confident headlines, a retro **pixel mono** for labels, and a vivid syntax palette (plum / gold / red) borrowed from Convex's own code theme. It reads like a developer product with taste.

> **Rebrand note (verify against live):** the legacy dark/amber (`#0A0A0A` bg, `#F5A623` amber) identity in older stubs is **retired**. Convex today is **light-first** on cream `#f6eedb`, with near-black CTAs and the plum/gold/red accent family.

## Color Palette

### Foundation
- Antique White (page): `#f6eedb` — the signature warm cream canvas
- Half White: `#fffff9`
- Ink (text / n12): `#141414`
- CTA (n11): `#292929`

### Neutral scale
`n1 #f6f6f6` · `n2 #f1f1f1` · `n3 #e5e5e5` · `n4 #d7d7d7` · `n5 #c2c2c2` · `n6 #a9a9ac` · `n7 #8b8b8e` · `n8 #6d6d70` · `n9 #4f4f52` · `n10 #38383a` · `n11 #292929` · `n12 #141414`

### Brand accents
- Plum: `#8d2676` (p4) — brand accent, actions (lights p1 `#f4e9f1` → p6 `#47133b`)
- Gold: `#f3b01c` (y3) — highlight, warm accent (`#fdefd2` → `#e7a71b`)
- Red: `#ee342f` (r3) — Convex red, errors/destructive (`#fcd6d5` → `#d62f2a`)
- Blue: `#074ee8` / ultramarine `#3d72f5`
- Green: `#4fb014` (g3) — success (`#e5f3dc` → `#479e12`)

### Code syntax ("Chalk" theme — code blocks only)
- Pink: `#fc618d`
- Green: `#7bd88f`
- Purple: `#948ae3`
- Cyan: `#5ad4e6`
- Yellow: `#fce566`
- Comment gray: `#bab6c0`

### Function types (dashboard)
- Query: `#3d72f5` (blue)
- Mutation: `#f3b01c` (gold)
- Action: `#8d2676` (plum)
- HTTP Action: `#4fb014` (green)

### Dark mode
Convex's dashboard is dark; step within the neutral hue anchored on n12.
- Base: `#141414` · Surface: `#1c1c1c` · Elevated: `#242424` · Border: `rgba(255,255,255,.10)`

## Typography

### Font Stack (all real Convex fonts, self-hosted, CORS-open)
- Display / UI: **GT America** (`gtAmerica`) — weights Light/Regular/Medium/Bold/Black. `--font-primary`.
- Serif headline: **Publico** (Publico Headline, Roman + Italic) — hero eyebrow, editorial pull-quotes. `--font-serif`.
- Pixel mono: **VCR OSD Mono** — section identifiers, labels, small caps accents. `--font-pixel`.
- Code: system `ui-monospace, SFMono-Regular, Menlo, monospace` (Convex ships no branded code mono).

### Scale
- xs 11 / sm 13 / base 15 / md 18 / lg 22 / xl 30 / 2xl 46

### Weights
Light 300 · Regular 400 · Medium 500 · Bold 700 · Black 900

## Components

### Buttons
- Primary: `#292929` (n11) fill, white text, fully-rounded (`rounded-full`), hover → `#141414` — "Start building"
- Secondary: transparent, 1px ink border, pill
- Accent: plum `#8d2676` for brand moments

### Function type badge
Pill with the function-type color + VCR/mono label: `query` (blue), `mutation` (gold), `action` (plum), `httpAction` (green).

### Reactive table
Document rows keyed by `_id` (mono), with `_creationTime`; new documents flash-highlight on insert (the reactivity tell).

## Signature Component — Reactive Data ("Always in sync")
Convex's core value is **reactivity**: a query function and the data it returns stay in sync automatically. The signature pairs a syntax-highlighted Convex **query function** (`api.tasks.list`) with the live `tasks` table it powers, plus a **mutation** composer. Running `api.tasks.add` inserts a document that appears in the table instantly with a highlight flash and bumps the live count; toggling a row's checkbox runs a mutation. Function-type badges (query/mutation/action) label each. This captures "everything is code" + "always in sync."

## Guardrails

**DO**
- Keep the page warm cream `#f6eedb` — the antique white IS the brand.
- Use near-black `#292929`/`#141414` for CTAs and body type.
- Reserve the Chalk syntax colors for code; use plum/gold/red for brand accents.
- Use GT America for UI, Publico serif for headline eyebrows, VCR pixel for labels.
- Map function types to their fixed colors consistently.

**DON'T**
- Don't revert to the legacy dark `#0A0A0A` background or amber `#F5A623` — that identity is retired.
- Don't cool the cream to plain white (`#ffffff`).
- Don't use pixel/VCR for body copy or code — it's for short labels only.
- Don't scatter syntax colors as general UI accents.
