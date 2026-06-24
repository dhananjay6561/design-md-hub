# Deno — Design System

Uncomplicate JavaScript. Deno is a modern JavaScript/TypeScript runtime with a secure-by-default architecture, built-in tooling, and native TypeScript support. Deno Deploy brings serverless JavaScript to the edge.

---

## Colors

### Brand

All confirmed from `--color-*` CSS custom properties in production (`deno.com/styles/app.css`).

| Token | Hex | Usage |
|---|---|---|
| black | `#0B0D11` | Primary black — body text, solid backgrounds |
| offblack | `#121417` | Near-black — dark surface alternative |
| default | `#12124B` | Deep navy/indigo — brand anchor color |
| runtime | `#70FFAF` | Neon green — Deno runtime accent |
| runtime-dark | `#172723` | Dark green surface for runtime sections |
| deploy | `#01C2FF` | Bright cyan — Deno Deploy primary |
| deploy-dark | `#0C212A` | Dark cyan surface for Deploy sections |
| fresh | `#FFDB1E` | Yellow — Fresh framework accent |
| fresh-dark | `#401C00` | Dark warm bg for Fresh sections |

### Deploy Color Scale (confirmed)

| Step | Hex |
|---|---|
| 50 | `#F0F7FF` |
| 100 | `#E0F0FF` |
| 200 | `#B3E0FF` |
| 300 | `#66C2FF` |
| 400 | `#1A9FFF` |
| 500 | `#007ACC` |
| 700 | `#004166` |
| 800 | `#002633` |
| 950 | `#000A0D` |

### Deploy Neutral Scale (confirmed)

| Step | Hex | Usage |
|---|---|---|
| 50 | `#F8F9FC` | Light bg |
| 100 | `#F1F3F9` | Subtle bg |
| 200 | `#EAEDF5` | Element bg |
| 350 | `#CBD1E1` | Border secondary |
| 400 | `#A8B2C8` | Border / muted |
| 500 | `#64708B` | Text-3 / placeholder |
| 600 | `#475269` | Text-2 |
| 700 | `#242D3E` | Dark surface |
| 800 | `#171C2B` | Darker surface |
| 900 | `#0A0E1C` | Dark bg |
| 950 | `#020617` | Darkest bg |

### Syntax Highlight Colors (confirmed)

| Token | Hex |
|---|---|
| code-1 / blue | `#01C2FF` |
| code-3 / purple | `#AE01FF` |
| code-5 / yellow | `#FFD601` |
| code-6 / green | `#01FF67` |
| code-7 / magenta | `#DB01FF` |

---

## Typography

### Font Families

| Role | Family | Weights | Source |
|---|---|---|---|
| UI / Body | Inter | 400 / 700 | `deno.com/fonts/inter/Inter-Regular.woff2` |
| Deploy display | Moranga | 400 / 700 | `deno.com/fonts/deploy/Moranga-Regular.woff2` |
| Deploy UI / Mono | Recursive | 300–1000 (variable) | `deno.com/fonts/deploy/Recursive_Variable.woff2` |

CSS variable: `--font-deploy-sans: Recursive, Inter, ui-sans-serif` and `--font-deploy-mono: Recursive, ui-monospace`. Recursive is activated for mono output with `font-variation-settings: "MONO" 1, "CASL" 0, "CRSV" 0, "slnt" 0`.

### Type Scale

| Level | Size | Weight | Font |
|---|---|---|---|
| h1 | 48px | 700 | Inter |
| h2 | 32px | 700 | Inter |
| h3 | 20px | 600 | Inter |
| body-lg | 16px | 400 | Inter |
| body | 14px | 400 | Inter |
| label | 11px | 600 | Inter |
| mono / terminal | 13px | 400 | Recursive (MONO=1) |

---

## Spacing & Radius

Base unit: 4px

| Token | Value |
|---|---|
| radius-sm | 4px |
| radius-md | 6px |
| radius-lg | 8px |
| radius-xl | 12px |
| radius-full | 9999px |

---

## Components

### Buttons

| Variant | Background | Text | Border |
|---|---|---|---|
| Primary | `#0B0D11` | `#FFF` | — |
| Secondary | `#EAEDF5` | `#0B0D11` | — |
| Outline | transparent | `#0B0D11` | `1px #CBD1E1` |
| Deploy CTA | `#01C2FF` | `#0B0D11` | — |

### Deployment Status Badges

| Status | Background | Text |
|---|---|---|
| Success | `rgba(112,255,175,.12)` | `#70FFAF` |
| Failed | `rgba(239,68,68,.12)` | `#FF6B6B` |
| In Progress | `rgba(1,194,255,.12)` | `#01C2FF` |
| Cancelled | `rgba(100,112,139,.12)` | `#A8B2C8` |

---

## Guardrails

**DO**
- Use `#70FFAF` neon green exclusively as the Deno runtime brand accent — never for success status
- Use `#01C2FF` cyan for Deno Deploy CTAs and interactive states on dark backgrounds
- Use Recursive with `"MONO" 1` for all terminal output, logs, and code blocks
- Keep dark surfaces on the deploy neutral scale: 700 → 800 → 900 → 950 for depth
- Primary CTA on the marketing site is black (#0B0D11) — clean, confident, minimal

**DON'T**
- Don't use `#70FFAF` (runtime green) for success badges — it's a brand color, not a semantic one
- Don't use `#FFDB1E` (fresh yellow) in Deploy or Runtime contexts — each product color is scoped
- Don't mix Moranga with Inter in the same context — Moranga is Deploy display only
- Don't use pure `#000` — Deno's black is `#0B0D11` (slight blue-black tint)
- Don't apply the deploy neutral scale to non-Deploy pages — use Tailwind gray for the main site
