# Arc — Design System

Design-token reference for **Arc** (arc.net), the browser from **The Browser Company**. All values live-fetched from `arc.net` and its `_next` CSS/HTML (July 2026). Arc's identity is a **warm cream canvas**, a friendly rounded display face (**Marlin**), an **indigo `#3139FB`** primary, and a **playful multi-color accent spectrum** used for Spaces and gradients. It's a calm, personal, colorful browser — not a corporate blue.

---

## Brand voice

- Hero name: **Arc** (from The Browser Company).
- Positioning (real meta): *"Experience a calmer, more personal internet in this browser designed for you. Let go of the clicks, the clutter, the distractions with the Arc browser."*
- Real headline on site: *"Arc is the Chrome replacement I've been waiting for."*
- Product vocabulary: **Spaces · Sidebar · Command Bar · Split View · Easels · Boosts · Little Arc · Pinned Tabs**.
- Tone: warm, human, a little whimsical.

---

## Typography

Arc self-hosts its fonts; the two that matter are **Marlin Soft Basic** (rounded display) and **Inter** (body), with **Space Mono** for mono. Marlin is served CORS-open (`access-control-allow-origin: *`) so it's used directly.

| Role | Family | Source | Usage |
|------|--------|--------|-------|
| Display | **Marlin Soft Basic** (`marlin.woff2`) | arc.net/fonts (CORS ✅) | Hero, headings — friendly rounded grotesque |
| Body / UI | **Inter** | Google Fonts (CORS ✅) — mirrors Arc's self-hosted Inter | Body, labels, tabs, buttons |
| Mono | **Space Mono** | Google Fonts (CORS ✅) — real Arc mono | URLs, shortcuts, metadata |

Marlin ships primarily Regular/Italic; keep display weight light-to-regular (its roundness carries the personality, not heavy weights).

---

## Color

Warm cream in light, indigo-tinted near-black in dark, with one indigo primary and a categorical accent spectrum (the colors that theme Spaces and gradients).

### Surfaces
| Token | Hex | Usage |
|-------|-----|-------|
| `cream` | `#FFFCEA` | Page background (light) — warm paper |
| `cream-2` | `#FFFADD` | Cards / raised (light) |
| `cream-3` | `#FEF4D5` | Fills, hover (light) |
| `paper-blue` | `#F0F1FF` | Cool tint panel |
| `ink` | `#17161C` | Page background (dark) |
| `ink-2` | `#201E28` | Raised (dark) |
| `ink-3` | `#2A2833` | Fill / border (dark) |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `text` (light) | `#17161C` | Primary |
| `text-2` | `#57545F` | Secondary |
| `text-3` | `#8A8794` | Muted |
| `text` (dark) | `#FFFCEA` | Primary on ink (warm white) |

### Accent & spectrum
| Token | Hex | Usage |
|-------|-----|-------|
| `arc-indigo` | `#3139FB` | Primary — links, buttons, active tab |
| `indigo-deep` | `#2702C2` / `#2404AA` | Pressed / gradient anchor |
| `amber` | `#FFB223` | Space theme / accent |
| `coral` | `#FF5060` | Space theme / accent |
| `red` | `#FB3A4D` | Error / accent |
| `pink` | `#F19E9C` | Space theme / accent |
| `orange` | `#F0B167` | Space theme / accent |
| `sky` | `#96C4FF` | Space theme / accent |
| `periwinkle` | `#C6C8F9` | Space theme / accent |

Spaces are themed with **gradients** built from adjacent spectrum colors (e.g. indigo→sky, coral→amber, pink→orange). Gradients are core to Arc — use them for Space headers, never for body text.

---

## Logo

The Arc mark (Simple Icons `arc`, viewBox `0 0 24 24`, single path — the interlocking-loops glyph). Real Arc renders it with a **colorful gradient**; here it's filled with an indigo→coral→amber gradient across the real spectrum. The glyph shape is fixed; only the fill is brand-flexible.

---

## Guardrails

**DO**
- Anchor light UI on warm cream `#FFFCEA` — never plain white.
- Use indigo `#3139FB` as the single primary; reach for the spectrum only for Space themes and gradients.
- Theme Spaces with gradients from adjacent spectrum colors — gradients are an Arc signature.
- Use Marlin for display/headings, Inter for body, Space Mono for URLs and shortcuts.
- Use real product vocabulary — Spaces, Command Bar, Pinned Tabs, Split View.

**DON'T**
- Use corporate flat blue or pure white — Arc is warm cream + indigo + playful spectrum.
- Apply gradients to body text or make the UI a rainbow — gradients are for Space headers/accents.
- Use heavy Marlin weights or swap it for a generic sans — its rounded regular is the personality.
- Recolor the mark to a single flat hue when a gradient is available.
- Randomize Space contents — tab lists and themes are deterministic per Space.
