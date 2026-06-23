# Raycast DESIGN.md

> Your shortcut to everything — a macOS productivity launcher built on dark chrome, vibrant gradient accents, and the principle that every interaction should feel instantaneous.

## Overview

Raycast's design philosophy treats the interface as an extension of the operating system rather than an app sitting on top of it. The aesthetic is dark-first, glass-morphic, and deliberately minimal: near-black surfaces rendered with translucency and blur, a strict no-drop-shadow rule (elevation derives entirely from a layered surface color scale), and accent color reserved as a single purposeful statement per screen. The window itself is 750 × 475 px, corner-radius 18 px, and floats as a floating panel rather than a standard document window.

The system adapts fully to both light and dark mode. In the app, theming is handled through a 12-slot color schema (background, backgroundSecondary, text, selection, loader, plus seven semantic accents). On the marketing site, Inter with `ss03` stylistic set carries the brand voice.

Design rules in one sentence: **fast surfaces, rare color, zero shadow, always keyboard-first**.

## Colors

### Theme Schema (App)

The Raycast app renders its palette from a 12-slot theme JSON. Each slot maps to CSS custom properties consumed by every UI layer. The defaults below reflect Raycast's own built-in dark and light modes as observed in the Theme Studio and community theme data.

#### Dark Mode (default app)

| Token | Hex | Usage |
|-------|-----|-------|
| `background` | `#111113` | Primary window background (applied at 40% opacity over backdrop blur) |
| `backgroundSecondary` | `#111113` | Gradient endpoint (bottom 70% of window) |
| `text` | `#F2F2F2` | Primary text |
| `selection` | `#FF6363` | Selected list row highlight, caret color |
| `loader` | `#FF6363` | Animated progress bar beneath search field |
| `--text-600` | `text @ 60%` | Section headers, subtle labels |
| `--text-400` | `text @ 40%` | Placeholder text in search input |
| `--text-100` | `text @ 10%` | Icon button backgrounds, keyboard shortcut chips |
| `--border-200` | `text @ 20%` | Window inset border (1 px, `box-shadow: inset 0 0 0 1px`) |
| `--border-100` | `text @ 10%` | Header/footer dividers |
| `--selection-100` | `selection @ 10%` | Selected row background fill |

#### Semantic Accents (app & marketing)

| Token | Hex | Usage |
|-------|-----|-------|
| `red` | `#FF6161` | Error badges, destructive actions, default loader/selection |
| `orange` | `#FF8C00` | Warning badges, secondary accent |
| `yellow` | `#FFC533` | Caution, "Pro" tier highlights |
| `green` | `#59D499` | Success, "online" status |
| `blue` | `#57C1FF` | Info, link tint |
| `purple` | `#A484FE` | Pro plan accent, decorative |
| `magenta` | `#FF79C6` | Decorative, rarely used |

Each accent also ships a `{color}-100` variant at **15% opacity** for badge backgrounds.

#### Marketing Site (ray.so / raycast.com)

| Token | Hex | Usage |
|-------|-----|-------|
| `canvas` | `#0D0D0D` | Page background |
| `surface` | `#181818` | Cards, panels (gray-2) |
| `surface-elevated` | `#212121` | Raised card surfaces (gray-3) |
| `surface-card` | `#282828` | Feature cards (gray-4) |
| `brand` | `#FF6060` | Primary CTA, logo mark |
| `hero-stripe-start` | `#FF5757` | Hero gradient diagonal stripe origin |
| `hero-stripe-end` | `#A1131A` | Hero gradient diagonal stripe terminus |
| `ink` | `#EDEDED` | Headings, high-contrast text (gray-12) |
| `body` | `#B3B3B3` | Body copy (gray-11) |
| `muted` | `#7A7A7A` | Secondary labels (gray-10) |
| `ash` | `#6D6D6D` | Disabled, de-emphasized text (gray-9) |
| `hairline` | `#393939` | Dividers, card borders (gray-6) |
| `on-primary` | `#000000` | Text on white CTA buttons |
| `cta-bg` | `#FFFFFF` | Primary download button background |
| `cta-pressed` | `#E8E8E8` | Primary button pressed state |

#### Light Mode

