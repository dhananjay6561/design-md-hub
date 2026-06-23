# Figma Design System

> A collaborative interface design tool that puts the entire product design workflow — wireframing, prototyping, handoff, and real-time collaboration — inside a single, browser-native canvas.

---

## 1. Overview

Figma's visual identity is built on three interlocking ideas: **clarity**, **energy**, and **craft**. The UI itself is a demonstration of the product: pixel-precise, densely information-rich yet uncluttered, and capable of fading into the background while creative work happens on the canvas. The marketing surface (figma.com) and the app UI share the same underlying philosophy but use different design modes — the website is expressive and bold; the app is disciplined and utilitarian.

The 2023 rebrand (Config 2023) introduced a custom type family (Figma Sans) and expanded the palette from the legacy five-color logo set to a broader system of bold primaries, electric neons, and muted earthy tones. The signature purple accent persists as the through-line between old and new.

**Core principles:**
- **Canvas-first:** chrome is minimal so work fills the screen.
- **Density without clutter:** small targets are permissible because users are professionals; generous breathing room is reserved for marketing.
- **Systematic color:** semantic tokens over raw hex; dark mode is a first-class concern.
- **Precision type:** optical sizing and tight tracking at display scale; slightly looser tracking at body scale.

---

## 2. Colors

### 2.1 Brand Palette (logo / marketing)

| Token | Hex | Name | Usage |
|---|---|---|---|
| `brand-red` | `#F24E1E` | Figma Red | Logo mark, error, destructive |
| `brand-orange` | `#FF7262` | Figma Orange | Accent, illustration |
| `brand-purple` | `#A259FF` | Figma Purple | Logo mark, brand accent |
| `brand-primary` | `#4D49FC` | Figma Indigo | Current UI primary CTA, nav active state (2024+) |
| `brand-blue` | `#1ABCFE` | Figma Blue | Information, FigJam accent |
| `brand-green` | `#0ACF83` | Figma Green | Success, positive states |

**Note:** The 2024+ brand uses `#4D49FC` (indigo) as the primary interactive color. `#A259FF` remains the canonical purple for the logo mark.

### 2.2 App UI — Light Mode (Figma Design)

These are the official CSS variables exposed to plugins and used internally in the UI:

| Token | Hex | Usage |
|---|---|---|
| `--figma-color-bg` | `#FFFFFF` | Primary panel / surface background |
| `--figma-color-bg-secondary` | `#F5F5F5` | Secondary surfaces, canvas default background |
| `--figma-color-bg-tertiary` | `#EBEBEB` | Tertiary fills, dividers |
| `--figma-color-bg-brand` | `#0D99FF` | Brand-accented backgrounds (Figma Design) |
| `--figma-color-bg-selected` | `#E8F4FF` | Selected row/cell background |
| `--figma-color-bg-danger` | `#F24822` | Error / destructive backgrounds |
| `--figma-color-bg-success` | `#14AE5C` | Success state backgrounds |
| `--figma-color-bg-warning` | `#FFCD29` | Warning state backgrounds |
| `--figma-color-text` | `#000000E5` | Primary text (90 % opacity black) |
| `--figma-color-text-secondary` | `#00000080` | Secondary text (50 % opacity black) |
| `--figma-color-text-tertiary` | `#0000004D` | Placeholder / disabled text (30 % opacity) |
| `--figma-color-text-brand` | `#007BE5` | Brand-colored text / links |
| `--figma-color-icon` | `#000000E5` | Icons (same as primary text) |
| `--figma-color-icon-brand` | `#007BE5` | Brand-colored icons |
| `--figma-color-border` | `#E6E6E6` | Default borders and dividers |
| `--figma-color-border-brand` | `#BDE3FF` | Brand-tinted borders |

### 2.3 App UI — Dark Mode (Figma Design)

| Token | Approx. Hex | Usage |
|---|---|---|
| `--figma-color-bg` | `#2C2C2C` | Primary panel background |
| `--figma-color-bg-secondary` | `#1E1E1E` | Canvas background (confirmed default) |
| `--figma-color-bg-tertiary` | `#3C3C3C` | Tertiary surfaces |
| `--figma-color-text` | `#FFFFFFE5` | Primary text (90 % opacity white) |
| `--figma-color-text-secondary` | `#FFFFFF80` | Secondary text (50 % opacity white) |
| `--figma-color-text-tertiary` | `#FFFFFF4D` | Disabled / placeholder (30 % opacity white) |
| `--figma-color-border` | `#3C3C3C` | Default borders |
| `--figma-color-bg-brand` | `#0D99FF` | Brand accent (unchanged in dark) |
| `--figma-color-bg-selected` | `#0D99FF26` | Selected rows in dark mode |

