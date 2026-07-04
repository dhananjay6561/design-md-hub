# Contentful Design System

## Brand Overview
Contentful is the composable content platform (now positioned as a **DXP** — digital experience platform) for headless content and AI-driven digital experiences. The current identity (post-rebrand) is bright, optimistic and editorial: a clean white canvas, one confident **electric blue**, soft pastel section washes, and the tri-color **orbit** mark. It reads as a modern content workspace built for both marketers and developers.

> **Rebrand note (verify against live):** the legacy navy `#2536CC` / deep-blue identity is **retired**. The current brand blue is `#1770E6`, and the mark is a full-color orbit (blue + orange + yellow), never flat navy.

## Color Palette

### Primary
- Brand Blue: `#1770E6` — primary actions, links, focus (dominant on live site)
- Blue Deep: `#2C407D` — headings-on-tint, deep accents
- Ink: `#2B2D31` — wordmark, primary text on light

### Orbit mark (fixed, never recolor)
- Mark Blue: `#1773EB`
- Mark Orange: `#E44F20`
- Mark Yellow: `#FFDA00`

### Section washes (pastel, light mode)
- Purple wash: `#F4EAFD`
- Orange wash: `#FCEDE9`
- Green wash: `#D8F6E7`
- Teal ink: `#4A6E70`

### Backgrounds — Light (default)
- Base: `#FFFFFF`
- Surface: `#F7F7F8`
- Elevated: `#FFFFFF`
- Border: `#E6E6E9`

### Backgrounds — Dark
Contentful is light-first with no rich dark palette; dark surfaces are stepped within a neutral near-black hue (anchored on the ink), with translucent-white borders.
- Base: `#17181A`
- Surface: `#1F2023`
- Elevated: `#27282B`
- Border: `rgba(255,255,255,.09)`

### Text
- Primary (light): `#2B2D31` / (dark): `#F3F3F4`
- Secondary: `#5C5F66` / `#A9ABB0`
- Muted: `#8A8D93` / `#71747A`

### Content status (Contentful web app entry workflow)
- Draft: `#C77700` (amber)
- Changed: `#1770E6` (blue)
- Published: `#0C8A5A` (green)
- Archived: `#8A8D93` (gray)

### Semantic
- Success: `#0C8A5A`
- Warning: `#C77700`
- Error: `#E44F20`
- Info: `#1770E6`

## Typography

### Font Stack
- Display / UI: `Avenir Next` — the real brand font, self-hosted by Contentful (`avenirNextFont`, `.woff`, CORS-open), weights **400** and **600**. Fallback: `Avenir, Montserrat, system-ui, sans-serif`.
- Code / IDs: `JetBrains Mono, monospace` (Contentful ships no branded mono).

### Scale
- xs: 11px / 1.5
- sm: 13px / 1.5
- base: 15px / 1.6
- md: 17px / 1.4
- lg: 22px / 1.3
- xl: 30px / 1.2
- 2xl: 44px / 1.05

### Weights
- Regular: 400
- Semibold: 600 (headings, buttons, emphasis — Avenir Next ships only 400/600)

## Components

### Buttons
- Primary: brand blue `#1770E6`, white text, radius 8px — "Get started for free"
- Secondary: transparent, 1px border, ink text — "Contact sales"
- Ghost / link: brand blue text — "Explore Contentful Platform"

### Entry status pill
Rounded pill carrying the workflow state: Draft (amber), Changed (blue), Published (green), Archived (gray). Always paired with a colored dot.

### Field row (content model)
Label + field-type chip (`Short text`, `Rich text`, `Reference`, `Boolean`) + input. Structured, editorial spacing.

## Signature Component — Entry Editor
Contentful's core value is **structured content + a publish workflow**. The signature is the web-app **Entry Editor**: a `blogPost` entry with typed fields (Title, Slug auto-generated, Rich-text body with a toolbar, a linked reference, a Boolean), and a right sidebar with the status pill + Publish button. Editing any field flips the status `Published → Changed`; pressing **Publish** commits it back to `Published`. This is the single UI most associated with Contentful.

## Guardrails

**DO**
- Use `#1770E6` as the one confident brand blue.
- Keep the orbit mark full-color (blue/orange/yellow) — it's the identity.
- Keep the canvas light and airy; use pastel washes to segment sections.
- Use the real entry-status colors and the Draft → Changed → Published workflow.
- Use Avenir Next (real font) for everything but code.

**DON'T**
- Don't use the legacy navy `#2536CC` or a dark-navy page background — that identity is retired.
- Don't flatten or single-color the orbit mark.
- Don't invent saturated dark-navy surfaces; dark mode is neutral near-black.
- Don't use bold weights other than 600 (the brand font ships only 400/600).
- Don't mix mono into body text — mono is for slugs, IDs, and code only.
