# Firebase Design System

## Overview

Firebase is Google's app development platform — "make your app the best it can be with Firebase and generative AI." The identity is anchored by the flame mark: a warm gradient of yellow → orange → red that signals energy and speed, paired with Google's neutral grays and Google Blue. It's friendlier and more colorful than most developer tools, and it sits firmly inside the wider Google / Material design language.

**Brand personality:** Fast, warm, full-stack, approachable, Google-backed.

**Positioning (live copy):** "Google's mobile and web app development platform that helps developers build apps and games that users will love."

---

## Colors

Firebase is **light-first** on the marketing surface (white and `#ECEFF1` on `#202124` text) with a Google-gray dark theme. The flame is the identity; Google Blue is the interactive/secondary color.

### Primary — the flame
| Token | Hex | Usage |
|-------|-----|-------|
| `--fb-amber` | `#FFCA28` | Primary brand highlight, flame core |
| `--fb-yellow` | `#FFC400` | Flame top, warm accent |
| `--fb-orange` | `#FF9100` | Flame mid, CTA hover |
| `--fb-orange-deep` | `#F57C00` | Deep orange, emphasis |
| `--fb-coral` | `#FF8A65` | Soft coral accent, illustration |
| `--fb-red` | `#DD2C00` | Flame base, danger, delete |

### Secondary — Google Blue
| Token | Hex | Usage |
|-------|-----|-------|
| `--g-blue` | `#1A73E8` | Links, interactive, primary buttons |
| `--g-blue-bright` | `#4285F4` | Focus, selected, accent |
| `--g-blue-light` | `#039BE5` | Info, secondary highlight |

### Surfaces — Light
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#FFFFFF` | Cards, panels |
| `--bg2` | `#ECEFF1` | Page background (Blue Grey 50) |
| `--bg3` | `#E1F3FC` | Selected / info fill |
| `--border` | `#CFD8DC` | Borders, dividers |

### Surfaces — Dark (Google grays)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#292A2D` | Cards, panels |
| `--bg2` | `#202124` | Page background (Google dark) |
| `--bg3` | `#35363A` | Elevated, hover |
| `--border` | `#3C4043` | Borders, dividers |

### Text
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `--text` | `#202124` | `#E8EAED` | Headings, body |
| `--text2` | `#5F6368` | `#9AA0A6` | Labels, secondary |
| `--text3` | `#80868B` | `#5F6368` | Muted, placeholder |

---

## Typography

| Role | Font | Notes |
|------|------|-------|
| Display / headings | **Google Sans** (≈ DM Sans) | Google Sans is Google-proprietary; DM Sans is the CORS-safe free substitute |
| UI / body | **Roboto** | Firebase's actual body font — Google Fonts |
| Mono / code | **Roboto Mono** | Console values, field types, code — Google Fonts |

### Scale
| Token | Size | Weight | Sample |
|-------|------|--------|--------|
| `display-2xl` | 52px | 700 | Firebase |
| `display-xl` | 32px | 600 | Build apps users love |
| `display-md` | 22px | 500 | Easy to integrate on iOS, Android, and the Web |
| `text-lg` | 16px | 400 | Body / lead copy |
| `text-sm` | 13px | 400 | UI copy, table cells |
| `ui-mono` | 12px | 400 | `users/uid_8f3a/displayName` |

---

## Components

- **Buttons:** Google Blue `#1A73E8` primary (white text, safe in both themes), tonal secondary, text button. Radius `4px` (Material).
- **Product cards:** icon + title + description — the Firebase console product grid.
- **Data browser:** the Cloud Firestore three-panel viewer — collections → documents → fields.
- **Field-type chips:** `string`, `number`, `boolean`, `timestamp`, `map`, `array` in Roboto Mono.
- **Inputs:** 1px border, `#1A73E8` focus ring at 2px.

### Radius & elevation
| Token | Value |
|-------|-------|
| `radius-sm` | 4px |
| `radius-md` | 8px |
| `radius-lg` | 12px |
| `shadow-card` | `0 1px 2px rgba(60,64,67,.1), 0 2px 6px rgba(60,64,67,.08)` |

---

## Signature component

**Cloud Firestore data explorer.** The Firebase console's most recognizable view: three panels — collections on the left, documents in the middle, the selected document's fields on the right. Click a collection to load its documents; click a document to inspect its fields with real Firestore field types. Lists are capped at 20 rows.

Seen with no branding, the collection → document → field panel with `string` / `timestamp` / `map` type chips is unmistakably Firestore.

---

## Guardrails

**DO**
- Keep the flame a warm gradient (yellow `#FFC400` → orange `#FF9100` → red `#DD2C00`) — that trio is the identity.
- Use Google Blue `#1A73E8` for interactive elements; reserve the flame colors for brand and warm accents.
- Sit inside Material: 4px base radius, Google grays, Roboto for UI.
- Use `#202124` (not pure black) for text and dark surfaces.
- Pair every field with its type chip in the data browser.

**DON'T**
- Don't recolor the flame or flatten it to a single hue — it's a three-color gradient mark.
- Don't use the flame red `#DD2C00` for links — links are Google Blue.
- Don't set display headings in Roboto Mono or the body font — Google Sans / DM Sans owns headings.
- Don't use pure black `#000` — Google's neutral is `#202124`.
- Don't fabricate metrics — use real Firebase product names and field types.