### 2.4 FigJam Accent (Purple Shift)

FigJam uses purple where Figma Design uses blue as its brand color:

| Token | Hex | Usage |
|---|---|---|
| `--figma-color-bg-brand` (FigJam) | `#9747FF` | FigJam brand accent background |
| `--figma-color-text-brand` (FigJam) | `#7B61FF` | FigJam brand text / links |

### 2.5 Semantic / Status Colors

| Name | Hex | Usage |
|---|---|---|
| Danger | `#F24822` | Errors, destructive actions |
| Warning | `#FFCD29` | Warnings, in-progress |
| Success | `#14AE5C` | Confirmations, completed states |
| Info | `#0D99FF` | Informational states, brand blue |

---

## 3. Typography

### 3.1 Font Families

| Family | Usage |
|---|---|
| **Figma Sans Text** | UI body copy, labels, navigation items, tooltips, panel text |
| **Figma Sans Display** | Hero headlines, section headings on marketing pages |
| **Figma Sans Condensed Text** | Tight labels, chips, badges, toolbar labels |
| **Figma Sans Condensed Display** | Large condensed hero lockups, campaign titles |
| **Figma Sans Mono** | Code snippets, developer handoff panels, token values |
| **Inter** | Fallback / legacy; still used in plugin UIs and community files |

All Figma Sans variants are proprietary — developed in-house by Figma's own type team, not publicly available. Preview fallback: `Inter` (Google Fonts) — the closest widely-available grotesque sans-serif in proportions and optical sizing behavior; also Figma's own legacy fallback. Preview mono fallback: `JetBrains Mono` (Google Fonts) — similar proportions to Figma Sans Mono for code contexts.

Figma Sans is a variable typeface. It supports 7 weight stops and an optical-size axis that opens letter-spacing at smaller scales and tightens it at display scale.

### 3.2 Type Scale (Marketing / figma.com)

| Step | Size | Line Height | Weight | Tracking | Usage |
|---|---|---|---|---|---|
| `display-2xl` | 72 px | 80 px | Black 900 | −0.04 em | Hero headline |
| `display-xl` | 60 px | 72 px | Bold 700 | −0.03 em | Section hero |
| `display-lg` | 48 px | 58 px | Bold 700 | −0.02 em | Page title |
| `display-md` | 36 px | 44 px | SemiBold 600 | −0.01 em | Sub-section heading |
| `display-sm` | 30 px | 38 px | SemiBold 600 | 0 | Card headline |
| `text-xl` | 20 px | 30 px | Regular 400 | 0 | Lead paragraph |
| `text-lg` | 18 px | 28 px | Regular 400 | 0 | Body large |
| `text-md` | 16 px | 24 px | Regular 400 | 0 | Body default |
| `text-sm` | 14 px | 20 px | Regular 400 | 0 | Secondary body, captions |
| `text-xs` | 12 px | 18 px | Regular 400 | 0 | Labels, helper text |

### 3.3 Type Scale (App UI)

| Step | Size | Line Height | Weight | Usage |
|---|---|---|---|---|
| `ui-xl` | 16 px | 24 px | SemiBold 600 | Panel section headers |
| `ui-lg` | 13 px | 20 px | Medium 500 | Layer names, property labels |
| `ui-md` | 12 px | 18 px | Regular 400 | Default UI text, dropdown items |
| `ui-sm` | 11 px | 16 px | Regular 400 | Tooltip text, secondary labels |
| `ui-xs` | 10 px | 14 px | Regular 400 | Badges, keyboard shortcut hints |
| `ui-mono` | 11 px | 16 px | Regular 400 | Hex fields, coordinate inputs |

---

## 4. Spacing

**Base unit:** 4 px. All spacing tokens are multiples of 4.

