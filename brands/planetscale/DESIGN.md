# PlanetScale DESIGN.md

> MySQL-compatible serverless database platform — developer-first, monochrome-bold, with a single combustion-orange accent that earns every pixel.

## Overview

PlanetScale's design philosophy is precision through reduction. The brand lives in near-black and near-white, trusting a single vivid orange (`#f35815`) to carry all energy and interaction. The marketing site uses a **monospace body font** as a deliberate brand statement — code is the product, so code aesthetics are the interface. Headings switch to system sans-serif for hierarchy but the monospace substrate communicates authenticity to developers without needing to perform it.

The dashboard defaults to **dark mode** (`:root` maps `--bg-primary` to `#111111`) but ships a complete light-mode token set. Both modes share the same neutral gray ramp; only the semantic aliases flip. Color gamut enhancement via `oklch()` is applied automatically in P3-capable displays for more vivid status colors.

Core principles:
- **Dark by default** — the dashboard renders `#111111` canvas from the very first paint; light mode is opt-in, not an afterthought
- **Monospace as brand** — system monospace for UI body text signals that PlanetScale is a product for engineers, not managers
- **One accent, one purpose** — `#f35815` (orange-500) is the brand color and the primary CTA color; it is never diluted with gradients or opacity in interactive contexts
- **Semantic token indirection** — every component references `--text-primary`, `--bg-secondary`, etc., never raw hex; swapping dark/light flips the entire system with a single class change
- **8 px grid** — all spacing is multiples of 8 px; the Tailwind scale is remapped accordingly (spacing-1 = 8 px)
- **Tight negative tracking on display text** — headings use progressive letter-spacing reduction (–0.006 em at 14 px, –0.019 em at 24 px) to compensate for optical expansion at size

---

## Colors

### Primitive Ramp

| Token | Hex | Description |
|-------|-----|-------------|
| `--white` | `rgba(255,255,255,1)` | Pure white |
| `--black` | `rgba(0,0,0,1)` | Pure black |
| `--gray-50` | `#fafafa` | Near-white surface |
| `--gray-100` | `#ebebeb` | Subtle divider / input bg |
| `--gray-200` | `#e1e1e1` | Disabled state bg |
| `--gray-300` | `#c1c1c1` | Border quiet |
| `--gray-400` | `#a1a1a1` | Placeholder / disabled text |
| `--gray-500` | `#818181` | Secondary icon |
| `--gray-550` | `#737373` | Mid-gray helper |
| `--gray-600` | `#616161` | Subdued label |
| `--gray-700` | `#414141` | Primary text (light mode) |
| `--gray-800` | `#2b2b2b` | Strong surface (light) |
| `--gray-850` | `#1a1a1a` | Secondary canvas (dark) |
| `--gray-900` | `#111111` | Primary canvas (dark) |

### Brand Accent — Orange

| Token | Hex | Usage |
|-------|-----|-------|
| `--orange-300` | `#fc9c66` | Hover tint on orange elements |
| `--orange-400` | `#fd812d` | Warm hover state |
| `--orange-500` | `#f35815` | **Primary brand accent; all CTA buttons** |
| `--orange-600` | `#b83a05` | Pressed / active button |
| `--orange-700` | `#962d00` | Destructive-adjacent emphasis |

### Semantic Tokens — Dark Mode (default `:root`)

| Token | Resolves to | Hex | Usage |
|-------|-------------|-----|-------|
| `--bg-primary` | `--gray-900` | `#111111` | Page / app canvas |
| `--bg-secondary` | `--gray-850` | `#1a1a1a` | Cards, panels, sidebar |
| `--bg-inverted` | `--white` | `#ffffff` | Inverted surfaces |
| `--text-primary` | `--gray-200` | `#e1e1e1` | Body text, labels |
| `--text-secondary` | `--gray-400` | `#a1a1a1` | Captions, metadata |
| `--text-contrast` | `--white` | `#ffffff` | Text on colored backgrounds |
| `--text-disabled` | `--gray-600` | `#616161` | Disabled text |
| `--text-orange` | `--orange-500` | `#f35815` | Accent text, icon tint |
| `--border-primary` | `--gray-700` | `#414141` | Default borders |

