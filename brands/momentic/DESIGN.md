# Momentic — Design System

> Catch real bugs before they ship.
> AI end-to-end testing for web and mobile — write tests in plain English; Momentic builds, runs, and maintains them.

Momentic's identity is **warm and confident**: an off-white paper canvas, near-black ink, a geometric grotesk, and one electric **lime** (`#87F700`) that owns every action. It reads like a modern testing tool with a personality — quiet warm neutrals, one loud accent, mono for anything that is code or a command.

---

## Colors

### Brand
| Token | Hex | Usage |
|-------|-----|-------|
| `lime-500` | `#87F700` | The brand — primary buttons, CTAs, links, active state |
| `lime-600` | `#6FE000` | Gradient end / hover |
| `olive` | `#7F806F` | Muted warm text, hero de-emphasis |

### Surfaces
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `paper` | `#F5F3F2` | `#171716` | App canvas (warm) |
| `card` | `#FBFBFB` | `#1C1C1C` | Cards / panels |
| `subtle` | `#EEECEA` | `#232322` | Wells / rows |
| `border` | `#E1DFDC` | `#33322F` | Hairlines |

### Text
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `ink` | `#1C1C1C` | `#F5F3F2` | Primary |
| `muted` | `#57574F` | `#B4B3AC` | Secondary |
| `faint` | `#7F806F` | `#83837A` | Meta |

### Test state (semantic)
| State | Hex | Meaning |
|-------|-----|---------|
| pass | `#22C55E` | Step / test passed |
| running | `#BD8A2C` | Executing |
| fail | `#C0584F` | Assertion failed · bug caught |
| bug | `#E35A3A` | Real bug found |

The primary button is lime with **black** text — never white text on lime.

---

## Typography

- **Space Grotesk** (≈ **BDO Grotesk**, Momentic's proprietary display face) — headings, UI, body. Google-hosted.
- **Space Mono** (≈ **Basically A Mono**, Momentic's proprietary mono) — CLI commands, code, test steps, selectors, metadata — often set uppercase.

| Role | Face | Spec |
|------|------|------|
| Display | Space Grotesk 500 | 56px, `-0.03em` |
| Heading | Space Grotesk 500 | 20px |
| Body | Inter 400 | 15px |
| Code / CLI | Space Mono 400 | 12–13px, uppercase for CTAs |

---

## Logo

The real Momentic **wordmark** (`viewBox 0 0 114 16`, `currentColor`), pulled verbatim from the live site and colored via `--logo` (near-black on paper, off-white on dark).

---

## Signature component — The plain-English test

Momentic's whole pitch: **you write E2E tests in plain English; the AI runs and maintains them.**

- A test written as natural-language **steps** (`Go to /login`, `Type into the Email field`, `Click "Sign in"`, `Assert the Dashboard is visible`).
- **Run** executes each step in order — running (amber spinner) → passed (green ✓). A mini browser frame reflects the current screen.
- The differentiator: when a selector has drifted, Momentic **self-heals** — a step shows an "AI re-located element" note and still passes. A second flow **catches a real bug**: a step fails red with the assertion diff.

Deterministic — fixed steps, index-driven execution, no `Math.random`.

---

## Guardrails

**Do**
- Keep the canvas warm off-white `#F5F3F2` with near-black ink and one electric `lime-500` for action.
- Put **black** text on the lime button — never white.
- Write test steps and CLI in Space Mono; the CTA reads as an uppercase mono command (`NPX @MOMENTIC/WIZARD@LATEST`).
- Color test state by meaning: green pass, amber running, red fail/bug.

**Don't**
- Use white text on the lime button, or tint the lime toward yellow-green mush — keep it electric `#87F700`.
- Swap the warm paper for a cold grey — the warmth is part of the identity.
- Set test steps or selectors in a proportional sans — they're mono.
- Add a second saturated accent — lime is the only one; the rest is warm neutral + state color.
