# Twilio Design System

## Overview

Twilio is "the platform for conversations in the AI era" — APIs for SMS, RCS, voice, and email, plus conversational AI and identity verification. The identity is anchored by one loud, confident red and the dot-circle bug (four dots inside a ring). It pairs that red with a deep navy "ink," a warm "paper" background, and clean humanist type — developer-first, but warmer and more human than most infrastructure brands.

**Brand personality:** Bold, human, communication-first, developer-grade, reliable.

**Positioning (live copy):** "Build amazing customer experiences on the Twilio platform with APIs for SMS, RCS, voice, and email — the infrastructure behind every magical customer moment."

---

## Colors

Twilio is **light-first** on a warm `#FDF7F4` paper background with white cards and `#000D25` ink text; dark mode is the ink navy. Red is the identity; blue is the interactive/link color.

### Primary — the red
| Token | Hex | Usage |
|-------|-----|-------|
| `--twilio-red` | `#F22F46` | Primary brand, CTAs, the bug |
| `--red-light` | `#EF223A` | Hover, bright red accent |
| `--red-dark` | `#B10F23` | Accessible red for text on light, pressed |

### Secondary — blue
| Token | Hex | Usage |
|-------|-----|-------|
| `--blue` | `#0263E0` | Links, secondary actions |
| `--cyan` | `#3ACEFA` | Bright accent, highlights (dark-mode links) |
| `--night` | `#001489` | Deep blue, emphasis, gradients |

### Surfaces — Light
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#FFFFFF` | Cards, panels |
| `--bg2` | `#FDF7F4` | Page background (warm paper) |
| `--bg3` | `#F5EDE8` | Fills, hover (warm) |
| `--border` | `#E8DFD9` | Borders, dividers (warm) |

### Surfaces — Dark (ink)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#0A1A38` | Cards, panels |
| `--bg2` | `#000D25` | Page background (ink) |
| `--bg3` | `#12244A` | Elevated, hover |
| `--border` | `#1E3157` | Borders, dividers |

### Text
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `--text` | `#000D25` | `#F5F7FA` | Headings, body (ink) |
| `--text2` | `#3D4A5C` | `#9AA8C0` | Labels, secondary |
| `--text3` | `#8A94A6` | `#64748B` | Muted, placeholder |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#0E7C3A` | Delivered, healthy (fill `#36D576`) |
| `--warning` | `#F47C22` | Queued, attention |
| `--danger` | `#F22F46` | Failed, undelivered, delete |

---

## Typography

| Role | Font | Notes |
|------|------|-------|
| Display / headings | **Buffalo** (≈ Source Sans 3, 700) | Buffalo is Twilio-proprietary; headings substitute the humanist body family at heavy weight |
| UI / body | **Whitney SSm** (≈ Source Sans 3) | Whitney is a commercial Hoefler face; Source Sans 3 is the CORS-safe humanist substitute |
| Mono / code | **Twilio Sans Mono** (≈ JetBrains Mono) | API snippets, Message SIDs, phone numbers |

### Scale
| Token | Size | Weight | Sample |
|-------|------|--------|--------|
| `display-2xl` | 52px | 700 | Twilio |
| `display-xl` | 32px | 700 | Build. Without limits. |
| `display-md` | 22px | 600 | Building blocks for every conversation |
| `text-lg` | 16px | 400 | Body / lead copy |
| `text-sm` | 13px | 400 | UI copy, table cells |
| `ui-mono` | 12px | 400 | `client.messages.create(...)` |

---

## Components

- **Buttons:** red `#F22F46` primary (white text, safe in both themes), outline secondary, blue link. Radius `4px`.
- **Message log table:** the Twilio Console Messaging pattern — SID, To, Body, Status badge, Segments, Price.
- **Status badges:** `queued` (orange), `sent` (blue), `delivered` (green), `failed` (red).
- **Code snippet:** dark ink card with language tabs (Node · Python · curl) showing `client.messages.create()`.
- **Inputs:** 1px warm border, `#F22F46` focus ring.

### Radius & elevation
| Token | Value |
|-------|-------|
| `radius-sm` | 4px |
| `radius-md` | 8px |
| `radius-lg` | 16px |
| `shadow-card` | `0 1px 2px rgba(0,13,37,.06), 0 6px 20px rgba(0,13,37,.08)` |

---

## Signature component

**Messaging logs + send.** Twilio's defining developer moment: send a message via the API and watch it move through delivery states. A code card shows `client.messages.create({ to, from, body })`; the composer sends a message that appends a row to the Console-style log with an auto-generated `SM…` Message SID and a status that animates **queued → sent → delivered**, plus segments and price. Log is capped at 20 rows.

Seen with no branding, the `SM…` SIDs and queued→sent→delivered status chips are unmistakably Twilio.

---

## Guardrails

**DO**
- Use Twilio Red `#F22F46` as the one loud primary — for CTAs, the bug, and emphasis.
- Keep the bug (four dots in a ring) monochrome red; render it on paper, white, or ink.
- Use the warm paper `#FDF7F4` for page backgrounds — it's part of the identity.
- Use blue `#0263E0` for links; reserve red for brand and destructive.
- Pair every message status with its colored chip and a real `SM…` SID.

**DON'T**
- Don't use the old flat red `#F30` / random reds — the brand red is `#F22F46`.
- Don't recolor or split the bug's fill — it's a single-color mark.
- Don't use pure black `#000` for text or dark surfaces — Twilio's ink is `#000D25`.
- Don't cool the background to plain white everywhere — keep the warm paper tint.
- Don't fake phone numbers or SIDs into random formats — use `+E.164` and `SM` + hex.