| Token | Hex | Usage |
|-------|-----|-------|
| `background` | `#EFEFEF` | App window background |
| `panel` | `#F2F2F2` | Panel surfaces |
| `text-primary` | `#1F1F1F` | Primary text (gray-12 light) |
| `text-secondary` | `#505050` | Secondary text (gray-11 light) |
| `border` | `#DDDDDD` | Dividers (gray-3 light) |

## Typography

### App (native macOS)

The Raycast app renders using **system-ui / SF Pro** — Apple's native system font — which guarantees crisp rendering at all macOS display densities. Users can increase the base size one step via **Preferences → Appearance → Font Size**.

| Scale | Size | Weight | Line Height | Usage |
|-------|------|--------|-------------|-------|
| `search-input` | 16 px | 400 | 1.0 | Search field placeholder |
| `list-title` | 14 px | 400 | 1.0 | List item primary title |
| `list-subtitle` | 13 px | 400 | 1.0 | List item secondary label |
| `section-header` | 12 px | 500 | 1.0 | Section group header (ALL CAPS in some contexts) |
| `badge` | 12 px | 400 | 1.0 | Accessory tags on list rows |
| `footer-label` | 12 px | 600 | 1.0 | Action label in footer bar |
| `keyboard-key` | 12 px | 400 | 1.0 | Keyboard shortcut chips |

Letter spacing: default (SF Pro tracks automatically). Icon size paired with `list-title`: **20 × 20 px**.

### Marketing Site (raycast.com / ray.so)

**Font variables (from live CSS):**
- `--main-font`: `var(--font-inter), sans-serif`
- `--font-inter`: `"Inter", "Inter Fallback"` (variable weight 100–900, loaded via `next/font`)
- `--monospace-font`: `var(--font-jetbrains-mono), Menlo, Monaco, Courier, monospace`
- `--font-jetbrains-mono`: `"JetBrains Mono", "JetBrains Mono Fallback"`
- `--font-geist-mono`: `"GeistMono", ui-monospace, SFMono-Regular, Roboto Mono, Menlo, monospace`

**Global settings:**
- **Font feature settings**: `"calt", "kern", "liga", "ss03"` enabled globally
- **Anti-aliasing**: `-webkit-font-smoothing: antialiased`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| `display-xl` | 64 px | 600 | Hero headline |
| `display-lg` | 56 px | 500 | Feature section headings |
| `display-md` | 40 px | 500 | Sub-section headings |
| `heading` | 24 px | 600 | Card titles |
| `body-lg` | 18 px | 400 | Feature descriptions |
| `body-md` | 16 px | 400 | Default body copy |
| `body-sm` | 14 px | 400 | Secondary descriptions |
| `button-md` | 14 px | 500 | Button labels |
| `label` | 12 px | 500 | Tags, overlines |
| `xxs` | 11 px | 400 | Legal, footnotes |

## Spacing

Base unit: **8 px** (half-step at 4px via `--spacing-0-5`)

Sourced from live `--spacing-*` CSS tokens on raycast.com:

| Token | Value | Usage |
|-------|-------|-------|
| `--spacing-0-5` | 4 px | Hairline gaps, icon inner padding |
| `--spacing-1` | 8 px | Icon-to-label gap, badge padding |
| `--spacing-1-5` | 12 px | Standard component gap |
| `--spacing-2` | 16 px | Card inner padding, section gap |
| `--spacing-2-5` | 20 px | Medium component spacing |
| `--spacing-3` | 24 px | Feature card padding, group spacing |
| `--spacing-4` | 32 px | Section top/bottom spacing |
| `--spacing-5` | 40 px | Larger component padding |
| `--spacing-6` | 48 px | Large layout gaps |
| `--spacing-7` | 56 px | Header/search bar height |
| `--spacing-8` | 64 px | Section vertical spacing |
| `--spacing-9` | 80 px | Hero top padding |
| `--spacing-10` | 96 px | Major section vertical rhythm |
| `--spacing-12` | 168 px | Large section spacing |

App-specific layout measurements:
- Window: `750 × 475 px`
- Header bar height: `56 px` (padding-x: `16 px`)
- Footer bar height: `40 px` (padding-x: `12 px`)
- List area vertical padding: `4 px` top/bottom, `8 px` left/right
- List item height: `40 px` (padding-x: `8 px`)
- Section header padding: `8 px` horizontal, `8 px` vertical

