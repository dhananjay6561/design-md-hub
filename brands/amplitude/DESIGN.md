# Amplitude Design System

## Brand Overview

Amplitude is "the AI analytics platform for modern digital analytics" — the tool teams use to *see what users do and improve what matters.* The identity is data-forward and confident: a single electric **brand blue `#1E61F0`**, blue→purple gradients for charts and highlights, and **warm off-white** neutrals (`#F5F4F0`) that keep dense dashboards from feeling clinical. Headings run in **Gellix** (geometric, characterful); body and UI in **IBM Plex Sans**; code in **IBM Plex Mono**.

Light-first: the marketing site and product both lead with warm-white surfaces and let the blue/purple data-viz carry the color.

> Verified live from amplitude.com (2026). Brand blue `#1E61F0` confirmed 29× in the production CSS; fonts confirmed Gellix (CORS-clean CDN) + the IBM Plex family.

## Color Palette

### Primary — brand blue
- **Blue**: `#1E61F0` — primary CTAs, links, chart lines, active states
- **Blue Deep**: `#0052F2` — hover/pressed, highlights
- **Blue Light**: `#3D6BFF` — dark-mode brand, secondary series
- **Navy**: `#001A4F` — deep gradient anchor, dark accents

### Data-viz gradient (blue → purple)
- **Purple**: `#A273FF` — second metric, gradient top
- **Purple Deep**: `#7C3AED` — purple text/accents
- Chart fills run `#1E61F0 → #A273FF` at low opacity — the signature Amplitude look

### Neutrals — warm
- **Ink**: `#0C0C0E` — headings, body
- **Grey**: `#373D42` · **Grey 2**: `#50565B` · **Muted**: `#868D95` · **Muted 2**: `#697077`
- **Warm off-white**: `#F5F4F0` (page) · **Warm border**: `#E8E7E2` · **White**: `#FFFFFF`
- **Cool tint**: `#F2F4F8` (hover, subtle fills)

### Semantic
- **Success**: `#00A86B` (uplift, positive delta)
- **Warning**: `#B26A00`
- **Error**: `#D64545` (negative delta)
- **Info**: `#1E61F0`

## Typography

Three fonts, one role each. Gellix is CORS-clean from its CDN; the IBM Plex family is on Google Fonts.

- **Display — Gellix** (400–800): hero, page + section headings
- **UI / Body — IBM Plex Sans** (300–700): all body, labels, nav, buttons, UI, table cells
- **Mono — IBM Plex Mono** (400–600): metrics, event names, code, API

### Scale
| Token | Size | Weight | Font | Use |
|-------|------|--------|------|-----|
| display | 56px | 700 | Gellix | Hero |
| h1 | 34px | 700 | Gellix | Page title |
| h2 | 22px | 600 | Gellix | Section heading |
| body-lg | 17px | 400 | IBM Plex Sans | Lead paragraph |
| body | 14px | 400 | IBM Plex Sans | Default UI |
| small | 12px | 400 | IBM Plex Sans | Metadata |
| mono | 12px | 400 | IBM Plex Mono | Metrics, event names |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons / inputs: 8px
- Cards / chart panels: 12px
- Pills / event chips: 9999px
- Base: 4px

## Components

### Button
- **Primary**: brand blue `#1E61F0`, white text. Labels: `Get started`, `Book a demo`, `Add chart`
- **Secondary**: transparent, warm border. Labels: `Contact sales`, `Export`
- On dark, blue lifts to `#3D6BFF` for contrast — white text in both

### Event chip
Fully-rounded metric selectors (Page Viewed / Signup Started / …). Active = blue fill + white text; inactive = warm surface. The primary control of every chart.

### Chart
Line + gradient area fill (`#1E61F0 → #A273FF`, low opacity), endpoint dot, warm gridless plot. A big stat with a colored delta (green up / red down) sits above it.

### Delta stat
Large mono number + `▲ 12.4%` in success green or `▼ 3.2%` in error red — the core analytics readout.

## Signature — Event Segmentation

Amplitude's defining view: an event-trends chart driven by chips. Pick an event and the line + gradient area + headline stat update live; toggle the measure (Event Totals ↔ Unique Users) and the whole series rescales; switch the date range (7D / 30D / 90D) to reslice. Deterministic, real-feeling data — never random.

## Guardrails

**DO**
- Use brand blue `#1E61F0` for primary actions, links, and the main chart series — it is the brand
- Fill chart areas with the `blue → purple` gradient at low opacity — Amplitude's signature
- Set headings in Gellix, body/UI in IBM Plex Sans, code in IBM Plex Mono — one role each
- Color deltas semantically: green for uplift, red for decline — never the reverse
- Keep light surfaces warm (`#F5F4F0`) — the warmth is part of the identity

**DON'T**
- Don't set the brand blue on dark at `#1E61F0` — contrast fails; lift to `#3D6BFF`
- Don't use purple as a primary action — it's a data-viz accent, not a CTA
- Don't set body or UI in Gellix — it's display only; IBM Plex Sans owns the UI
- Don't cool the light neutrals to pure grey — Amplitude's off-white is warm
- Don't fabricate chart data — plot a real, deterministic series
</content>
