# WorkOS Design System

## Brand Overview
WorkOS makes apps **Enterprise Ready** — SSO, Directory Sync (SCIM), Audit Logs, and AuthKit for B2B SaaS. The identity is polished and enterprise-grade: a deep **navy** canvas, a confident **indigo** brand color, a fresh **mint** for active/success states, and a small support spectrum (blue, periwinkle, purple). It reads trustworthy and developer-first — compliance without the drab.

> **Palette note (verify against live):** the real brand indigo is `#6363F1` with blue `#558ADB`, periwinkle `#B1B3F6`, mint `#23F0C3`, and purple `#D272FF`; dark surfaces are true navy (`#030527` / `#181B39`), not generic near-black.

## Color Palette

### Primary
- Brand Indigo: `#6363F1` — actions, links, the logo mark
- Blue: `#558ADB` — secondary accent
- Periwinkle: `#B1B3F6` — accents on dark
- Mint: `#23F0C3` — active / success / connected
- Purple: `#D272FF` — spectrum accent

### Backgrounds — Dark (default)
- Base: `#030527` — deep navy page
- Surface: `#0E1330`
- Elevated: `#181B39`
- Raised: `#24274C`
- Border: `rgba(255,255,255,.10)`

### Backgrounds — Light
- Base: `#F9F9FB`
- Surface: `#FFFFFF`
- Border: `#E8EAED`

### Text
- Primary (dark): `#F5F6FF` / (light): `#030527`
- Secondary: `#8F96BD` / `#5D6C7B`
- Muted: `#5D6485`

### Connection status
- Active: `#23F0C3` (mint)
- Validating: `#6363F1` (indigo, in progress)
- Pending: `#F5A623` (amber)
- Draft: `#8F96BD` (gray)
- Error: `#EA384C`

## Typography

### Font Stack (real WorkOS fonts)
- Display / UI: **Untitled Sans** (Klim, proprietary) — approximated by **Inter**, which WorkOS also ships as its fallback. `Inter, "Untitled Sans", system-ui, sans-serif`.
- Code / mono: **IBM Plex Mono** (real WorkOS mono, Google Fonts) — org ids, connection ids, code.

### Scale
- xs 11 / sm 13 / base 15 / md 18 / lg 22 / xl 30 / 2xl 46

### Weights
Regular 400 · Medium 500 · Semibold 600 · Bold 700

## Components

### Buttons
- Primary: indigo `#6363F1`, white text, radius 8px — "Get started"
- Secondary: transparent, 1px border — "Talk to an expert"
- Ghost / link: indigo text — "Read the docs"

### Connection row
Org name + identity-provider label (IBM Plex Mono) + connection type (SSO/SAML, SCIM) + status pill. Draft/Pending rows expose a **Provision** action.

### Status pill
Rounded pill + dot; colors map to the connection-status table (Active mint / Validating indigo / Pending amber / Draft gray).

## Signature Component — SSO Connections
WorkOS's core value is **enterprise connections** — wiring a customer's identity provider into your app. The signature is the Dashboard **Organizations / SSO Connections** panel: a stat header (organizations, active connections), and a table of enterprise orgs each with their IdP (Okta, Azure AD, Google Workspace, OneLogin, Entra ID), connection type, and status. **Provisioning** a Draft/Pending connection steps it `Draft → Validating (indigo spinner) → Active (mint)` and bumps the active count. This is the single UI most associated with WorkOS.

## Guardrails

**DO**
- Use indigo `#6363F1` for the brand and mark; mint `#23F0C3` for active/connected.
- Keep dark surfaces true navy (`#030527` / `#181B39`), not generic black.
- Render org ids, connection ids, and IdP labels in IBM Plex Mono.
- Map connection status to its fixed colors consistently.

**DON'T**
- Don't swap indigo for a generic purple, or drop the mint active state.
- Don't use a flat near-black `#09090B` page — it's navy.
- Don't render connection/org identifiers in a proportional font.
- Don't overuse the purple/blue spectrum — indigo leads, mint signals success.