### Semantic Tokens — Light Mode (`.light` class)

| Token | Resolves to | Hex | Usage |
|-------|-------------|-----|-------|
| `--bg-primary` | `--gray-50` | `#fafafa` | Page canvas |
| `--bg-secondary` | `--gray-100` | `#ebebeb` | Cards, panels |
| `--bg-inverted` | `--gray-900` | `#111111` | Dark surfaces in light mode |
| `--text-primary` | `--gray-700` | `#414141` | Body text |
| `--text-secondary` | `--gray-550` | `#737373` | Captions |
| `--text-contrast` | `--black` | `#000000` | Maximum contrast text |
| `--text-disabled` | `--gray-400` | `#a1a1a1` | Disabled text |
| `--border-primary` | `--gray-700` | `#414141` | Default borders |

### Status / Semantic Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--blue-500` | `#1e9de7` | Focus rings, interactive highlights, info |
| `--blue-600` | `#0b6ec5` | Info text (light mode) |
| `--green-500` | `#27b648` | Success bg; success text (dark mode) |
| `--green-600` | `#13862e` | Success text (light mode) |
| `--red-400` | `#ff7082` | Error text (dark mode) |
| `--red-600` | `#d92038` | Error text (light mode) |
| `--yellow-300` | `#f2b600` | Warning highlight |
| `--purple-400` | `#a18bf5` | Postgres accent / premium indicator |
| `--text-postgres` | `#336791` | PostgreSQL brand color |

---

## Typography

### Font Families

| Role | Stack | Notes |
|------|-------|-------|
| **UI body / marketing body** | `ui-monospace, SFMono-Regular, "SF Mono", Menlo, Consolas, "Liberation Mono", monospace` | Default `body` font; distinctive developer brand choice |
| **Marketing headings** | `ui-sans-serif, system-ui, sans-serif` | Applied via `.sans-prose` class for long-form content |
| **Brand materials** | `Inter` | Specified in brand guidelines for off-product assets |
| **Code blocks** | `Roboto Mono` | Brand guidelines; falls back to system monospace |

> The monospace-as-default-body is intentional and distinctive — it communicates that PlanetScale is a developer tool at a glance without any copy.

### Type Scale

| Token | Size | Line Height | Letter Spacing | Weight | Usage |
|-------|------|-------------|----------------|--------|-------|
| `text-xs` | `12px` | — | `0` | 400 | Labels, badges, captions |
| `text-sm` | `14px` | — | `−0.006em` | 400 / 500 | Secondary text, table cells |
| `text-base` | `16px` | `1.5` | — | 400 | Body text, form inputs |
| `text-lg` | `18px` | — | `−0.014em` | 400 | Lead text, large labels |
| `text-2xl` | `24px` | `1.2` | `−0.019em` | 600 | Card headings, section titles |
| `text-[32px]` | `32px` | — | — | 600 | Page titles (utility class) |

### Heading Scale (`.sans-prose` context)

| Level | Size | Line Height | Letter Spacing | Weight |
|-------|------|-------------|----------------|--------|
| `h1` | `24px` | `1.2` | `−0.019em` | `600` |
| `h2` | `20px` | `1.1` | `−0.017em` | `600` |
| `h3` | `18px` | — | `−0.014em` | `600` |
| `h4` | inherited | — | — | `600` |
| `h5` | `14px` | — | `−0.006em` | `600` |
| `h6` | `12px` | — | `0` | `600` |

### Font Weights

