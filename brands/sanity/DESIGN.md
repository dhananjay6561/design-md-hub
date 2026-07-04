# Sanity Design System

## Brand Overview

Sanity is the Content Operating System for the AI era — a real-time, structured content platform
whose heart is **Studio**, a configurable editing environment. The identity pairs the iconic
**Sanity red `#F03E2F`** with a clean neutral canvas and a playful neon accent spectrum on
marketing surfaces. The Studio itself is calm and neutral so structured content leads. Light-first.

> "The Content Operating System for the AI era."

## Typography

- **Waldenburg** — Sanity's proprietary brand typeface (CORS-locked to the Studio; not
  distributable). **Inter** is used here as the ≈ fallback for display and UI.
- **Mono** — GROQ queries, field names, slugs, document IDs (here: **JetBrains Mono**).

## Color Palette

### Primary
- Sanity Red: `#F03E2F` — logo, brand, critical actions
- Red Hover: `#D43020`
- Studio Blue: `#2276FC` — focus, primary Studio actions
- Publish Green: `#3AB667` — publish / positive

### Neon Accents (marketing spectrum)
- Yellow: `#FFF500` · Green: `#96FF6F` · Magenta: `#F500FF` · Sky: `#AFE3FF`

### Surfaces — Light
- Page: `#FFFFFF`
- Panel: `#F6F6F8`
- Sunken: `#FBFBFC`
- Border: `#E3E4E8`

### Surfaces — Dark (real Studio dark)
- Page: `#101112`
- Surface: `#1A1B1D`
- Elevated: `#232428`
- Border: `#313238`

### Text
- Primary (light `#101112` / dark `#F5F5F5`)
- Secondary: `#6E6E76`
- Muted: `#9898A6`

### Semantic
- Success: `#3AB667` · Warning: `#F5A623` · Critical: `#F03E2F`

## Logo

The **Sanity mark** — the overlapping-planes polygon (viewBox `0 0 24 24`, single path),
rendered in Sanity red `#F03E2F`. Pairs with the "Sanity" wordmark; the mark is never recolored
off the brand red in primary contexts.

## Signature Component — Studio

The Sanity Studio document editor: a document header with type + status, structured **fields**
(Title, Slug, a Portable Text body with a formatting toolbar, Categories), collaborator
presence, and a **Publish** bar. Editing the Title regenerates the slug and flips the document to
"Edited — unpublished changes"; **Publish** commits it to "Published just now". This is the core
Sanity editing moment: real-time, structured, configurable.

## Guardrails

**DO**
- Render the Sanity mark in brand red `#F03E2F`.
- Keep the Studio canvas neutral so structured content and fields lead.
- Use Studio blue `#2276FC` for focus and primary field actions; green for Publish.
- Show document status truthfully (Draft / Edited / Published).
- Set GROQ, slugs, and field names in the mono stack.

**DON'T**
- Don't recolor the Sanity mark off brand red in primary contexts.
- Don't flood the Studio with neon — the spectrum is for marketing, not editing UI.
- Don't invent dark surfaces; anchor on the real Studio dark `#101112`.
- Don't hide unpublished-changes state — editors rely on it.
- Don't set slugs or field keys in a proportional font.
