# Pinecone Design System

## Brand Overview
Pinecone is the vector database to build knowledgeable AI — "give agents knowledge." The current (rebranded) identity is crisp and technical with a retro-computing wink: a clean near-white canvas, a confident **electric blue**, a violet/periwinkle support range, and a distinctive **Apple II pixel** typeface used for accents. It reads like precise data infrastructure with personality.

> **Rebrand note (verify against live):** the older stub's teal-green `#1ECA8A` is retired — the current brand is **electric blue `#002BFF`** with violet `#3D11A0` and frost-blue `#B3D5FF`.

## Color Palette

### Primary
- Brand Blue: `#002BFF` — primary actions, links, high similarity
- Blue-violet: `#1C17FF` / `#3352D4`
- Periwinkle: `#5B7AEE` — support, medium similarity
- Violet: `#3D11A0` (`--brand-violet`)
- Frost Blue: `#B3D5FF` (`--brand-frost-blue`)

### Accent spectrum
- Purple: `#A440CE`
- Cyan: `#8BF6FF`

### Backgrounds — Light (default)
- Base: `#FBFBFC` — cool near-white page
- Paper: `#FFFFFF`
- Surface: `#F2F3F6`
- Border: `#E7E5E4` / Divider `#D8DDDF`

### Backgrounds — Dark
Neutral near-black (not navy).
- Base: `#171717`
- Elevated: `#1C1C1C` / `#262626`
- Border: `rgba(255,255,255,.10)`

### Text
- Primary (light): `#1C1917` / (dark): `#F1F5F8`
- Secondary: `#57534E` / `#A8A29E`
- Tertiary / muted: `#72788D`

### Semantic
- Success: `#15B077`
- Warning: `#DD815D`
- Error: `#E31957`
- Info: `#0028FF`

### Similarity score
- High (≥ 0.85): `#002BFF`
- Medium (0.70–0.85): `#5B7AEE`
- Low (< 0.70): `#A8A29E`

## Typography

### Font Stack (all real Pinecone fonts, self-hosted, CORS-open)
- Display / UI: **GT Planar** (`gtPlanar`, variable) — headings, body, buttons. Fallback `Space Grotesk, system-ui, sans-serif`.
- Retro accent: **Apple II Pro** (`appleIIPro`) — eyebrow labels, section identifiers, badges. Pixel/terminal flavor; short strings only.
- Code / mono: **JetBrains Mono** (`--font-mono`) — vector IDs, scores, code.

### Scale
- xs 11 / sm 13 / base 15 / md 18 / lg 22 / xl 30 / 2xl 46

### Weights
Extralight 200 · Light 300 · Regular 400 · Medium 500 · Bold 700

## Components

### Buttons
- Primary: blue `#002BFF`, white text, radius 8px — "Get started"
- Secondary: transparent, 1px border — "Contact sales"
- Ghost / link: blue text

### Vector result row
Rank + vector id (JetBrains Mono) + similarity score + a score bar colored by band + metadata snippet + namespace.

### Score bar
Horizontal fill = score; color maps to the similarity band (high blue / medium periwinkle / low gray).

## Signature Component — Vector Search
Pinecone's core value is **semantic similarity search** over a vector index. The signature is a **Query** panel: an index header (name, `1536` dims, `cosine` metric, vector count), a natural-language query with preset chips, and a **Search** button that returns the **top-K** nearest matches ranked by similarity score with colored score bars, snippet text and namespace. Each query maps to a deterministic ranked result set. This is the single UI most associated with a vector database.

## Guardrails

**DO**
- Use electric blue `#002BFF` as the brand; periwinkle/violet as support.
- Keep the light canvas cool near-white `#FBFBFC`; dark mode is neutral near-black.
- Use Apple II pixel font for short accent labels only; GT Planar for everything else; JetBrains Mono for ids/scores.
- Map similarity bands to their fixed colors consistently.

**DON'T**
- Don't use the legacy teal `#1ECA8A` as the brand color.
- Don't set dark mode to navy — it's neutral `#171717`.
- Don't use the Apple II font for body copy or long strings.
- Don't render vector ids or scores in a proportional font.
