# Vercel Design System

**A stark, developer-first deployment platform defined by pure contrast, zero ornamentation, and ruthless typographic precision.**

---

## 1. Overview

Vercel's visual language is built around aggressive reduction. Every decorative element that cannot justify its presence is removed. The result is an interface that communicates speed, reliability, and engineering authority through what it omits rather than what it adds.

The system — called **Geist** — is named after the Bauhaus concept of a unified aesthetic spirit. It ships as both a typeface family (Geist Sans, Geist Mono) and a full component/token system used across vercel.com and the Vercel dashboard.

**Core principles:**

- **Contrast over color.** The palette is almost entirely black and white. Color appears only to carry semantic meaning (errors, warnings, success states) or to mark a single primary action per view.
- **Grid is the aesthetic.** The 8px base grid is not an implementation detail — it is a visual expression of engineering discipline. Every layout decision is grid-derived.
- **Typography does the heavy lifting.** Hierarchy is achieved through weight and size variation within a single typeface family, not through color or decoration.
- **Motion clarifies; it never decorates.** Transitions are fast (150–300ms), purposeful, and respect `prefers-reduced-motion`.
- **Accessibility is non-negotiable.** WCAG AA contrast (4.5:1 minimum) is the floor, not the target.

---

## 2. Colors

### Philosophy

Vercel uses true neutrals with no warm or cool undertone bias. This "developer tool neutrality" prevents the palette from reading as playful or corporate. Pure black (`#000000`) and pure white (`#ffffff`) anchor the system; `#171717` (Vercel Black) serves as the primary text color to prevent visual harshness at small sizes.

Accent colors appear at most once per view and exclusively for primary interactive actions. The rule is: if something is not interactive or semantic, it should be gray.

### Light Mode

| Token | Hex | Usage |
|---|---|---|
| `background-100` | `#ffffff` | Default page background |
| `background-200` | `#fafafa` | Secondary surfaces, input fills |
| `gray-100` | `#f7f7f7` | Subtle component backgrounds |
| `gray-200` | `#ebebeb` | Card borders, dividers, table rules |
| `gray-300` | `#e0e0e0` | Disabled state borders |
| `gray-400` | `#a8a8a8` | Placeholder text, secondary icons |
| `gray-500` | `#737373` | Tertiary labels, meta text |
| `gray-600` | `#525252` | Secondary body text |
| `gray-700` | `#3d3d3d` | De-emphasized headings |
| `gray-800` | `#292929` | Strong body text |
| `gray-900` | `#1a1a1a` | Secondary text, labels |
| `gray-1000` | `#171717` | Primary text, headings (Vercel Black) |
| `foreground` | `#000000` | Pure black — hero text, logotype |
| `border` | `rgba(0,0,0,0.08)` | Default border (shadow-based) |
| `border-strong` | `rgba(0,0,0,0.15)` | Focused or elevated borders |

### Dark Mode

| Token | Hex | Usage |
|---|---|---|
| `background-100` | `#0a0a0a` | Default dark page background |
| `background-200` | `#000000` | Deepest surface, nav backgrounds |
| `gray-100` | `#111111` | Subtle dark component backgrounds |
| `gray-200` | `#1a1a1a` | Dark card borders, dividers |
| `gray-300` | `#262626` | Disabled borders in dark mode |
| `gray-400` | `#3d3d3d` | Dark mode secondary icons |
| `gray-500` | `#525252` | Dark meta text |
| `gray-600` | `#737373` | Dark secondary body text |
| `gray-700` | `#8c8c8c` | Dark de-emphasized labels |
| `gray-800` | `#a8a8a8` | Dark strong text |
| `gray-900` | `#ededed` | Dark secondary headings |
| `gray-1000` | `#fafafa` | Primary dark-mode text |
| `foreground` | `#ffffff` | Pure white — hero text in dark mode |
| `border` | `rgba(255,255,255,0.08)` | Default dark border |
| `border-strong` | `rgba(255,255,255,0.15)` | Focused dark borders |

### Accent & Semantic Colors