| Token | Value | Usage |
|---|---|---|
| `space-0` | 0 px | Reset |
| `space-1` | 4 px | Tight internal padding (icon gaps, chip gaps) |
| `space-2` | 8 px | Default gap between related items |
| `space-3` | 12 px | Component internal padding (small button) |
| `space-4` | 16 px | Standard content padding |
| `space-5` | 20 px | Medium section gap |
| `space-6` | 24 px | Card internal padding |
| `space-8` | 32 px | Large section separation |
| `space-10` | 40 px | Section padding (mobile) |
| `space-12` | 48 px | Section padding (desktop, tight) |
| `space-16` | 64 px | Section padding (desktop, comfortable) |
| `space-20` | 80 px | Hero vertical padding |
| `space-24` | 96 px | Maximum vertical rhythm |

**App UI micro-spacing:**

| Token | Value | Usage |
|---|---|---|
| `panel-padding` | 8 px | Panels, sidebars |
| `row-height-sm` | 24 px | Dense list rows |
| `row-height-md` | 32 px | Standard list rows |
| `toolbar-height` | 40 px | Top / bottom toolbars |
| `panel-width` | 240 px | Left/right panel default width |

---

## 5. Border Radius

| Token | Value | Usage |
|---|---|---|
| `radius-none` | 0 px | Sharp corners (tables, grid cells) |
| `radius-xs` | 2 px | Micro chips, keyboard shortcut pills |
| `radius-sm` | 4 px | Inputs, dropdowns, tooltips, context menus |
| `radius-md` | 6 px | Buttons (default), cards (small), badges |
| `radius-lg` | 8 px | Modals, popovers, cards (standard) |
| `radius-xl` | 12 px | Large cards, dialog boxes |
| `radius-2xl` | 16 px | Feature panels, onboarding cards |
| `radius-3xl` | 24 px | Large modal sheets |
| `radius-full` | 9999 px | Pills, avatar bubbles, toggle tracks |

---

## 6. Shadows

Figma uses restrained shadow depth. The app UI is nearly flat; elevation is communicated primarily through background-color differences. Marketing components use slightly deeper shadows for lift.

| Token | Value | Usage |
|---|---|---|
| `shadow-xs` | `0 1px 2px rgba(0,0,0,0.05)` | Subtle card lift, tooltip |
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.10), 0 1px 2px rgba(0,0,0,0.06)` | Dropdown menus, popovers |
| `shadow-md` | `0 4px 6px rgba(0,0,0,0.07), 0 2px 4px rgba(0,0,0,0.06)` | Cards, floating toolbar |
| `shadow-lg` | `0 10px 15px rgba(0,0,0,0.10), 0 4px 6px rgba(0,0,0,0.05)` | Modals, dialogs |
| `shadow-xl` | `0 20px 25px rgba(0,0,0,0.10), 0 10px 10px rgba(0,0,0,0.04)` | Full-screen overlays |
| `shadow-focus` | `0 0 0 3px rgba(13,153,255,0.40)` | Keyboard focus ring (blue tint) |
| `shadow-focus-purple` | `0 0 0 3px rgba(162,89,255,0.40)` | Focus ring on brand-purple elements |

Dark mode shadows use a reduced opacity (approximately 60% of light-mode values) because dark surfaces are already visually recessed.

---

## 7. Components

### 7.1 Button

Figma uses three visual tiers of button, each with standard/hover/pressed/disabled states.

**Primary (filled)**
- Background: `#0D99FF` (Figma Design) / `#9747FF` (FigJam)
- Text: `#FFFFFF`
- Height: 32 px
- Padding: 8 px 16 px
- Border radius: `radius-md` (6 px)
- Font: Figma Sans Text, Medium 500, 13 px
- Hover: background darkens ~8 % (`#0A80D9`)
- Disabled: background `#0D99FF` at 40 % opacity, text 40 % opacity

**Secondary (outlined)**
- Background: transparent
- Border: 1 px solid `--figma-color-border` (`#E6E6E6` light / `#3C3C3C` dark)
- Text: `--figma-color-text`
- Height: 32 px
- Padding: 8 px 16 px
- Border radius: `radius-md` (6 px)
- Hover: background `--figma-color-bg-tertiary`

**Ghost / Text**
- Background: transparent, no border
- Text: `--figma-color-text-brand` (`#007BE5`)
- Height: 32 px
- Padding: 8 px 12 px
- Border radius: `radius-sm` (4 px)
- Hover: background `--figma-color-bg-selected`

**Destructive**
- Background: `#F24822`
- Text: `#FFFFFF`
- Same sizing as Primary

**Small variant:** Height 24 px, padding 4 px 12 px, font 11 px.

