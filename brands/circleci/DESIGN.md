# CircleCI Design System

## Brand Overview
CircleCI is the CI/CD platform for autonomous validation. The current identity — the internal **"Morph"** design system — is a sharp, terminal-flavored, **dark-first** look: a true near-black canvas, a deep midnight-navy for panels, a vivid **spring green** that reads as "passed," and a pixel display face for eyebrow labels that nods to the build-log heritage. Color is disciplined and semantic — green means passing, red means failed — with a soft pastel gradient (mint → cyan → pink → yellow) reserved for marketing hero moments only.

## Color Palette

### Primary
- **Green** `#00DB74` — brand, passing builds, primary success (the `positive`/`passed` token)
- **Green light** `#C4EDCF` — success tint / subtle fills
- **Blue** `#2152E5` — links, running jobs, interactive accents
- **Blue bright** `#0055FF` — hero / high-emphasis links

### Build status (semantic — never repurpose)
- **Success / passed** `#00DB74`
- **Running** `#2152E5` (animated pulse)
- **On hold / needs approval** `#DD9F54` (bronze)
- **Failed** `#CC4242`
- **Not run / queued** `#6A6A6A` (neutral)

### Surfaces (dark-first)
- **Terminal** `#161616` — page background (`--color-morph-terminal`)
- **Midnight** `#1C273A` — primary panels/cards (`--color-morph-midnight`)
- **Deep** `#0D1520` — wells, code areas
- **Slate** `#2E3C52` — raised surfaces, hover
- **Border** `rgba(255,255,255,.10)` — hairlines on dark

### Neutrals (light mode + text)
- **Fog** `#EDEDED`  ·  **Body light** `#FAFAFA`  ·  **Neutral-40** `#F7F7F7`
- **Cool grey** `#ECEEF2` / `#C5CAD4` / `#B4B8C6`  ·  **Neutral-400** `#6A6A6A`
- **Text on dark** `#FAFAFA` / muted `#B4B8C6` / faint `#6A6A6A`

### Morph gradient (marketing hero only)
- **Mint** `#B3FFDE` → **Cyan** `#83F1FF` → **Pink** `#FFBDFB` → **Yellow** `#FFF67B`

## Typography
All four Morph faces are on Google Fonts and used directly.
- **Display / "mega"** — `Space Grotesk` — hero H1, big headings
- **UI / body** — `Inter` — all product text, labels, buttons, job cards
- **Mono** — `Roboto Mono` — job names, branch names, commit SHAs, config, durations
- **Pixel** — `Silkscreen` — small uppercase eyebrow labels / section identifiers (terminal flavor)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 8px  ·  Cards / panels: 12px  ·  Job pills: 9999px (pill)  ·  Status badges: 6px  ·  Inputs: 8px

## Components

### Workflow graph (signature)
Jobs as pills laid out in stage columns, dependencies as directed connectors. Pill color/dot reflects live job status. Parallel jobs share a stage column. Approval jobs hold as bronze until manually approved.

### Pipeline row
Branch name + commit SHA in mono, status dot left, duration right; expands to its workflows.

### Job pill
Status dot + job name (mono) + duration (mono). Running jobs pulse; failed jobs are unmissable red.

### Button
Green `#00DB74` primary with terminal-black text (green is too bright for white text — a dual-theme contrast trap); secondary is a translucent-white outline on dark.

## Guardrails

**DO**
- Use `#00DB74` as the brand green — the retired `#04AA51`-style dull greens are legacy.
- Keep build-status colors strictly semantic (green passed / red failed / blue running / bronze on-hold).
- Put branch names, commit SHAs, job names, and durations in monospace.
- Pulse running jobs; make failed jobs prominent and impossible to miss.
- Use black text on the green button — never white (contrast trap).

**DON'T**
- Don't use the Morph pastel gradient inside product UI — it's marketing-hero only.
- Don't put white text on `#00DB74`.
- Don't repurpose status colors for decoration.
- Don't hide duration on completed jobs.
- Don't use the pixel face (Silkscreen) for body or long strings — short uppercase labels only.