| Token | Hex | Usage |
|---|---|---|
| `blue-600` | `#0070f3` | Primary interactive accent (console, links) |
| `blue-700` | `#0072f5` | Link color, focus ring base |
| `blue-800` | `#0068d6` | Badge text, active nav states |
| `blue-100` | `#ebf5ff` | Badge backgrounds, info surfaces |
| `develop-blue` | `#0a72ef` | Develop workflow marker |
| `preview-pink` | `#de1d8d` | Preview workflow marker |
| `ship-red` | `#ff5b4f` | Ship workflow marker |
| `success` | `#16a34a` | Positive status |
| `warning` | `#eab308` | Warning status |
| `error` | `#dc2626` | Error status |
| `focus-ring` | `0 0 0 2px #fff, 0 0 0 4px #0072f5` | Keyboard focus indicator |

### Alpha Gray (Overlay Utility)

Used for borders, dividers, and overlays that must work on any surface color:

| Token | Value | Usage |
|---|---|---|
| `gray-alpha-100` | `rgba(0,0,0,0.05)` | Hairline tints |
| `gray-alpha-200` | `rgba(0,0,0,0.08)` | Default borders |
| `gray-alpha-400` | `rgba(0,0,0,0.14)` | Stronger dividers |
| `gray-alpha-700` | `rgba(0,0,0,0.40)` | Overlay scrims |
| `gray-alpha-900` | `rgba(0,0,0,0.75)` | Tooltip backgrounds |

---

## 3. Typography

### Font Families

| Role | Family | Fallback Stack |
|---|---|---|
| UI & prose | `Geist Sans` | `Arial, -apple-system, "Segoe UI", sans-serif` |
| Code & data | `Geist Mono` | `"ui-monospace", "SFMono-Regular", "Roboto Mono", "Menlo", "Courier New", monospace` |

OpenType `liga` (ligatures) is enabled globally. `tnum` (tabular numbers) is applied in dashboards, data tables, and anywhere numeric columns appear.

Geist was released by Vercel in 2023 as an open-source typeface. It is available via the `geist` npm package and Google Fonts.

### Type Scale

All sizes use `px` in specification; implement in `rem` (1rem = 16px) in production.

#### Headings — Geist Sans, weight 600, tight letter-spacing

| Token | Size | Weight | Line Height | Letter Spacing | Usage |
|---|---|---|---|---|---|
| `heading-72` | 72px | 600 | 1.1 | -0.05em | Marketing heroes only |
| `heading-56` | 56px | 600 | 1.1 | -0.04em | Section heroes |
| `heading-48` | 48px | 600 | 1.1 | -0.04em | Page titles |
| `heading-40` | 40px | 600 | 1.1 | -0.03em | Section headings |
| `heading-32` | 32px | 600 | 1.15 | -0.03em | Card group headers |
| `heading-24` | 24px | 600 | 1.2 | -0.02em | Card titles, dialog headings |
| `heading-20` | 20px | 600 | 1.25 | -0.01em | Sub-section headings |
| `heading-16` | 16px | 600 | 1.3 | -0.01em | Inline headings |
| `heading-14` | 14px | 600 | 1.4 | 0 | Micro headings, table headers |

#### Labels — Geist Sans, weight 400–500, single-line UI text

| Token | Size | Weight | Line Height | Usage |
|---|---|---|---|---|
| `label-20` | 20px | 500 | 1.4 | Navigation items (large) |
| `label-16` | 16px | 500 | 1.4 | Default nav, form labels |
| `label-14` | 14px | 400 | 1.4 | Secondary labels, table cells |
| `label-13` | 13px | 400 | 1.4 | Metadata, timestamps |
| `label-12` | 12px | 400 | 1.4 | Captions, helper text |

#### Body Copy — Geist Sans, weight 400, multi-line text

| Token | Size | Weight | Line Height | Usage |
|---|---|---|---|---|
| `copy-24` | 24px | 400 | 1.5 | Large lead paragraphs |
| `copy-20` | 20px | 400 | 1.5 | Article body |
| `copy-18` | 18px | 400 | 1.5 | Standard body text |
| `copy-16` | 16px | 400 | 1.5 | Default prose |
| `copy-14` | 14px | 400 | 1.5 | Secondary body text |
| `copy-13` | 13px | 400 | 1.5 | Fine print |

#### Buttons — Geist Sans, weight 500

| Token | Size | Weight | Line Height | Usage |
|---|---|---|---|---|
| `button-16` | 16px | 500 | 1 | Large CTA buttons |
| `button-14` | 14px | 500 | 1 | Default buttons |
| `button-12` | 12px | 500 | 1 | Small/compact buttons, inputs |

