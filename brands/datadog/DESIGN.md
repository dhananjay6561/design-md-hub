# Datadog — Design System

AI-powered observability and security. Datadog is the monitoring platform for cloud-scale infrastructure — surfacing metrics, traces, logs, and alerts in one unified interface for engineers who live in dashboards.

---

## Colors

### Brand

| Token | Hex | Usage |
|---|---|---|
| brand-purple | `#632CA6` | Primary brand, logo mark, CTAs, nav active state |
| neon-purple | `#8000FF` | Marketing gradient start, accent highlights |
| hot-pink | `#FF0080` | Marketing gradient end, graph accent |
| lemon | `#FFCF00` | Warning monitors, alert indicators |
| mint | `#00CF72` | OK status, success indicators |

### Purple Scale

| Step | Hex |
|---|---|
| 50 | `#EFE0FF` |
| 100 | `#CCADFF` |
| 200 | `#BEAAFF` |
| 400 | `#8000FF` |
| 600 | `#632CA6` |
| 800 | `#4B01AD` |
| 900 | `#34005E` |

### Surfaces

> **Confirmed sources:** `#F9F8F8` (light bg — CSS, 10 occurrences), `#F0EAF7` (elevated light — Tailwind utility class), `#110617` (darkest confirmed dark — CSS var `--callout-bg-gradient`). Dark product surface values below are **estimated** — app.datadoghq.com requires login and has no public CSS tokens. Derived by stepping lightness up from `#110617` with the brand's purple-navy hue.

| Token | Dark | Light | Dark confirmed? |
|---|---|---|---|
| bg | `#1A1E2C` | `#F9F8F8` | estimated |
| surface | `#232838` | `#FFFFFF` | estimated |
| elevated | `#2C3347` | `#F0EAF7` | estimated / light confirmed |
| border | `#3A4258` | `#DDD5EC` | estimated |
| text | `#FFFFFF` | `#110617` | confirmed (light text = confirmed hero dark) |
| text-2 | `#AAB1C1` | `#4A4A6A` | estimated |
| text-3 | `#6B7A97` | `#7A6A9A` | estimated |

### Semantic

| Role | Dark bg | Dark text | Light bg | Light text |
|---|---|---|---|---|
| OK / Success | `rgba(0,207,114,.12)` | `#00CF72` | `rgba(0,207,114,.10)` | `#007A43` |
| Warning | `rgba(255,207,0,.12)` | `#FFCF00` | `rgba(255,207,0,.12)` | `#8A6E00` |
| Critical / Error | `rgba(255,58,68,.12)` | `#FF3A44` | `rgba(255,58,68,.10)` | `#C0000A` |
| Info | `rgba(0,96,255,.12)` | `#0060FF` | `rgba(0,96,255,.10)` | `#0050CC` |
| No Data | `rgba(107,122,151,.12)` | `#6B7A97` | `rgba(107,122,151,.10)` | `#4A5568` |

### Marketing Gradients

| Name | Value |
|---|---|
| CTA gradient | `linear-gradient(90deg, #8000FF 0%, #FF0080 100%)` |
| Hero callout | `linear-gradient(360deg, #8904FF, #110617)` |
| Blog accent | `linear-gradient(90deg, #6A00FF 0%, #FFC8F9 100%)` |

---

## Typography

### Font Families

| Role | Family | Weights | Source |
|---|---|---|---|
| Display / UI | NationalWeb | 300 / 400 / 600 / 700 | `datadoghq.com/fonts/web-fonts/` |
| Code / Metrics / Queries | Roboto Mono | 400 / 700 | `datadoghq.com/fonts/web-fonts/` |

### Type Scale

| Level | Size | Weight | Line Height | Font |
|---|---|---|---|---|
| h1 | 40px | 600 | 1.15 | NationalWeb |
| h2 | 28px | 600 | 1.2 | NationalWeb |
| h3 | 20px | 600 | 1.3 | NationalWeb |
| body-lg | 16px | 400 | 1.6 | NationalWeb |
| body | 14px | 400 | 1.5 | NationalWeb |
| label | 11px | 600 | 1 | NationalWeb |
| metric | 28px | 600 | 1 | Roboto Mono |
| code | 13px | 400 | 1.6 | Roboto Mono |

---

## Spacing & Radius

Base unit: 4px

| Token | Value |
|---|---|
| radius-sm | 3px |
| radius-md | 4px |
| radius-lg | 6px |
| radius-xl | 8px |

---

## Components

### Buttons

| Variant | Background | Text | Border |
|---|---|---|---|
| Primary | `linear-gradient(90deg, #8000FF, #FF0080)` | `#FFF` | — |
| Purple | `#632CA6` | `#FFF` | — |
| Ghost | transparent | `#AAB1C1` | `1px #3A4860` |
| Danger | `#FF3A44` | `#FFF` | — |

### Monitor Status Badges

| Status | Dark bg | Dark text |
|---|---|---|
| OK | `rgba(0,207,114,.12)` | `#00CF72` |
| Warn | `rgba(255,207,0,.12)` | `#FFCF00` |
| Alert / Critical | `rgba(255,58,68,.12)` | `#FF3A44` |
| No Data | `rgba(107,122,151,.12)` | `#6B7A97` |
| Ignored | `rgba(107,122,151,.08)` | `#6B7A97` |

### Metric Widget

```
bg: var(--surface)
border: 1px solid var(--border)
radius: 6px
value: 28px 600 Roboto Mono var(--text)
unit: 12px NationalWeb var(--text-3)
label: 11px 600 NationalWeb var(--text-2)
```

### Tags / Service Labels

```
bg: rgba(99,44,166,.15)
text: #BEAAFF
border: rgba(99,44,166,.30)
font: 11px 600 NationalWeb
radius: 3px
padding: 2px 6px
```

---

## Guardrails

**DO**
- Use Roboto Mono for all metric values, log lines, query results, and trace IDs
- Use `#632CA6` purple as the single interactive/CTA color in product UI
- Use the neon/pink gradient for marketing CTAs only — never in the product
- Keep dark mode as the default — engineers run Datadog during incidents, light mode strains eyes
- Color-code monitor status consistently: green OK, yellow Warn, red Alert — always

**DON'T**
- Don't use IBM Plex, Inter, or any Google Font — NationalWeb is the brand font
- Don't use pure `#000000` or `#FFFFFF` as backgrounds — the brand dark is `#1C222D`
- Don't use the neon purple `#8000FF` for interactive states in the product — `#632CA6` owns that role
- Don't round corners beyond 8px — enterprise products stay sharp
- Don't use hot pink `#FF0080` for alert or error states — that color is graph/marketing only
