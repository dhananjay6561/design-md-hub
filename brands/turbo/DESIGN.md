# Turborepo — Design System

> Make ship happen.

Turborepo is a high-performance build system for JavaScript and TypeScript codebases, written in Rust. It caches the work your tasks produce so you never do the same work twice — and when everything is a cache hit, it prints its signature line: `>>> FULL TURBO`.

The brand is a Vercel-family design language: a near-black canvas, Geist typography, restrained neutral grays for chrome — and one unmistakable flourish, the **pink → blue gradient** that runs through the logomark and every hero accent. Everything else stays monochrome so the gradient carries the identity.

---

## Color

### Brand gradient (the signature)
Turborepo's identity is a single diagonal gradient from **pink-red** to **blue**. It appears in the logomark ring, hero headlines, and key accents — never as a flat fill for large areas.

| Stop | Hex | |
|---|---|---|
| Start | `#FF1E56` | pink-red |
| … | `#DB2F6E` `#B34288` `#8B56A4` `#6368BE` `#4F71CB` `#2885E6` | interpolated stops |
| End | `#0096FF` | blue |

`background:linear-gradient(90deg,#FF1E56,#0096FF)` — the canonical two-stop form.

### Surfaces (neutral, near-black first)
| Token | Dark | Light | Usage |
|---|---|---|---|
| `--background` | `#0A0A0A` | `#FFFFFF` | Page background |
| card / raised | `#121212` | `#F5F5F5` | Cards, terminals, docs surface |
| `--accent` | `#262626` | `#F5F5F5` | Hover / subtle fill |
| border | `#2E2E2E` | `#EBEBEB` | Hairline borders |

### Text
| Token | Dark | Light |
|---|---|---|
| foreground | `#FAFAFA` | `#0A0A0A` |
| muted | `#A1A1A1` | `#666666` |
| faint | `#737373` | `#8F8F8F` |

### Semantic (task / cache states)
| State | Color | Usage |
|---|---|---|
| cache HIT / success | `#0096FF` → `#3ECF8E` green `#30A46C` | replayed from cache |
| cache MISS / running | `#FF1E56` | task executed fresh |
| warning | `#F5A623` | skipped / stale |
| FULL TURBO | gradient | all tasks cached |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display + UI | **Geist** (`400 / 500 / 600 / 700`) | Vercel's grotesk. Hero, headings, body, labels. |
| Code / CLI / metrics | **Geist Mono** (`400 / 500`) | Terminal output, task names, durations, hashes, `turbo run …`. |

Both are self-hosted on turbo.build (CORS-open) and mirrored on Google Fonts. Scale: hero 52–64px `-0.03em`, section 22px, body 14–15px, mono 12–13px. Headlines lean tight and large; mono is used liberally because the product *is* a CLI.

---

## Shape, spacing & motion

- **Radius:** cards `12px`, inner tiles `8–10px`, pills/badges `9999px`, buttons `8px`. Tighter than consumer brands — this is a developer tool.
- **Spacing:** 4px base grid, dense but breathable. Terminal output uses `1.6` line-height.
- **Elevation:** flat. Borders (`1px`) do the separating, not shadows. On dark, borders are `#2E2E2E`; a faint gradient hairline may top a hero card.
- **Motion:** fast and mechanical (100–200ms). Task rows stream in as a run progresses; the `>>> FULL TURBO` line lands last. No springy overshoot — Turborepo feels *instant*, which is the whole point.

---

## Components

- **`turbo run` panel** — a terminal listing each `package#task` with a cache status chip (MISS = ran, HIT = replayed) and a duration. Ends in a summary: `Tasks:`, `Cached:`, `Time:`, and `>>> FULL TURBO` when everything hit.
- **Task graph** — packages as nodes connected by dependency edges (topological order left → right). Nodes glow on the gradient when part of the active task set.
- **Buttons** — primary is a solid foreground fill (`#FAFAFA` on dark → black text); the gradient is reserved for the marquee CTA.
- **Badges** — mono, pill-shaped: `cache hit`, `cache miss`, `replayed`, `Rust`.

---

## Guardrails

**Do**
- Keep the canvas monochrome and near-black; let the pink→blue gradient be the only color event.
- Use Geist Mono for anything CLI — task names, durations, cache hashes, `turbo run build`.
- Show real Turborepo semantics: `cache hit, replaying logs`, `>>> FULL TURBO`, `Tasks: N successful`.
- Reserve the gradient for the logomark, one hero headline, and marquee accents.

**Don't**
- Splash the gradient across large flat areas or multiple elements at once — it loses its punch.
- Introduce a second accent hue — the gradient already spans pink to blue.
- Use heavy shadows or rounded, consumer-soft cards — this is a fast, flat dev tool.
- Fake cache math — a warm run is near-instant (`>>> FULL TURBO`); a cold run takes real time.
