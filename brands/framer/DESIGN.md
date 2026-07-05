# Framer — Design System

Design-token reference for **Framer** (framer.com), the no-code AI website builder. All values live-fetched from `framer.com` and its inline CSS (July 2026). Framer's identity is **near-monochrome black/white** with a single electric **blue `#0099FF`** accent and the iconic triangular-**F** mark; the Designer canvas is a dark product cockpit.

---

## Brand voice

- Hero H1: **"The web design agent for professional sites"**.
- Positioning (real meta): *"Create a professional website with Framer's no-code AI website builder. Design freely, manage CMS content, optimize SEO, collaborate, and publish fast."*
- CTAs on live site: **"Get started for free"**, **"Log in"**, **"Sign up"**, **"Publish"**.
- Product surface vocabulary: **Canvas · Layers · Insert · Components · CMS · Breakpoints · Publish**.

---

## Typography

Framer ships **Inter** as its product & marketing typeface (self-hosted on `app.framerstatic.com`); the many other faces on the homepage (Geist, Space Grotesk, EB Garamond, VT323…) are *template previews*, not the brand font.

| Role | Family | Source | Usage |
|------|--------|--------|-------|
| Display / UI / body | **Inter** | Google Fonts (CORS ✅) — mirrors Framer's self-hosted Inter | Hero, headings, body, canvas, buttons |
| Mono | **JetBrains Mono** | Google Fonts (CORS ✅) | Layer names, dimensions, CSS values, breakpoint widths |

Headings are heavy Inter (600–700), tight tracking; body 400.

---

## Color

Near-monochrome shell (white in light, near-black in dark) with one electric blue accent.

### Surfaces
| Token | Hex | Usage |
|-------|-----|-------|
| `bg` (light) | `#FFFFFF` | Page background |
| `bg-2` (light) | `#F3F3F3` | Cards, panels |
| `bg-3` (light) | `#EBEBEB` | Fills, hover |
| `bg` (dark) | `#141414` | Page + Designer canvas chrome |
| `bg-2` (dark) | `#1F1F1F` | Panels (real `#212121`) |
| `bg-3` (dark) | `#303030` | Raised / fills |
| `ink` | `#080808` | Deepest surface / near-black |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `text` (light) | `#141414` | Primary |
| `text-2` | `#4B4B4B` | Secondary |
| `text-3` | `#757575` | Muted |
| `text` (dark) | `#FFFFFF` | Primary on dark |
| `text-2` (dark) | `#CBCBCB` | Secondary on dark |

### Accent & semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `framer-blue` | `#0099FF` | Brand accent — selection, links, primary buttons (used with alpha `#0099FF1A`/`26`/`4D` for tints/rings/glows) |
| `green` | `#00C65E` | Success / "Published" |
| `red` | `#FF3B30` | Error / destructive |

---

## Logo

Iconic triangular **"F"** (viewBox `0 0 24 24`, path `M4 0h16v8h-8zM4 8h8l8 8H4zM4 16h8v8z`) — three stacked triangles. Rendered in **`#0099FF`** brand blue, or mono ink/white when locked up with the wordmark. The mark shape is fixed; only its single fill changes.

---

## Guardrails

**DO**
- Keep the shell monochrome — white (light) / `#141414` (dark) — with `#0099FF` as the *only* accent.
- Use blue for selection outlines, links and primary buttons; tint with alpha (`#0099FF1A`) for subtle fills.
- Keep the Designer canvas chrome dark (`#141414`/`#1F1F1F`) even in light mode — it's a product cockpit.
- Use Inter everywhere; JetBrains Mono only for layer names, dimensions and CSS values.
- Show real product vocabulary (Canvas, Layers, Breakpoints, CMS, Publish).

**DON'T**
- Introduce a second accent hue — Framer is blue-on-monochrome.
- Treat the homepage's template-preview fonts (Geist, VT323, EB Garamond…) as the brand font — it's Inter.
- Recolor the F mark to a gradient or multiple fills — one solid fill only.
- Use `#000`/`#fff` naively for text on the opposite surface — use the ink/cbcbcb steps.
- Randomize the canvas — element edits must deterministically repaint from control state.
