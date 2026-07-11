# Checkly — Design System

> The active reliability layer for developers & agents.

Checkly is a monitoring platform built to be operated by developers and agents — **Monitoring as Code**: you define API and browser checks as TypeScript constructs, run them from locations around the world, and get a clear signal of application health. The identity is a **deep navy canvas** lit by one **electric Checkly blue**, with an Inter UI and a JetBrains-Mono / Dracula code voice.

It reads as an engineering instrument: dark, precise, signal-over-noise — the check result, the latency curve, and the pass/fail heartbeat are the whole story.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| checkly-blue | `#0075FF` | Primary accent — links, primary button, active check, logo mark |
| blue-600 | `#036CED` | Hover / pressed |
| blue-deep | `#1D4ED8` | Secondary blue, chart line |

> Note: Checkly is **blue**, not purple — verified against the live site. Don't use a purple accent.

### Surfaces (dark-first — the marketing & product canvas is deep navy)
| Token | Dark | Light | Usage |
|---|---|---|---|
| canvas | `#041734` | `#F8F9FB` | App background |
| panel | `#071F42` | `#FFFFFF` | Cards, panels |
| raised | `#0E2A54` | `#EEF4FB` | Hover / secondary surface |
| border | `#163157` | `#E5E7EB` | Hairlines |
| border-strong | `#24436E` | `#D3DCE6` | Inputs, stronger dividers |

### Text
| Token | Dark | Light |
|---|---|---|
| primary | `#EAF1F8` | `#041734` |
| secondary | `#A7BABE` | `#454F52` |
| faint | `#6B8296` | `#6B7A85` |

### Semantics — check state
| Token | Hex | Usage |
|---|---|---|
| passing | `#20DF6F` | Passing check / healthy region |
| failing | `#FF5C5C` | Failed check / down region |
| degraded | `#FFB86C` | Degraded response time |
| running | `#0075FF` | Check in progress |

### Code — Dracula (Checkly's documented code theme)
| Token | Hex |
|---|---|
| code-bg | `#0B1B34` |
| foreground | `#F8F8F2` |
| keyword (pink) | `#FF79C6` |
| string (green) | `#50FA7B` |
| function (cyan) | `#8BE9FD` |
| constant (purple) | `#BD93F9` |
| number (orange) | `#FFB86C` |
| comment | `#6272A4` |

---

## Typography

| Role | Font | Notes |
|---|---|---|
| UI / body / display | **Inter** | `--font-inter` — the whole product & marketing UI |
| Code / monitoring-as-code | **JetBrains Mono** | Check constructs, CLI, metrics |

Both are Google-hosted and used directly. Inter carries display and body — Checkly has no separate display face; hierarchy comes from weight and size. The `active` word in the hero is set in `checkly-blue`.

---

## Logo

The Checkly wordmark (`Checkly`, viewBox `0 0 100 30`) in `--logo-wm`, with a single `checkly-blue` accent glyph. On the navy canvas the wordmark is white; on light it's navy. The accent mark stays `#0075FF`.

---

## Signature component — the check monitor

If you saw only this, you'd know it was Checkly: a **Monitoring-as-Code** editor (a real `ApiCheck` construct) beside its live result — a **global latency chart**, a **region grid** (N. Virginia / Frankfurt / Singapore / São Paulo), and the iconic **pass/fail heartbeat bar**. Hit **Run check** and it executes: status flips to Running, a region briefly degrades and recovers, latency re-plots, and a fresh tick appends to the heartbeat.

- Left: TS `ApiCheck` construct with Dracula highlighting (real `checkly/constructs` API)
- Right: latency area chart + per-region latency/status + heartbeat timeline
- Deterministic frames (no `Math.random`) so screenshots are stable

---

## Guardrails

**Do**
- Keep the canvas deep navy `#041734` with one electric `checkly-blue` for action and active state.
- Show checks as **code** — Monitoring as Code is the product's whole thesis.
- Color check state by meaning: green passing, red failing, orange degraded.
- Report real global regions and latency; the heartbeat bar is the signal.

**Don't**
- Use a purple accent — Checkly is blue. (Correct the old "purple monitoring" assumption.)
- Add a second bright accent — blue carries the brand; green/red/orange are state-only.
- Render checks as opaque config UI without the code — that erases the differentiator.
- Set code in the UI sans — code is JetBrains Mono in the Dracula palette.
