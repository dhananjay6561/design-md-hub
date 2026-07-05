# Groq — Design System

Design-token reference for **Groq** (groq.com) — the fast, low-cost AI inference company behind the **LPU** (Language Processing Unit) and **GroqCloud**. Not to be confused with Grok/xAI. Every token below is traced from Groq's live site CSS (`_next/static/css/*`) and homepage markup.

> Tagline (live H1): *"Groq delivers fast, low cost inference that doesn't flake when things get real."*
> Page title: *"Groq is fast, low cost inference."*

---

## Brand foundations

Groq's identity is built on one idea: **speed**. The visual language is warm-neutral (paper-and-ink), spare, and engineering-forward, with a single hot **orange** accent (`#F43E01`) doing all the emphasis work, backed by a "fluorescent" utility palette used sparingly for section theming and data.

---

## Color

Groq's tokens are defined with CSS `light-dark()`, so the same semantic token resolves differently per theme. Backgrounds are **warm** neutrals (a yellow-tinted greyscale), not pure `#fff`/`#000`.

### Primary — Orange
| Token | Hex | Usage |
|---|---|---|
| `--color-orange` / `--color-orange-base` / `--color-orange-brand` | `#F43E01` | Brand accent, primary button bg, links, emphasis |
| `--color-orange-dark` | `#C23101` | Hover / pressed orange |
| `--color-orange-middle` | `#FE9E20` | Warm secondary, gradients |
| `--color-orange-light` | `#FFD1A3` | Tint fills, soft backgrounds |

`--color-orange`, `--color-orange-base`, and `--color-orange-brand` all resolve to the **same** `#F43E01` in live CSS.

### Surfaces (warm neutral scale)
| Token | Hex | Usage |
|---|---|---|
| `--color-utility-98-yellow` | `#FAFAF8` | Lightest surface |
| `--color-utility-95-yellow` | `#F3F3EE` | **Light-mode page background** (`--color-bg` light) |
| `--color-utility-91-yellow` | `#E8E8DE` | Light raised surface / section |
| `--color-utility-81-yellow` | `#CECEBF` | Light borders, dividers |
| `--color-utility-20-yellow` | `#34342E` | Dark raised surface |
| `--color-utility-16-yellow` | `#2A2A25` | **Dark-mode page background** (`--color-bg` dark) |
| `--color-utility-20-blue` | `#2D2F33` | Ink / dark section bg |
| `--color-utility-16-blue` | `#26292E` | Deepest cool dark |
| `--color-white` | `#FFFFFF` | Pure white (cards on dark, button text) |
| `--color-black` | `#000000` | Pure black (rare) |

### Text
| Token | Resolves to | Usage |
|---|---|---|
| `--color-text` (light) | `#2D2F33` (`utility-20-blue`) | Primary text on light |
| `--color-text` (dark) | `#FFFFFF` | Primary text on dark |
| `--color-bd` (border) | `light-dark(black 20%, white 20%)` | Hairline borders via `color-mix` |

### Semantic — "Fluorescent" utility palette
Groq uses a bright fluorescent set (each with a `-base` and `-light` variant) for section theming, data viz, and status. `-base` for solids/text-on-dark, `-light` for tint fills.

| Token | Base | Light | Usage |
|---|---|---|---|
| `--color-fluorescent-green` | `#10E68D` | `#A9FFDB` | Success / online / positive |
| `--color-fluorescent-blue` | `#5FC0FF` | `#BFE4FC` | Info / links (accent) |
| `--color-fluorescent-yellow` | `#FDEB20` | `#F4FD90` | Attention / warning |
| `--color-fluorescent-pink` | `#F392DD` | `#FAD8FF` | Highlight |
| `--color-fluorescent-purple` | `#D377FD` | `#E3DCF8` | Highlight / category |

---

## Typography

Two families, live-loaded via Next.js font pipeline (both are also native Google Fonts, CORS-open):

