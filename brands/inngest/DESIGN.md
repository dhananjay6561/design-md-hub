# Inngest — Design System

> Durable execution for workflows & AI.

Inngest is a durable execution engine: you write ordinary functions, split them into **steps**, and Inngest guarantees each step runs to completion — with automatic retries, flow control, and step-level observability, no queues or workers to run. A function is triggered by an **event**; each `step.run` / `step.sleep` / `step.waitForEvent` is independently checkpointed and memoized, so a crash resumes exactly where it left off.

The identity is bold and editorial: a **dark, near-black textured canvas** scattered with orange-red embers, oversized grotesque display type (some words set as hollow outlines), and one hot **flame** accent — `#F75536`. The voice is blunt and confident ("Unbreakable agents." · "Invisible infra." · "No workers. No queues. No refactoring."). Green, amber and blue are not brand colors — they're the functional **step-state** signals borrowed from the product's run dashboard.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| flame | `#F75536` | Primary brand accent — CTAs, links, logo, `step` markers, active state |
| coral | `#FF8C80` | Light tint / secondary accent on dark, gradient partner |
| ember | `#FF7A5C` | Hover / bright highlight |
| deep | `#E0402E` | Pressed / deeper flame |
| flame gradient | `#F75536 → #FF8C80` | Logo mark, hero glow, marquee accents |

### Step-state semantics (from the run dashboard — functional, not brand)
| Token | Hex | Usage |
|---|---|---|
| completed | `#2C9B63` (dark) · `#027A48` (light) | Completed step ✓ (Inngest "matcha" green) |
| running | `#FCC43F` (dark) · `#D56B13` (light) | In-progress step, pulsing |
| waiting | `#4FA9F5` (dark) · `#1365D6` (light) | `sleep` & `waitForEvent` steps (breeze) |
| failed | `#FF6B5E` (dark) · `#CB2A1D` (light) | Failed attempt / error (ruby) |

### Surfaces (dark-first — the brand canvas is black)
| Token | Dark | Light | Usage |
|---|---|---|---|
| canvas | `#0A0A0A` | `#FBFAF9` | App background (dark is textured with embers) |
| panel | `#141414` | `#FFFFFF` | Cards, code & trace panels |
| subtle | `#1A1A1A` | `#F4F3F2` | Muted rows, code gutter |
| raised | `#1F1F1F` | `#EFEEED` | Hover / selected step |
| border | `#282828` | `#E6E4E2` | Hairlines |

### Text
| Token | Dark | Light |
|---|---|---|
| primary | `#F7F7F7` | `#0A0A0A` |
| secondary | `#B0B0B0` | `#4B4B4B` |
| faint | `#7C7C7C` | `#7C7C7C` |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / headings | **CircularXX** (`700`) | Lineto geometric sans — Inngest's core face. Oversized, tight tracking; hero words are sometimes set as hollow outlines. Self-hosted, CORS-open, loaded straight from `fonts-cdn.inngest.com`. |
| UI / body | **CircularXX** (`400 / 500`) | Product UI, body, labels, step names, buttons. Fallback: Inter. |
| Code / mono | **CircularXXMono** | SDK source, event names, step IDs, durations, the blunt uppercase marquee (`NO WORKERS · NO QUEUES`). Fallback: JetBrains Mono. |

Scale: hero 52–64px (CircularXX 700), section 22px, step name 13.5px, code 12.5px mono, body 14.5px, mono marquee/labels 11px uppercase (`.08em` tracking).

---

## Shape, spacing & motion

- **Radius:** cards & panels `12px`, code/trace window `14px`, step rows `9px`, buttons `8px`, status chips/pills `9999px`. The signature `step` marker is a small **square** (`2px`), not a dot — it's the brand's bullet.
- **Spacing:** 8px grid; step rows stack with a hairline connector (a vertical rail down the status glyphs) so a run reads top-to-bottom as a timeline.
- **Elevation:** on the dark canvas, panels sit on near-black with a subtle flame glow behind the hero; step rows are flat, separated by the timeline rail. No heavy consumer shadows.
- **Motion:** mechanical and legible. Steps transition `queued → running → completed`; a failed attempt flips to red then a retry re-runs it (the durable-execution signature); `sleep` fast-forwards a countdown; `waitForEvent` resolves when its event arrives. Everything is deterministic — no randomness.

---

## Components

- **Step row** — the atom: a status glyph on the timeline rail, a step ID (`create-stripe-customer`), a type badge (`step.run` / `step.sleep` / `step.waitForEvent`), and a duration. States: queued (gray), running (amber, pulsing), completed (green ✓), failed (red ✕), sleeping/waiting (blue).
- **Run trace** — the flagship view: a triggering **event pill** at the top, then the ordered steps as a vertical timeline, ending in a run summary (`Completed · 5 steps · 1 retry · 3.4s`).
- **Event pill** — a mono chip naming the trigger event (`user/signed.up`) with a flame square and its payload id.
- **Retry marker** — under a step: `Attempt 1 failed · 429 · retrying in 2s` → the step re-runs and succeeds; the retry count surfaces in the summary.
- **`step` marker** — a small flame **square** prefixing `step.run()` in marketing/code contexts. It's the brand bullet.
- **Buttons / chips** — solid **flame** primary (white text); ghost secondary with a hairline border; mono status pills.

---

## Guardrails

**Do**
- Anchor on a **dark, near-black** canvas with one hot **flame** (`#F75536`) accent — bold and editorial, not soft.
- Model work as **steps** on a **timeline** — a run is an ordered trace, not one opaque spinner.
- Set display type oversized in CircularXX; lean into the blunt voice (`Unbreakable agents.`, `No workers. No queues.`).
- Keep green/amber/blue strictly as **step-state** signals — they are functional, never brand chrome.
- Show durability out loud — a failed attempt that **retries and succeeds**, a `sleep` that resumes, a `waitForEvent` that wakes on its event.
- Use real SDK vocabulary: `createFunction`, `event`, `step.run`, `step.sleep`, `step.waitForEvent`, `retries`; prefix steps with the flame **square**.

**Don't**
- Make green (the completed-step color) the brand accent — the brand is flame on black.
- Reduce a run to one status — the point is per-step observability.
- Use heavy shadows or large consumer radii, or a light/pastel canvas as the primary identity — Inngest is dark and confident.
- Set body or code in the display weight, or hide retries — durability is the story.
