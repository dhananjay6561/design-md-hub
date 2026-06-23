# GitHub DESIGN.md

> The world's home for code — a developer collaboration platform where functional density and open-source culture shape every design decision.

## Overview

GitHub's design system, Primer, is built on a philosophy of **functional clarity**. The UI is a tool used by millions of developers daily; ornamentation is minimized, information density is respected, and every component earns its presence by serving workflow. The aesthetic reads as clean and professional rather than decorative: cool neutral grays, a single confident blue accent, and a typography system borrowed from system fonts that feels native across every OS.

Core principles:
- **Developer ergonomics first** — dense layouts are acceptable when they match the cognitive model of power users
- **Semantic color, not decorative color** — color signals meaning (danger, success, open, closed, merged) rather than style
- **Adaptive theming** — full light and dark mode parity; neither is an afterthought
- **Accessible by default** — WCAG AA contrast enforced across all semantic tokens; color is never the sole signal
- **System-native feel** — system font stacks and border radiuses that feel at home in any OS or browser
- **Functional motion** — transitions are short (80ms) and purposeful; no animations for their own sake

---

## Colors

### Light Mode

| Token | Hex | Usage |
|-------|-----|-------|
| `--bgColor-default` | `#FFFFFF` | Page background, card surfaces, modal backgrounds |
| `--bgColor-muted` | `#F6F8FA` | Secondary surfaces, code block backgrounds, sidebar fills |
| `--bgColor-emphasis` | `#25292E` | High-contrast backgrounds, tooltips |
| `--bgColor-inverse` | `#1F2328` | Inverted sections, dark banners |
| `--fgColor-default` | `#1F2328` | Primary text, headings, body copy |
| `--fgColor-muted` | `#59636E` | Secondary text, timestamps, metadata, placeholders |
| `--fgColor-disabled` | `#818B98` | Disabled text and icons |
| `--fgColor-onEmphasis` | `#FFFFFF` | Text on emphasis/dark backgrounds |
| `--borderColor-default` | `#D1D9E0` | Standard dividers, input borders, card edges |
| `--borderColor-muted` | `#D1D9E0B3` | Subtle dividers, de-emphasized separators |
| `--borderColor-emphasis` | `#818B98` | Prominent borders, selected states |
| `--fgColor-accent` | `#0969DA` | Links, interactive elements, primary icon color |
| `--bgColor-accent-muted` | `#DDF4FF` | Accent tint backgrounds, info banners |
| `--bgColor-accent-emphasis` | `#0969DA` | Accent filled backgrounds |
| `--fgColor-success` | `#1A7F37` | Success text, open issue/PR icons |
| `--bgColor-success-muted` | `#DAFBE1` | Success tint backgrounds |
| `--bgColor-success-emphasis` | `#1F883D` | Success filled backgrounds |
| `--fgColor-danger` | `#D1242F` | Error text, destructive actions, closed state |
| `--bgColor-danger-muted` | `#FFEBE9` | Error tint backgrounds |
| `--bgColor-danger-emphasis` | `#CF222E` | Danger filled backgrounds, destructive buttons |
| `--fgColor-attention` | `#9A6700` | Warning/caution text |
| `--bgColor-attention-muted` | `#FFF8C5` | Warning tint backgrounds |
| `--bgColor-attention-emphasis` | `#BF8700` | Warning filled backgrounds |
| `--fgColor-severe` | `#BC4C00` | Severe warning text (more urgent than attention) |
| `--bgColor-severe-muted` | `#FFF1E5` | Severe tint backgrounds |
| `--fgColor-done` | `#8250DF` | Merged PR, completed state text and icons |
| `--bgColor-done-muted` | `#FBEFFF` | Done/merged tint backgrounds |
| `--bgColor-done-emphasis` | `#8250DF` | Done filled backgrounds |
| `--fgColor-sponsors` | `#BF3989` | GitHub Sponsors UI elements |
| `--bgColor-sponsors-muted` | `#FFEFF7` | Sponsors tint backgrounds |

### Dark Mode

