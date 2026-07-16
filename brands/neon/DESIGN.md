# Neon — Design System

> Postgres backends for apps and agents.
> The backend for apps and agents — Serverless Postgres, Auth, Functions, Storage, and an AI Gateway: instant, branchable, serverless.

Neon's identity is **technical, dark, and fast-feeling**: deep near-black surfaces, one signature electric **green** (`#00E599`), a custom display face (**esbuild**), and monospace for anything that is code, a branch, or an ID. It references terminal culture without being retro — clean, precise, engineered.

Dark is the product/console experience (and the brand's signature); the 2025 marketing site is light-first. This showcase leads with the dark console identity, and supports light.

---

## Colors

### Brand
| Token | Hex | Usage |
|-------|-----|-------|
| `green` | `#00E599` | The brand — CTAs, active branch, success, focus glow |
| `green-teal` | `#00E5BF` | Secondary green / gradient end |
| `green-dim` | `rgba(0,229,153,.10)` | Subtle accent backgrounds |
| `green-glow` | `rgba(0,229,153,.16)` | Focus glow |

### Surfaces
| Token | Hex (dark) | Hex (light) | Usage |
|-------|------------|-------------|-------|
| `bg` | `#0B0C0D` | `#FFFFFF` | App background |
| `surface` | `#131415` | `#FAFAFA` | Cards, code panels (real live token) |
| `raised` | `#18191B` | `#F4F4F5` | Elevated surfaces, rows |
| `overlay` | `#1F1F22` | `#EDEDEF` | Modals, popovers |
| `border` | `#2A2A2E` | `#E4E4E7` | Dividers |
| `border-strong` | `#38383D` | `#D4D4D8` | Inputs, emphasis |

### Text
| Token | Hex (dark) | Hex (light) | Usage |
|-------|------------|-------------|-------|
| `fg` | `#FAFAFA` | `#1A1A1A` | Primary |
| `fg-secondary` | `#A1A1AA` | `#52525B` | Supporting |
| `fg-muted` | `#6E6E76` | `#8C8F94` | Placeholders, meta |

### Semantic / state
| State | Hex | Meaning |
|-------|-----|---------|
| active / success | `#00E599` | Active branch, query ok |
| idle | `#6E6E76` | Idle branch (scale-to-zero) |
| error | `#F04747` | Errors |
| warning | `#F5A623` | Warnings |

---

## Typography

All three faces are used directly — **esbuild** and IBM Plex Sans are self-hosted on neon.com and **CORS-open** (`access-control-allow-origin: *`); Inter and Geist Mono are Google-hosted.

- **esbuild** — Neon's custom display face (single weight, Medium 500) for the hero, the wordmark, and big headings. `neon.com/_next/static/media/ESBuild_Medium*.woff2`.
- **Inter** — the UI/body face (`--font-inter` on `body`).
- **Geist Mono** — code, SQL, branch names, connection strings, IDs, metrics (the site ships `GeistMono`).

| Role | Face | Spec |
|------|------|------|
| Display | esbuild 500 | 44–56px, `-0.02em` |
| Heading | esbuild 500 / Inter 600 | 20px |
| Body | Inter 400 | 14px |
| Code / SQL / branch | Geist Mono | 13px |

---

## Logo

The Neon **mark** — the hollow "N" formed by a rectangle with an angled internal cut (`viewBox 0 0 24 24`, single path, Simple Icons `neon`) — filled brand green `#00E599`, beside a **Neon** wordmark set in the esbuild display face. (The site favicon uses a muted `#37C38F`/`#34D59A`; the brand accent is `#00E599`.)

---

## Signature component — Branching + SQL

Neon's magic: **database branches are instant, copy-on-write, and serverless** — like `git branch` for Postgres.

- A **branch tree** (`main → dev → feat/*`) with a status dot (active green / idle grey — branches scale to zero), storage size, and latency, all in Geist Mono. Click a branch to select it.
- **+ Create branch** forks the selected branch **instantly** — a new child node appears with `copy-on-write · 0 ms · just now`, the Neon differentiator (no data copy, ready immediately).
- A **SQL console** scoped to the selected branch: a real Postgres query (Geist Mono, green keywords) + **Run** → a results grid with row count and query latency. Different branches return different data (prod on `main`, a subset on `dev`), proving isolation.

Deterministic — fixed branches/queries, index-driven forking, no `Math.random`.

---

## Guardrails

**Do**
- Use the green `#00E599` accent only for CTAs, active states, success, and focus — never decoration.
- Set code, SQL, branch names, IDs, and connection strings in **Geist Mono**; the hero + headings in **esbuild**.
- Build depth from layered near-black surfaces (`#0B0C0D → #131415 → #18191B`), not shadows.
- Make metrics, branches, and query results the visual hero — this is an engineer's tool.

**Don't**
- Use the green glow decoratively — only on interactive focus/active.
- Use corners larger than ~8px — keep the UI sharp.
- Add marketing illustrations inside the console; prefer skeletons over spinners.
- Invent neutral tints — Neon's darks are the real cool near-blacks (`#131415`, `#18191B`).
