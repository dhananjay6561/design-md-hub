# GitLab Design System

## Brand Overview

GitLab is the AI-native platform for the entire software lifecycle — "Ship faster. With trust." The identity pairs the unmistakable **tanuki** (a three-tone orange mark) with a confident **brand purple `#7759C2`** and a deep purple-black ink `#171321`. The design language (Pajamas) is calm, dense, and developer-first: purple drives actions, orange carries the brand and "in-progress" energy, and status color (green/blue/red) does the heavy lifting in the product.

Light-first: about.gitlab.com leads with white/lilac surfaces and purple accents; the product and footers use the dark purple-black `#171321`.

> Verified live from about.gitlab.com (2026). Tanuki fills, brand purple `#7759C2`, and ink `#171321` confirmed in the live markup. GitLab Sans / GitLab Mono are served without CORS, so this reference uses their open-source lineage — **Inter** (GitLab Sans is Inter-derived) and **JetBrains Mono** (GitLab Mono is JetBrains-Mono-derived).

## Color Palette

### Primary — brand purple
- **Purple**: `#7759C2` — brand purple, active/selected
- **Purple Deep**: `#6E49CB` — primary CTAs
- **Purple Dark**: `#380D75` — deep accent, dark surfaces
- **Purple Pale**: `#F6F3FE` — hover, subtle fills (light)

### Tanuki — the mark (fixed)
- **Red-orange**: `#E24329` · **Orange**: `#FC6D26` · **Light orange**: `#FCA326`
- Orange doubles as the "running / in-progress" accent

### Neutrals
- **Ink**: `#171321` — headings, body, dark page
- **Grey**: `#74717A` — secondary text
- **Border**: `#D1D0D3` · **Fill**: `#E8E7EB` · **Page tint**: `#F2F1F5` · **White**: `#FFFFFF`

### Status (Pajamas / pipelines)
- **Passed**: `#108548` (green)
- **Running**: `#1F75CB` (blue)
- **Failed**: `#DD2B0E` (red)
- **Pending / manual**: `#89888D` (grey)

## Typography

Two fonts, one role each — the open-source equivalents of GitLab's brand fonts, both on Google Fonts.

- **UI / Body / Display — Inter** (≈ GitLab Sans) (400/500/600/700): headings, body, nav, buttons, UI
- **Mono — JetBrains Mono** (≈ GitLab Mono) (400/500): job names, SHAs, code, pipeline meta

### Scale
| Token | Size | Weight | Font | Use |
|-------|------|--------|------|-----|
| display | 52px | 700 | Inter | Hero |
| h1 | 32px | 700 | Inter | Page title |
| h2 | 22px | 600 | Inter | Section heading |
| body-lg | 17px | 400 | Inter | Lead paragraph |
| body | 14px | 400 | Inter | Default UI |
| small | 12px | 400 | Inter | Metadata |
| mono | 12px | 400 | JetBrains Mono | SHAs, job names, code |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons / inputs: 8px
- Cards / panels: 8px
- Job nodes: 8px
- Pills / badges: 9999px
- Base: 4px

## Components

### Button
- **Primary**: purple `#6E49CB`, white text. Labels: `Get free trial`, `Run pipeline`, `Merge`
- **Secondary**: transparent, `--border-strong` outline. Labels: `Contact sales`, `Edit`
- On dark, purple lifts to `#8151E6` for contrast — white text in both

### Status badge / job node
Pill (or 8px node) with a status icon + label: passed (green ✓), running (blue ◔, animated), failed (red ✕), pending/manual (grey). The atom of every pipeline.

### Pipeline stage
A column of job nodes per stage (build / test / deploy), connected by curved lines — the core CI/CD visual.

## Signature — CI/CD Pipeline

GitLab's defining view: a staged pipeline graph. **Run pipeline** resets every job to pending, then runs them stage by stage — build → test (parallel) → deploy — each node animating pending → running → passed, with the overall status badge updating live and `deploy:production` held as a manual play step. Real-looking job names, stages, and a `#pipeline` id.

## Guardrails

**DO**
- Use purple `#6E49CB` for primary actions — purple is the action color
- Keep the tanuki three-tone (`#E24329 / #FC6D26 / #FCA326`) — never recolor or flatten it
- Use orange for brand + in-progress energy, and green/blue/red for pipeline status
- Set UI/headings in Inter (GitLab Sans), code/SHAs in JetBrains Mono (GitLab Mono)
- Lift purple to `#8151E6` on the dark purple-black so it stays legible

**DON'T**
- Don't set the brand purple on dark at `#7759C2` — contrast dips; lift it
- Don't use tanuki orange as a primary button — it's brand/accent, not the CTA
- Don't tint dark surfaces neutral-grey — GitLab's dark is purple-black `#171321`
- Don't color a passed job orange or a running job green — status color is semantic
- Don't fabricate pipeline data — use real stage/job names and a deterministic run
</content>