---

### 7.2 Input

- Background: `--figma-color-bg` (white / dark panel)
- Border: 1 px solid `--figma-color-border`
- Border radius: `radius-sm` (4 px)
- Height: 32 px (standard), 24 px (compact)
- Padding: 6 px 8 px
- Font: Figma Sans Text / Figma Sans Mono for numeric fields, 12 px
- Placeholder: `--figma-color-text-tertiary`
- Focus: border becomes `#0D99FF`, `shadow-focus` applied
- Error: border `#F24822`
- Disabled: background `--figma-color-bg-tertiary`, text 40 % opacity

Number/coordinate inputs (X, Y, W, H) in the Properties panel use 6 px height with monospace font, no visible border until hover.

---

### 7.3 Card

**Marketing card (figma.com)**
- Background: `#FFFFFF` (light) / `#1E1E1E` (dark)
- Border: 1 px solid `rgba(0,0,0,0.08)` (light) / `rgba(255,255,255,0.08)` (dark)
- Border radius: `radius-xl` (12 px)
- Padding: 24 px
- Shadow: `shadow-sm` at rest, `shadow-md` on hover
- Transition: 150 ms ease

**App UI panel card / section**
- Background: `--figma-color-bg-secondary`
- Border: none (background differentiation only)
- Border radius: `radius-sm` (4 px)
- Padding: 8 px

---

### 7.4 Navigation

**Marketing top nav (figma.com)**
- Background: `#FFFFFF` with 1 px bottom border `#E6E6E6`
- Height: 64 px
- Padding: 0 40 px
- Logo left, links center/right
- Font: Figma Sans Text, Regular 400, 15 px
- Active link: `--figma-color-text` (black)
- Hover link: `--figma-color-text-secondary`
- CTA button: `#0D99FF` fill, white text, `radius-md`

**App top bar (Figma Design, UI3)**
- Background: `--figma-color-bg`
- Height: 40 px
- Contains: Figma menu (F logo), Move/Frame/etc. tools, Share button, View toggles
- Separator: 1 px `--figma-color-border`

**App floating toolbar (UI3, bottom)**
- Background: `--figma-color-bg`
- Border radius: `radius-lg` (8 px)
- Shadow: `shadow-md`
- Height: 44 px
- Padding: 4 px 8 px
- Tool icons: 24 × 24 px touch target, 16 × 16 px icon
- Selected tool: background `--figma-color-bg-selected`, icon color `--figma-color-icon-brand`

**Left panel (Layers/Assets)**
- Width: 240 px (default, resizable)
- Background: `--figma-color-bg`
- Border right: 1 px `--figma-color-border`
- Row height: 24 px (dense list)
- Selected row: background `--figma-color-bg-selected`

**Right panel (Design/Prototype/Inspect)**
- Width: 240 px (default)
- Background: `--figma-color-bg`
- Border left: 1 px `--figma-color-border`
- Section header: font 11 px, uppercase, Medium 500, letter-spacing 0.08 em, `--figma-color-text-secondary`

---

### 7.5 Badge

| Variant | Background | Text | Border radius |
|---|---|---|---|
| Default | `--figma-color-bg-tertiary` | `--figma-color-text-secondary` | `radius-full` |
| Brand | `#0D99FF1A` (10 % blue) | `#007BE5` | `radius-full` |
| Success | `#14AE5C1A` | `#0F8B49` | `radius-full` |
| Warning | `#FFCD291A` | `#B38600` | `radius-full` |
| Danger | `#F248221A` | `#C43518` | `radius-full` |
| Purple | `#A259FF1A` | `#7B44CC` | `radius-full` |

- Height: 20 px
- Padding: 2 px 8 px
- Font: Figma Sans Text, Medium 500, 11 px

---

### 7.6 Toolbar (App context menu / action bar)

Toolbars in the app context (right-click context menu, quick actions bar):
- Background: `--figma-color-bg`
- Border radius: `radius-lg` (8 px)
- Shadow: `shadow-lg`
- Item height: 32 px
- Item padding: 8 px 12 px
- Icon size: 16 × 16 px
- Divider: 1 px `--figma-color-border`, margin 4 px vertical
- Keyboard shortcut label: `--figma-color-text-tertiary`, `Figma Sans Mono` 11 px
- Hover item: background `--figma-color-bg-tertiary`
- Destructive item text: `#F24822`

---

