# Hume — Design System

Design-token reference for **Hume AI** (hume.ai), the empathic AI research lab building emotionally intelligent voice models. All values live-fetched from `hume.ai` and its `_next` CSS (July 2026). Hume's identity is a **warm cream canvas**, a **navy-black ink**, a **lavender** accent, and — most distinctively — an **emotion color spectrum**: Hume measures emotional expression, and it visualizes those emotions as warm ambers, corals, pinks and lavenders.

---

## Brand voice

- Hero H1: **"The Emotional Intelligence Lab for Voice AI"**.
- Positioning (real meta): *"Providing the open source models, datasets, and evaluation APIs to embed emotional intelligence into your voice models."*
- Products: **EVI** (Empathic Voice Interface) · **Octave** (TTS) · **Expression Measurement**.
- CTAs on live site: **"Get Started with Hume Today"**, **"Contact research"**.
- Tone: scientific but warm — a research lab studying human emotion.

---

## Typography

Hume self-hosts its fonts; both are served CORS-open (`access-control-allow-origin: *`), so they're used directly.

| Role | Family | Source | Usage |
|------|--------|--------|-------|
| Display / UI / body | **Fellix** (`FellixVF.woff2`, variable) | hume.ai (CORS ✅) — real `--font-sans` | Hero, headings, body, buttons |
| Mono | **PP Fraktion Mono** (`PPFraktionMono-Variable.ttf`) | hume.ai (CORS ✅) — real `--font-mono` | Emotion scores, code, metadata |

Real tokens: `--font-sans:"Fellix"`, `--font-mono:"PP Fraktion Mono"` (weights 300/400/500/700). Fellix is a geometric humanist sans; PP Fraktion Mono is a distinctive slab-ish mono.

---

## Color

Warm cream in light, navy-black in dark, one lavender accent, and the emotion spectrum for expression data.

### Surfaces
| Token | Hex | Usage |
|-------|-----|-------|
| `cream` | `#FFF9F3` | Page background (light) — warm off-white |
| `cream-2` | `#FDF2E7` | Cards (light) |
| `cream-3` | `#F6E8D8` | Fills, hover (light) |
| `ink` | `#0B0E14` | Page background (dark) — navy-black |
| `ink-2` | `#16171D` | Raised (dark) |
| `ink-3` | `#232323` | Fill / border (dark) |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `text` (light) | `#0B0E14` | Primary |
| `text-2` | `#4A4852` | Secondary |
| `text-3` | `#8A8790` | Muted |
| `text` (dark) | `#FFF9F3` | Primary on ink (warm white) |

### Accent
| Token | Hex | Usage |
|-------|-----|-------|
| `lavender` | `#C094E4` (dark) / `#8B5CC7` (light — for contrast on cream) | Links, focus, accent |
| `ink-btn` | `#0B0E14` / `#FFF9F3` | Primary buttons (ink on cream / warm-white on dark) |

### Emotion spectrum (Expression Measurement)
Warm-dominant, since Hume's data leans toward expressive emotion:
| Emotion | Hex |
|---------|-----|
| Joy / Satisfaction | `#FFB760` |
| Excitement / Determination | `#FE6E00` |
| Contentment | `#FFC783` |
| Triumph / Warmth | `#FF8D87` |
| Surprise | `#FF6568` |
| Amusement / Admiration | `#FDA5D5` |
| Interest / Sympathy | `#C094E4` |
| Calmness / Concentration | `#9BB8E8` |

---

## Logo

Wordmark **"hume"** (lowercase, set in Fellix) alongside an **emotion-spectrum orb** — a soft radial/conic blend of the emotion colors (amber→coral→pink→lavender), reflecting Hume's core motif of emotion-as-color. The wordmark is the fixed brand asset; the orb is decorative and may re-blend across the spectrum.

---

## Guardrails

**DO**
- Anchor light UI on warm cream `#FFF9F3` and dark on navy-black `#0B0E14` — never plain white/black.
- Use the emotion spectrum for expression data (scores, bars, waveforms) — that mapping IS the product.
- Use lavender as the single accent (`#8B5CC7` on cream, `#C094E4` on ink); ink for primary buttons.
- Use Fellix for display/body and PP Fraktion Mono for scores, code and metadata.
- Use real product names — EVI, Octave, Expression Measurement — and real emotion labels.

**DON'T**
- Use pure white / pure black surfaces — Hume is warm cream + navy ink.
- Turn the whole UI rainbow — the spectrum is scoped to emotion data, not chrome.
- Swap Fellix or PP Fraktion Mono for generic substitutes (both are CORS-open, use them).
- Invent emotion labels or randomize scores — use real Hume emotions with deterministic values.
- Put lavender text on cream at `#C094E4` — it fails contrast; step to `#8B5CC7`.
