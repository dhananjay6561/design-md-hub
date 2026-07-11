# incident.io — Design System

> Move fast when you break things.
> The all-in-one AI platform for on-call, incident response, and status pages — built for fast-moving teams.

incident.io's identity is **warm and editorial**: a cream paper canvas, near-black ink, a confident serif display, and one signature coral — internally named **"alarmalade"** (`#F25533`). Playful touches (a handwritten annotation font, pixel accents) keep it human, while the product surfaces stay crisp and status-driven.

---

## Colors

### Brand
| Token | Hex | Usage |
|-------|-----|-------|
| `alarmalade-500` | `#F25533` | The brand coral — primary button, flame mark, links, accents |
| `alarmalade-bright` | `#FF492C` | Hover / emphasis |
| `alarmalade-deep` | `#5A0A17` | Deep maroon — dark coral surfaces |

### Surfaces (light — default)
| Token | Hex | Usage |
|-------|-----|-------|
| `paper` | `#F8F5EF` | App canvas (warm cream) |
| `card` | `#FFFFFF` | Cards / panels |
| `sand` | `#F1EBE2` | Insets / wells |
| `beige` | `#E4D9C8` | Warm dividers / tags |
| `border` | `#E7E1D6` | Hairlines |

### Surfaces (dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `ink` | `#161618` | Canvas |
| `panel` | `#1D1D20` | Cards |
| `raised` | `#26262A` | Rows |
| `border` | `#2E2E32` | Hairlines |

### Text
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `fg` | `#161618` | `#F5F3EE` | Primary |
| `muted` | `#6B675E` | `#A7A399` | Secondary |
| `subtle` | `#9A9488` | `#726E66` | Meta |

### Incident status & severity (semantic)
| State | Hex | Meaning |
|-------|-----|---------|
| triage | `#9A9488` | Just declared |
| investigating | `#E9A23B` | Investigating (amber) |
| identified / fixing | `#F25533` | Cause identified · fixing (coral) |
| monitoring | `#4B73FF` | Watching the fix (blue) |
| resolved | `#10B981` | Resolved (green) |
| SEV1 | `#E50914` | Critical |
| SEV2 | `#FE7B02` | Major |

---

## Typography

- **Newsreader** (≈ **STK Bureau Serif**, incident.io's proprietary display serif — CORS-locked) — hero + editorial headings. Google-hosted.
- **Inter** (≈ **Untitled Sans**, the UI face) — body, labels, buttons, product UI. Google-hosted.
- **Geist Mono** — incident IDs, code, timestamps, channel names.
- **Kalam** — a handwritten annotation face (a real incident.io flourish), used sparingly for margin notes. Google-hosted, used directly.

| Role | Face | Spec |
|------|------|------|
| Display | Newsreader 500 | 56px, `-0.02em` |
| Heading | Inter 600 | 20px |
| Body | Inter 400 | 15px |
| Code / IDs | Geist Mono 400 | 12–13px |
| Annotation | Kalam 400 | 15px, coral |

---

## Logo

The real incident.io **wordmark** — a coral (`alarmalade`) flame mark beside the "incident.io" wordmark (`viewBox 0 0 1000 248`), pulled verbatim from the live site. The flame stays coral (`--logo-flame`); the wordmark text is themed via `--logo-wm` (near-black on cream, cream on ink).

---

## Signature component — The incident

incident.io's core loop: **declare an incident, then drive it to resolution.**

- A header with the incident title, a **severity** badge (SEV2), and the current **status** pill.
- Details: Incident Lead, Comms Lead, affected component, and the channel (`#inc-7450-…`) in mono.
- A **timeline** of updates — each with an actor, a mono timestamp, and a message — plus a handwritten Kalam annotation for a human touch.
- **Advance status** walks the lifecycle: Investigating → Identified → Monitoring → Resolved, appending a timeline entry and recoloring the status pill at each step. On resolution it prints the total duration.

Deterministic — fixed frames, index-driven, no `Math.random`.

---

## Guardrails

**Do**
- Keep the canvas warm cream `#F8F5EF` (or ink `#161618`) with near-black text and one coral `alarmalade` accent.
- Set the hero and editorial headings in the serif; keep product UI in Inter.
- Color incident status by meaning: amber investigating, coral fixing, blue monitoring, green resolved.
- Use Geist Mono for incident IDs, channels, and timestamps; a light Kalam annotation is on-brand.

**Don't**
- Swap the warm cream for a cold grey — the paper tint is part of the identity.
- Use a second saturated accent alongside coral — the spectrum beyond it is status-only.
- Set incident IDs or timestamps in a proportional sans — they're mono.
- Recolor the flame — it's always `alarmalade` coral.