| Token | Hex | Usage |
|-------|-----|-------|
| `--bgColor-default` | `#0D1117` | Page background |
| `--bgColor-muted` | `#151B23` | Secondary surfaces, code block backgrounds |
| `--bgColor-emphasis` | `#3D444D` | High-contrast backgrounds, tooltips |
| `--fgColor-default` | `#F0F6FC` | Primary text (maps to neutral.12 in dark palette) |
| `--fgColor-muted` | `#9198A1` | Secondary text, metadata |
| `--fgColor-disabled` | `#656C76` | Disabled states |
| `--borderColor-default` | `#3D444D` | Standard borders |
| `--borderColor-muted` | `#3D444DB3` | Subtle borders |
| `--fgColor-accent` | `#4493F8` | Links, interactive elements |
| `--bgColor-accent-muted` | `#388BFD1A` | Accent tint backgrounds |
| `--fgColor-success` | `#3FB950` | Success / open state text |
| `--bgColor-success-muted` | `#2EA04326` | Success tint |
| `--bgColor-success-emphasis` | `#238636` | Success filled |
| `--fgColor-danger` | `#F85149` | Danger / error text |
| `--bgColor-danger-muted` | `#F851491A` | Danger tint |
| `--bgColor-danger-emphasis` | `#DA3633` | Danger filled |
| `--fgColor-attention` | `#D29922` | Warning text |
| `--bgColor-attention-muted` | `#BB800926` | Warning tint |
| `--fgColor-done` | `#AB7DF8` | Merged/done text |
| `--bgColor-done-muted` | `#AB7DF826` | Done tint |

### Base Color Scales (Light)

These are the raw palette values underlying the semantic tokens above.

| Scale | 0 (lightest) | 1 | 2 | 3 | 4 | 5 (default) |
|-------|-------------|---|---|---|---|-------------|
| **Blue** | `#DDF4FF` | `#B6E3FF` | `#80CCFF` | `#54AEFF` | `#218BFF` | `#0969DA` |
| **Green** | `#DAFBE1` | `#ACEEBB` | `#6FDD8B` | `#4AC26B` | `#2DA44E` | `#1A7F37` |
| **Red** | `#FFEBE9` | `#FFCECB` | `#FFABA8` | `#FF8182` | `#FA4549` | `#CF222E` |
| **Purple** | `#FBEFFF` | `#ECD8FF` | `#D8B9FF` | `#C297FF` | `#A475F9` | `#8250DF` |
| **Yellow** | `#FFF8C5` | `#FAE17D` | `#EAC54F` | `#D4A72C` | `#BF8700` | `#9A6700` |
| **Orange** | `#FFF1E5` | `#FFD8B5` | `#FFB77C` | `#FB8F44` | `#E16F24` | `#BC4C00` |
| **Pink** | `#FFEFF7` | `#FFD3EB` | `#FFADDA` | `#FF80C8` | `#E85AAD` | `#BF3989` |

### Neutral Scale (Light)

| Step | Hex | Usage |
|------|-----|-------|
| `neutral.0` | `#FFFFFF` | Default background |
| `neutral.1` | `#F6F8FA` | Muted background |
| `neutral.2` | `#EFF2F5` | — |
| `neutral.3` | `#E6EAEF` | — |
| `neutral.4` | `#E0E6EB` | — |
| `neutral.5` | `#DAE0E7` | — |
| `neutral.6` | `#D1D9E0` | Default border |
| `neutral.7` | `#C8D1DA` | — |
| `neutral.8` | `#818B98` | Disabled text / emphasis border |
| `neutral.9` | `#59636E` | Muted text |
| `neutral.10` | `#454C54` | — |
| `neutral.11` | `#393F46` | — |
| `neutral.12` | `#25292E` | Emphasis background |
| `neutral.13` | `#1F2328` | Default text (black) |

---

## Typography

### Font Families

| Token | Stack | Usage |
|-------|-------|-------|
| `--fontStack-sansSerif` | `'Mona Sans VF', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji'` | All UI text, body, labels, headings. Mona Sans VF leads the stack as GitHub's primary brand font. |
| `--fontStack-monospace` | `ui-monospace, SFMono-Regular, SF Mono, Menlo, Consolas, Liberation Mono, monospace` | Code blocks, inline code, terminal output, commit SHAs |