#### Mono Variants — Geist Mono

Available for all `label` and `copy` sizes. Used for: code blocks, terminal output, deployment URLs, commit hashes, environment variable names, and numeric dashboards.

---

## 4. Spacing

**Base unit: 8px.** All spacing values are multiples or half-multiples of 8.

| Token | Value | Usage |
|---|---|---|
| `space-1` | 4px | Icon padding, micro gaps |
| `space-2` | 8px | Internal component padding, inline gaps |
| `space-3` | 12px | Compact component padding |
| `space-4` | 16px | Standard element padding, form field height contribution |
| `space-5` | 20px | Comfortable padding |
| `space-6` | 24px | Card internal padding (standard) |
| `space-8` | 32px | Section sub-group separation |
| `space-10` | 40px | Component-to-component gap |
| `space-12` | 48px | Section gap (mobile) |
| `space-16` | 64px | Section gap (tablet) |
| `space-20` | 80px | Large section gap |
| `space-24` | 96px | Section gap (desktop) |
| `space-32` | 128px | Major section separation |
| `space-48` | 192px | Hero-scale section spacing |

**Rhythm guidance:**
- 8px between items in the same group
- 16px between groups within a component
- 32–40px between distinct components on a page
- 64–96px between page-level sections

---

## 5. Border Radius

Vercel uses a tight, almost-square aesthetic. Marketing pages predominantly use `0px` or `4px`. The dashboard uses `6px` and `8px` as standard. Pill radius (`9999px`) is reserved for badges and tags only — never for primary action buttons.

**Rule: do not mix radius families within a single view.** Pick a maximum of two adjacent radius values and apply them consistently.

| Token | Value | Usage |
|---|---|---|
| `radius-none` | 0px | Code blocks, full-bleed images, skeleton loaders |
| `radius-micro` | 2px | Inline code chips, tiny badges |
| `radius-sm` | 4px | Tooltips, dropdown items |
| `radius-md` | 6px | Buttons, inputs, standard cards |
| `radius-lg` | 8px | Modal dialogs, featured cards |
| `radius-xl` | 12px | Hero cards, highlighted panels |
| `radius-2xl` | 16px | Large modals (rare) |
| `radius-full` | 9999px | Pill badges, avatar chips, toggles |

---

## 6. Shadows

Vercel uses **shadow-based borders** instead of CSS `border` on most components. This allows borders to adapt to any background color and enables multi-layer depth effects without additional DOM elements.

| Token | Value | Usage |
|---|---|---|
| `shadow-border` | `0 0 0 1px rgba(0,0,0,0.08)` | Default card/component outline |
| `shadow-border-strong` | `0 0 0 1px rgba(0,0,0,0.15)` | Hover/focused component outline |
| `shadow-sm` | `0 2px 2px rgba(0,0,0,0.04)` | Subtle card lift |
| `shadow-md` | `0 0 0 1px rgba(0,0,0,0.08), 0 2px 2px rgba(0,0,0,0.04), 0 8px 8px -8px rgba(0,0,0,0.04)` | Standard card shadow |
| `shadow-card` | `0 0 0 1px rgba(0,0,0,0.08), 0 2px 2px rgba(0,0,0,0.04), 0 8px 8px -8px rgba(0,0,0,0.04), 0 0 0 1px #fafafa` | Full card with background ring |
| `shadow-popover` | `0 1px 1px rgba(0,0,0,0.02), 0 4px 8px -4px rgba(0,0,0,0.04), 0 16px 24px -8px rgba(0,0,0,0.06)` | Dropdown menus, popovers |
| `shadow-modal` | `0 1px 1px rgba(0,0,0,0.02), 0 8px 16px -4px rgba(0,0,0,0.04), 0 24px 32px -8px rgba(0,0,0,0.06)` | Dialog overlays |
| `shadow-focus` | `0 0 0 2px #ffffff, 0 0 0 4px #0072f5` | Keyboard focus ring (white gap + blue ring) |

**Dark mode:** Replace `rgba(0,0,0,…)` with `rgba(255,255,255,…)` at halved opacity values for equivalent visual weight.

---

## 7. Components

### Button

Vercel uses three functional button variants. Buttons never use gradients or drop shadows.