| Value | Class | Usage |
|-------|-------|-------|
| `400` | `font-normal` | Body text, table data |
| `500` | `font-medium` | Secondary labels, badges |
| `600` | `font-semibold` | Headings, button labels, emphasized text |
| `700` | `font-bold` | Rare; reserved for maximum emphasis |

> Brand guidelines explicitly say: **avoid Bold (700) weight** in brand materials. Semibold (600) is the maximum intended weight.

### Smoothing

`-webkit-font-smoothing: antialiased` and `-moz-osx-font-smoothing: grayscale` are applied globally to `body`.

---

## Spacing

Base unit: **8 px**. The Tailwind spacing scale is remapped so that spacing-1 = 8 px (not the default 4 px). All padding, margin, and gap values in the system are multiples of 8 px.

| Token | Value | Common usage |
|-------|-------|-------------|
| `spacing-0` | `0px` | Reset |
| `spacing-1` | `8px` | Icon padding, tight gaps, badge padding |
| `spacing-2` | `16px` | Button horizontal padding, form field padding |
| `spacing-3` | `24px` | Card padding, section rhythm |
| `spacing-4` | `32px` | Section padding, page gutters |
| `spacing-5` | `40px` | Button height (standard), hero spacing |
| `spacing-6` | `48px` | Panel padding, large gaps |
| `spacing-8` | `64px` | Section vertical margins |
| `spacing-9` | `72px` | Large section separators |
| `spacing-12` | `96px` | Hero and marketing section padding |

---

## Border Radius

PlanetScale's radius vocabulary is intentionally minimal — almost nothing is rounded, reinforcing a precise, technical aesthetic.

| Token | Value | Usage |
|-------|-------|-------|
| `rounded-sm` | `2px` (`.125rem`) | Checkboxes, radio buttons, micro-elements |
| `rounded` | `4px` (`.25rem`) | Inputs, cards, dropdowns, code blocks, buttons |
| `rounded-full` | `9999px` | Pills (badges, tags, toggle indicators) |

> Buttons use `rounded` (4 px). There is no `rounded-lg`, `rounded-xl`, or `rounded-2xl` in use — the system deliberately avoids soft, approachable curves.

---

## Shadows

PlanetScale's dark-first design minimizes shadow usage since elevation is communicated through background color contrast rather than drop shadows.

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 2px 0 rgb(0 0 0 / 0.05)` | Subtle lift on inputs and small cards |
| `shadow-lg` | `0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1)` | Dropdown menus, floating panels |
| `shadow-black/20` | `rgb(0 0 0 / 0.2)` tint | Combined with other shadows for deep panels |
| `shadow-black/35` | `rgb(0 0 0 / 0.35)` tint | Modal overlays |
| Focus ring | `0 0 0 1px #1e9de7` + offset | All interactive elements on focus |

> In dark mode, elevation is primarily conveyed by `--bg-secondary` (`#1a1a1a`) sitting above `--bg-primary` (`#111111`) — shadows play a supporting role.

---

## Components

### Button

The primary button is the only consistently colored element in the interface. Every other surface is neutral.

| Property | Value |
|----------|-------|
| Background | `#f35815` (`--orange-500`) |
| Text color | `#ffffff` |
| Font weight | `600` |
| Font size | `16px` (base) |
| Height | `40px` |
| Horizontal padding | `16px` |
| Border radius | `4px` |
| Display | `inline-flex`, `align-items: center`, `gap: 4px` |
| Hover background | `#fd812d` (`--orange-400`) |
| Active / pressed | `#b83a05` (`--orange-600`) |
| Focus ring | `0 0 0 2px #1e9de7` with 2 px offset |
| Transition | `all 150ms cubic-bezier(0.4, 0, 0.2, 1)` |

**Small variant:**
- Height: `32px`
- Horizontal padding: `8px`

**Secondary / ghost variant (dark mode):**
- Background: transparent
- Border: `1px solid --border-primary` (`#414141`)
- Text: `--text-primary` (`#e1e1e1`)
- Hover: background `--bg-secondary` (`#1a1a1a`)