- **`--ff-sans` / `--ff-heading` / `--ff-display`** → **Space Grotesk** (`"Space Grotesk", "Space Grotesk Fallback", system-ui, "Helvetica Neue", Arial, sans-serif`). Used for hero, headings, body, UI — Groq maps display/text/sans all to Space Grotesk.
- **`--ff-mono`** → **IBM Plex Mono** (`"IBM Plex Mono", ui-monospace, "Cascadia Code", "Source Code Pro", Menlo, Consolas, monospace`). Code blocks, model IDs, metrics, tokens/sec counters, section eyebrows.

Roles: Space Grotesk carries everything visible; IBM Plex Mono is reserved for code, model names, numeric metrics, and metadata chips.

---

## Iconography / logo

The Groq wordmark is a single-path SVG, `viewBox="0 0 187 71"`, `fill="currentColor"` — so it adapts to text color per theme (orange on brand surfaces, ink on light, white on dark). The full path is embedded in `preview.html`.

---

## Real product copy (verbatim from live site)

- H1: "Groq delivers fast, low cost inference that doesn't flake when things get real."
- "Inference is Fuel for AI"
- "Speed at a winning cost"
- "OpenAI compatible in just two lines."
- "Instant intelligence. Deployed worldwide."
- "The LPU is the cartridge. GroqCloud is the console."
- "Born for this. Literally."
- "Benchmarks don't ship. Workloads do."
- "Devs trust GroqCloud for inference that stays smart, fast and affordable."
- CTAs: **Start Building** · **Free API key** · **Try Groq for Free** · **See Pricing** · **View Models** · **Get Started**

### GroqCloud models (real model IDs)
`llama-3.3-70b-versatile` · `llama-3.1-8b-instant` · `llama-4-scout-17b-16e-instruct` · `qwen3-32b` · `deepseek-r1-distill-llama-70b` · `gemma2-9b-it` · `mixtral-8x7b`

### API (OpenAI-compatible, verbatim shape)
GroqCloud is OpenAI-compatible: point the OpenAI client at `https://api.groq.com/openai/v1` with `client.chat.completions.create(...)`.

---

## Components

- **Buttons:** primary = orange (`#F43E01`) bg, white text; **hover inverts** to white bg + orange text (`--color-btn-primary-bg-hover: white`, `--color-btn-primary-text-hover: orange`). Never hardcode button text color — it flips on hover. Radius `4px` (`--border-radius-input`).
- **Inputs:** `1px solid var(--color-bd)`, `4px` radius.
- **Section theming:** whole sections adopt a fluorescent bg + matching accent text (`--color-bg-section-*`).

---

## Guardrails

**DO**
- Use one hot orange (`#F43E01`) as the single accent; let warm neutrals carry the layout.
- Keep backgrounds warm — `#F3F3EE` light, `#2A2A25` dark — never pure `#fff`/`#000` for page bg.
- Make **speed the hero**: tokens/sec, time-to-first-token, and total latency are the headline metrics.
- Use IBM Plex Mono for model IDs, code, and all numeric/latency readouts.
- Reserve fluorescent colors for section theming, data, and status — not body text.

**DON'T**
- Confuse Groq with Grok/xAI — Groq is orange, LPU-based inference; no black "X" branding.
- Hardcode primary-button text color (it inverts to orange on hover).
- Stack multiple bright accents in one component — orange leads, fluorescents support.
- Use cool grey/blue neutrals for surfaces — the greyscale is yellow-warm.
- Invent latency numbers — pair speed claims with a concrete tokens/sec figure.

---

*Sources: live-fetched from groq.com homepage HTML + `_next/static/css/*.css` (deploy `dpl_141GY4EJek3hchwrNW1PiqejzzSf`). Color tokens, `light-dark()` resolutions, font families, hero/section copy, CTA labels, model IDs, and wordmark path are all traced from live; nothing guessed.*
