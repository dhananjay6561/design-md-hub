# MotherDuck — Design System

The cloud data warehouse built on DuckDB. Warm, playful, and technical: a paper-cream canvas, a friendly duck-on-clouds mascot, one signature yellow, and a wide-tracked display face. The voice is confident and plain-spoken — *"Infrastructure for Answers."*

> **Source of truth:** values below are traced from the live `motherduck.com` markup + stylesheet (fonts, `@font-face` src, hero copy) and the rendered homepage (palette in situ). Where the app UI differs from the marketing site, the marketing identity wins.

---

## Brand foundations

MotherDuck is light-first. The page sits on a warm off-white paper, text is a soft near-black (never pure `#000`), and color arrives in small, high-energy doses: a saturated yellow marquee, an orange call-to-action, and a sky-blue that ties back to the cloud illustrations. Ducks and clouds carry the personality; the UI stays clean.

- **Do not** reach for pure black or pure white as the base — the warm paper `#F4EFEA` and soft ink `#383838` are part of the identity.
- **Do not** let yellow carry text. `#FFDE00` is a block/marquee color; it fails contrast as a foreground.
- Orange is the primary action; sky-blue is data + links.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| `--md-ink` | `#383838` | Primary text, wordmark, borders on light |
| `--md-yellow` | `#FFDE00` | Signature marquee band, highlight blocks |
| `--md-orange` | `#FF9538` | Primary CTA (`START FREE`), duck mascot swooshes |
| `--md-sky` | `#6FC2FF` | Cloud illustration, data accent (dark) |
| `--md-blue` | `#2BA5FF` | Links, focus, data accent |

### Surfaces
| Token | Light | Dark | Usage |
|---|---|---|---|
| `--bg` | `#F4EFEA` | `#171613` | Page canvas (warm paper / warm near-black) |
| `--surface` | `#FFFFFF` | `#211F1B` | Cards, panels, notebook |
| `--surface-2` | `#F8F8F7` | `#2A2823` | Insets, table headers, code wells |
| `--border` | `#E1D6CB` | `rgba(255,255,255,.10)` | Hairlines, dividers |

### Text
| Token | Light | Dark | Usage |
|---|---|---|---|
| `--text` | `#383838` | `#F4EFEA` | Body, headings |
| `--text-muted` | `#666666` | `#A9A29A` | Secondary, captions |
| `--text-faint` | `#818181` | `#7C766E` | Meta, disabled |

### Semantic / data
Result-grid + execution states. The data-viz accents double as the cloud palette.
| Token | Hex | Meaning |
|---|---|---|
| `--ok` | `#2BA36B` | Success, cache hit, positive delta |
| `--cloud` | `#2BA5FF` | Cloud compute (MotherDuck) |
| `--local` | `#FF9538` | Local compute (DuckDB-WASM in your client) |
| `--teal` | `#53DBC9` | Categorical / measure |
| `--warn` | `#F5B161` | Warning |
| `--danger` | `#FF7169` | Error, negative delta |

**Neon-accent rule:** `#2BA5FF` and `#6FC2FF` read on the warm-dark canvas but wash out as text on cream — links/data text on light step down to `#1478C4`.

---

## Typography

Three families, one role each. Do not mix roles — that is the "AI-generated" tell.

| Family | Role | Notes |
|---|---|---|
| **Aeonik Fono** | Display — hero H1, section identity, big numbers | Wide letter-spacing (`.08–.14em`) uppercase for hero; the signature look |
| **Aeonik Mono** | Mono UI — SQL, table headers, execution badges, chips | Regular 400 + Bold 700 |
| **Inter** | Body & UI — paragraphs, labels, nav, cells | 300 / 400 / 600 / 700 |

All three are self-hosted on `motherduck.com` and **CORS-open** (`access-control-allow-origin: *`), so they are used directly via `@font-face`:

```
Aeonik Fono → /fonts/AeonikMono/AeonikFono-Regular.woff2
Aeonik Mono → /fonts/AeonikMono/AeonikMono-Regular.woff2 · -Bold.woff2
Inter       → /fonts/Inter/inter-{300,400,600,700}.woff2
```

- **Hero H1:** Aeonik Fono, uppercase, wide tracking (`letter-spacing:.10em`) — e.g. `INFRASTRUCTURE FOR ANSWERS`.
- **Section titles:** Aeonik Mono, 11px, uppercase, `letter-spacing:.08em`, muted.

---

## Spacing, radius, shadow

- **Radius:** cards/panels `12px`, buttons `8px`, chips/pills `6px`, full for avatars. Friendly but not bubbly.
- **Shadow:** soft and low — `0 1px 3px rgba(56,56,56,.10), 0 1px 2px -1px rgba(56,56,56,.10)`. Clouds float; UI barely lifts.
- **Spacing:** 4px base grid; section padding 40–56px.

---

## Components

- **Primary button:** orange `#FF9538` fill, ink text, radius 8px, uppercase Aeonik Mono label — `START FREE`, `RUN`. Hover darkens ~6%.
- **Secondary button:** transparent, `--border` ring, ink text — `BOOK A DEMO`, `LOG IN`.
- **Marquee band:** full-bleed `#FFDE00` strip, ink Aeonik Fono text scrolling — `DATA WAREHOUSE + AI`.
- **Chips / badges:** mono, 11–12px, tinted-surface fill + hairline. Execution badges pair a duck/cloud glyph with a timing.
- **Table:** mono headers on `--surface-2`, Inter cells, right-aligned numerics with `tabular-nums`; hover 1–2 steps darker than base (never equal).

---

## Signature — MotherDuck notebook (hybrid execution)

The most MotherDuck-specific pattern: a SQL notebook whose query spans **local + cloud**, plus a natural-language mode that turns a question into traceable SQL.

- **Two modes:** `SQL` (write DuckDB SQL) and `Ask AI` (type a question → it generates SQL, streaming). Mirrors the homepage *"in SQL or natural language."*
- **Hybrid execution plan** — the differentiator: the huge `orders` scan/filter/aggregate runs in the **cloud** (`#2BA5FF`), the small `products` join + final sort runs **locally** in DuckDB-WASM (`#FF9538`). A split bar shows where each stage ran, with timings — *"hybrid queries over local and humongous remote."*
- **Results grid:** real analytics shape (category · orders · revenue · AOV), `tabular-nums`, ≤ 20 rows.
- **Footer meta:** rows scanned, wall time, and `ran on: Hybrid (local + cloud)`.
- **Deterministic:** fixed dataset + computed aggregates, no `Math.random()` — screenshots stay stable.

---

## Guardrails

**Do**
- Anchor on warm paper `#F4EFEA` + soft ink `#383838`; keep pure black/white out of the base.
- Use orange for actions, yellow for marquee/highlight blocks only, sky-blue for data + links.
- Set the hero in Aeonik Fono, uppercase, wide tracking; keep SQL/headers in Aeonik Mono, body in Inter.
- Let the duck-and-cloud mascot carry the playfulness; keep the working UI calm.
- Step blue down to `#1478C4` for link/data text on the cream canvas.

**Don't**
- Don't use `#FFDE00` for text — it fails contrast; it's a block color.
- Don't mix the font roles (Fono display / Mono code / Inter body).
- Don't invent evenly-lightened dark tints — the dark canvas is a warm near-black `#171613`, borders are translucent white.
- Don't make table hover equal the base surface after the light swap.
- Don't use `Math.random()` in the signature — keep it deterministic.
