# Tailwind CSS Design System

## Brand Overview
Tailwind CSS is a utility-first CSS framework — "rapidly build modern websites without ever leaving your HTML." The brand is **dark-first**, engineered, and confident: deep slate surfaces, a single luminous **sky-cyan** accent (and its gradient), the famous Tailwind color scale on display, and a two-wave mark. Everything is systematic — the marketing *is* the design system: real tokens, real spacing, real utilities.

## Color Palette

### Brand
- **Sky 400** `#38BDF8` — the signature accent: mark, links, highlights, primary
- **Sky 500** `#0EA5E9` — hover / stronger accent
- **Sky 600** `#0284C7` — pressed / on-light accent
- **Sky 300** `#7DD3FC` — soft accent, dark-mode text-on-accent
- **Brand gradient** `#38BDF8 → #2563EB` (sky → blue-600) — hero washes, feature art

### Surfaces (dark-first — the slate scale)
- **Slate 950** `#020617` — page background
- **Slate 900** `#0F172A` — panels, cards
- **Slate 800** `#1E293B` — raised surfaces, code wells, hover
- **Slate 700** `#334155` — borders on dark
- **Slate 400** `#94A3B8` — muted text
- **Slate 200** `#E2E8F0` — primary text on dark
- **Slate 50** `#F8FAFC` — light-mode panel / white-ish

### Light mode
- Page `#FFFFFF` · panel `#F8FAFC` (slate-50) · border `#E2E8F0` (slate-200) · text `#0F172A` (slate-900) · muted `#64748B` (slate-500). Sky accent drops to `#0284C7` (sky-600) for text/links so it stays legible on white.

### The Tailwind scale (reference — the palette IS the product)
Each hue ships 50→950. Signature stops used across the docs:
`slate` neutral · `sky` brand · plus `rose #F43F5E` · `amber #F59E0B` · `emerald #10B981` · `violet #8B5CF6` · `blue #3B82F6`.

## Typography
Tailwind ships **Inter** (UI/body) and **IBM Plex Mono** (code) — both real, both on Google Fonts, used directly.
- **Display / UI** — `Inter` (variable) — headings, body, buttons, everything
- **Mono** — `IBM Plex Mono` — utility class names, code samples, the class-string bar

Headings tighten (`-0.02em` to `-0.04em`) and go heavy (700–800). Body is 400–500.

## Spacing
The Tailwind spacing scale — `0.25rem` (4px) base: `1`=4 · `2`=8 · `3`=12 · `4`=16 · `6`=24 · `8`=32 · `10`=40 · `12`=48 · `16`=64.

## Border Radius
`rounded` 4px · `rounded-lg` 8px · `rounded-xl` 12px · `rounded-2xl` 16px · `rounded-full` 9999px.

## Shadows
`shadow` `0 1px 3px rgb(0 0 0/.1)` · `shadow-lg` `0 10px 15px -3px rgb(0 0 0/.1)` · `shadow-2xl` `0 25px 50px -12px rgb(0 0 0/.25)`.

## Components

### Utility playground (signature)
A live preview element wired to grouped utility toggles (background / text / padding / radius / shadow / layout). Selecting a utility both restyles the element and appends the class to a monospace class-string bar — the core Tailwind loop made visible.

### Button
Sky primary (`bg-sky-400` dark / `bg-sky-500` on hover) with slate-950 text — sky is bright enough that dark text beats white (contrast trap). Secondary is a slate outline.

### Code / class token
Utility class names in IBM Plex Mono; the property prefix (`bg-`, `p-`, `rounded-`) tinted sky to read as syntax.

## Guardrails

**DO**
- Keep the mark's wave in sky `#38BDF8` (fixed); let the wordmark adapt to the theme.
- Build surfaces from the slate scale; use sky as the single accent.
- Use dark text on the sky button — sky is too bright for white text.
- Put utility class names and code in IBM Plex Mono.
- Reach for real scale tokens (slate-800, sky-400, p-6) — never arbitrary off-scale hexes/sizes when a token exists.

**DON'T**
- Don't introduce a second brand accent — sky owns it.
- Don't use pure black `#000` for surfaces — the darkest is slate-950 `#020617`.
- Don't put white text on `#38BDF8`.
- Don't recolor the sky wave in the mark.
- Don't set body copy in the mono face — Inter for text, Plex Mono for code only.
