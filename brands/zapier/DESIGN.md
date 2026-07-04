# Zapier Design System

## Brand Overview
Zapier is the automation platform that connects apps into no-code workflows ("Zaps") — trigger → action, no glue code. The 2024 identity is **warm, editorial, and confident**: a cream paper canvas, a single hot **Zapier orange**, a warm near-black ink, and a big-personality **Degular Display** headline face balanced by a quiet serif and Inter for UI. Light-first, generous, human — automation made approachable.

## Color Palette

### Brand
- **Zapier orange** `#FF4F00` — the signature: mark, primary CTAs, active Zap state, links-that-act
- **Ink** `#201515` — warm near-black: headings, body, wordmark (the dominant text color)
- **Clay** `#D97757` — warm secondary accent (illustration, subtle highlights)

### Surfaces (light-first — warm paper)
- **Cream** `#F9F7F3` — page background (warm, never pure white)
- **Paper** `#FFFEFB` — cards, raised surfaces
- **Sand** `#ECEAE3` — secondary fills, hover
- **Border** `#D6D5D2` — hairlines; **strong** `#C5C0B1`

### Text & warm neutrals
- **Text primary** `#201515` · **secondary** `#55544F` · **muted** `#72716D` · **faint** `#A8A6A0`

### Semantic
- **Success** `#1F8A4C` (green) · **Warning** `#FBBC05` (gold) · **Error** `#E52D27` (red)

### Dark mode (warm near-black — anchored on ink, never cool)
- **Page** `#1A1210` · **Card** `#241A17` · **Raised** `#2E211D` · **Border** `rgba(255,255,255,.09)`
- **Text** `#F9F7F3` / muted `#B7B0AB`. Orange `#FF4F00` is retained (lifts to `#FF6A2B` for text on dark).

## Typography
Zapier ships **Degular Display** (headlines), a serif ("Serrif"), **Inter** (UI), and **JetBrains Mono**. Degular Display is CORS-open and used directly here; Inter + JetBrains Mono via Google Fonts.
- **Display** — `Degular Display` (500/600/700) — hero H1, big headings (tight, characterful)
- **UI / body** — `Inter` — nav, labels, buttons, step cards, controls
- **Mono** — `JetBrains Mono` — Zap IDs, field names, code/webhook payloads

## Spacing
4px base — 4, 8, 12, 16, 20, 24, 32, 40, 48, 64.

## Border Radius
- Buttons / inputs: 8px · Step cards: 12px · App icon tiles: 8px · Pills/toggle: 9999px · Cards/panels: 16px.

## Components

### Zap editor (signature)
A vertical sequence of steps — a **Trigger** followed by one or more **Actions** — each a card with an app-icon tile, a step number, the app name, and the chosen event. Steps are joined by a connector line with a `+` to insert steps. A master **on/off** switch (orange when on) and **Test** run drive the whole Zap.

### Step card
App icon tile (brand-colored) + `1. Trigger` / `2. Action` label + app name + event line. Running state shows a spinner; success shows a green check.

### Button
Orange `#FF4F00` primary with white text (rounded 8px); secondary is a warm outline on cream.

### Toggle
Pill switch; off = sand, on = orange.

## Guardrails

**DO**
- Keep the wordmark's dot/mark orange `#FF4F00` (fixed); let the letters adapt to the theme.
- Keep the canvas warm cream `#F9F7F3` — surfaces are `#FFFEFB`, never pure white.
- Use orange for brand, primary actions, and the active Zap state — sparingly.
- Set headlines in Degular Display; UI/body in Inter; IDs & payloads in mono.
- Keep dark mode warm near-black `#1A1210` — never a cool blue-black.

**DON'T**
- Don't use a second saturated accent competing with orange.
- Don't set body copy in Degular Display — it's a display face for headlines.
- Don't cool the neutrals — Zapier's grays are warm.
- Don't recolor the orange mark.
- Don't crowd the Zap editor — the step sequence should read top-to-bottom at a glance.
