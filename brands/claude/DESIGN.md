# Claude Design System

## Brand Overview
Claude is Anthropic's AI assistant. The identity is warm, editorial, and human — the deliberate opposite of cold enterprise blue. A **cream paper** canvas, a single distinctive **clay-orange** accent, near-black warm ink, and a transitional **serif** for headings give it a calm, considered, almost literary feel. Generous whitespace, no glassmorphism, no decorative gradients. The mark is the Claude "sunburst" (radiating spokes) rendered in clay.

## Color Palette

### Primary
- **Clay** `#D97757` — the signature accent: primary CTAs, send button, active states, the mark
- **Clay deep** `#C15F3C` — hover / pressed
- **Ink** `#141413` — headings, primary text, dark surfaces

### Surfaces (light-first)
- **Cream / paper** `#F0EEE6` — page background (the signature warm canvas)
- **Card** `#FAF9F5` — chat surface, panels (warm off-white, never pure `#FFFFFF`)
- **Deep cream** `#E8E6DC` — secondary surface, hover, user message bubble
- **Border** `#DEDBCE` — hairlines on cream
- **Border strong** `#CDC9BA` — emphasized dividers, inputs

### Text & warm neutrals
- **Text primary** `#141413`
- **Text secondary** `#3D3D3A`
- **Text muted** `#87867F`
- **Faint** `#B0AEA5`

### Dark mode (warm near-black — anchored on ink, never cool navy)
- **Page** `#1F1E1C`  ·  **Card** `#262523`  ·  **Raised** `#302E2A`
- **Border** `rgba(255,255,255,.09)`  ·  **Text** `#F0EEE6` / muted `#8F8D83`
- Clay `#D97757` is retained unchanged — it reads on both cream and warm-dark.

### Semantic
- **Success** `#43A047`  ·  **Error** `#E5484A`

## Typography
Anthropic ships **Anthropic Sans / Serif / Mono** (self-hosted). Their web fonts are CORS-locked to Anthropic's own origins, so this reference falls back to close Google Fonts equivalents (documented `≈`).
- **Serif (display)** — `Anthropic Serif` ≈ **Newsreader** — greetings, headings, the editorial voice (the "Good evening" moment)
- **Sans (UI / body)** — `Anthropic Sans` ≈ **DM Sans** — all product text, labels, buttons, message body
- **Mono** — `Anthropic Mono` ≈ **JetBrains Mono** — code blocks, artifacts, metadata

Weights kept to 400 / 500 / 600. Headings tighten to `-0.01em`; body sits at 1.6 line-height. Never all-caps headings.

## Spacing
4px base — 4, 8, 12, 16, 20, 24, 32, 40, 48.

## Border Radius
- Buttons / inputs: 10px  ·  Cards & message bubbles: 16px  ·  Chips / pills: 9999px  ·  Send button: 50%
- Bubbles use a 16px radius with one 4px corner as the tail.

## Components

### Chat message
- **User** — deep-cream `#E8E6DC` bubble, right-aligned, 16px radius (tail top-right).
- **Claude** — flush on the canvas (no bubble) with the clay sunburst avatar, left-aligned; responses stream token-by-token with a blinking caret.

### Artifact panel
Claude's signature feature. A side panel with **Preview / Code** tabs that opens when Claude generates something runnable — the preview is live and interactive, the code tab shows the source in mono.

### Composer
Rounded input with suggested-prompt chips above, a model chip (`Claude Opus 4.8`), and a circular clay send button (up-arrow).

### Button
Clay `#D97757` primary with white text, 10px radius, no harsh shadow. Secondary is a hairline outline on cream.

## Guardrails

**DO**
- Keep the canvas warm cream `#F0EEE6` — never pure white; surfaces are off-white `#FAF9F5`.
- Use clay `#D97757` sparingly — ideally one primary action per view.
- Lead headings and greetings with the serif; keep body in the sans.
- Keep dark mode warm (near-black `#1F1E1C`), never a cool blue-black.
- Animate with `ease` curves under 200ms; use whitespace instead of borders where possible.

**DON'T**
- Don't use blue as a primary color — it conflicts with the brand's warmth.
- Don't use all-caps headings, heavy drop shadows, or glassmorphism.
- Don't render the Claude mark in any color but clay.
- Don't set body copy in the serif or long strings in the mono.
- Don't crowd the layout — density reads as anxious; the brand is calm.
