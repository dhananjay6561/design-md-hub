# Loops — Design System

> One platform, every email — marketing, lifecycle and transactional email for SaaS teams.

Loops is email software built for SaaS: send marketing broadcasts, automated **lifecycle loops**, and transactional email from one product. The identity is warm and editorial — a clean white canvas, a warm near-black ink, and a single **hot orange** (`#FC5200`) accent — paired with a **serif display** (Newsreader) that gives the marketing voice a considered, magazine-like feel over an otherwise plain sans UI. The signature mark is a spiralling **double loop** (the "loop" made literal). It feels crafted, calm and confident, not loud.

---

## Color

### Brand — one orange
| Token | Hex | Usage |
|---|---|---|
| orange | `#FC5200` | Primary accent — logo, CTAs, links, active flow |
| ember | `#FC671F` | Hover / lighter tint |
| coral | `#FD8C57` | Soft tint, glows, gradient end |
| flow gradient | `#FC5200 → #FD8C57` | Logo mark, run button, the live path |

Orange is the **only** brand hue. Everything else is monochrome; color beyond orange appears only as functional node-type / status signals inside the product (see below).

### Surfaces (light-first — Loops is a bright, warm product)
| Token | Light | Dark | Usage |
|---|---|---|---|
| canvas | `#FFFFFF` | `#141310` | App background |
| panel | `#FFFFFF` | `#1C1A16` | Cards, editor, node cards |
| subtle | `#F7F6F4` | `#221F19` | Muted rows, column wells |
| raised | `#F0EEEA` | `#2A2721` | Hover / selected |
| border | `#E8E6E1` | `#322E26` | Hairlines |

### Text
| Token | Light | Dark |
|---|---|---|
| primary (ink) | `#1A1917` | `#F7F5F0` |
| secondary | `#6B6863` | `#B4AFA4` |
| muted | `#9B978F` | `#7E796E` |
| link | `#FC5200` | `#FF7A33` |

### Functional signals (product only — not brand)
| Token | Hex | Meaning |
|---|---|---|
| timer amber | `#E0A03A` | Wait / delay node |
| filter violet | `#7C6BDB` | Branch / condition node |
| success green | `#2E9E5B` | Activated · email delivered · converted |
| exit slate | `#8A8681` | Exit / removed from flow |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / marketing headings | **Newsreader** (`600`) | A transitional serif — the brand's editorial voice. Used for hero and section headings ("One platform, every email"). It's what makes Loops feel considered rather than generic-SaaS. |
| UI / body | **Inter** (`400 / 500 / 600`) | All product UI, labels, node cards, body copy. |
| Mono / code / meta | **IBM Plex Mono** (`400 / 500`) | API endpoints, timestamps, event log, contact ids. |

All three are on Google Fonts (Loops self-hosts equivalents via Framer, CORS-open; Google Fonts is used here for complete glyph coverage). Scale: hero 54px (Newsreader 600), section heading 30px, node label 14px (Inter), meta 11px (Plex Mono). Set marketing display in the **serif**; never set UI or body in it.

---

## Shape, spacing & motion

- **Radius:** cards & panels `12px`, node cards `10px`, buttons `9px`, chips/pills `9999px`. Rounded and friendly, not sharp.
- **Spacing:** 8px grid; the loop builder reads left→right as **Start · Branch · Finish** columns with generous gutters and connector rails between them.
- **Elevation:** panels float on a soft warm shadow (`0 18px 50px rgba(40,30,10,.10)`); the active node in a running loop gets an orange left-rail + soft orange glow.
- **Motion:** a contact **token** flows through the loop node-by-node — each node lights up as the token occupies it, connectors along the taken path turn orange, then it settles into an outcome. Smooth, sequential, **deterministic** — no randomness; every contact has a fixed, predetermined journey.

---

## Components

- **Logo mark** — a spiralling **double loop** (two offset elliptical strokes with an almond negative space), in orange; pairs with the `Loops` wordmark.
- **Loop builder** — the core surface: columns of **node cards** (Trigger · Timer · Send · Filter · Exit), each a small icon + type label + value, wired by connector rails. This is where lifecycle email is composed.
- **Node cards** — white card, monochrome by default; the type icon carries a functional tint (trigger orange, timer amber, filter violet, exit slate). Active/occupied → orange rail + glow.
- **Contact chip** — a circular monogram avatar + name; the unit that flows through a loop.
- **Email preview** — a compact rendered email (from · subject · body) that updates when a Send node fires — the payload of the whole system.
- **Buttons** — solid orange primary (white text), ghost secondary (ink border). Run/trigger actions are always orange.

---

## Guardrails

**Do**
- Keep a **bright white, warm canvas** with a warm near-black ink — Loops is a light product (dark mode is secondary).
- Use **one orange** (`#FC5200`) for all brand chrome — logo, CTAs, links, and the active flow path.
- Set marketing **display headings in Newsreader** (serif); keep all UI and body in Inter.
- Make lifecycle **loops literal** — Trigger → Timer → Send → Filter → Exit node cards wired left-to-right, a contact flowing through.
- Treat amber/violet/green/slate as **functional node/status signals only**, never as secondary brand colors.

**Don't**
- Lead with a dark or cold canvas, or a second brand hue competing with the orange.
- Set UI, labels or node cards in the serif — the serif is for marketing display only.
- Render the loop as a flat list — the value is the **branch** (activated vs not) and the paths it creates.
- Make orange garish or neon; it's a single confident hot-orange, warmed by coral tints.
- Drop the spiral loop mark for a generic envelope — the double loop is the identity.
