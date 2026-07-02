# Algolia Design System

## Brand Overview

Algolia is "the AI search and retrieval platform" — positioned today around **Agentic. Generative. Search.** The visual identity is built on one unmistakable color: **electric nebula blue `#003DFF`**, set against clean white/blue-tinted surfaces and deep midnight navy. Headings run in **Sora** (geometric, confident); everything else is **Inter**. The feel is fast, precise, and technical — the design equivalent of "results in 1ms."

Light-first: the marketing site and dashboard are predominantly white `#FFFFFF` / blue-white `#F9F9FF`, with the blue doing all the work. Dark mode anchors on midnight navy `#000033`.

> Verified live from algolia.com (2026). Fonts confirmed: Sora + Inter (both on Google Fonts). Primary blue `#003DFF` confirmed 22× in the production CSS.

## Color Palette

### Primary — nebula blue
- **Blue**: `#003DFF` — primary CTAs, links, the mark, highlighted search matches
- **Blue Hover**: `#1E59FF` — hover/pressed
- **Blue Light**: `#457AFF` — secondary accent, dark-mode brand
- **Midnight**: `#000033` — deep navy, dark page background

### Accent spectrum (Agentic · Generative · Search)
- **Purple**: `#B75AFF` — generative / AI features (deep `#5612B7`)
- **Pink**: `#FF2A6A` — magenta accent, highlights
- **Blue tints**: `#DFE9FF`, `#BBD1FF` — soft fills, pale backgrounds

### Neutrals
- **Ink**: `#23263B` — headings, body
- **Indigo-grey**: `#484C7A` — secondary text
- **Muted**: `#B6B7D5` · **Border**: `#D6D6E7` · **Off-white**: `#F9F9FF` · **White**: `#FFFFFF`

### Semantic
- **Success**: `#00A648`
- **Warning**: `#FFA724`
- **Error**: `#FF2A6A`
- **Info**: `#003DFF`

## Typography

Two brand fonts, one role each — both on Google Fonts. Code uses a system monospace stack (Algolia ships no branded mono).

- **Display — Sora** (400–800): hero, page + section headings
- **UI / Body — Inter** (400/500/600/700): all body, labels, nav, buttons, UI
- **Mono — system** (`ui-monospace, SFMono-Regular, Menlo, monospace`): API keys, query strings, code

### Scale
| Token | Size | Weight | Font | Use |
|-------|------|--------|------|-----|
| display | 56px | 800 | Sora | Hero |
| h1 | 34px | 700 | Sora | Page title |
| h2 | 22px | 600 | Sora | Section heading |
| body-lg | 17px | 400 | Inter | Lead paragraph |
| body | 14px | 400 | Inter | Default UI |
| small | 12px | 400 | Inter | Metadata |
| mono | 12px | 400 | system mono | API keys, queries |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons / inputs: 8px
- Cards / panels: 12px
- Search box: 10px
- Pills / facets: 9999px
- Base: 4px

## Components

### Button
- **Primary**: nebula blue `#003DFF`, white text. Labels: `Get started`, `Start free`, `Search`
- **Secondary**: transparent, `--border-strong` outline. Labels: `Contact sales`, `View docs`
- On dark, brand lifts to `#457AFF` for contrast on midnight — white text in both

### Facet pill
Fully-rounded category filters (All / Audio / Phones / …). Active = blue fill + white text; inactive = subtle surface. Core to the search UX.

### Search input
Rounded (10px) with a leading search icon, blue focus ring `rgba(0,61,255,.22)`. The centerpiece of the brand.

### Highlighted match
Search results highlight the matched substring in **blue, semi-bold**, on a pale blue background — Algolia's signature `<mark>` treatment.

## Signature — InstantSearch

The search-as-you-type experience Algolia is known for: a search box over a product index, results filtering **live** on every keystroke with the matched text highlighted, category facet pills that combine with the query, and a `N results found in Xms` footer. Fast, instant, and unmistakably Algolia. Max 20 results shown.

## Guardrails

**DO**
- Use nebula blue `#003DFF` for every primary action, link, and the mark — it is the brand
- Set headings in Sora, body/UI in Inter, code in a system mono — one role each
- Highlight matched search text in blue semi-bold — never leave results un-highlighted
- Show the speed: surface "results in Xms" — instant is the promise
- Lift the blue to `#457AFF` on midnight navy so it stays legible in dark mode

**DON'T**
- Don't set the brand blue on dark navy at `#003DFF` — contrast fails; brighten it
- Don't use the purple/pink accents as primary actions — they signal generative/AI, not "go"
- Don't set body or UI in Sora — it's display only; Inter owns the UI
- Don't tint dark surfaces neutral-grey — Algolia's dark is midnight navy `#000033`
- Don't fake search results — filter a real index and highlight real matches
</content>