## Border Radius

Sourced from live `--rounding-*` CSS tokens on raycast.com:

| Token | Value | Usage |
|-------|-------|-------|
| `--rounding-none` | 0 px | Flat edges |
| `--rounding-xs` | 4 px | Micro elements |
| `--rounding-sm` | 6 px | Tags, chips, keyboard keys |
| `--rounding-normal` | 8 px | Badge/tag components, list item selected state |
| `--rounding-md` | 12 px | Cards, component containers |
| `--rounding-lg` | 16 px | Larger cards, panels |
| `--rounding-xl` | 20 px | Section cards on marketing site |
| `--rounding-xxl` | 24 px | Hero cards, large feature blocks |
| `window` | 18 px | Main Raycast floating window (custom, not in scale) |
| `--rounding-full` | 100% | Pill buttons, CTA download button |

## Shadows

Raycast's core rule: **no freestanding drop shadows on surfaces**. Elevation is communicated exclusively through background color steps (the surface ladder). The one permitted shadow pattern is an **inset border** on the window.

| Token | Value | Usage |
|-------|-------|-------|
| `window-inset` | `inset 0 0 0 1px rgba(text, 0.20)` | Window chrome boundary (1 px) |
| `window-backdrop` | `backdrop-filter: blur(72px)` | Frosted-glass window translucency |
| `selection-glow` | none | Selection is color fill, not shadow |
| `loader-bar` | `linear-gradient(to right, transparent, var(--loader), transparent)` | 200 × 1 px loading indicator |

The marketing site follows the same convention — cards use `border: 1px solid #393939` (hairline) rather than box-shadow.

## Components

### Button

Three tiers, no shadows on any tier.

| Variant | Background | Text | Border | Height | Padding | Radius |
|---------|------------|------|--------|--------|---------|--------|
| Primary | `#FFFFFF` | `#000000` | none | 36 px | `8px 16px` | `9999px` (pill) |
| Primary (pressed) | `#E8E8E8` | `#000000` | none | 36 px | `8px 16px` | `9999px` |
| Secondary | transparent | `text` | `1px solid hairline` | 36 px | `8px 16px` | `9999px` |
| Tertiary | surface-elevated | `text` | none | 32 px | `6px 12px` | 8 px |
| Icon Button | `--text-100` (10% text) | `--text` | none | 24 px | equal | 6–8 px |

### Input (Search Field)

The search field is the hero of Raycast's UI — full-width, no border, no background.

| Property | Value |
|----------|-------|
| Height | 56 px (full header bar) |
| Padding | `0 16px` |
| Font | SF Pro 16 px / 400 |
| Color | `--text-400` (placeholder), `--text` (value) |
| Background | transparent |
| Border | none (parent header has `border-b border-[--border-100]`) |
| Caret | `--loader` / `--selection` color |
| Radius | 0 (spans full header) |

### List Item (Command Row)

The standard result row. Matches the dimensions found directly in the Raycast Theme Explorer source.

| Property | Value |
|----------|-------|
| Height | 40 px |
| Padding | `0 8px` |
| Icon area | 20 × 20 px, `shrink-0` |
| Icon-to-title gap | 12 px (`gap-3`) |
| Title | SF Pro 14 px / 400, color `--text` |
| Subtitle | SF Pro 13 px / 400, color `--text-600` |
| Accessories (right) | flex row, `gap-8px`, height 22 px |
| Background (default) | transparent |
| Background (selected) | `--selection-100` (accent at 10% opacity) |
| Radius (selected) | 10 px |

### Section Header

| Property | Value |
|----------|-------|
| Height | auto |
| Padding | `8px 8px` |
| Font | SF Pro 12 px / 500, tracking `0.1 px` |
| Color | `--text-600` (text at 60% opacity) |
| Background | transparent |

### Badge / Tag Accessory

Used as accessories on list rows and in the Theme Explorer preview.

| Property | Value |
|----------|-------|
| Height | 22 px |
| Padding | `0 8px` (`px-2`) |
| Font | SF Pro / Inter 12–14 px / 400 |
| Text color | semantic accent (e.g., `--red`, `--green`) |
| Background | accent at 15% opacity (e.g., `--red-100`) |
| Radius | 8 px (`rounded-md`) |
| Border | none |

### Keyboard Shortcut Chip

