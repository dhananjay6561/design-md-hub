# Liveblocks Design System

## Brand Overview

Liveblocks is realtime infrastructure for multiplayer apps and agents — presence, live cursors,
comments, and collaborative editing as a service. The identity is clean and precise: near-black
and off-white surfaces, a confident **brand blue `#0057FF`**, and a **rainbow presence palette**
that colors every collaborator's cursor and avatar. Multiplayer is the whole story. Light-first.

> "Realtime infrastructure for multiplayer apps and agents."

## Typography

- **Suisse Intl** (Regular / Medium / SemiBold) — the real brand typeface, self-hosted, CORS ✅
  — **used directly** for display, headings, and UI.
- **Inter** — secondary UI / long-form (Liveblocks ships it too).
- **Mono** — code, IDs (here: **JetBrains Mono**).

## Color Palette

### Primary
- Brand Blue: `#0057FF` — CTAs, links, focus
- Blue Link: `#0090FF`
- Black: `#000000`
- Off-White: `#FDFCFD`

### Presence — multiplayer cursors & avatars (the rainbow set)
- `#EC5184` pink · `#51A1EC` blue · `#CDEC51` lime · `#C551EC` purple
- `#EC9E51` orange · `#51ECC5` teal · `#7A51EC` violet · `#ECCA51` yellow
- `#5160EC` indigo · `#EC5151` red · `#51ECB8` mint

### Surfaces — Light
- Page: `#FDFCFD`
- Sunken: `#F7F7F8`
- Card: `#FFFFFF`
- Border: `#EBECF0`

### Surfaces — Dark (real near-black)
- Page: `#161618`
- Surface: `#1C1C1F`
- Elevated: `#232327`
- Border: `#2C2C30`

### Text
- Primary (light `#000000` / dark `#FDFCFD`)
- Secondary: `#808080`
- Muted: `#A0A0A5`

### Accent & Semantic
- Purple: `#8F6CEF` · Success: `#22C55E` · Error: `#F44E6B`

## Logo

The **Liveblocks wordmark** (viewBox `0 0 128 24`, single-color path set) rendered in
`currentColor` — black on light, off-white on dark. The product's signature motif is the
**live cursor**: a pointer + name label in that collaborator's presence color.

## Signature Component — Live Cursors

A shared multiplayer canvas: a presence **avatar stack** (each collaborator in a presence color)
over a workspace where remote **cursors glide** along their own paths, each labelled with a name
in its color. Your own cursor follows the pointer over the canvas — the exact Liveblocks
"multiplayer in minutes" moment.

## Guardrails

**DO**
- Give every collaborator a distinct presence color for cursor + avatar + selection.
- Use brand blue `#0057FF` for CTAs, links, and focus.
- Keep surfaces near-black / off-white so presence colors pop.
- Pair a live cursor with a name label in the same presence color.
- Use Suisse Intl for display; Inter for dense UI.

**DON'T**
- Don't make the brand orange — Liveblocks is blue `#0057FF` with a rainbow presence set.
- Don't reuse one presence color for two collaborators in the same room.
- Don't invent dark surfaces; anchor on the real near-black `#161618`.
- Don't show a cursor without an owner (name + color).
- Don't let presence colors double as semantic status colors.
