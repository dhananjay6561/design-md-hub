# Storybook Design System

## Brand Overview
Storybook is the frontend workshop for building, testing, and documenting UI components in isolation. The identity is friendly and tool-like: a rounded, warm **Nunito Sans** voice, a hot **coral-pink** brand mark (the "book"), and a calm neutral chrome that gets out of the way so the *component* is the hero. It's **light-first** (the Manager UI ships light) with a true dark theme, and it leans on a small, confident accent set — pink for brand, blue for links, plus a status spectrum.

## Color Palette

### Brand
- **Coral** `#FF4785` — the signature: mark, primary buttons, active nav, selection
- **Blue** `#1EA7FD` — links, focus, informational (the "ocean" accent)
- **Blue alt** `#029CFD` — pressed / stronger link
- **Seafoam** `#37D5D3` — teal accent, decorative highlights

### Status spectrum (addon/badge semantics)
- **Positive** `#66BF3C` (green) · **Warning** `#FDA700` (gold) · **Negative** `#FF4400` (red-orange) · **Purple** `#6F2CAC`

### Neutrals & surfaces
- **Ink** `#2E3438` — primary text (light mode)
- **Medium** `#73828C` — secondary text, muted labels
- **Light border** `#D9E0E6` — hairlines, control borders
- **Panel** `#F6F9FC` — sidebar, addons panel, secondary surfaces
- **White** `#FFFFFF` — canvas, cards, page

### Dark theme
- **Page/sidebar** `#1B1C1D` · **Panel** `#222425` · **Canvas** `#131415`
- **Border** `#292C2E` / `#35393B` · **Text** `#C9CDCF` / muted `#98A0A6`
- Coral `#FF4785` is retained; links lift to `#4CB3FF`.

## Typography
Storybook ships **Nunito Sans** as its brand/UI font (real, on Google Fonts, used directly). Code uses a system monospace stack.
- **UI / body / headings** — `Nunito Sans` — nav, labels, controls, story names, buttons (700–800 for headings, 400–600 for UI)
- **Mono** — `ui-monospace, SFMono-Regular, Menlo, …` (values, code snippets, arg types) — here rendered with `JetBrains Mono` as the mono stand-in

Nunito Sans's rounded terminals *are* the friendliness — don't swap it for a sharp grotesque.

## Spacing
Storybook design-system scale (px): 4, 8, 12, 16, 20, 24, 32, 40, 48.

## Border Radius
- Controls / inputs: 4px · Buttons: 4px (Storybook buttons are famously `3em`/pill for the marketing Button, but UI controls use 4px) · Cards / panels: 6px · Badges: 3em (pill) · Mark: intrinsic.

## Components

### Story explorer (signature)
The three-pane Manager: a **sidebar** story tree (components → stories), a **canvas** rendering the selected story in isolation, and an **addons panel** whose **Controls** tab is an args table. Editing an arg (variant, size, label, boolean) re-renders the canvas live — the core Storybook loop.

### Controls (args) table
Rows of `name` (mono) + an editor matched to the arg type: select, radio, text, boolean toggle, number. Values reflect and drive the live story.

### Button (the canonical demo component)
Pill button; `primary` = coral fill, white text; `secondary` = transparent with a `1px` neutral ring; sizes small/medium/large scale padding + font.

### Badge
Pill with a status color at low-opacity background + saturated text (positive/warning/negative/neutral).

## Guardrails

**DO**
- Keep the book mark coral `#FF4785` (fixed); let the wordmark adapt to the theme.
- Use Nunito Sans for all UI text — its roundness is the brand.
- Keep the chrome neutral so the component in the canvas is the focus.
- Use coral for brand/primary/active, blue for links/focus — don't cross them.
- Show arg `name`s and values in mono in the Controls table.

**DON'T**
- Don't recolor the coral mark or use coral for informational states (that's blue).
- Don't set the UI in a sharp grotesque — Nunito Sans's warmth is intentional.
- Don't clutter the canvas with chrome; the story is isolated on purpose.
- Don't use more than the one accent + link + status set in a single view.
- Don't put body/UI copy in the mono face — mono is for arg names, values, and code.
