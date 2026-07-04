# Replit Design System

## Brand Overview
Replit is the browser-based IDE and AI app builder — write, run, and ship software without leaving the tab. The 2024 identity is **warm**: a cream paper marketing canvas, a single hot **Replit orange**, and warm near-black surfaces for the workspace itself. The product cockpit (editor + console) stays **dark** even on the light marketing site — a real code environment. Type is the neutral **Diatype** grotesque with a mono for code and a pixel face for accents.

## Color Palette

### Brand
- **Orange** `#FF3C00` — the signature: mark, Run button, primary CTAs, active states
- **Orange lift** `#FF5A2B` — hover / on-dark accent
- **Peach** `#FFB199` — warm accent tint, gradients
- **Coral** `#F45D48` — secondary warm accent

### Surfaces
- **Cream** `#FAF6F1` — light marketing page (warm, never pure white)
- **Ink** `#191818` — warm near-black: dark page, workspace base
- **Warm dark** `#312E2E` — raised warm surface
- **Editor black** `#1B1A19` — the IDE panel (always dark)

### Text & neutrals
- **Text** `#191818` (light) / `#FAF6F1` (dark) · **secondary** `#57534E` · **muted** `#767270` · **border** `#E7E1D8` (light) / `rgba(255,255,255,.09)` (dark)

### Console / syntax (fixed, in the IDE)
- **keyword** `#FF5A2B` · **string** `#7FBA00`→ soft `#B5E890` · **func** `#49CCF9` · **number** `#BE9BF8` · **comment** `#767270` · **stdout** `#E2E2E2`

### Semantic
- **Success** `#4FB477` (exit 0) · **Error** `#FF4D4D`

## Typography
Replit ships **Replit Diatype / ABC Diatype** (sans), **Replit Diatype Mono** (code), and **ABC Diatype Pixel** (accent) — all proprietary (ABC Dinamo, CORS-locked), so this reference falls back to close equivalents (documented `≈`).
- **UI / display** — `Replit Diatype` ≈ **Inter** — headings, body, buttons
- **Mono** — `Replit Diatype Mono` ≈ **JetBrains Mono** — the editor, console, filenames, everything code
- **Pixel** — `ABC Diatype Pixel` ≈ **Silkscreen** — small uppercase accent labels

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 40, 48, 64.

## Border Radius
- Buttons / inputs: 8px · Cards / IDE panel: 12px · App tiles: 10px · Pills: 9999px.

## Components

### Workspace / IDE (signature)
A dark editor cockpit: a filename tab, a line-numbered code editor with syntax highlighting, an orange **Run** button, and a console pane. Pressing Run streams the program's stdout line-by-line, then an exit status. The IDE panel is dark regardless of page theme.

### Run button
Solid orange `#FF3C00`, white text, rounded; the single most important action.

### Console line
Monospace stdout in `#E2E2E2` on editor black; the run header (`> python main.py`) muted; exit status in success green or error red.

## Guardrails

**DO**
- Keep the mark orange `#FF3C00` (fixed); let the wordmark adapt to the theme.
- Keep the marketing canvas warm cream `#FAF6F1`; keep the IDE/workspace panel dark on both themes.
- Use orange for the Run button and primary actions — it's the one accent.
- Set all code, filenames, and console output in the mono face.
- Keep dark surfaces warm near-black `#191818` — never a cool blue-black.

**DON'T**
- Don't render the IDE panel light — the workspace is a dark cockpit.
- Don't introduce a second saturated accent competing with orange.
- Don't set code or console text in a proportional font.
- Don't cool the neutrals — Replit's grays/darks are warm.
- Don't recolor the orange mark.
