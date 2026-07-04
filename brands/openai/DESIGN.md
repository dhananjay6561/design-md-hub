# OpenAI Design System

## Brand Overview

OpenAI's visual identity was rebuilt in February 2025 — its first full rebrand — led by
Head of Design Veit Moeller and Design Director Shannon Jager with ABC Dinamo (typeface)
and Studio Dumbar (motion). The system is intentionally reductive: **black and white are the
primary brand colors**, a bespoke geometric typeface (OpenAI Sans) carries every headline,
and the redesigned **Blossom** symbol appears on its own, never locked up beside the wordmark.
Black stands for technological depth; white for openness and accessibility.

The ChatGPT green (`#10A37F`) that many associate with OpenAI is **no longer the corporate
brand color** — since the rebrand it is scoped to ChatGPT product surfaces and interactive
elements. Treat the identity as monochrome first, green second.

> Mission: *"Our mission is to ensure that artificial general intelligence benefits all of humanity."*

## Typography

- **OpenAI Sans** — custom geometric sans-serif by ABC Dinamo (2025), five weights + italics,
  a perfectly circular `O`, geometric structure softened with humanist warmth. Proprietary.
- **Fallbacks used here** (proprietary font is not distributable):
  - Display / headings / wordmark → **Sora** (≈ OpenAI Sans — geometric, circular `O`)
  - Body / UI → **Inter**
  - Mono / code → **JetBrains Mono**
- Pre-2025 the brand used **Söhne** (Klim). Documented for context; do not reintroduce it.

Roles are strict: Sora for display only, Inter for all body/UI/labels, mono for code and API
identifiers.

## Color Palette

### Primary (monochrome — the brand)
- Black: `#000000`
- White: `#FFFFFF`
- Cod Gray (supporting near-black): `#080808`

### Accent (ChatGPT / interactive — scoped, not corporate)
- OpenAI Green: `#10A37F`
- Green Light: `#19C37D`
- Green Dark: `#0D8C6C`

### Surfaces — Light
- Page: `#FFFFFF`
- Surface (sidebar): `#F7F7F8`
- Elevated: `#ECECF1`
- Border: `#E3E3E6`

### Surfaces — Dark (real ChatGPT / platform values)
- Page: `#0D0D0D`
- Surface (sidebar): `#171717`
- Elevated (thread): `#212121`
- Raised (composer): `#303030`
- Border: `#2F2F2F`

### Text
- Primary (light `#0D0D0D` / dark `#ECECEC`)
- Secondary (light `#5D5D5D` / dark `#B4B4B4`)
- Muted: `#8E8EA0`

### Semantic (used sparingly)
- Success: `#10A37F`
- Error: `#EF4444`
- Warning: `#F59E0B`

## Logo

The **Blossom** — an interwoven hexagonal-knot mark (viewBox `0 0 24 24`, single path).
Rendered in `currentColor`: black on light, white on dark. The primary **wordmark** ("OpenAI")
is set in OpenAI Sans and, per brand guidelines, is used **on its own** — the Blossom is never
placed beside the wordmark in a lockup.

## Signature Component — Playground

An interactive Chat Playground mirroring `platform.openai.com`: a system + user message stack,
a model selector (`gpt-4o`, `gpt-4o-mini`, `o3`, `o4-mini`, `gpt-4.1`), a temperature control,
and a **Run** button that streams the assistant response token-by-token with a live cursor,
then a `tokens · latency · model` footer. A **Chat / Code** toggle reveals the equivalent
Python snippet using the current **Responses API** (`client.responses.create`), kept in sync
with the selected model and temperature.

## Guardrails

**DO**
- Lead with the wordmark and give it the prescribed clear space.
- Keep the palette monochrome — black and white are the primary brand colors.
- Use the Blossom on its own; render it in a single flat color.
- Reserve OpenAI green for ChatGPT product surfaces and interactive states.
- Set headlines in OpenAI Sans (or the closest available geometric fallback).

**DON'T**
- Don't lock the Blossom up beside the wordmark.
- Don't recolor, gradient, stretch, or rotate the wordmark or Blossom.
- Don't treat green as the corporate brand color — it's a ChatGPT accent since the 2025 rebrand.
- Don't reintroduce the pre-2025 Söhne typography as the brand voice.
- Don't place the logo on low-contrast or busy backgrounds.
