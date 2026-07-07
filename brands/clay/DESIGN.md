# Clay — Design System

> Build systems to grow revenue — the all-in-one platform GTM engineers build on.

Clay is a go-to-market data platform: pull companies and people into a spreadsheet, then **enrich** every row from 100+ data providers using a **waterfall** (try provider 1 → if empty, provider 2 → 3 …, paying only for hits), and run agentic outbound on top. The identity is warm, tactile and **playful-serious**: a warm **cream** canvas, crisp **black** UI, and an unmistakable **claymation** world — hand-sculpted 3D clay objects in a joyful palette (sky-blue, clay-orange, pink, green, yellow, red) — anchored by the **rainbow-arch** logo. Type pairs **Roobert** (a warm geometric grotesque) for UI and headings with **Canela** (an elegant serif) for editorial moments. Clay looks like software that's fun to build in but means business.

---

## Color

### Brand — cream, black & the clay palette
| Token | Hex | Usage |
|---|---|---|
| ink / primary | `#0A0A0A` | Primary buttons, headings, wordmark |
| plum | `#4A0232` | Deep editorial dark — accent sections, emphasis |
| clay-blue | `#5AD0E6` | The signature claymation sky; playful accent |
| clay-orange | `#E3791D` | Warm clay accent — the brand's tactile warmth |
| clay-pink | `#EB6ABF` | Playful accent |
| clay-green | `#56A088` | Playful accent |
| clay-yellow | `#F5D93D` | Playful accent |
| clay-red | `#D0421D` | Playful accent |

The **clay palette** is expressive — used for illustration, decoration and category color, not a single "brand hue". The workhorses are warm **cream + black**; color brings the joy.

### Surfaces (light-first — Clay is a warm, bright product)
| Token | Light | Dark | Usage |
|---|---|---|---|
| canvas | `#F9F8F6` | `#14110D` | App background (warm cream) |
| panel | `#FFFFFF` | `#1E1A15` | Cards, table, sheets |
| subtle | `#F4F3F0` | `#24201A` | Muted rows, wells, table stripes |
| raised | `#EEE9DF` | `#2C2720` | Hover / selected |
| border | `#E6E2D9` | `#38322A` | Hairlines, cell grid |

### Text
| Token | Light | Dark |
|---|---|---|
| ink | `#1A1714` | `#F4F1EA` |
| secondary | `#6B655C` | `#B4ADA0` |
| muted | `#9A9388` | `#7E776B` |
| link | `#0A0A0A` | `#F4F1EA` |

### Functional signals (product — enrichment status, not brand)
| Token | Hex | Meaning |
|---|---|---|
| searching | `#1E93C9` | Waterfall running · trying a provider |
| found | `#2F9E63` | Data found · cell filled |
| not found | `#C0472E` | Waterfall exhausted · no match |
| credit | `#A8792A` | Credits spent on a hit |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| UI / headings | **Roobert** (`400 / 500 / 600`) | The brand face — a warm geometric grotesque (Displaay). Wordmark, headings, table, all product UI. Self-hosted on Clay's CDN, CORS-open — used directly. |
| Editorial serif | **Canela** (`300 / 400`) | Commercial Type's high-contrast serif — reserved for editorial display / pull-quotes, a touch of elegance against the playful clay. Self-hosted, CORS-open. |
| Mono / data / meta | **Space Mono** (`400 / 700`) | Numbers, domains, credits, provider names, timings — the data texture. (Clay uses Space Mono; Google-hosted here.) |

Scale: hero 56px (Roobert 600), Canela editorial 34px, section 26px, table cell 13px (Roobert), meta 11px (Space Mono). Set UI and dense tables in **Roobert**; use Canela only for large editorial lines.

---

## Shape, spacing & motion

- **Radius:** cards & sheets `14px`, buttons `10px`, cells `0` (a crisp spreadsheet grid), pills/chips `9999px`, the logo arch is a rounded semicircle. Soft outer shells, sharp data grid.
- **Spacing:** 8px grid; the product is a **spreadsheet** — a dense grid of rows × columns with roomy toolbars around it.
- **Elevation:** cards and popovers float on a soft warm shadow (`0 18px 50px rgba(60,45,20,.12)`); claymation art casts soft, rounded, tactile shadows — never hard/flat.
- **Motion:** the signature moment is the **enrichment waterfall** — a cell shows providers being tried in sequence (spinner → ✗ → ✗ → ✓), then fills with the found value and the provider that hit. Sequential, legible, **deterministic** — every row has a fixed waterfall outcome. Playful but never chaotic.

---

## Components

- **Logo mark** — a **rainbow arch**: concentric rounded semicircle bands, navy-blue on the outside warming through red → orange → yellow inside; pairs with the lowercase `clay` wordmark in Roobert.
- **Enrichment table** — the core surface: a spreadsheet of accounts/people (company + firmographics) plus **enrichment columns** whose values are filled by waterfalls; crisp cell grid, colored column headers.
- **Waterfall** — Clay's signature: an ordered list of data **providers** tried until one returns a value (✗ ✗ ✓), spending credits only on the hit. Shown inline in a cell popover and as a run log.
- **Provider chip** — a small pill naming a data source (Prospeo, Hunter, Datagma, Apollo…) with a ✓/✗ result.
- **Buttons** — black primary ("Run", "Start free trial"), cream/bordered secondary ("Get a demo").
- **Claymation art** — hand-sculpted 3D clay objects in the full palette; the brand's joyful, tactile signature (decorative, on marketing surfaces).

---

## Guardrails

**Do**
- Anchor on a warm **cream canvas** with crisp **black** UI — the workhorses; color brings the joy.
- Bring in the **clay palette** (blue, orange, pink, green, yellow, red) for illustration and category color — playful but purposeful.
- Set UI and tables in **Roobert**; use **Canela** serif only for large editorial lines; data/meta in Space Mono.
- Make the **enrichment waterfall** legible — providers tried in order, ✓/✗, credits only on hits (the core product idea).
- Keep the **rainbow-arch** logo and the tactile **claymation** style — soft rounded 3D, never flat clip-art.

**Don't**
- Reduce Clay to one flat accent color — the identity is cream + black + a *playful multi-color* clay world.
- Set dense tables or body in Canela — the serif is for editorial display only.
- Use hard, flat drop shadows on the clay art — it's sculpted and soft.
- Present enrichment as a single API call — the point is the **waterfall** across many providers.
- Make the palette garish or neon — these are warm, matte, clay-like tones.