---

### Input

| Property | Value |
|----------|-------|
| Background | `--bg-secondary` (`#1a1a1a` dark / `#ebebeb` light) |
| Text color | `--text-primary` |
| Border | `1px solid --border-primary` (`#414141`) |
| Border radius | `4px` |
| Padding | `8px 12px` |
| Font size | `16px` |
| Line height | `1.5` |
| Placeholder color | `#a1a1a1` (`--gray-400`) |
| Focus border | `#1e9de7` (`--blue-500`) |
| Focus ring | `0 0 0 1px #1e9de7` |
| Disabled | Background `--bg-primary`, text `--text-disabled`, opacity 0.5 |

---

### Card

Cards use `--bg-secondary` to float above the `--bg-primary` canvas without needing a shadow.

| Property | Value |
|----------|-------|
| Background | `--bg-secondary` (`#1a1a1a` dark / `#ebebeb` light) |
| Border | `1px solid --border-primary` (`#414141`) |
| Border radius | `4px` |
| Padding | `24px` (standard) / `16px` (compact) |
| Header font weight | `600` |
| Body font size | `14px` |
| Body text color | `--text-secondary` |

---

### Navigation (Sidebar)

PlanetScale's app dashboard uses a collapsible left sidebar.

| Property | Value |
|----------|-------|
| Background | `--bg-primary` (`#111111`) |
| Width (expanded) | ~220px |
| Width (collapsed) | icon-only (~48px) |
| Nav item padding | `8px 16px` |
| Nav item radius | `4px` |
| Nav item font size | `14px` |
| Nav item font weight | `400` (resting), `500` (active) |
| Active item bg | `--bg-secondary` (`#1a1a1a`) |
| Active item text | `--text-primary` (`#e1e1e1`) |
| Hover item bg | `rgb(65 65 65 / 0.5)` |
| Icon color | `--text-secondary` (`#a1a1a1`) |
| Icon color (active) | `--text-primary` (`#e1e1e1`) |
| Border right | `1px solid --border-primary` |
| Breadcrumb separator | `--text-secondary` |

---

### Badge

| Variant | BG | Text | Border |
|---------|-----|------|--------|
| Default / neutral | `--bg-secondary` | `--text-secondary` | `--border-primary` |
| Success | `--green-950` (`#041A0A`) | `--green-400` (`#40d763`) | `--green-700` |
| Error | `--red-950` (`#200A0D`) | `--red-400` (`#ff7082`) | `--red-700` |
| Warning | `--yellow-950` (`#171101`) | `--yellow-300` (`#f2b600`) | `--yellow-600` |
| Info | `--blue-950` (`#04122E`) | `--blue-400` (`#47b7f8`) | `--blue-700` |
| Orange / brand | `--orange-950` (`#240B00`) | `--orange-300` (`#fc9c66`) | `--orange-600` |

| Property | Value |
|----------|-------|
| Border radius | `9999px` (pill) |
| Padding | `2px 8px` |
| Font size | `12px` |
| Font weight | `500` |
| Line height | `1.5` |

---

### Table

| Property | Value |
|----------|-------|
| Background | `--bg-primary` |
| Header bg | `--bg-secondary` |
| Header font size | `12px` |
| Header font weight | `500` |
| Header text color | `--text-secondary` |
| Header letter spacing | `0.04em` (uppercase tracking) |
| Cell padding | `12px 16px` |
| Cell font size | `14px` |
| Row border | `1px solid --border-primary` (`#414141`) |
| Hover row bg | `rgb(65 65 65 / 0.3)` |
| Border collapse | `collapse` |

---

## Layout Principles

