# n8n Design System

> "AI agents and workflows you can see and control." n8n is a **source-available workflow-automation platform** — a visual, node-based canvas that combines AI with 400+ integrations, deployable on your own infrastructure. The identity is dark, energetic, technical: a deep purple-black canvas lit by a signature **orange → red** gradient. Dark-first.

Identity confirmed by **headless-screenshotting the live `n8n.io`** (Nuxt SPA). The hero is a purple-black field with an orange-red "energy" lightning graphic; the primary CTA is orange-red `#FF2B09`.

---

## Colors

### Signature — orange → red
| Token | Hex | Usage |
|---|---|---|
| `--brand` | `#FF3B21` | Primary orange-red — buttons, active nodes, links, brand mark |
| `--brand-hot` | `#FF2B09` | Hottest red — CTA hover, run pulse (live "Sign up" button) |
| `--orange` | `#FD8925` | Gradient start / secondary energy |
| `--grad` | `linear-gradient(100deg,#FD8925,#FF2B09)` | Hero energy, run state, accents |
| `--brand-ink` | `#E23A12` | Orange-red darkened for links/text on light |

### Purple-black canvas (the n8n signature neutral)
| Token | Hex | Usage |
|---|---|---|
| `--ink-950` | `#0E0918` | **Main dark canvas — the most identifiable n8n neutral** |
| `--ink-900` | `#16111F` | Raised dark surface |
| `--ink-850` | `#1A1624` | Cards, node bodies |
| `--ink-800` | `#1B1728` | Panels |
| `--ink-border` | `#2A2440` / `#362E52` | Borders on dark |

### Semantic (node execution)
| State | Hex |
|---|---|
| Success / executed | `#2FBE6E` green |
| Running / pinned | `#FF3B21` orange-red |
| Waiting / disabled | `#6E6690` muted purple |
| Error | `#FF2B09` red |

### Surfaces & text
| Token | Dark (default) | Light |
|---|---|---|
| `--bg` | `#0E0918` | `#FFFFFF` |
| `--bg2` | `#16111F` | `#F7F6FB` |
| `--surface` | `#1A1624` | `#FFFFFF` |
| `--border` | `#2A2440` | `#E7E4F0` |
| `--text` | `#ECEAF5` | `#1A1624` |
| `--text2` | `#A7A0C0` | `#5B5470` |
| `--text3` | `#6E6690` | `#8B84A5` |
| `--brand` (themed) | `#FF3B21` | `#E8330F` (darkened for light contrast) |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / UI / body | **Geomanist** (`--font-geomanist`) | n8n's geometric brand sans. Proprietary/Next-hosted → documented ≈ **Manrope** (Google), the closest geometric-humanist match. |
| Code / nodes / expressions | **JetBrains Mono** | Node params, `{{ $json }}` expressions, JSON, HTTP methods. |

Hierarchy: Manrope 600 for headings + node titles; 400 for body. Mono for every expression, endpoint, and JSON payload.

---

## Logo

Real n8n logo (viewBox `0 0 87 24`, 2 paths): the iconic **connected-nodes mark** — three linked circles branching from a central node (the workflow-graph motif) — plus the **"n8n"** wordmark. Pulled verbatim from the live header.

**Theming:** mark = `var(--brand)` orange-red (the signature) · wordmark = `var(--logo-text)` (near-white on dark / near-black on light).

---

## Components

- **Buttons** — Primary: `background:var(--brand)`, white text, radius 8px; hover → `--brand-hot`. Never orange text on the orange button.
- **Node card** — rounded card, left icon-chip colored by node type, title + subtitle; selected = orange-red ring; executed = green ring + item-count pill.
- **Trigger node** — distinctive rounded-left ("play") edge to mark the start of a flow.
- **Connection** — bezier curve between node ports; grey at rest, orange-red + dashed-flow while executing.
- **Expression chip** — mono `{{ $json.field }}`, purple-tinted.

---

## Signature — the workflow canvas

n8n's whole identity is the **node editor**: a dotted-grid canvas of nodes wired together, executed left-to-right.

- Nodes: `Schedule Trigger` → `HTTP Request` → `IF` → (true) `Send Slack message` / (false) `Google Sheets`, connected by bezier curves on a dotted grid.
- **Execute workflow** runs the flow: each node pulses orange-red, then resolves to a green success ring with an **item-count pill** ("1 item", "12 items"), and connection lines animate a dashed data-flow — in deterministic order (index-driven, no `Math.random`).
- Click any node to select it (orange-red ring) and reveal its params in a side panel (HTTP method + URL, the IF condition `{{ $json.status }} == "active"`, etc.).

---

## Guardrails

### DO
- Anchor on the purple-black canvas `#0E0918`; light it with the orange→red gradient.
- Darken orange-red to `#E8330F` for text/links on light surfaces.
- Set the UI in Geomanist (≈ Manrope); reserve mono for expressions & JSON.
- Color nodes by type; mark execution with green success + item counts.
- Frame everything as a **visual, node-based workflow you can see and control**.

### DON'T
- Don't use a plain black or grey canvas — the purple-black `#0E0918` is the n8n signal.
- Don't put orange text on the orange button.
- Don't invent node data — use real n8n language (Trigger, HTTP Request, IF, expressions `{{ }}`, items).
- Don't use `Math.random()` — keep the execution deterministic.