| Variant | Background | Text | Border | Height | Padding | Radius |
|---|---|---|---|---|---|---|
| Primary | `#171717` (light) / `#ffffff` (dark) | `#ffffff` / `#000000` | none | 40px (md) | 8px 16px | 6px |
| Secondary | `#fafafa` | `#171717` | `1px solid rgba(0,0,0,0.15)` | 40px (md) | 8px 16px | 6px |
| Ghost/Tertiary | transparent | `#171717` | none | 40px (md) | 8px 16px | 6px |
| Destructive | `#dc2626` | `#ffffff` | none | 40px (md) | 8px 16px | 6px |

**Sizes:**
- Small: 32px height, `button-12` type, 6px 12px padding
- Medium: 40px height, `button-14` type, 8px 16px padding (default)
- Large: 48px height, `button-16` type, 10px 20px padding

**States:**
- Hover: background darkened ~8% via `color-mix(in oklab, var(--bg), black 8%)`
- Active: background darkened ~14%
- Disabled: 40% opacity, `cursor: not-allowed`
- Focus: `shadow-focus` ring applied

---

### Input

| Property | Value |
|---|---|
| Background | `#fafafa` (light) / `#111111` (dark) |
| Text | `#171717` / `#fafafa` |
| Placeholder | `#a8a8a8` |
| Border | `1px solid rgba(0,0,0,0.15)` via shadow |
| Border (focus) | `1px solid #0072f5` + focus ring |
| Border (error) | `1px solid #dc2626` |
| Height | 32px (sm) / 40px (md) / 48px (lg) |
| Padding | 0 12px (md default) |
| Radius | 6px |
| Font | `label-14` (14px, weight 400) |

Labels sit above the input with 8px gap, using `label-14` weight 500. Helper text and error messages appear 4px below the input using `label-12` in `gray-500` or `error` color respectively.

---

### Card

Cards are the primary surface for grouping related content in the Vercel dashboard.

| Property | Value |
|---|---|
| Background | `#ffffff` (light) / `#0a0a0a` (dark) |
| Border | `shadow-card` (shadow-based, no CSS border) |
| Padding | 24px (standard) / 16px (compact) / 32px (hero) |
| Radius | 8px (standard) / 12px (featured/hero) |
| Header border-bottom | `1px solid rgba(0,0,0,0.08)` |
| Inner gap | 16px between card sections |

Cards never use drop shadows for elevation — the border ring (`shadow-card`) provides all depth cues. Hover state adds `shadow-border-strong`.

---

### Navigation

Vercel's top navigation is a minimal horizontal bar with no background color in light mode.

| Property | Value |
|---|---|
| Height | 64px |
| Background | `transparent` → `rgba(255,255,255,0.8)` on scroll (with backdrop-filter blur) |
| Border-bottom | `1px solid rgba(0,0,0,0.08)` |
| Logo | Vercel triangle logotype, `#000000` / `#ffffff` |
| Nav item typography | `label-14`, weight 500, `#171717` |
| Nav item hover | `gray-900` text, no background change |
| Active/current page | `gray-1000` text, weight 600 |
| Dropdown | `shadow-popover`, 6px radius, `background-100` surface |
| CTA button | Primary button variant, right-aligned |

On mobile, navigation collapses to a hamburger menu. The mobile drawer uses full-height overlay with `background-100` fill.

---

### Badge

Badges communicate status, categories, or metadata in a compact pill format.

| Variant | Background | Text | Border | Padding | Radius | Font |
|---|---|---|---|---|---|---|
| Default/Gray | `#f7f7f7` | `#525252` | `rgba(0,0,0,0.08)` | 0 8px | 9999px | `label-12` weight 500 |
| Blue/Info | `#ebf5ff` | `#0068d6` | none | 0 8px | 9999px | `label-12` weight 500 |
| Green/Success | `#dcfce7` | `#15803d` | none | 0 8px | 9999px | `label-12` weight 500 |
| Red/Error | `#fee2e2` | `#b91c1c` | none | 0 8px | 9999px | `label-12` weight 500 |
| Amber/Warning | `#fef3c7` | `#92400e` | none | 0 8px | 9999px | `label-12` weight 500 |
| Black (CTA) | `#171717` | `#ffffff` | none | 0 10px | 9999px | `label-12` weight 500 |