The primary font family uses OS-native system fonts. GitHub ships **Mona Sans** (a variable sans-serif) as an enhanced brand-level override (`'Mona Sans VF'`) when available, falling back to the system stack seamlessly.

### Type Scale

| Name | Size (rem) | Size (px) | Weight | Line Height | Usage |
|------|-----------|-----------|--------|-------------|-------|
| Display | 2.5rem | 40px | 500 | 1.375 | Hero headings, marketing |
| Title Large (`h00`) | 3rem | 48px (desktop) | 600 | 1.25 | Page-level super-headings |
| `h0` | 2.5rem | 40px (desktop) / 32px (mobile) | 600 | 1.25 | Section super-titles |
| `h1` | 2rem | 32px (desktop) / 26px (mobile) | 600 | 1.25 | Page titles |
| `h2` | 1.5rem | 24px (desktop) / 22px (mobile) | 600 | 1.25 | Section headings |
| `h3` | 1.25rem | 20px (desktop) / 18px (mobile) | 600 | 1.25 | Sub-section headings |
| `h4` | 1rem | 16px | 600 | 1.5 | Component headings |
| `h5` | 0.875rem | 14px | 600 | 1.5 | Small headings, labels |
| `h6` | 0.75rem | 12px | 600 | 1.5 | Micro headings, captions |
| Body (default) | 0.875rem | 14px | 400 | 1.5 | Body text, UI labels |
| Body Large | 1rem | 16px | 400 | 1.5 | Larger body text |
| Caption / Small | 0.75rem | 12px | 400 | 1.25 | Timestamps, metadata, helper text |

### Font Weights

| Token | Value | Usage |
|-------|-------|-------|
| `--base-text-weight-light` | 300 | Display/hero text (marketing only) |
| `--base-text-weight-normal` | 400 | Body text, paragraph copy |
| `--base-text-weight-medium` | 500 | Semibold UI labels, emphasized text |
| `--base-text-weight-semibold` | 600 | All headings, button text, strong emphasis |

### Line Heights

| Name | Value | Usage |
|------|-------|-------|
| `tight` / condensed | 1.25 | Headings, compact lists |
| `snug` | 1.375 | Display headings |
| `normal` / default | 1.5 | Body text, UI labels |
| `relaxed` | 1.625 | Long-form prose |
| `loose` | 1.75 | Large text, accessibility contexts |

> **Note:** The base body font size is **14px** (not 16px). GitHub's UI is intentionally compact to support information-dense developer workflows. All dimension tokens use `rem` so they scale with browser zoom.

---

## Spacing

The base spacer unit is **8px**. The scale doubles and expands from this foundation.

| Token | Variable | Value | Usage |
|-------|----------|-------|-------|
| `space.xxs` | `--base-size-2` | 2px | Form field separators, tight dividers |
| `space.xs` | `--base-size-4` | 4px | Badge padding, icon gaps, tight internal margins |
| `space.sm` | `--base-size-8` | 8px | Standard component gaps, flex/grid item separation |
| `space.md` | `--base-size-12` | 12px | Comfortable container padding, section separators |
| `space.lg` | `--base-size-16` | 16px | Major layout divisions, primary container margins |
| `space.xl` | `--base-size-24` | 24px | Large section separation, page-level padding |
| — | `--base-size-32` | 32px | Feature section gaps |
| — | `--base-size-40` | 40px | Large feature areas |
| — | `--base-size-48` | 48px | Stack condensed padding |
| — | `--base-size-64` | 64px | Page-level vertical rhythm |
| — | `--base-size-80` | 80px | Hero section padding |
| — | `--base-size-96` | 96px | Extra-large section spacing |
| — | `--base-size-128` | 128px | Maximum vertical section gap |

### Semantic Stack Tokens

