# PagerDuty Design System

## Brand Overview

PagerDuty is "the AI-first operations platform" — the tool on-call engineers live in when something breaks. The identity is high-signal and calm-under-pressure: the brand **green `#06AC38`**, an energetic **electric-jade `#ADF07E`** for actions, a deep **cosmic-ocean navy `#082B56`**, and a near-black `#09090B` operations surface. Incident status color (red triggered → amber acknowledged → green resolved) does the semantic work everywhere.

Dark-first: incident response happens in dark dashboards at 3am. Green is the brand; electric-jade drives the primary action.

> Verified live from pagerduty.com (2026). `--color-accent: #06AC38` and the electric-jade tokens (`#ADF07E` / `#9EE86A`) confirmed in the production CSS; the "Plain" brand font (`plainFont`) is self-hosted without CORS, so this reference uses **Inter** (a close neo-grotesque) plus **JetBrains Mono** for incident IDs/timestamps.

## Color Palette

### Primary
- **Green**: `#06AC38` — brand, the mark, resolved status, accents
- **Green Deep**: `#048A24` — hover, green text on light
- **Electric Jade**: `#ADF07E` — primary CTA (dark text on it), energetic accent (hover `#9EE86A`)
- **Cosmic Ocean**: `#082B56` — deep navy, secondary surfaces

### Incident status (semantic — the core)
- **Triggered**: `#FB2C36` red
- **Acknowledged**: `#FAC800` amber/yellow
- **Resolved**: `#22C55E` / `#06AC38` green

### Neutrals (zinc)
- **Ink**: `#09090B` — dark page, headings
- **Grey**: `#525252` · **Muted**: `#737373` · **Line**: `#A3A3A3`
- **Border**: `#E5E5E5` · **Fill**: `#F5F5F5` · **Off-white**: `#FAFAFA` · **White**: `#FFFFFF`

## Typography

Two fonts, one role each. Plain is CORS-locked, so this reference approximates it with Inter; mono is not a branded PagerDuty face.

- **UI / Body / Display — Inter** (≈ Plain) (300/400/500/700): headings, body, nav, buttons, UI
- **Mono — JetBrains Mono** (400/500): incident IDs, timestamps, service names, code

### Scale
| Token | Size | Weight | Font | Use |
|-------|------|--------|------|-----|
| display | 52px | 700 | Inter | Hero |
| h1 | 32px | 700 | Inter | Page title |
| h2 | 22px | 600 | Inter | Section heading |
| body-lg | 17px | 400 | Inter | Lead paragraph |
| body | 14px | 400 | Inter | Default UI |
| small | 12px | 400 | Inter | Metadata |
| mono | 12px | 400 | JetBrains Mono | Incident IDs, timestamps |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons / inputs: 8px
- Cards / panels: 12px
- Status pills: 9999px
- Base: 6px

## Components

### Button
- **Primary**: electric-jade `#ADF07E`, **dark `#09090B`** text (jade is too light for white). Labels: `Get a demo`, `Acknowledge`, `Resolve`
- **Secondary**: transparent, `--border-strong` outline. Labels: `Escalate`, `View runbook`
- Green `#06AC38` is the brand/resolved color, not the default CTA

### Status badge
Pill with a status dot: triggered (red), acknowledged (amber), resolved (green). The atom of every incident.

### Incident row
Severity tag (SEV-1…3) + title + service (mono) + urgency + status badge. Clicking opens its timeline.

### Timeline entry
Timestamp (mono) + colored dot by kind (triggered / ack / resolved / note) + actor & action — the audit trail of a response.

## Signature — Incident Response

PagerDuty's defining view: an incident list beside a live timeline. Select an incident to see its escalation timeline; **Acknowledge** flips it to amber and appends "Acknowledged by …", **Resolve** flips it to green and closes it out — the exact triggered → acknowledged → resolved lifecycle, with real service names and SEV levels.

## Guardrails

**DO**
- Use electric-jade `#ADF07E` with **dark text** for the primary action — never white on jade
- Use brand green `#06AC38` for the mark, resolved state, and accents
- Color incident status semantically: red triggered, amber acknowledged, green resolved — never swap
- Set UI in Inter (≈ Plain), incident IDs / timestamps in JetBrains Mono
- Keep operations surfaces dark (`#09090B`) — that's where on-call lives

**DON'T**
- Don't put white text on electric-jade or green buttons — contrast fails; use dark ink
- Don't use green for a triggered/unresolved incident — green means resolved
- Don't tint dark surfaces navy-heavy — the ops surface is near-black zinc, navy is an accent
- Don't render incident timestamps or IDs in a sans — mono carries the log
- Don't fabricate incident data — use real SEV levels, service names, and a real lifecycle
</content>