| Property | Value |
|----------|-------|
| Width | 20–24 px (single key) |
| Height | 20 px |
| Padding | `0 4px` |
| Font | 12 px / 400 |
| Text color | `--text` |
| Background | `--text-100` (text at 10%) |
| Radius | 6 px (`rounded-md`) |

### Footer Action Bar

| Property | Value |
|----------|-------|
| Height | 40 px |
| Padding | `0 12px` |
| Background | `rgba(255,255,255, 0.05)` dark / `rgba(255,255,255, 0.20)` light |
| Border | `border-t border-[--text-100]` (1 px top divider) |
| Label font | 12 px / 600 |
| Label color | `--text-600` (secondary) / `--text` (active label) |

## Layout Principles

1. **Floating panel, not a window**: Raycast renders as an 18 px-radius floating panel with backdrop blur, without a macOS title bar. It appears centered horizontally, slightly above vertical center.

2. **Surface ladder over shadow**: Every depth step is expressed by a color value one tone lighter on the gray scale — never a box-shadow. Background → Panel → Elevated Card is the only ladder needed.

3. **Single accent per view**: The loader/selection color is the only saturated hue allowed on chrome. All other accent colors (red, green, blue…) stay confined to accessory badges on list rows or extension-category illustrations.

4. **Keyboard geometry baked into spacing**: Row heights (40 px) and header height (56 px) are sized for easy cursor targeting but optimized for keyboard navigation. Mouse interaction is secondary.

5. **No decorative gradients on text or interactive surfaces**: Gradients are reserved for the window background (`background → backgroundSecondary`, top to bottom, 0–70%) and the hero stripe on marketing pages (maximum once per page).

6. **Icon consistency**: All list-row icons are 20 × 20 px. Extension icons follow a square canvas with 10 px radius; system icons use `@raycast/icons` at `w-5 h-5` (20 px).

7. **Typography weight discipline**: Heavy weights (600+) appear only on footer action labels and marketing display type. The app interior uses weight 400–500 exclusively to maintain visual calm at small sizes.

## Responsive Behavior

Raycast is a **macOS-only** application. There is no mobile or tablet breakpoint. The floating window is a fixed `750 × 475 px` panel at standard font size (scales if the user enables large font). All layout is absolute and non-fluid.

The marketing site (`raycast.com`, `ray.so`) does have responsive breakpoints:

| Breakpoint | Name | Notes |
|------------|------|-------|
| `< 960 px` | mobile | Single-column layout, navigation collapses |
| `≥ 960 px + ≥ 840 px height` | `desktop` | Full navigation, multi-column grids |
| `≥ 840 px height` | `tall` | Extended vertical sections revealed |

Footer link grid: 6-column at desktop → 2-column → 1-column stacked. The "Download" CTA remains visible at every breakpoint.

The theme explorer preview (`ray.so/themes`) always renders the Raycast window mock at its fixed `750 × 475 px` size, centered inside a simulated macOS desktop.

## Tone & Guardrails

### Do

- Use the surface ladder (background → panel → elevated) instead of shadows for depth.
- Keep saturated accent colors on data/status — never on navigation chrome.
- Restrict gradients to the window background gradient and one hero stripe per marketing page.
- Use Inter with `ss03` on the web; SF Pro (system-ui) in native contexts.
- Maintain 40 px row heights for keyboard-navigable lists.
- Apply the `selection` color to both the loader bar and selected-row highlight for coherence.
- Use `inset 0 0 0 1px` border-shadow on floating containers instead of outlines or actual borders where possible.
- Let backdrop blur (`72px`) carry the frosted-glass effect on the window.

### Don't

- Don't add drop shadows to cards, panels, or popups — elevation is color, not shadow.
- Don't use the red/orange brand gradient on interactive elements like buttons or tabs.
- Don't mix multiple accent hues on a single screen's chrome elements.
- Don't use font weights above 600 inside the app window (marketing display is the exception).
- Don't add decorative rounded corners below 6 px or above 18 px except for pill buttons.
- Don't add hover backgrounds to list items unless they are keyboard-focused or selected.
- Don't use more than one gradient direction per view — all window backgrounds use top-to-bottom.
- Don't render Raycast-style UI inside a scrollable, multi-column layout — the command palette is always a focused, single-panel view.
