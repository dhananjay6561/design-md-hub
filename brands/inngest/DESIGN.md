# Inngest — Design System

> Durable execution for workflows & AI.

Inngest is a durable execution engine: you write ordinary functions, split them into **steps**, and Inngest guarantees each step runs to completion — with automatic retries, flow control, and step-level observability, no queues or extra infrastructure to run. A function is triggered by an **event**; each `step.run` / `step.sleep` / `step.waitForEvent` is independently checkpointed and memoized, so a crash resumes exactly where it left off.

The identity is a calm, near-monochrome **carbon** neutral canvas with one confident **matcha** green as the primary action and success signal, set in Lineto's **CircularXX** geometric sans. It reads as infrastructure you trust: precise, quiet, and legible under a wall of run traces.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| matcha-600 | `#027A48` | Primary button, completed step, links (light) |
| matcha-500 | `#2C9B63` | Success / completed step (dark), accent |
| matcha-400 | `#66BD8B` | Bright accent, timeline connectors on dark |
| matcha-100 | `#DFF5E6` | Success tint / step background |

### Semantic (from the product design system)
| Token | Hex | Usage |
|---|---|---|
| honey-300 | `#FCC43F` | Running / in-progress step, warnings |
| honey-500 | `#D56B13` | Throttled / retry-scheduled |
| breeze-500 | `#2389F1` | Info · `sleep` & `waitForEvent` steps |
| ruby-500 | `#F54A3F` | Failed attempt / error (dark) |
| ruby-600 | `#CB2A1D` | Failed attempt / error (light) |

### Surfaces (dark-first)
| Token | Dark | Light | Usage |
|---|---|---|---|
| canvas | `#0A0B0D` | `#FEFEFE` | App background |
| panel | `#121212` | `#FFFFFF` | Cards, code & trace panels |
| subtle | `#181818` | `#F6F6F6` | Muted rows, code gutter |
| raised | `#1E1E1E` | `#F0F0F0` | Hover / selected step |
| border | `#2A2A2A` | `#E2E2E2` | Hairlines (carbon-100/-800) |

### Text (carbon)
| Token | Dark | Light |
|---|---|---|
| primary | `#F6F6F6` | `#121212` |
| secondary | `#B0B0B0` | `#4B4B4B` |
| faint | `#7C7C7C` | `#7C7C7C` |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / headings | **CircularXX** (`600 / 700`) | Lineto geometric sans — Inngest's core face. Self-hosted, CORS-open; loaded straight from `fonts-cdn.inngest.com`. |
| UI / body | **CircularXX** (`400 / 500`) | Product UI, body, labels, step names, buttons. Fallback: Inter. |
| Code / mono | **CircularXXMono** | SDK source, event names, step IDs, durations, run metadata. Fallback: JetBrains Mono. |

Scale: hero 50px (CircularXX 700), section 22px, step name 13.5px, code 12.5px mono, body 14.5px, labels 11px uppercase (`.08em` tracking).

---

## Shape, spacing & motion

- **Radius:** cards & panels `12px`, code/trace window `14px`, step rows `9px`, buttons `8px`, status chips/pills `9999px`. Modern, softly rounded.
- **Spacing:** 8px grid; step rows stack with a hairline connector (a vertical rail down the status glyphs) so a run reads top-to-bottom as a timeline.
- **Elevation:** panels float on one soft shadow; inside, step rows are flat, separated by the timeline rail. A running step gets a pulsing amber glyph; the active step gets a matcha left-tint — no heavy shadows.
- **Motion:** mechanical and legible. Steps transition `queued → running → completed`; a failed attempt flips to ruby then a retry re-runs it (the durable-execution signature); `sleep` fast-forwards a countdown; `waitForEvent` resolves when its event arrives. Everything is deterministic — no randomness.

---

## Components

- **Step row** — the atom: a status glyph on the timeline rail, a step ID (`create-stripe-customer`), a type badge (`step.run` / `step.sleep` / `step.waitForEvent`), and a duration. States: queued (gray), running (amber, pulsing), completed (matcha ✓), failed (ruby ✕), sleeping/waiting (breeze blue).
- **Run trace** — the flagship view: a triggering **event pill** at the top, then the ordered steps as a vertical timeline, ending in a run summary (`Completed · 5 steps · 1 retry · 3.4s`).
- **Event pill** — a mono chip naming the trigger event (`user/signed.up`) with its payload id.
- **Retry marker** — under a step: `Attempt 1 failed · 429 · retrying in 2s` → the step re-runs and succeeds; the retry count surfaces in the summary.
- **Buttons / chips** — solid matcha primary (white text); ghost secondary with a carbon border; mono status pills.

---

## Guardrails

**Do**
- Model work as **steps** on a **timeline** — a run is an ordered trace, not a single opaque spinner.
- Keep the canvas near-monochrome carbon and let one **matcha** green carry primary action and success.
- Color steps by state: matcha completed, amber running, ruby failed, breeze for `sleep`/`waitForEvent`.
- Show durability out loud — a failed attempt that **retries and succeeds**, a `sleep` that resumes, a `waitForEvent` that wakes on its event.
- Use real SDK vocabulary: `createFunction`, `event`, `step.run`, `step.sleep`, `step.waitForEvent`, `retries`.
- Set code, event names, step IDs and durations in CircularXXMono.

**Don't**
- Reduce a run to one status — the point is per-step observability.
- Add a second bright brand hue; matcha is the accent, the rest are functional state colors.
- Use heavy shadows or large consumer radii — Inngest is quiet infrastructure, tightly rounded.
- Set body or code in the display weight, or hide retries — durability is the story, show it.