- **Max content width: 1200px**, centered with auto horizontal margins
- **Page gutter**: `24px` mobile → `48px` desktop
- **Section vertical rhythm**: `64px–96px` between major page sections
- **Sidebar layout**: fixed left sidebar + scrollable main content area; sidebar collapses to icon-only on narrow screens
- **Grid**: 12-column CSS grid for marketing pages; single-column with sidebar for app dashboard
- **Breakpoints** (Tailwind defaults): `sm: 640px`, `md: 768px`, `lg: 1024px`, `xl: 1280px`
- **Consistent 8 px grid**: all element sizing and spacing snaps to 8 px multiples
- **No decorative gradients in UI**: gradients are reserved for hero/marketing backgrounds; product UI uses flat color only
- **Z-index ladder**: base (0) → cards (10) → sticky header (100) → dropdown (200) → modal (300) → toast (400)

---

## Responsive Behavior

| Viewport | Behavior |
|----------|----------|
| `< 640px` (mobile) | Sidebar collapses to bottom nav or hamburger drawer; single-column layout; page padding 16px |
| `640–1024px` (tablet) | Sidebar auto-collapses to icon-only; content area expands to fill; page padding 24px |
| `> 1024px` (desktop) | Full sidebar visible; two-column or three-column layouts unlock; page padding 48px |

- Mobile navigation uses the same sidebar UI in a slide-out drawer pattern
- Tables on mobile scroll horizontally within their container; no column hiding
- Cards stack vertically below `md` breakpoint
- The brand hero gradient canvas downgrades gracefully — `prefers-reduced-motion` disables the animated pixel grid
- Typography does **not** use fluid/clamp scaling; sizes are fixed across breakpoints

---

## Tone & Guardrails

### DO

- **Use `#f35815` (orange-500) for one thing: primary actions.** CTAs, active states, and brand moments. Don't dilute it.
- **Keep button labels short** — maximum 3 words. PlanetScale's UI copy is terse: "Get started", "Deploy", "Connect", never "Click here to get started".
- **Use monospace for code, data, branch names, and keys** — the font stack communicates precision in these contexts.
- **Pair `--text-primary` with `--bg-primary`** for reading comfort; avoid placing light gray text on slightly-lighter-gray backgrounds.
- **Communicate status exclusively with the status palette** — green for live/success, red for error, yellow for warning. Never use orange for status (it belongs to the brand layer).
- **Use `border-primary` (#414141) borders to define structure** — a 1 px border on a card is always more precise than a shadow.
- **Default to dark mode** in any embedded widget, screenshot, or code example that reflects the product.
- **Maintain 4 px border radius on interactive elements** — consistency here is load-bearing for the "precise tool" aesthetic.

### DON'T

- **Don't use orange for more than one thing** — mixing it into status indicators, hover states, and decorative elements destroys the accent's signal value.
- **Don't use `font-weight: 700` (bold)** in brand-facing copy — semibold (600) is the maximum per brand guidelines.
- **Don't round corners beyond 4 px** in the product UI — `rounded-lg` or `rounded-xl` (8 px+) read as consumer-app softness, not developer tool precision.
- **Don't use shadow-heavy elevation** in the dark UI — elevation is expressed through the `#111111` → `#1a1a1a` background step. Adding drop shadows over that creates visual noise.
- **Don't use more than two neutral grays in a single component** — pick `--text-primary` and `--text-secondary`; introducing a third neutral creates ambiguous hierarchy.
- **Don't fake the monospace aesthetic** — don't use a proportional font and apply `letter-spacing` to mimic it. Use the actual system monospace stack.
- **Don't place text on the orange accent** except in white — orange-on-orange-tint and orange-on-dark-orange both fail contrast thresholds.
- **Don't use the orange gradient** from the marketing hero canvas in the product UI — it's a brand set-piece for landing pages, not an interface element.
- **Don't add decorative illustrations** — PlanetScale's product UI uses 3D renders and data-driven diagrams for visual interest, not icon sets or flat illustrations.
- **Don't use purple (`--purple-*`) outside of Postgres-specific contexts** — it is reserved as a semantic differentiator for the PostgreSQL product line.
