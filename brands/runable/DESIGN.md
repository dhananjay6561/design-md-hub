# Runable Design System

> "Best way to work with AI." Runable is a **general-purpose AI agent** — describe a task ("What needs to be done?") and it builds apps, slides, videos, and websites end-to-end. The identity is calm and product-first: a clean white canvas, a confident **cyan-teal** primary, and a signature **teal → mint-green gradient**. Light-first.

Identity confirmed by **headless-screenshotting the live `runable.com`** (the page is a Tailwind SPA with no inline tokens). Note: the `#1a73e8` blue + Google Sans / Roboto in the DOM belong to an embedded **Google Sign-In widget**, *not* Runable — the real brand is teal + mint.

---

## Colors

### Primary — cyan-teal
| Token | Hex | Usage |
|---|---|---|
| `--brand` | `#00B7CA` | Primary cyan-teal — the "Sign In" / run button, links, active states (pixel-sampled from live) |
| `--brand-deep` | `#00828C` | Deep teal — gradient base, hover, pressed |
| `--brand-ink` | `#047B86` | Teal darkened for legible teal *text* on white (contrast) |
| `--brand-tint` | `rgba(0,183,202,.10)` | Teal wash — selected chip, agent-step highlight |

### Accent — mint & signature gradient
| Token | Hex | Usage |
|---|---|---|
| `--mint` | `#76E5A9` | Mint green — success ticks, gradient highlight |
| `--mint-2` | `#6DC696` | Deeper mint — gradient mid |
| `--grad` | `linear-gradient(135deg,#00B7CA,#00828C 55%,#6DC696)` | The teal→mint band ("How can Runable help you?") |
| `--orange` | `#F0A23C` | "Loved by 1M+ customers" badge only |

### Semantic (agent run state)
| State | Hex |
|---|---|
| Running / thinking | `#00B7CA` teal |
| Done / success | `#3FB984` mint-green (light) / `#76E5A9` (dark) |
| Error | `#E5573D` coral-red |
| Queued / idle | `#9AA0A6` slate |

### Surfaces & text
| Token | Light | Dark |
|---|---|---|
| `--bg` | `#FFFFFF` | `#061A1C` (deep teal-black, from live `rgb(5,30,32)`) |
| `--bg2` | `#F6F7F7` | `#0D2427` |
| `--surface` | `#FFFFFF` | `#10292C` |
| `--border` | `#E7EAE9` | `#1E3B3E` |
| `--text` | `#1A1A1A` | `#EAF2F1` |
| `--text2` | `#5F6368` | `#9FB4B2` |
| `--text3` | `#9AA0A6` | `#6C8280` |
| `--brand` (themed) | `#00B7CA` | `#2FD6E2` (brightened for contrast) |

---

## Typography

Runable ships **no custom webfont** — it uses Tailwind's default `ui-sans-serif, system-ui` stack (system UI sans). Documented stand-in for consistent rendering:

| Role | Family | Notes |
|---|---|---|
| Display / UI / body | **Inter** | Neutral geometric stand-in for the system-ui stack (Google Fonts). |
| Agent log / code / tool calls | **JetBrains Mono** | The agent's step console, file names, and generated code. |

Hierarchy: Inter 600 for the hero question + headings; 400 for body. Mono only in the agent console and artifacts.

---

## Logo

Real Runable **mark** — a rounded-triangular cluster of three lobed shapes (an "atom/gear" motif, viewBox `0 0 737 665`, 3 paths, `fill:currentColor`), pulled verbatim from the live header, themed via `var(--logo-text)`. Paired with the **"Runable"** wordmark in Inter.

**Theming:** mark + wordmark both follow `var(--logo-text)` (near-black on light / near-white on dark) — the brand mark is monochrome.

---

## Components

- **Prompt bar** — the hero input "Type your ideas here…", rounded-2xl, 1px border, with a teal circular send button.
- **Task chips** — `Build Apps`, `Create Slides`, `Generate Videos`, `Build Websites`, `More` — pill buttons; selected = teal tint + teal border.
- **Run button** — teal `--brand`, white text, rounded. Never teal text on the teal button.
- **Agent step** — spinner (teal) → check (mint) with a mono label; the differentiator is the visible plan → tool-call → artifact flow.
- **Badge** — "Loved by 1M+ customers", orange, pill.

---

## Signature — the Runable agent

The product *is* the prompt: "What needs to be done?" Pick a task; the agent plans, runs tools, and produces the artifact.

- **Prompt + task chips**: Build Apps / Create Slides / Generate Videos / Build Websites.
- **Agent console** (left): streams a deterministic plan per task — e.g. Build Apps → `Planning app structure` → `Scaffolding React + Tailwind` → `Writing components` → `Installing dependencies` → `Preview ready`; teal spinners resolve to mint checks.
- **Artifact preview** (right): assembles the deliverable per task — a mini app UI, a slide deck, a video storyboard, or a website hero. Each of the four tasks has its own fixed steps + artifact. Deterministic (index-driven, no `Math.random`).

---

## Guardrails

### DO
- Lead with cyan-teal `#00B7CA`; use the teal→mint gradient for hero/section bands.
- Darken teal to `#047B86` when it must be *text* on white.
- Keep the canvas clean and white; let the agent's work carry the color.
- Frame everything as a **task the agent does** ("What needs to be done?").
- Use mint-green for success/done states.

### DON'T
- Don't treat the Google Sign-In blue `#1a73e8` as a brand color — it's a third-party widget.
- Don't put teal text on the teal button.
- Don't invent agent output — mirror real task types (apps, slides, videos, websites).
- Don't use `Math.random()` in the signature — keep runs deterministic.
