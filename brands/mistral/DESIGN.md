# Mistral AI — Design System

Design-token reference for **Mistral AI** (mistral.ai), reconstructed from the live site's Astro/Tailwind CSS (`/_astro/astro.ClAR0fNs.css`) and homepage markup. Mistral's identity is a warm, editorial system: cream paper surfaces, a deep navy dark mode, and the iconic pixel-grid flame mark that steps from yellow to raspberry. Everything below is live-fetched ground truth; anything unconfirmed is flagged.

---

## Brand

- **Homepage H1 (visually hidden):** "Frontier AI. In your hands."
- **Title tag:** "Frontier AI LLMs, assistants, agents, services | Mistral"
- **Primary CTAs:** "Start building", "Contact sales", "Talk to sales"
- **Product surface names (nav):** Mistral Medium 3.5, Mistral Small 4, Mistral OCR 4, Voxtral TTS, Codestral, Le Chat, La Plateforme.

---

## Typography

Three roles, one each — mirrors the live stack.

| Role | Family (live) | This repo | Notes |
|------|---------------|-----------|-------|
| Display / UI sans | **ALTMistral** (`/fonts/alt-mistral/…woff2`, weights 400/500/600) | **Space Grotesk ≈** | ALTMistral is proprietary, self-hosted, and served **without** `Access-Control-Allow-Origin: *`, so it fails from `file://`. Space Grotesk is the nearest CORS-open Google Font — same geometric, slightly-condensed grotesque character. Marked `≈`. |
| Mono | **Space Mono** (self-hosted TTF) | **Space Mono** (Google Fonts, CORS `*`) | Real brand mono — used verbatim. |
| Body (secondary) | **Inter** (self-hosted variable) | Inter | Used for long-form body / secondary copy on the live site. |

Live type scale (`:root`): display 2.5rem/3rem · h1 2.5rem/3rem · h2 1.75rem/2.5rem · h3 1.5rem/1.75rem · h4 1.25rem/1.5rem · body-large 1rem/1.5rem · eyebrow 0.75rem/1rem.

---

## Color

All hex values below are lifted directly from the live CSS custom properties.

### Flame mark (fixed — never re-tint)
The pixel-grid "M" logo uses fixed brand colors in this exact order (top warm → bottom cool):

| Token | Hex | In logo |
|-------|-----|---------|
| yellow-500 | `#FFAF01` | top squares |
| tangerine-500 | `#FF8204` | upper band |
| orange-600 | `#FA500F` | mid band |
| orange-500 | `#FF5229` | brand surface accent |
| red-600 | `#E61300` | lower squares |
| raspberry-700 | `#C4001D` | base row |

`--color-surface-brand` = `--color-orange-strong` = `orange-500` `#FF5229` (primary action / brand fill).

### Surfaces
- **Light (cream):** `surface-brand-primary` `#FBFBF8` · `surface-brand-secondary` `#F5F4EF` · `surface-brand-tertiary` `#EBE9E0` · `cream-50` `#FAFAF4` · `cream-100` `#F2F1E8`.
- **Dark (navy, `surface-invert`):** `navy-950` `#151524` · `navy-900` `#242433` · `navy-800` `#343446` · `navy-700` `#56566C`.

### Text
Light: primary `zinc-900`, secondary `zinc-800`, muted `zinc-500`. Dark: primary `zinc-50`, secondary `zinc-300`, muted `zinc-400`. (Tailwind zinc, defined as oklch on the live site; approximated to hex here for the swatches.)

### Borders
Light `border-primary` `#E4E3DE`, `border-secondary` `#C9C9C4`. Dark `border-primary` `#31313A`, `border-secondary` `#474754`.

### Semantic accents
`blue-600` `#0082E6` (brand-2 / info) · `green-500` `#44BA82` (success) · `red-600` `#E61300` (danger, shared with flame) · `yellow-500` `#FFAF01` (attention).

---

## Signature component — Le Chat / La Plateforme completion

The showcase's interactive piece is a **Mistral chat playground**: a model selector (`Mistral Large`, `Mistral Medium 3.5`, `Mistral Small 4`, `Codestral`, `Pixtral Large`), a temperature control, and a **Run** that streams a deterministic assistant reply token-by-token, closing with a real token/latency footer. Alongside is the real Python SDK snippet using `client.chat.complete`. Streaming is index-driven (no `Math.random`) so screenshots are stable.

API IDs used (real): `mistral-large-latest`, `mistral-medium-latest`, `mistral-small-latest`, `codestral-latest`, `pixtral-large-latest`.

---

## Guardrails

**DO**
- Anchor light UI on the cream surfaces (`#FBFBF8` → `#EBE9E0`), not pure white — the warm tint is identity.
- Keep the flame mark's six colors fixed and in order; it is a mark, not a palette to remix.
- Use `orange-500` `#FF5229` as the single brand action color; reserve blue/green/red for info/success/danger.
- Pair Space Grotesk (display) with Space Mono (code, model IDs, metrics) — one role each.
- Use `navy-950` `#151524` (not black) as the dark canvas.

**DON'T**
- Don't recolor or gradient-blend the flame squares into a smooth ramp — they are discrete pixels.
- Don't put brand orange on large surfaces; it's an accent, not a background.
- Don't use pure `#000000`/`#FFFFFF` for text or page — use zinc text on cream/navy.
- Don't mix font roles (mono for headings, display for code).

---

*Fonts: ALTMistral → Space Grotesk (≈, CORS-locked original); Space Mono + Inter used directly. All colors and copy live-fetched from mistral.ai; oklch neutrals approximated to hex for swatch display.*
