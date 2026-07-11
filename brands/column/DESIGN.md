# Column — Design System

> Move, hold, and lend the dollar at scale.
> The only nationally chartered bank designed to help you build and fund new financial products.

Column is a bank you program. Its identity is **institutional but modern**: a clean white canvas, deep navy ink (`#011821`), slate-grey structure, and one signature **teal** (`#167E6C`) for accents, positive state, and feature surfaces. It reads like trustworthy financial infrastructure — restrained, precise, money set in mono with tabular figures.

---

## Colors

### Brand
| Token | Hex | Usage |
|-------|-----|-------|
| `teal-600` | `#167E6C` | The brand — links, settled state, feature surfaces, accents |
| `teal-tint` | `#E6F1EC` | Wash behind teal elements |
| `navy` | `#011821` | Ink · primary button · logo |

### Surfaces
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `bg` | `#FFFFFF` | `#011821` | App canvas |
| `card` | `#F6F6F8` | `#0A1E27` | Cards / panels |
| `field` | `#F0F2F5` | `#0E2731` | Rows / inputs |
| `border` | `#E3E9F2` | `#172C34` | Hairlines |

### Text (navy + slate)
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `ink` | `#011821` | `#E3E9F2` | Primary |
| `slate` | `#465962` | `#A9ACB6` | Secondary |
| `muted` | `#575A64` | `#7E8A92` | Meta |
| `faint` | `#A9ACB6` | `#5A6B73` | Captions |

### Ledger / transfer state (semantic)
| State | Hex | Meaning |
|-------|-----|---------|
| settled | `#167E6C` | Transfer settled · credit |
| pending | `#C98A2C` | Pending / in flight |
| returned | `#D80027` | Returned / failed |

On dark surfaces the teal lightens to `#3BAF97` for legibility.

---

## Typography

- **Suisse Intl** (`--font-ui`) — UI, body, headings. Suisse is proprietary/CORS-locked, so documented as **≈ Inter** (Google).
- **Suisse Intl Mono / SF Mono** (`--font-mono`) — account numbers, amounts, API code, transfer IDs. Documented as **≈ JetBrains Mono**.

Money and account numbers use **tabular figures** so columns of digits align.

| Role | Face | Spec |
|------|------|------|
| Display | Inter 600 | 52px, `-0.03em` |
| Heading | Inter 600 | 20px |
| Body | Inter 400 | 15px |
| Amounts / code | JetBrains Mono 400 | 12–13px, tabular |

---

## Logo

The real Column **wordmark** (`viewBox 0 0 179 41`, single path with the integrated mark), pulled verbatim from the site and colored via `--logo-wm` (navy on light, pale on dark).

---

## Signature component — Move money via API

Column is a bank with an API; the signature shows a **transfer hitting the ledger**.

- A left **API request** — the real `column.transfers.book()` / ACH call in JetBrains Mono, syntax-highlighted, reflecting the last action.
- A right **ledger**: two accounts (`Operating`, `Reserve`) with balances and masked account numbers, plus a list of recent transfers (type chip `ACH` / `WIRE` / `BOOK`, amount, status dot).
- **Send transfer** originates a book transfer: it debits Operating, credits Reserve, prepends a ledger row that goes **Pending → Settled** (amber → teal), and the balances update with tabular figures.

Deterministic — fixed accounts, index-driven settlement, no `Math.random`.

---

## Guardrails

**Do**
- Keep the canvas clean white (or navy `#011821`) with navy ink and one teal `#167E6C` for accents and settled state.
- Set every amount, account number, and API value in mono with **tabular figures**.
- Color transfer state by meaning: teal settled, amber pending, red returned.
- Keep the tone institutional and precise — this is regulated banking infrastructure.

**Don't**
- Introduce a second bright accent — teal is the only brand color; navy and slate carry structure.
- Render money in a proportional sans — amounts are mono and tabular.
- Use flag/currency spectrum colors (blue/red/yellow) as UI accents — those are illustrative only.
- Recolor the wordmark — it's monochrome (`--logo-wm`).
