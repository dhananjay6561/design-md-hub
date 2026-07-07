# Mercury — Design System

> Radically different banking — everything you do with money, all in one place.

Mercury is online business banking for startups and scaling companies: checking, savings, treasury, cards, bill pay and more in one refined product. The identity is **calm, precise and aspirational** — a bright near-white canvas, generous whitespace, a single confident **periwinkle-indigo** (`#5266EB`), and soft **dawn gradients** (lavender warming to peach) on marketing surfaces. Everything is set in **Arcadia**, Mercury's custom humanist grotesque, used as a single-typeface system. Numbers are tabular and quiet; charts are smooth and understated. Mercury looks less like a bank and more like a beautifully engineered instrument.

---

## Color

### Brand — one periwinkle-indigo
| Token | Hex | Usage |
|---|---|---|
| indigo | `#5266EB` | Primary accent — buttons, links, chart line, active |
| indigo-light | `#7B8AF0` | Hover, tints, dark-mode accent |
| indigo-deep | `#3D4FD1` | Pressed, emphasis |
| lavender | `#B8C0F2` | Soft fills, gradient start |
| dawn gradient | `#B8C0F2 → #E9D5D0 → #F0DCCF` | Marketing hero — a lavender-to-peach dawn |

Indigo is the single brand hue; the dawn gradient is the atmospheric marketing wash. The product itself is mostly monochrome + indigo, letting the numbers lead.

### Surfaces (light-first — Mercury is a bright, calm product)
| Token | Light | Dark | Usage |
|---|---|---|---|
| canvas | `#FAFAFC` | `#0F1016` | App background |
| panel | `#FFFFFF` | `#171826` | Cards, sheets, chart |
| subtle | `#F4F5FA` | `#1D1F2E` | Sidebar, wells, rows |
| raised | `#EDEFF7` | `#262940` | Hover / selected |
| border | `#E6E8F2` | `#2C2F44` | Hairlines |

### Text
| Token | Light | Dark |
|---|---|---|
| ink | `#16171F` | `#F2F3F9` |
| secondary | `#5C5F72` | `#A6AAC0` |
| muted | `#9599AC` | `#71768E` |
| link | `#5266EB` | `#8592F2` |

### Functional signals (product — money movement, not brand)
| Token | Hex | Meaning |
|---|---|---|
| inflow | `#1E9E6A` | Money in · positive amount |
| outflow | `#16171F` | Money out (ink, not red — spending is normal) |
| pending | `#C79A3E` | Pending / scheduled |
| alert | `#D8503C` | Declined / attention |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Everything — display, UI, numbers | **Arcadia** (`400 / 500 / 600 / 700`) | Mercury's custom humanist grotesque — a single-typeface system for headings, body, tables and figures. Self-hosted on `cdn.mercury.com`, but **CORS-locked** → documented fallback **≈ Hanken Grotesk** (Google), a warm humanist grotesque with the same calm, even texture. |
| Meta / mono | **IBM Plex Mono** (`400 / 500`) | Account numbers, routing digits, tiny meta — used sparingly. |

Set money and figures with **tabular numerals** (`font-variant-numeric: tabular-nums`) so columns align. Scale: hero 54px, balance figure 40px, section 22px, body 15px, table 13.5px, meta 11px. One face carries the whole system — keep it quiet and consistent.

---

## Shape, spacing & motion

- **Radius:** cards & sheets `16px`, buttons & inputs `10px`, chips/pills `9999px`, chart nodes are circles. Soft, calm corners.
- **Spacing:** generous — a bright three-region product: **account sidebar** · **balance + chart** · **transactions**. Whitespace is a feature.
- **Elevation:** panels rest on a soft indigo-tinted shadow (`0 16px 46px rgba(30,35,90,.10)`); nothing is heavy. The dawn gradient glows behind marketing heroes.
- **Motion:** smooth and understated — the balance **chart eases** between time ranges, a **hover crosshair** reveals the balance on a date, and a transfer settles with a quiet confirm. Everything is **deterministic** — fixed series, fixed transactions; no randomness. Precision over flourish.

---

## Components

- **Logo mark** — an ornate circular **seal** of interlocking spirals (the Mercury emblem), paired with the letter-spaced `MERCURY` wordmark in Arcadia. Renders in one ink color (themeable).
- **Banking dashboard** — the core surface: an **account switcher** (Checking / Savings / Treasury), a **balance card** with % change, a smooth **cashflow area chart** with a time-range toggle and hover crosshair, and a **transactions** list.
- **Transaction row** — merchant chip + name + category tag + date + amount (inflow green, outflow ink, tabular-aligned).
- **Balance figure** — large tabular number with a small colored delta.
- **Buttons** — indigo primary ("Open account", "Send"), quiet bordered secondary; pill-shaped nav CTAs.
- **Dawn gradient** — the lavender→peach atmospheric wash used behind marketing heroes (never inside dense product UI).

---

## Guardrails

**Do**
- Keep a bright near-white canvas with **generous whitespace** and one confident **periwinkle-indigo**.
- Set the whole system in **Arcadia** (≈ Hanken Grotesk); use **tabular numerals** for all money.
- Reserve the soft **dawn gradient** for marketing heroes; keep product UI clean and monochrome + indigo.
- Render money movement as **inflow green / outflow ink** — spending is normal, not alarming.
- Keep charts smooth and quiet, with a subtle **hover crosshair**; let the numbers lead.

**Don't**
- Crowd the UI — Mercury's calm comes from space; don't fill every pixel.
- Introduce a second brand hue competing with the indigo, or make the gradient loud/neon.
- Color ordinary spending red — reserve red for declines / attention only.
- Set figures in a proportional/non-tabular way so columns jitter.
- Drop the ornate **seal** mark for a generic bank/card icon.
