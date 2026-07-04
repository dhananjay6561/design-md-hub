# Stytch Design System

## Brand Overview
Stytch is the developer-first authentication & authorization platform — "a better way to build auth" — passwordless login, OTP, passkeys, OAuth, sessions, and auth for AI agents. The current (rebranded) identity is warm and editorial: a **warm off-white** canvas, near-black ink, a confident **blue** for actions, a vivid **lime-yellow** highlight, and soft pastel accents. It reads clean, trustworthy, and modern rather than the old neon-violet-on-black.

> **Rebrand note (verify against live):** the older stub's violet-on-black (`#9747FF` / `#080812`) is retired. The current identity is warm off-white `#FBFAF9` + ink `#1D1D1D` + blue `#348CFF` + lime `#E6FD13`.

## Color Palette

### Primary
- Blue (action): `#348CFF` — primary buttons, links, focus
- Ink: `#1D1D1D` — text, dark surfaces
- Lime highlight: `#E6FD13` — emphasis, accents

### Backgrounds — Light (default)
- Base: `#FBFAF9` — warm off-white page
- Paper: `#FFFFFF`
- Cream: `#F2F0EE` — alt sections
- Border: `#E7E3DE`

### Backgrounds — Dark
Neutral warm near-black (the brand ink).
- Base: `#1D1D1D`
- Elevated: `#262626` / `#2A2A2A`
- Hairline: `#383838`
- Border: `rgba(255,255,255,.11)`

### Pastel accents
- Teal: `#B2D6DE`
- Purple: `#D4CEFF`
- Pink: `#FFCEF1`

### Text
- Primary (light): `#1D1D1D` / (dark): `#FBFAF9`
- Secondary: `#525151` / `#CECECE`
- Muted: `#8A8A88` / `#8B8B8B`

### Semantic
- Success: `#1FA971`
- Error: `#E5484D`
- Warning: `#F59E0B`
- Info: `#348CFF`

## Typography

### Font Stack
- Display / UI: **Booton** (proprietary; approximated here by **Space Grotesk**) — headings, body, buttons. `Space Grotesk, Booton, system-ui, sans-serif`.
- Code / mono: **Chivo Mono** (Google Fonts, real Stytch mono) — codes, tokens, code snippets.

### Scale
- xs 11 / sm 13 / base 15 / md 18 / lg 22 / xl 30 / 2xl 46

### Weights
Regular 400 · Medium 500 · Semibold 600 · Bold 700

## Components

### Buttons
- Primary: blue `#348CFF`, white text, radius 8px — "Start building for free"
- Secondary: ink outline / cream fill — "Talk to an expert"
- Lime CTA: `#E6FD13` fill, ink text — high-emphasis moments

### Auth method tab
Pill/segmented control switching login method: Email magic link · One-time passcode · Passkey · OAuth.

### OTP input
Six single-character boxes (Chivo Mono), active box outlined in blue; fills sequentially.

### OAuth button
Full-width, provider glyph + label (Google / GitHub / Microsoft), neutral outline.

## Signature Component — Login (Auth flow)
Stytch's core value is **drop-in auth**. The signature is a **Login** widget: method tabs, an email field with **Continue**, and an OAuth row. Submitting email advances to a **one-time passcode** screen (six Chivo-Mono boxes); entering/verifying the code lands on a **Signed in ✓** state with a session line. The whole passwordless flow (email → code → session) plays out in one card. This is the single UI most associated with Stytch.

## Guardrails

**DO**
- Keep the light canvas warm off-white `#FBFAF9`; dark mode is warm near-black `#1D1D1D`.
- Use blue `#348CFF` for actions; lime `#E6FD13` and pastels as accents only.
- Render OTP codes, tokens, and session IDs in Chivo Mono.
- Present auth as a clean, trustworthy flow (email → code → session).

**DON'T**
- Don't use the legacy neon-violet `#9747FF` or a pure-black `#080812` background.
- Don't cool the off-white to plain white for the whole page — keep the warmth.
- Don't overuse lime — it's a highlight, not a surface or body color.
- Don't render codes/tokens in a proportional font.
