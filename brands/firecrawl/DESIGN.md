# Firecrawl — Design System

> The context API to search, scrape, and interact with the web at scale. 🔥
> Turn any website into clean, LLM-ready data.

Firecrawl's identity is **utilitarian and bright**: a near-white paper canvas, crisp black ink, and one hot **"heat" orange** (`#fa5d19`) that carries the whole brand — the flame mark, links, primary actions, and the `[&_span]` highlight in the hero. It reads like a well-built developer tool: monochrome structure, a single warm accent, mono for anything that is code or data.

---

## Colors

### Brand
| Token | Hex | Usage |
|-------|-----|-------|
| `heat-100` | `#fa5d19` | The brand — flame mark, links, primary buttons, hero highlight |
| `heat-80` | `#fb7d47` | Lighter heat — hover fills, secondary emphasis |
| `heat-8` | `rgba(250,93,25,.08)` | Tint wash behind heat elements |
| `heat-4` | `rgba(250,93,25,.04)` | Faint tint |

The homepage also uses a **flame gradient** for illustrative fire (`#FABC12` → `#F26625` → `#F94543` → `#eb3424`) and a muted **agent purple** `#9061ff` / `#a07aff` for AI/agent accents. These are decorative/illustrative — never the primary UI accent. `heat-100` is.

### Surfaces (light — default)
| Token | Hex | Usage |
|-------|-----|-------|
| `background-base` | `#FDFDFD` | App canvas |
| `white` | `#FFFFFF` | Cards / panels |
| `surface` | `#F9F9F9` | Raised / code wells |
| `surface-2` | `#F5F5F5` | Inset rows |
| `border` | `#E8E8E8` | Hairlines |
| `border-faint` | `#EDEDED` | Faint dividers, corner ticks |

### Surfaces (dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `bg` | `#0A0A0A` | Canvas |
| `panel` | `#141414` | Cards / panels |
| `raised` | `#1C1C1C` | Wells |
| `border` | `#262626` | Hairlines (real Firecrawl neutral) |

### Text
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `ink` | `#000000` | `#F7F7F7` | Primary |
| `ink-2` | `#262626` | `#D4D4D4` | Headings / strong body |
| `muted` | `#6B6B6B` | `#8F8F8F` | Secondary |
| `faint` | `#9E9E9E` | `#6B6B6B` | Meta / captions |

### Semantic (scrape state)
| State | Hex | Meaning |
|-------|-----|---------|
| success | `#16A34A` | Scrape complete · 200 |
| running | `#fa5d19` | Fetching / crawling |
| warn | `#FABC12` | Rate-limited / retry |
| error | `#eb3424` | Failed page |

---

## Typography

- **Suisse Intl** (`--font-suisse`) — display + UI + body. Suisse is proprietary and CORS-locked, so this showcase documents it as **≈ Inter** (Google) — the closest neutral Swiss grotesque.
- **Geist Mono** (`--font-geist-mono`) — code, API endpoints, JSON, extracted markdown, metrics. Firecrawl also ships Roboto Mono as a mono fallback; Geist Mono is Google-hosted and used directly here.

One role each: Suisse/Inter for everything human-readable, Geist Mono for everything that is code or machine data.

| Role | Face | Spec |
|------|------|------|
| Display | Inter 600 | 52px, `-0.03em` |
| Heading | Inter 600 | 20px |
| Body | Inter 400 | 15px |
| Code / data | Geist Mono 400 | 12–13px |

---

## Logo

The real Firecrawl **flame mark** — a single sculpted flame path filled `heat-100` with a `background-base` cut-out — pulled verbatim from the live site (`viewBox 0 0 600 600`). The flame is the brand; pair it with the "Firecrawl" wordmark set in Inter/Suisse.

---

## Signature component — The scrape (URL → clean markdown)

Firecrawl's whole thesis in one panel: a messy webpage becomes **LLM-ready data**.

- A URL bar with an endpoint chip `POST /v1/scrape`, preset targets, and a **format toggle** — `Markdown` / `JSON` / `Links`.
- **Scrape** runs a deterministic step log: `Fetching → Parsing → Cleaning → Extracting` (spinner → green ✓).
- The output panel renders the result in the selected format: clean rendered **Markdown** (headings + prose + code, no nav/ads), a structured **JSON** payload with `metadata` (`title`, `description`, `sourceURL`, `statusCode`), or the **Links** the crawler discovered.

Deterministic — three presets, fixed payloads, index-based streaming, no `Math.random`.

---

## Guardrails

**Do**
- Keep the canvas near-white `#FDFDFD` with crisp black ink; let one `heat-100` orange carry the brand.
- Set every endpoint, JSON key, and extracted line in Geist Mono — code and data are always mono.
- Show the core value: raw web → **clean markdown**. The output panel is the point.
- Use corner ticks / faint hairlines for the boxed, technical feel.

**Don't**
- Use the flame gradient (`#FABC12`→`#F94543`) or agent-purple as the primary UI accent — they are illustrative only; the accent is `heat-100`.
- Add a second competing bright color — orange is the single accent; green/yellow/red are scrape-state signals only.
- Render extracted content in a proportional sans as if it were UI — it is data; keep it mono.
- Recreate the flame in a different hue — the flame is always `heat-100`.
