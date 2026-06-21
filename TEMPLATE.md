# preview.html Template Spec

## Layout

- NO navbar / sticky header
- Floating dark/light toggle — fixed top-right corner, `16px` from edge, pill button with sun/moon icon
- Full-width sections, max-content-width `1100px` centered with auto margins
- Sections scroll naturally, no scroll-spy needed

## Structure (in order)

### 1. Hero
- Brand SVG logo (large, ~80px tall) — use real inline SVG, not emoji or text
- Brand name as `h1`
- One-line tagline from DESIGN.md
- Brand accent color as a subtle background or gradient behind hero

### 2. Colors
- Section title: "Colors"
- Swatches in a CSS grid (repeat auto-fill, min 160px)
- Each swatch: color block (80px tall) + token name + hex value + usage text
- Click to copy hex → toast notification bottom-center
- Group by: Primary, Surfaces, Text, Semantic (separate sub-headings)

### 3. Typography
- Section title: "Typography"
- Each row: scale name | live rendered text at actual size/weight | spec pills (size, weight, line-height)
- Mono scale shown separately with a code sample

### 4. Components
- Section title: "Components"
- Grid of component blocks, each in a card:
  - Buttons (all variants side by side)
  - Inputs (default, focus, error, disabled)
  - Badges (all variants)
  - A realistic card component

### 5. Spacing
- Section title: "Spacing"
- Horizontal bars, width proportional to value
- Token name | pixel value | visual bar

### 6. Guardrails
- Section title: "Tone & Guardrails"
- Two columns: DO (green left border) | DON'T (red left border)
- Each rule as a list item

## CSS Rules

- Use `data-theme="dark"` or `data-theme="light"` on `<html>`
- All colors as CSS custom properties: `--primary`, `--background`, `--surface`, `--text-primary`, etc.
- Font loaded via Google Fonts `@import` at top of `<style>`
- Body font: brand's actual font from DESIGN.md
- Transitions: `150ms ease` on all interactive elements

## Logo Sources (inline SVG)

Use these exact SVGs:

**Linear**: Purple L-shape mark
**Vercel**: Black/white triangle ▲
**GitHub**: Octocat SVG
**Notion**: Bold N in a rounded square
**Stripe**: S wordmark
**Supabase**: Green lightning bolt
**Figma**: Figma component mark (4 circles + center)
**Raycast**: Red/orange R mark
**Cursor**: Blue C mark
**PlanetScale**: PS branching mark
**Perplexity**: Teal circle with P
**Neon**: Green N mark
**Railway**: Purple train track mark
**Clerk**: Violet C mark
**Retool**: Blue grid mark