| Token | Value | Usage |
|-------|-------|-------|
| `--stack-gap-condensed` | 8px | Tight component groupings |
| `--stack-gap-normal` | 16px | Default component spacing |
| `--stack-gap-spacious` | 24px | Relaxed, open layouts |
| `--stack-padding-condensed` | 8px | Tight container insets |
| `--stack-padding-normal` | 16px | Default container insets |
| `--stack-padding-spacious` | 24px | Generous container insets |

---

## Border Radius

| Token | Variable | Value | Usage |
|-------|----------|-------|-------|
| `borderRadius-small` | `$border-radius-1` | 4px | Badges, labels, small tags, inputs |
| `borderRadius-medium` | `$border-radius-2` | 6px | Buttons, cards, dropdown menus (default) |
| `borderRadius-large` | `$border-radius-3` | 8px | Modals, popovers, dialogs, larger containers |
| `borderRadius-full` | — | 50% / 9999px | Avatars, circular icon buttons, pill-shaped badges |

The default border radius for interactive elements (`$border-radius`) is **6px**.

---

## Shadows

Primer uses a layered shadow vocabulary. Light and dark modes have distinct shadow colors (dark neutral tones in light mode, dark-transparent overlays in dark mode).

| Token | CSS Equivalent | Usage |
|-------|---------------|-------|
| `shadow.inset` | `inset 0 1px 0 rgba(dark, 0.04)` | Inset for input fields, pressed buttons, wells |
| `shadow.resting.xsmall` | `0 1px 1px rgba(dark, 0.05)` | Subtle lift for inline elements |
| `shadow.resting.small` | `0 1px 2px rgba(dark, 0.07), 0 1px 1px rgba(dark, 0.05)` | Buttons (default rest state), small cards |
| `shadow.resting.medium` | `0 3px 6px rgba(dark, 0.08), 0 2px 4px rgba(dark, 0.06)` | Dropdown menus, popovers |
| `shadow.resting.large` | `0 8px 24px rgba(dark, 0.12)` | Modals, overlays, dialogs |
| `shadow.resting.xlarge` | `0 16px 48px rgba(dark, 0.14)` | Full-screen dialogs, large overlays |
| `shadow.floating.small` | `0 1px 3px rgba(dark, 0.12), 0 8px 24px rgba(dark, 0.12)` | Floating action elements |
| `shadow.floating.medium` | `0 1px 3px rgba(dark, 0.12), 0 16px 32px rgba(dark, 0.16)` | Floating panels, autocomplete lists |
| `shadow.highlight` | `inset 0 1px 0 rgba(white, 0.25)` | Top-edge highlight on primary/dark buttons |
| `shadow.focus` | `0 0 0 3px rgba(accent, 0.40)` | Keyboard focus ring on all interactive elements |

---

## Components

### Button

Buttons use a **6px border radius**, **14px font size** (body default), **weight 600 (semibold)**, and a fixed **20px line height** (not inherited). The base padding is `5px 16px` for medium.

| Variant | Background | Text | Border | Usage |
|---------|------------|------|--------|-------|
| **Default** | `--button-default-bgColor-rest` ≈ `#F6F8FA` | `--fgColor-default` `#1F2328` | `--borderColor-default` `#D1D9E0` | Standard secondary actions |
| **Primary** | `--button-primary-bgColor-rest` ≈ `#1F883D` | `#FFFFFF` | `--button-primary-borderColor-rest` ≈ `#1A7F37` | Highest-priority CTA; use at most once per group |
| **Danger** | `--bgColor-danger-emphasis` `#CF222E` | `#FFFFFF` | `#B91C1C` | Destructive actions; always confirm before submit |
| **Invisible** | `transparent` | `--fgColor-accent` `#0969DA` | `transparent` | Minimal UI, compound component actions |

**Sizes:**

| Size | Height | Padding | Font |
|------|--------|---------|------|
| Small | 28px | `3px 12px` | 12px |
| Medium (default) | 32px | `5px 16px` | 14px |
| Large | 40px | `9px 20px` | 16px |

**States:** Hover shifts background slightly lighter/darker; active applies an inset shadow; disabled sets `--fgColor-disabled` text and `cursor: default`; loading replaces visual slot with a spinner.

