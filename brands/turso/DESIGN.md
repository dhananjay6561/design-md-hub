# Turso — Design System

> Millions of Databases. One Architecture.

Turso is the lightweight database that scales to millions of agents — a full SQLite drop-in (built on libSQL, now rewritten in Rust) that you deploy **everywhere**: on servers, in browsers, on devices, *just like files*. Spin a database for every user, agent, and tenant.

The identity is a **deep ink-navy canvas** lit by one signature **mint-teal** (`#4FF7D1`), an Inter UI, and a mono voice split between IBM Plex Mono brand labels and Geist Mono for SQL. It reads as infrastructure for the agentic future — technical, fast, database-dense.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| teal | `#4FF7D1` | Primary accent — CTA, links, active DB, metrics, brand mark glow |
| teal-alt | `#4FF8D2` | Hover / gradient partner |
| teal-deep | `#0F4F62` | Teal-tinted surface / deep accent |
| orange | `#E0953C` | Secondary accent / warning |
| red | `#FF6663` | Error / destructive |

### Surfaces (dark-first — the product is dark)
| Token | Hex | Usage |
|---|---|---|
| canvas | `#0F1419` | App background |
| surface | `#121B22` | Panels |
| raised | `#18222B` | Cards / rows |
| raised-2 | `#1B252D` | Hover |
| border | `#232E36` | Hairlines |
| border-strong | `#293945` | Inputs, stronger dividers |

### Text
| Token | Hex | Usage |
|---|---|---|
| primary | `#FAFAFA` | Primary |
| secondary | `#C5CACE` | Secondary |
| muted | `#9CA3AF` | Muted |
| faint | `#6B7280` | Faint |

---

## Typography

| Role | Font | Notes |
|---|---|---|
| Display / UI / body | **Inter** (`--font-inter`) | Headings + product UI |
| Brand labels / eyebrows | **IBM Plex Mono** (`--font-ibm-plex-mono`) | Retro-mono badges & section eyebrows, the logo voice |
| Code / SQL / data | **Geist Mono** (`--font-geist-mono`) | SQL shell, results, IDs, sizes |

All three are Google-hosted and used directly. Keep roles separate: Inter for sentences, IBM Plex Mono for short uppercase brand labels, Geist Mono for anything code- or data-shaped.

---

## Logo

The `turso` wordmark preceded by the **globe mark** — a circle crossed by a rotated ellipse and a directional arrow-cross (SQLite-everywhere / replication). Mark stroke and wordmark both take `--logo-wm` (white on ink, ink on light). A teal glow may sit behind the mark.

---

## Signature component — the database explorer

If you saw only this, you'd know it was Turso: a **group** holding *millions* of tiny databases — one per tenant, user, and agent — beside a **libSQL SQL shell**. Pick a database and its `turso db shell` query and result grid load; hit **+ New database** and one spins up instantly (*like a file*, in milliseconds) and selects itself. This is "Millions of Databases. One Architecture." made literal.

- Left: database list (per-tenant/user/agent) with region + size + status; a create button
- Right: `turso db shell <name>` — a real SQL query (Geist Mono, syntax-colored) + result grid
- Deterministic per-database queries/results (no `Math.random`)

---

## Guardrails

**Do**
- Keep the canvas deep ink-navy `#0F1419`; reserve **teal** for the CTA, active database, links, and headline metrics.
- Treat databases as *cheap and plural* — many small per-tenant DBs, spun up like files.
- Show SQL in Geist Mono; use IBM Plex Mono for short uppercase brand labels.
- Report real numbers (database counts, regions, sizes) — density is the story.

**Don't**
- Use the legacy purple identity — Turso is teal-on-ink now.
- Add a second bright accent — teal carries it; orange/red are state-only.
- Set body copy in a mono — Inter carries sentences.
- Render one monolithic database — the many-database architecture is the whole point.