Height is always 20px for inline badges, 24px for standalone badges. Optional dot indicator (8px circle) precedes the label for status variants.

---

## 8. Layout Principles

**Container system:**

| Name | Max Width | Gutter |
|---|---|---|
| Content | 1200px | 24px (desktop), 16px (tablet), 12px (mobile) |
| Wide | 1440px | 24px |
| Full | 100% | 24px |
| Prose | 680px | 24px |

**Grid:**
- 12-column grid on desktop
- 8-column on tablet
- 4-column on mobile
- Column gap: 24px desktop, 16px tablet, 12px mobile

**Vertical rhythm:**
- All section vertical gaps are multiples of the 8px base unit
- Hero sections: 96px top/bottom padding
- Standard sections: 64px top/bottom padding
- Feature sections: 48px top/bottom padding

**Z-index scale:**

| Layer | Value |
|---|---|
| Base | 0 |
| Raised | 10 |
| Dropdown | 100 |
| Sticky nav | 200 |
| Modal backdrop | 300 |
| Modal | 400 |
| Toast/Notification | 500 |

**Alignment:** Left-align body text and UI components by default. Center-align only for marketing hero content and short isolated CTAs. Never center-align multi-line body copy.

---

## 9. Responsive Behavior

| Breakpoint | Token | Min Width | Behavior |
|---|---|---|---|
| Mobile | `sm` | 0–400px | Single column, full-width components |
| Tablet-sm | `md` | 401–600px | 2-column grids begin, navigation collapses |
| Tablet | `lg` | 601–960px | 3-column grids, side-nav may appear |
| Desktop | `xl` | 961–1200px | Full layout, all columns active |
| Wide | `2xl` | 1201–1400px | Max-width containers centered |
| Ultra-wide | `3xl` | 1401px+ | Layout locked at max-width, outer whitespace grows |

**Responsive rules:**
- Navigation collapses to hamburger at `< 601px`
- Cards stack to single column at `< 601px`
- Typography scales down one step at `< 401px` (e.g., `heading-48` → `heading-40`)
- Horizontal padding reduces from 24px → 16px → 12px across breakpoints
- Touch targets must be minimum 44×44px at all breakpoints
- Line length for body text: 60–80 characters; enforce via `max-width: 680px` on prose containers

---

## 10. Tone & Guardrails

### DO

- Use `#171717` (not `#000000`) for body text in light mode — it reads as black but avoids optical harshness
- Use shadow-based borders (`box-shadow: 0 0 0 1px rgba(0,0,0,0.08)`) rather than CSS `border` on cards and components
- Apply the 2px white gap + 2px blue ring focus pattern for all interactive keyboard targets
- Reserve blue accent (`#0070f3` / `#0072f5`) for exactly one primary action per view
- Use `9999px` radius only for badges and pills — never for standard buttons
- Maintain consistent spacing rhythm using the 8px grid; all spacing values must be multiples of 4px minimum
- Use Geist Mono for all code snippets, CLI output, environment variable names, deployment IDs, and numeric dashboards
- Keep motion fast: 150ms for micro-interactions, 200ms for popovers, 300ms for page-level overlays
- Apply `prefers-reduced-motion` media query to all transitions and animations
- Use WCAG AA contrast (4.5:1) as the minimum; AA+ (7:1) for primary body text

### DON'T

- Don't use gradients on interactive UI (marketing hero backgrounds are the sole exception)
- Don't use more than one accent color per view
- Don't apply drop shadows for elevation on cards — use the ring-border shadow technique instead
- Don't mix border-radius families within a single view (e.g., 6px and 12px in the same card group)
- Don't use color to convey meaning without a secondary indicator (icon or text label) — support color-blind users
- Don't center-align multi-line body text or lists
- Don't use font weights other than 400, 500, and 600 — Vercel's visual language depends on this tight weight discipline
- Don't add decorative illustrations, stock photos, or abstract graphics in the dashboard UI
- Don't animate layout properties (width, height, top, left) — animate only `transform` and `opacity`
- Don't use `rgba(0,0,0,…)` dark-mode borders without inverting to `rgba(255,255,255,…)` equivalents
- Don't use the pill radius (`9999px`) on primary CTA buttons — it reads as friendly/playful, not as authoritative
- Don't deviate from the Geist typeface family in UI; third-party embed fonts are isolated to content areas only