## 8. Layout Principles

- **Grid:** 12-column grid for marketing pages. App UI uses no formal column grid — panels and canvas are fluid/resizable.
- **Max content width:** 1280 px container on marketing pages; full-bleed sections allowed for hero/feature stripes.
- **Horizontal padding:** 40 px at ≥ 1280 px, 24 px at tablet, 16 px at mobile.
- **Vertical rhythm:** 8 px baseline. Section vertical spacing follows `space-16` (64 px) to `space-24` (96 px).
- **Alignment:** Left-aligned body content; center alignment reserved for hero headlines and single-stat callouts.
- **Z-index layers (app):** Canvas (0) → Panels (100) → Floating toolbar (200) → Tooltips (300) → Modals (400) → Notifications (500).
- **Density:** App UI targets 24–32 px row height for all interactive list items. Compact mode drops to 20 px.

---

## 9. Responsive Behavior

| Breakpoint | Width | Notes |
|---|---|---|
| Mobile | < 768 px | Single-column layout; nav collapses to hamburger; hero text drops to `display-lg` (48 px) |
| Tablet | 768–1024 px | Two-column grids; side-by-side feature pairs collapse to stacked; nav may show text links |
| Desktop | 1024–1280 px | Full nav, standard column grids |
| Wide | ≥ 1280 px | Max-width container locks at 1280 px; full bleed sections extend to viewport edge |
| Ultrawide | ≥ 1920 px | Content container unchanged; hero backgrounds tile/extend; no unbounded stretching of text containers |

**Marketing-specific:**
- Hero headline font size: 72 px (≥ 1280), 60 px (768–1280), 40 px (< 768).
- Feature grids: 3-up at ≥ 1024, 2-up at 768–1024, 1-up at < 768.
- Pricing table: horizontal scroll at < 768 px (don't collapse columns).

**App-specific:**
- The app is not designed to run below approximately 960 px width.
- Panel widths are adjustable between 180–320 px.
- On narrow viewports the left panel defaults to collapsed; accessible via keyboard shortcut.

---

## 10. Tone and Guardrails

### DO

- Use `Figma Sans` for all new product and marketing surfaces.
- Apply `Inter` only as a fallback in contexts where Figma Sans is unavailable (legacy plugin UIs, third-party integrations).
- Keep backgrounds neutral — white `#FFFFFF`, `#F5F5F5`, or their dark-mode equivalents — and let illustrations/screenshots carry color.
- Use purple (`#A259FF`) exclusively as a brand accent; do not use it for purely informational states (use blue `#0D99FF` for info).
- Use semantic tokens (`--figma-color-bg-brand`, `--figma-color-text`) rather than raw hex values in plugin and product code.
- Ensure a minimum 4.5:1 contrast ratio between text and its background at all times.
- Apply `shadow-focus` (blue ring) on interactive elements for keyboard accessibility.
- Maintain the app's information density — do not add padding to app-UI components to "breathe" without a deliberate reason; this is a professional tool, not a consumer app.
- Use `#F24822` (Figma Red) consistently for all destructive and error states; never use orange or a lighter red.
- Keep motion fast: 100–200 ms for micro-interactions, 200–300 ms for panel transitions, ease-out curves.

### DON'T

- Don't use brand purple (`#A259FF`) or brand blue (`#0D99FF`) as full-surface backgrounds on large areas; they work as accents, buttons, and highlights only.
- Don't mix Figma Sans with other grotesque sans-serifs (Helvetica, Arial, DM Sans) in the same composition — it creates tonal conflict.
- Don't use decorative shadows on app UI components; reserve `shadow-md` and above for floating surfaces (modals, popovers, toolbars).
- Don't use full black `#000000` as text color in the app; the system uses `#000000E5` (90 % opacity) to soften rendering on retina screens.
- Don't produce hard corners (radius 0) for interactive components on the marketing site — the brand refresh is warm and rounded.
- Don't use the Figma logo, wordmark, or brand marks inside app UI components or icons you ship.
- Don't rely on color alone to communicate state — always pair color changes with an icon, label, or shape change.
- Don't exceed 6 colors in a single component or layout section; the palette is broad by design but should be curated per context.
- Don't animate the canvas itself (the infinite scroll/zoom space) — only chrome elements should animate.
- Don't apply `Figma Sans Mono` to anything other than code, coordinates, hex values, or token names; it is not a display face.
