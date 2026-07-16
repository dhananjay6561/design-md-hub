# Momentic — Design System

> Catch real bugs before they ship.
> AI end-to-end testing for web and mobile — write tests in plain English; Momentic runs them everywhere and keeps them up to date.

Momentic's identity is **warm and confident**: a warm off-white paper canvas, near-black ink, the proprietary **BDO Grotesk** grotesk, and one electric **lime** (`#87F700`) used as punctuation — eyebrows, accent CTAs, live counters, and the ▶ triangle. Anything that is code, a command, a selector, or a stat is set in **Basically A Mono**.

The primary action is **ink** (`#1C1C1C`), not lime — lime is the loud accent, ink is the workhorse button.

---

## Colors

### Brand / accent
| Token | Hex | Usage |
|-------|-----|-------|
| `accent` | `#87F700` | The lime — accent CTAs, mono eyebrows, live stat numbers, ▶ triangle, focus ring |
| `accent-hover` | `#79E000` | Accent button hover |
| `accent-active` | `#6FCE00` | Accent button active |
| `accent-pulse` | `#6FE000` | Pulse / gradient end |
| `olive` | `#7F806F` | Border + muted warm text (`--border` is olive; tinted via `rgb(127 128 111 / α)`) |

### Surfaces
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `bg` | `#F5F3F2` | `#171716` | App canvas (warm paper) |
| `bg-100` | `#FAFAF9` | `#1A1A19` | Alt canvas |
| `raised` | `#FBFBFB` | `#1C1C1C` | Cards / panels |
| `illus-surface` | `#EEECEA` | `#232322` | Preview canvas / wells |
| `border` | `#7F806F @ .12–.16` | translucent | Hairlines (olive tint) |

### Text
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `ink` | `#1C1C1C` | `#F5F3F2` | Primary |
| `muted` | `#57574F` | `#B4B3AC` | Secondary |
| `faint` | `#7F806F` | `#83837A` | Meta |

### Buttons
| Token | Hex | Usage |
|-------|-----|-------|
| `btn-primary-bg` | `#1C1C1C` | Primary button (ink), hover `#333` |
| `btn-accent-bg` | `#87F700` | Accent button (lime), **black text always** |
| `btn-secondary` | olive `@ .06` | Secondary button, hover olive `@ .12` |

### Test state (semantic — the product's real tokens)
| State | Hex | Meaning |
|-------|-----|---------|
| pass | `#3A9460` | Step / test passed (`--prev-pass`) |
| running / warn | `#BD8A2C` | Executing (`--prev-warn`) |
| fail / error | `#C0584F` | Assertion failed · bug caught (`--prev-fail` / `--error`) |
| diff add | `#E6F1E9` | Expected value (green well) |
| diff del | `#F8E9E7` | Received value (red well) |

The accent button uses **black** text — never white on lime.

---

## Typography

Both faces are Momentic's own, self-hosted, and **CORS-open** (`access-control-allow-origin: *`) — used directly from `momentic.ai/fonts/`, no fallback needed.

- **BDO Grotesk** — display, headings, UI, body (`--h-ff` and `--l-ff` are both BDO Grotesk). Weights Regular 400 / Medium 500 / DemiBold 600.
- **Basically A Mono** — CLI commands, code, test steps, selectors, eyebrows, metadata, stat numbers — often set uppercase. Weights Regular 400 / Medium 500 / Bold 700.

| Role | Face | Spec |
|------|------|------|
| Display | BDO Grotesk 500 | 56px, `-0.035em` |
| Heading | BDO Grotesk 500 | 20px |
| Body | BDO Grotesk 400 | 15px |
| Code / CLI / eyebrow | Basically A Mono | 11–13px, uppercase for labels & CTAs |

Hero highlight ("real bugs") is set in **olive `#7F806F`** (`--h-span`), not lime.

---

## Logo

The real Momentic **wordmark + bracket mark** (`viewBox 0 0 1280 179`, 10 paths, `fill="currentColor"`), pulled verbatim from the live nav and colored via `--logo` (near-black on paper, off-white on dark).

---

## Signature component — The Momentic run

Momentic's whole pitch: **you write E2E tests in plain English; the AI runs and maintains them across web and mobile.**

- A test written as natural-language **steps** (`GO TO /login`, `TYPE ada@acme.com`, `CLICK Sign in`, `ASSERT Dashboard visible`) beside a **device preview** that reflects the current screen.
- A **Web ⟷ iOS** platform toggle — Web flows render a browser frame, the mobile flow renders an iOS phone frame (Momentic tests web *and* mobile).
- **Run** executes each step in order — running (amber spinner) → passed (green ✓) — with a live counter of steps, **auto-heals**, and elapsed time.
- The differentiators, both first-class: when a selector drifts, a step **auto-heals** (lime ⚡ badge, "AI re-located element", still passes and bumps the auto-heal counter — Momentic has run 8.9M+ of these). The Checkout flow **catches a real bug**: a step fails red and an **assertion diff** panel expands with expected (green) vs received (red).

Deterministic — fixed flows, index-driven execution, no `Math.random`.

**Real numbers from the live site** (usable in specimens): 70,607,819 test runs executed · 77,813 tests created · 8,932,104 auto-heals · 80,290 PRs verified · 96% signal-to-noise ratio.

---

## Guardrails

**Do**
- Keep the canvas warm off-white `#F5F3F2` with near-black ink; use one electric `lime #87F700` as *punctuation* (eyebrows, accent CTA, live counters, ▶).
- Make the **primary** button ink `#1C1C1C`; use lime only for the accent CTA, and put **black** text on it.
- Set test steps, selectors, CLI, eyebrows, and stat numbers in Basically A Mono; the install command reads as an uppercase mono command (`NPX @MOMENTIC/WIZARD@LATEST`).
- Color test state by meaning: green `#3A9460` pass, amber `#BD8A2C` running, red `#C0584F` fail/bug.

**Don't**
- Make lime the primary button, or put white text on lime — ink is primary; lime text is black.
- Swap the warm paper for a cold grey — the warmth is part of the identity.
- Set test steps or selectors in a proportional sans — they're Basically A Mono.
- Add a second saturated accent — lime is the only one; the rest is warm neutral + state color.
