# RunAnywhere Design System

> "Inference, from the metal up." RunAnywhere is a **research-first inference lab** — it hand-writes the GPU and NPU kernels that make consumer silicon fast, and open-sources the SDKs, infrastructure, and console that run models on **every platform**. The identity is warm, editorial, research-paper calm: a cream canvas, a high-contrast **serif** display, and a signature **orange → red** gradient.

Identity confirmed by **headless-screenshotting the live `runanywhere.ai`** (Next.js SPA, self-hosted fonts). The green/red/amber traffic-light dots in the DOM are terminal-chrome, not brand.

---

## Colors

### Signature — orange → red gradient
| Token | Hex | Usage |
|---|---|---|
| `--orange` | `#FF6900` | Primary — buttons, links, logo start, gradient start (8× in live CSS) |
| `--red` | `#FB2C36` | Gradient end, hot accents, error |
| `--grad` | `linear-gradient(100deg,#FF6900,#FB2C36)` | The hero display gradient ("from the metal up"), logo mark |
| `--orange-ink` | `#D2470A` | Orange darkened for orange *text/links* on cream (contrast) |

### Semantic
| State | Hex |
|---|---|
| Success / passing | `#1B9E77` green (light-ink `#16815F`) / `#3FBE93` (dark) |
| Running / hot | `#FF6900` orange |
| Error | `#FB2C36` red |
| Idle | `#97938C` warm slate |

### Surfaces & text
| Token | Light | Dark |
|---|---|---|
| `--bg` | `#FBF9F9` (warm near-white, sampled) | `#141210` |
| `--bg2` | `#F3F0ED` | `#1D1A16` |
| `--surface` | `#FFFFFF` | `#211E19` |
| `--border` | `#E8E3DE` | `#332E27` |
| `--text` | `#1C1A17` (warm near-black) | `#F5F1EA` |
| `--text2` | `#63605A` | `#B0A99E` |
| `--text3` | `#97938C` | `#7A746B` |
| `--orange` (themed) | `#FF6900` | `#FF7A1A` (nudged for dark contrast) |

The inference console is **always dark** (`#17140F`) in both themes.

---

## Typography

RunAnywhere self-hosts its fonts via Next.js. Traced roles + documented stand-ins:

| Role | Family | Notes |
|---|---|---|
| Display / hero (`font-serif`) | **Newsreader** | High-contrast editorial serif; the hero "Inference, *from the metal up.*" (proprietary Next font → ≈ Newsreader, Google). |
| UI / body (`font-sans`) | **Inter** | Neutral grotesque for body, nav, labels (≈, Google). |
| Metrics / kernels / console | **JetBrains Mono** | tok/s counters, SDK code, kernel names, the inference console. |

Hierarchy: serif for the hero + section display only; Inter for everything structural; mono for all numbers, code, and the console.

---

## Logo

Real RunAnywhere **mark** — two interlocking chevron/comma forms (an "R/A" motif, viewBox `0 0 41 45`, 2 paths) filled with the **orange→red gradient** (`#FF6900 → #FB2C36`), pulled verbatim from the live header (gradient id namespaced to avoid collisions). Paired with the **"RunAnywhere"** wordmark in Inter (`fill:var(--logo-text)`, themed).

**Theming:** mark = gradient (fixed) · wordmark = `var(--logo-text)` (warm near-black on cream / warm near-white on dark).

---

## Components

- **Buttons** — Primary: `background:var(--orange)`, white text, pill radius; the "Talk to us →" CTA. Never orange text on the orange button.
- **Eyebrow** — mono, uppercase, tracked: "A RESEARCH-FIRST INFERENCE LAB".
- **Stat tile** — big mono number + small label (tok/s, latency, downloads, platforms).
- **Platform chip** — iOS / Android / macOS / WebGPU / Jetson — the "run anywhere" targets.
- **Kernel/model chip** — mono, e.g. `Llama-3.2-3B`, `Qwen2.5-1.5B`.

---

## Signature — run anywhere

The whole thesis: one model, hand-tuned kernels, running fast on **any** device.

- **SDK + target**: a real `RunAnywhere` SDK snippet, a model chip, and a **platform selector** (iPhone 16 Pro / Pixel 9 / M3 MacBook / WebGPU / Jetson Orin).
- **Run** streams tokens into an always-dark console with a live **tokens/sec** counter, **time-to-first-token**, and peak memory — each platform has its own deterministic numbers (index-driven, no `Math.random`).
- A small **platform bar** compares tok/s across devices, so "from the metal up" is legible at a glance.

---

## Guardrails

### DO
- Lead with the orange→red gradient for display; use solid orange `#FF6900` for controls.
- Darken orange to `#D2470A` for orange text/links on the cream canvas.
- Set the hero and section display in the serif; keep body/UI in the sans.
- Keep the inference console dark in both themes.
- Frame the product around **platforms** — the same model, running everywhere.

### DON'T
- Don't set body text in the serif — it's display-only.
- Don't put orange text on the orange button.
- Don't invent metrics — use real inference language (tok/s, TTFT, kernels, NPU/GPU).
- Don't use `Math.random()` — keep the benchmark deterministic.
