# Trigger.dev — Design System

> Build and deploy fully-managed AI agents and workflows.

Trigger.dev is the open-source platform for building AI workflows in TypeScript — long-running tasks with **retries, queues, observability, and elastic scaling**. You write a `task()` in your codebase; Trigger.dev runs it durably, survives redeploys and crashes, and shows you every attempt on a run timeline.

The identity is a **deep charcoal canvas** cut by one electric **apple-green** (`#A8FF53`), a lavender secondary, and a full run-state spectrum. Satoshi sets the display voice; Geist and Geist Mono carry the product and its code.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| apple | `#A8FF53` | Primary accent — CTA, completed runs, brand mark |
| lavender | `#7655FD` | Secondary — executing state, links, gradient partner |
| logo gradient (Trigger) | `#41FF54 → #E7FF52` | Green wordmark gradient |
| logo gradient (.dev) | `#2563EB → #A855F7` | Blue→purple `.dev` gradient |

### Surfaces — charcoal scale (dark-first; the product is dark)
| Token | Hex | Usage |
|---|---|---|
| charcoal-950 | `#0D0E12` | Deepest background |
| charcoal-900 | `#121317` | App canvas |
| charcoal-850 | `#15171A` | Panels |
| charcoal-800 | `#1A1B1F` | Raised surface |
| charcoal-750 | `#212327` | Hover / rows |
| charcoal-700 | `#272A2E` | Borders |
| charcoal-600 | `#3B3E45` | Strong borders |

### Text (charcoal)
| Token | Hex | Usage |
|---|---|---|
| charcoal-100 | `#E8E9EC` | Primary |
| charcoal-300 | `#B5B8C0` | Secondary |
| charcoal-400 | `#878C99` | Muted |
| charcoal-500 | `#5F6570` | Faint |

### Run-state spectrum (the observability signal)
| Token | Hex | Meaning |
|---|---|---|
| apple | `#A8FF53` | Completed |
| lavender | `#7655FD` | Executing |
| rose | `#F43F5E` | Failed |
| sun | `#ECCF06` | Waiting / delayed |
| aqua | `#479DEC` | Info / queued |
| barbie | `#FA3ABF` | Extra category |

---

## Typography

| Role | Font | Notes |
|---|---|---|
| Display / headings | **Satoshi** (`font-title`) | Self-hosted on trigger.dev, **CORS-open** — used directly |
| UI / body | **Geist** (`font-sans`) | Google-hosted here (trigger.dev CDN is CORS-locked) |
| Code / logs | **Geist Mono** (`font-mono`) | Task code, run logs, IDs |

Hero and section headings are Satoshi semibold; everything else is Geist. Code, run IDs, timestamps and logs are Geist Mono.

---

## Logo

The `Trigger.dev` wordmark (viewBox `0 0 751 130`) — "Trigger" in a green gradient (`#41FF54 → #E7FF52`), `.dev` in a blue→purple gradient (`#2563EB → #A855F7`). Self-contained SVG with its own gradient defs; used verbatim.

---

## Signature component — the task run

If you saw only this, you'd know it was Trigger.dev: a real `task()` definition beside its **run timeline** — a waterfall of spans (trigger → `transcode` attempt 1 **fails** → retry **completes** → `wait.for` 30s → `store.put` → done) with a live log stream. Each span is colored by run state. Hit **Replay run** and it executes: the run goes EXECUTING, an attempt fails rose, a retry succeeds, the wait fast-forwards, and the run completes apple-green.

- Left: real `@trigger.dev/sdk` task (`task({ id, retry, run })`, `wait.for`, `logger`) in Geist Mono
- Right: run header (run id · status · duration · attempts) + span waterfall + logs
- Deterministic frames (no `Math.random`)

---

## Guardrails

**Do**
- Keep the canvas deep charcoal `#121317`; reserve **apple-green** for the CTA, brand, and completed state.
- Color runs by state — apple completed, lavender executing, rose failed, sun waiting.
- Show tasks as **code** and runs as a **timeline** — durable execution + observability is the whole thesis.
- Set headings in Satoshi; body in Geist; code and IDs in Geist Mono.

**Don't**
- Add a second bright brand accent — apple carries it; the rest are run-state only.
- Put run logs or code in the sans — logs are Geist Mono.
- Use a light canvas for the run view — the console is charcoal in both themes.
- Invent state colors; use the charcoal + apple/lavender/rose/sun spectrum.