---

### Input / Text Input

| Property | Value |
|----------|-------|
| Height (medium) | 32px |
| Height (small) | 28px |
| Height (large) | 40px |
| Padding | `5px 12px` (medium) |
| Border | `1px solid --borderColor-default` (`#D1D9E0`) |
| Border radius | 6px |
| Background | `--bgColor-default` (`#FFFFFF`) |
| Font size | 14px |
| Font family | `--fontStack-sansSerif` |
| Focus border | `--borderColor-accent-emphasis` (`#0969DA`) |
| Focus ring | `0 0 0 3px rgba(#0969DA, 0.40)` |
| Error border | `--borderColor-danger-emphasis` (`#CF222E`) |
| Disabled background | `--bgColor-muted` (`#F6F8FA`) |
| Monospace variant | Uses `--fontStack-monospace` — for tokens, SHAs, config values |

---

### Card

Cards are content containers using `--bgColor-default` in light mode and `--bgColor-muted` in dark mode (the inversion is intentional — in dark mode, cards are slightly lighter than the page).

| Property | Value |
|----------|-------|
| Background | Light: `#FFFFFF` / Dark: `#151B23` |
| Border | `1px solid --borderColor-default` (`#D1D9E0` light, `#3D444D` dark) |
| Border radius | 6px |
| Padding | 16px (normal) or 24px (spacious) |
| Shadow | `shadow.resting.small` on hover/interaction; none at rest for inline cards |

Cards never have background fills for decorative purposes; color only appears in semantic variants (accent, danger, success).

---

### Navigation

GitHub uses two primary navigation patterns: the **global header bar** and the **side NavList**.

**Global Header (`header`):**

| Property | Value |
|----------|-------|
| Background | `#161B22` (dark, consistent across light/dark page themes) |
| Text color | `#E6EDF3` |
| Height | 48px |
| Padding | `0 16px` |
| Logo color | `#FFFFFF` |
| Border-bottom | `1px solid #30363D` |

**Side NavList:**

| State | Background | Text |
|-------|------------|------|
| Rest | `transparent` | `--fgColor-default` |
| Hover | `--bgColor-muted` (`#F6F8FA`) | `--fgColor-default` |
| Active / current page | `--bgColor-accent-muted` (`#DDF4FF`) | `--fgColor-accent` (`#0969DA`) |

- Items: `8px` horizontal padding, `6px` vertical padding, `6px` border radius
- Active state uses a left border or background tint to signal current location
- Leading visuals (Octicons) sized at 16px, color inherits from text

---

### Badge / Label

Labels are small inline metadata chips. Default size is small; a large variant is available.

| Property | Small | Large |
|----------|-------|-------|
| Font size | 12px | 14px |
| Padding | `0 7px` (5px vertical) | `0 10px` (6px vertical) |
| Height | ~20px | ~24px |
| Border radius | 999px (pill) for status labels; 4px for category labels |
| Font weight | 500 |

**Semantic color variants:**

| Variant | Background | Text | Border | Usage |
|---------|------------|------|--------|-------|
| Default | `#EFF2F5` | `#454C54` | `#D1D9E0` | Neutral tags |
| Accent / Info | `#DDF4FF` | `#0969DA` | `#B6E3FF` | Informational state |
| Success / Open | `#DAFBE1` | `#1A7F37` | `#ACEEBB` | Open issues, PRs |
| Danger / Closed | `#FFEBE9` | `#CF222E` | `#FFCECB` | Closed items, errors |
| Attention | `#FFF8C5` | `#9A6700` | `#FAE17D` | Warnings |
| Done / Merged | `#FBEFFF` | `#8250DF` | `#ECD8FF` | Merged PRs, completed |
| Draft | `#EFF2F5` | `#59636E` | `#D1D9E0` | Draft / WIP states |
| Sponsors | `#FFEFF7` | `#BF3989` | `#FFD3EB` | Sponsors feature |

---

## Layout Principles

**Container widths:**

