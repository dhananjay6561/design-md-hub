# Netlify Design System

## Overview

Netlify is the platform to "push your ideas to the web" — build with code or AI and deploy instantly on production infrastructure. The identity is anchored by its teal and the spark/rays wordmark, paired with dark teal-tinted surfaces and clean geometric type. It reads fast, developer-joyful, and modern — build-and-ship in one platform.

**Brand personality:** Fast, developer-joyful, modern, ship-instantly.

**Positioning (live copy):** "Create with AI or code, deploy instantly on production infrastructure. One platform to build and ship."

---

## Colors

Netlify is **light-first** (white cards on a soft `#F4F7F7`) with a dark teal-black mode. Teal is the identity; a deep blue is the secondary accent.

### Primary — teal
| Token | Hex | Usage |
|-------|-----|-------|
| `--teal` | `#00C7B7` | Primary brand, CTAs, Published state, the mark |
| `--teal-bright` | `#14D8D4` | Bright accent, highlights |
| `--teal-light` | `#5DE4C7` | Soft accent, illustration |
| `--teal-deep` | `#014847` | Deep teal, dark accents |

### Secondary
| Token | Hex | Usage |
|-------|-----|-------|
| `--blue` | `#2E51ED` | Links, secondary accent |

### Surfaces — Light
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#FFFFFF` | Cards, panels |
| `--bg2` | `#F4F7F7` | Page background |
| `--bg3` | `#E9F0F0` | Fills, hover |
| `--border` | `#E1E8E8` | Borders, dividers |

### Surfaces — Dark (teal-black)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#13201F` | Cards, panels |
| `--bg2` | `#0D1818` | Page background |
| `--bg3` | `#1C2B29` | Elevated, hover |
| `--border` | `rgba(255,255,255,.09)` | Borders, dividers |

### Text & semantic
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `--text` | `#181A1C` | `#E9F2F1` | Headings, body |
| `--text2` | `#545A61` | `#9DB0AE` | Labels, secondary |
| `--text3` | `#8A9491` | `#6B807E` | Muted, placeholder |
| `--success` | `#00C7B7` | `#00C7B7` | Published, live |
| `--warning` | `#FBB13D` | `#FBB13D` | Building, enqueued |
| `--danger` | `#FE4E5C` | `#FE4E5C` | Failed deploy, error |

---

## Typography

| Role | Font | Notes |
|------|------|-------|
| Display / body | **Mabry Pro** (≈ Manrope) | Mabry Pro is Netlify's commercial brand face; Manrope is the CORS-safe geometric substitute |
| Mono / code | **Roboto Mono** | Deploy IDs, commit SHAs, build log, CLI |

### Scale
| Token | Size | Weight | Sample |
|-------|------|--------|--------|
| `display-2xl` | 52px | 800 | Netlify |
| `display-xl` | 32px | 700 | Push your ideas to the web |
| `display-md` | 22px | 600 | Build your way. Ship on one platform. |
| `text-lg` | 16px | 400 | Body / lead copy |
| `text-sm` | 13px | 400 | UI copy, table cells |
| `ui-mono` | 12px | 400 | `netlify deploy --prod` |

---

## Components

- **Buttons:** teal `#00C7B7` primary (dark ink text — teal is bright), outline secondary, text link. Radius `8px`.
- **Deploys list:** status dot + commit + branch + time — the Netlify Deploys view.
- **Status badges:** `Published` (teal), `Building` (amber), `Failed` (red), `Enqueued` (gray).
- **Build log:** dark surface, mono, streaming stages (Initializing → Building → Deploying → Published).
- **Inputs:** 1px border, `#00C7B7` focus ring.

### Radius & elevation
| Token | Value |
|-------|-------|
| `radius-sm` | 6px |
| `radius-md` | 8px |
| `radius-lg` | 12px |
| `shadow-card` | `0 1px 2px rgba(13,24,24,.06), 0 8px 24px rgba(13,24,24,.08)` |

---

## Signature component

**Deploys + build log.** Netlify's defining moment: push and it's live. The Deploys panel lists deploys (status dot, commit message, branch, time); **Trigger deploy** prepends a new deploy that streams a build log through **Initializing → Building → Deploying**, then flips its status to **Published** in teal. Selecting any deploy loads its log. Lists are capped at 20.

Seen with no branding, the deploys list with the teal "Published" badge and a streaming build log is unmistakably Netlify.

---

## Guardrails

**DO**
- Use teal `#00C7B7` as the one primary — CTAs, the mark, the Published state.
- Use dark ink text on teal buttons — teal is too bright for white text.
- Keep dark surfaces teal-tinted black (`#0D1818`), not neutral gray or navy.
- Use amber for Building and red for Failed — never teal for a non-live state.
- Keep the spark/rays wordmark monochrome (dark on light, white on dark).

**DON'T**
- Don't put white text on the teal button — contrast fails; use ink.
- Don't use teal for anything that isn't live/published/primary.
- Don't tint dark surfaces navy or neutral — Netlify's dark is teal-black.
- Don't set display headings in Roboto Mono — Mabry / Manrope owns headings.
- Don't fake deploy data — use real commit SHAs, branches, and states.
