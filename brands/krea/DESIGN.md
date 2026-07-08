# Krea — Design System

*"The world's most powerful creative AI suite."* Krea generates, enhances, and edits images, video, and 3D — in real time. The brand is deliberately restrained so the work can shine: a near-black canvas, crisp white, one twisting bloom mark, and a clean Swiss grotesque. **All the color comes from the generations, not the chrome.**

> **Source of truth:** traced from live `krea.ai` markup + the rendered homepage and OG artwork (mark, palette, hero copy). Font is confirmed from the site's `@font-face` src.

---

## Brand foundations

Krea is monochrome by design. The UI is black, white, and grey; vivid color belongs to the generated images, videos and 3D that fill the canvas. The interface stays out of the way — *"Dead simple UI. No tutorials needed."*

- Near-black `#141414` / navy-black `#11191F` surfaces; pure white type.
- The **primary action inverts** with theme (white pill on dark, black pill on light) — never a colored button in the chrome.
- Generation outputs carry the palette: warm peach/gold sunsets, neon blue/violet cyberpunk, chrome. The chrome itself does not.

---

## Color

### Core (chrome)
| Token | Light | Dark | Usage |
|---|---|---|---|
| `--bg` | `#FFFFFF` | `#0E0F12` | Canvas |
| `--surface` | `#FAFAFA` | `#16171B` | Panels, cards |
| `--surface-2` | `#F2F2F3` | `#1E2026` | Insets, wells |
| `--ink` | `#141414` | `#FFFFFF` | Primary text (near-black / white) |
| `--navy` | `#11191F` | `#11191F` | Deep app frame |
| `--muted` | `#6B6B6E` | `#9A9AA2` | Secondary text |
| `--border` | `#ECECEC` | `rgba(255,255,255,.10)` | Hairlines |

### Generation spectrum (outputs only)
Sampled from Krea's live imagery + palette — used in *generated content*, never as UI chrome.
| Token | Hex | Where |
|---|---|---|
| `--violet` | `#A78DFF` | Neon / creative accents |
| `--blue` | `#1C7DFF` | Realtime indicator, links, cool light |
| `--blue-deep` | `#004EFF` | Deep highlight |
| `--gold` | `#FFC32F` | Warm sun, highlights |
| `--peach` | `#F0DCD6` | Warm skin / sky |

**Restraint rule:** the interface is monochrome. If a hue appears in the UI it's a link/realtime cue (`--blue`) — everything else colorful lives inside a generation frame.

---

## Typography

| Family | Role | Notes |
|---|---|---|
| **Suisse Intl** ≈ **Inter** | Everything — hero, UI, labels, body | Krea self-hosts Suisse Intl (Regular/Medium/SemiBold/Bold) but it's **CORS-locked** (no `access-control-allow-origin`), so this showcase uses **Inter** (Google Fonts) as the documented ≈ — near-identical neutral Swiss grotesque |
| **JetBrains Mono** | Model IDs, dimensions, latency, meta | e.g. `Krea 1`, `1024×1365`, `⚡ 0.04s` |

- **Hero H1:** ≈36–48px, weight 600, tight tracking (`-0.02em`). The `.ai` in the wordmark drops to `--muted`.
- **Section labels:** JetBrains Mono, 11px, uppercase, `letter-spacing:.08em`.

---

## Spacing, radius, shadow

- **Radius:** panels/canvas `16px`, cards `12px`, buttons/chips `9999px` (fully rounded pills — Krea's buttons are pill-shaped), inputs `10px`.
- **Shadow:** soft and sparse — `0 10px 40px rgba(0,0,0,.10)` on the app; on dark, depth is borders + a subtle glow around active generations.
- **Spacing:** 4px base grid; roomy canvas padding.

---

## Components

- **Primary button (pill):** inverts with theme — white fill + `#141414` text on dark, `#141414` fill + white text on light. Labels: `Start for free`, `Generate`, `Launch App`.
- **Secondary / ghost:** transparent with a 1px `--border`; used for `Contact Sales`, tool switches.
- **Model chip:** pill with a small dot + mono label (`Krea 1`, `Flux`, `Krea 2`).
- **Slider:** thin track, round thumb; drives realtime parameters (strength / stylize).
- **Realtime badge:** `⚡ Realtime · 0.04s` — mono, `--blue`, signals live rendering.
- **Aspect / resolution chips:** `3:4`, `1:1`, `16:9`, `1K` — mono.

---

## Signature — realtime generation canvas

Krea pioneered **real-time** image generation: the output re-renders the instant you change the prompt or a parameter — no "generate and wait." The signature reproduces that feel.

- **Prompt + preset scenes:** a prompt field plus chips (sunset lake, cyberpunk street, studio portrait, liquid chrome). Selecting one re-renders the canvas **instantly**.
- **Realtime parameter:** a *stylize* slider morphs the current render live, with a `⚡ Realtime · 0.0Xs` latency cue — the wow moment.
- **Model + format:** switch model (`Krea 1` / `Flux` / `Krea 2`) and aspect (`3:4`), then **Enhance to 1K** does a quick detail sweep to `1024×1365`.
- **Outputs are procedural** — layered CSS/SVG gradient meshes per scene (warm sun, neon city, portrait light, chrome), so color lives in the *generation* while the UI stays monochrome. Fully **deterministic**, no `Math.random()`.

---

## Guardrails

**Do**
- Keep the chrome monochrome — black, white, grey; let generations carry all color.
- Invert the primary pill with theme (white-on-dark / black-on-light); never a colored chrome button.
- Use the twisting **bloom mark** in white/black; pair with a clean Swiss grotesque.
- Reserve `--blue` for realtime cues and links; keep the rest of the palette inside generation frames.
- Show the **realtime** feel — instant re-render + a latency cue — it's the product.

**Don't**
- Don't paint the UI with the generation palette — that breaks the "let the work shine" identity.
- Don't use square, heavy buttons — Krea's actions are rounded pills.
- Don't set body in a serif or a quirky display face — it's neutral Suisse/Inter.
- Don't add a colored default accent to the chrome; monochrome is the point.
- Don't use `Math.random()` — presets and renders are deterministic.