| Container | Width | Usage |
|-----------|-------|-------|
| Default | `980px` | Repository pages, standard content |
| Full-width | `100%` | Code editors, diff views, dashboards |
| Narrow | `544px` | Auth flows, settings forms |

**Grid gutters:**

| Breakpoint | Gutter |
|------------|--------|
| md (768px+) | 16px |
| lg (1012px+) | 24px |
| xl (1280px+) | 32px |

**Sidebar widths:**

| Sidebar type | md | lg | xl |
|-------------|----|----|-----|
| Standard | 220px | 256px | 296px |
| Narrow | 240px | 256px | — |
| Wide | — | 320px | 336px |

**Column system:** GitHub uses a 12-column grid at md+ breakpoints. Repository pages favor a ~75/25 split between main content and sidebar. Diff views go full-width.

**Z-index layers:** Overlays > Dialogs > Sticky navigation > Standard content.

---

## Responsive Behavior

| Breakpoint | Name | Width | Behavior |
|------------|------|-------|----------|
| `xs` | Mobile | 0–543px | Single column; sidebar collapses to drawer; tabs replace split panels |
| `sm` | Small | 544px+ | Two-column layouts begin; navigation hamburger |
| `md` | Tablet | 768px+ | Full navigation header; sidebar appears inline |
| `lg` | Desktop | 1012px+ | Full layout; 980px container + gutters |
| `xl` | Wide | 1280px+ | Expanded container; generous gutters |
| Wide | — | 1400px+ | Viewport-wide layout for dashboards |

**Key responsive rules:**

- **Minimum viewport:** 320px width, 256px height (supports 400% browser zoom on 1280px display)
- **Touch targets:** 24px minimum (AA), 44px recommended (AAA) on mobile — medium buttons expand their tap target without changing visual size
- **Navigation:** Global header collapses to hamburger at `sm`; side NavLists slide in as an off-canvas drawer
- **Tables and diffs:** Use horizontal scroll on mobile rather than reformatting — preserving the code structure is more important than filling the viewport
- **Font sizes:** All use `rem` units so browser zoom and accessibility font scaling work without breakage
- **Motion:** Respects `prefers-reduced-motion`; all transitions reduce to instant when set

---

## Tone & Guardrails

### DO

- Use **semantic tokens** (`--fgColor-danger`, `--bgColor-success-muted`) rather than raw hex values — this ensures light/dark mode correctness automatically
- Use **`--fgColor-default`** (`#1F2328`) for all primary text
- Use **`--fgColor-muted`** for timestamps, metadata, helper text, and secondary labels
- Use **`--fgColor-accent`** for all text links (never use a different color for links)
- Use **weight 600** for button labels, headings, and any emphasized UI text
- Use the **monospace font stack** for all code, SHAs, file paths, tokens, and terminal output
- Reserve **primary buttons** for one-per-context; every other action uses Default or Invisible
- Use **6px border radius** as the default for interactive elements
- Keep **line widths under ~80 characters** for prose to maintain readability
- Align text to the **left with ragged right** — never justify body text

### DON'T

- **Don't use color as the only signal** — always pair a color state with a label, icon, or pattern (critical for accessibility and colorblind users)
- **Don't use raw hex values** — always use design tokens so themes and high-contrast modes work
- **Don't use more than one primary button** in a single action group
- **Don't use the Danger button** without a confirmation step (dialog or double-confirm)
- **Don't use arbitrary font weights** — only use 300, 400, 500, or 600
- **Don't center-align body text** — Primer explicitly discourages centered paragraphs
- **Don't animate decoratively** — all motion must serve a functional purpose; keep durations under 300ms
- **Don't use orange for general highlighting** — orange maps to the `severe` semantic role and implies urgency
- **Don't use purple** outside the `done`/merged state context — it has strong semantic meaning in the GitHub UI
- **Don't override hover/focus states** — Primer's focus ring (`0 0 0 3px rgba(#0969DA, 0.40)`) must remain intact for keyboard navigation compliance
- **Don't use `fgColor-white` or `fgColor-black` directly** — they don't respect theme inversion; use `fgColor-onEmphasis` for text on dark backgrounds instead
