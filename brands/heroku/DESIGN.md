# Heroku Design System

> "The Cloud Application Platform For Building, Deploying, and Scaling Apps." Heroku (a Salesforce company) is the original `git push` PaaS — a managed container platform built on **dynos**, buildpacks, and add-ons. The identity pairs a confident **brand purple** with a bright **mint-teal** accent; light-first, developer-warm.

---

## Colors

Traced from live `heroku.com` CSS (2025 redesign).

### Primary — purple
| Token | Hex | Usage |
|---|---|---|
| `--brand` | `#5A1BA9` | Primary brand violet — buttons, links, `----->` build arrows, active states |
| `--brand-deep` | `#300B60` | Deep purple — hero gradients, footers, deepest surfaces |
| `--mark` | `#6762A6` | The logomark rounded-square purple (fixed on the logo) |
| `--brand-tint` | `rgba(90,27,169,.08)` | Purple wash — active nav, selected rows |

### Accent
| Token | Hex | Usage |
|---|---|---|
| `--teal` | `#5EEAD4` | Signature mint accent — highlights, deploy success ticks, hero art (30× in live CSS) |
| `--teal-ink` | `#0E9A87` | Darkened teal for legible teal *text* on light surfaces (contrast trap) |
| `--coral` | `#EE643F` | Secondary accent — illustration, warning-ish highlights |
| `--gold` | `#F7B500` | Tertiary accent — badges, sparingly |

### Semantic (dyno / build state)
| State | Hex |
|---|---|
| Building / running | `#5A1BA9` purple |
| Succeeded / up | `#0E9A87` teal-ink (light) / `#5EEAD4` teal (dark) |
| Crashed / error | `#EE643F` coral-red |
| Idle / scaled-to-zero | `#8A85A0` slate |

### Surfaces & text
| Token | Light | Dark |
|---|---|---|
| `--bg` | `#FFFFFF` | `#1A1523` |
| `--bg2` | `#F7F5FB` | `#211A2E` |
| `--surface` | `#FFFFFF` | `#241D33` |
| `--border` | `#E7E2F1` | `#372B4D` |
| `--text` | `#1B1B29` | `#F2EEF9` |
| `--text2` | `#55506B` | `#B8AECC` |
| `--text3` | `#8A85A0` | `#7E7594` |
| `--brand` (themed) | `#5A1BA9` | `#A78BEA` (lightened for contrast) |

The build/deploy terminal is **always dark** (`#17141F`) in both themes — like a real `git push heroku main` session.

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / UI / body | **BentonSans** | Heroku's brand humanist sans. Self-hosted on `heroku.com`, **CORS-open (`access-control-allow-origin: *`) → used directly.** Weights: regular 400, medium 500. |
| Code / terminal / dyno | **JetBrains Mono** | Build logs, `heroku` CLI, dyno counts, app URLs (Google Fonts; Heroku ships no brand mono). |

Hierarchy: BentonSans medium for H1/H2/labels/buttons; regular for body. Mono is reserved for the CLI/terminal, app names, and dyno formation.

---

## Logo

Real Heroku **logomark** — a rounded square (`fill:#6762A6`, recolored to `--brand` for cohesion) enclosing a white geometric **"h"** (viewBox `0 0 5.12 5.12`, 2 paths), from the official vector asset. Paired with a **"Heroku"** wordmark set in BentonSans (`fill:var(--logo-text)`, themed).

**Theming:** mark square = brand purple (fixed hue) · wordmark text = `var(--logo-text)` (near-black on light / near-white on dark).

---

## Components

- **Buttons** — Primary: `background:var(--brand)`, white text, radius 6px, BentonSans medium. Secondary: transparent, 1px border. Never put purple text on a purple button.
- **Dyno pill** — process-type chip (`web`, `worker`) + count stepper. Running dynos render as purple blocks; scaled-to-zero as hollow slate.
- **Build-arrow line** — the iconic `----->` prefixed step, arrow in `--brand`, message in terminal text.
- **Add-on chip** — `heroku-postgresql`, `heroku-redis` etc., mono, teal-tinted.

---

## Signature — `git push heroku main`

The unmistakable Heroku moment: push code, watch the remote build stream, scale dynos.

- **Deploy terminal** (always dark): `$ git push heroku main` → streamed build log — buildpack detection, `-----> Python app detected`, dependency install, `Discovering process types`, `Compressing`, `Launching`, `Released v23`, `https://calm-river-4823.herokuapp.com deployed to Heroku`. Purple `----->` arrows, teal success. **Deploy** replays deterministically (index-driven, no `Math.random`).
- **Dyno formation**: app `calm-river-4823`, process types `web` / `worker`, each with a `− N +` scale stepper rendering dyno blocks and a live `heroku ps:scale web=N` echo + monthly cost estimate.

---

## Guardrails

### DO
- Lead with brand purple `#5A1BA9`; use teal `#5EEAD4` as the bright accent.
- Darken teal to `#0E9A87` when it must be *text* on a light surface.
- Keep the build terminal dark in both themes.
- Use BentonSans everywhere except code/CLI (JetBrains Mono).
- Call the units **dynos**; use real buildpack/process-type language.

### DON'T
- Don't use teal `#5EEAD4` as small text on white — it fails contrast.
- Don't put purple text on the purple primary button.
- Don't invent deploy copy — mirror real Heroku build-log phrasing (`-----> …`, `Released vN`).
- Don't use `Math.random()` in the signature — keep deploys deterministic.
