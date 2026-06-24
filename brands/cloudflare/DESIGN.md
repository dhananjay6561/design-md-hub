# Cloudflare Design System

## Overview

Cloudflare is the Internet's connectivity cloud — powering 42% of the Fortune 500 across networking, security, performance, and developer compute. The visual language is bold and confident: a signature orange palette anchored by Tangerine, generous white space, and Inter as the primary typeface. One platform for apps, agents, and workforce.

**Brand positioning (live from cloudflare.com):** "Build for the agent era" / "One platform for your apps, agents, and workforce. Build, secure, and scale without managing infrastructure."

---

## Colors

All values sourced from `cloudflare.com/brand/color/` (official Brand Guidelines).

### Primary Palette

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Tangerine** (lead orange) | `#F6821F` | 246, 130, 31 | Primary brand color. Present in every layout. CTAs, nav "Start building" button |
| **Ruby** | `#FF6633` | 255, 102, 51 | Gradient accent (Dawn left stop, hero background) |
| **Mango** | `#FBAD41` | 251, 173, 64 | Gradient accent (Dawn right stop, logomark right side) |
| **White** | `#FFFFFF` | 255, 255, 255 | Ample white space, complements the orange palette |

From live CSS (`/_astro/_separator.C94y8mHA.css`):
- `--color-accent-100` → Tangerine (`#F6821F`)
- `--color-accent-200` → Tangerine hover state
- `--color-foreground-100` → foreground/text token
- `--color-background-100` → background token
- `--color-border-100` → border token
- `--color-light-foreground` → white on orange backgrounds
- `--color-on-accent` → text color when placed on the accent surface

From live HTML (hero section): `bg-accent-100` class used on hero, `text-accent-100` on the cloud logo icon.

Hex colors confirmed from homepage source: `#FF500A` (4 occurrences), `#ff4801` (theme-color meta), `#FF9910` (logomark path), `#FF5F08` (logomark path).

### Secondary Palette (diagrams & illustrations only — never primary graphics)

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Lemon** | `#FFD43C` | 255, 212, 60 | Bullets, charts, details |
| **Blueberry** | `#3E74FF` | 62, 116, 255 | Bullets, charts |
| **Raspberry** | `#CE2F55` | 206, 47, 85 | Status / danger |
| **Blackberry** | `#0F006B` | 15, 0, 107 | Deep accent |
| **Cherry** | `#960C3E` | 150, 12, 62 | Error states |
| **Black (text)** | `#000000` | 0, 0, 0 | Typography only — never as background |

### Brand Gradients

| Name | Stops | Usage |
|------|-------|-------|
| **Dawn** | Ruby `#FF6633` → Tangerine `#F6821F` → Mango `#FBAD41` | Hero backgrounds, marketing pages |
| **Haze** | Ruby `#FF6633` → Tangerine `#F6821F` → Mango `#FBAD41` (alternate) | Secondary backgrounds |

### Nav / UI Tokens (live from CSS)

| Token | Usage |
|-------|-------|
| `--color-accent-100` | CTA button fill (`#nav-start-building-button`), logo icon color |
| `--color-light-foreground` | Text on accent/dark backgrounds |
| `--color-foreground-100` | Default text color |
| `--color-background-100` | Page / nav background |
| `--color-border-100` | Borders, nav dividers, button outlines |
| `--color-on-accent` | Text overlaid on accent-colored surfaces |
| `--color-security-100` | "Under attack?" alert link color |

---

## Typography

Sourced from `cloudflare.com/brand/typography/`.

### Primary Typeface: Inter

> "Our main typeface is Inter, a contemporary and flexible open-source sans-serif typeface designed by Swedish designer programmer Rasmus Andersson. It's a typeface carefully crafted and designed for computer screens. It provides a consistent, legible, and friendly typographic voice for our brand."

- **Weights used:** Regular, Medium, Semibold (4 weights total for consistency and readability)
- **Available at:** Google Fonts (`Inter`)

### Secondary Typeface: Kunst Grotesk

Cloudflare's website uses `Kunst Grotesk` as the site UI font (preloaded from `/fonts/Kunst%20Grotesk%20Regular.woff2` and `/fonts/Kunst%20Grotesk%20Medium.woff2`).

- **Weights preloaded:** Regular, Medium
- **Usage:** Main website navigation, headings, body copy on cloudflare.com

### Fallback for Non-Latin: Noto Sans CJK

> "Noto (short for 'no more tofu') is a cohesive, pan-language set of fonts. Supports 800 languages and 100 scripts."

### Type Roles (from Brand Guidelines)

| Role | Case | Weight | Tracking | Leading |
|------|------|--------|----------|---------|
| Eyebrow | ALL CAPS | Semibold | +5% | 100% |
| Headline | Sentence | Semibold | −3% | 100% |
| Sub headline | Sentence | Medium | −3% | 110% |
| Body | Sentence | Regular | −2% | 120% |
| URL / Label | Sentence | Medium | −3% | 100% |

### Type Scale (from live CSS custom properties)

| Property | Token |
|----------|-------|
| `--type-h4-size` | H4 font size |
| `--type-h4-size-md` | H4 size at medium breakpoint |
| `--type-h4-leading` | H4 line-height |
| `--type-h4-tracking` | H4 letter-spacing |
| `--type-h5-size` | H5 font size |
| `--type-h5-leading` | H5 line-height |
| `--type-h5-tracking` | H5 letter-spacing |
| `--type-h1-weight` | 600 (semibold) on mobile from live CSS |

---

## Logo

Sourced from live nav HTML at `cloudflare.com` and `cloudflare.com/brand/logo/`.

### Logomark

Two-path SVG cloud shape. `viewBox="0 0 341 156"`.

- **Left cloud path / body:** Fill `#FF5F08` (Tangerine/Ruby mid-tone)
- **Right cloud puff:** Fill `#FF9910` (Mango-adjacent)
- **On dark / inverted backgrounds:** `currentColor` (white)

The logo has two states toggled by CSS:
- `.cf-logo-base` — colored (orange) version, shown on light/transparent nav
- `.cf-logo-light` — monochrome version (`currentColor`), shown when nav is over a dark section

### Wordmark

SVG wordmark spelling "Cloudflare" in the custom logotype. `viewBox="0 0 719 59"`. Uses `currentColor` fill, adapts to light/dark context.

### Logo Usage Rules (from brand.cloudflare.com)

- Primary: stacked (logomark above logotype, right-aligned to edge of "E")
- Horizontal: when space is constrained
- Clear space: minimum 100% of logomark height on all sides
- Minimum size: 0.7 inch / 75px wide (stacked) or 1 inch / 100px wide (horizontal)
- Logotype color: Black `#000000`
- Logomark left: Tangerine `#F6821F`
- Logomark right: Mango `#FBAD41`
- Never use black as a background color

---

## Spacing

Cloudflare uses Tailwind's spacing scale with a 4px base unit.

| Token | Value | Usage |
|-------|-------|-------|
| `gap-1` | 4px | Tight element gaps |
| `gap-2` | 8px | Icon + text gaps |
| `gap-3` | 12px | Nav item spacing |
| `gap-4` | 16px | Component internal padding |
| `gap-6` | 24px | Section-internal spacing |
| `gap-8` | 32px | Card grid gaps |
| `px-4` / `px-6` / `px-8` | 16px / 24px / 32px | Responsive horizontal padding (mobile → tablet → desktop) |
| `max-w-[1480px]` | 1480px | Max content width (from live HTML) |

---

## Border Radius

From live HTML class usage:

| Token | Value | Usage |
|-------|-------|-------|
| `rounded-md` | 6px | Nav items, buttons, small elements |
| `rounded-xl` | 12px | Hero card (mobile) |
| `rounded-2xl` | 16px | Hero card (desktop) |
| `rounded-[50%]` | 50% | Blur/glow decorative elements |

---

## Shadows

From live CSS (`--color-accent-100` inline shadow):

| Name | Value | Usage |
|------|-------|-------|
| `shadow-stack` | (Tailwind shadow-stack) | Hero card on desktop |
| Beam glow | `inset 0 0 14px 2px color-mix(in srgb, var(--color-accent-100) 28%, transparent)` | Animated orange beam border |

---

## Components

### Buttons

From live nav HTML and CSS:

| Variant | Background | Color | Border | Usage |
|---------|-----------|-------|--------|-------|
| **Primary / Start building** | `--color-accent-100` (#F6821F) | `--color-light-foreground` (white) | Same as bg | Primary CTA |
| **Ghost / Log in** | Transparent | `--color-foreground-100` | `--color-border-100` | Secondary nav action |
| **Ghost / Contact sales** | Transparent | `--color-foreground-100` | `--color-border-100` | Secondary nav action |

Button shape: `rounded-md` (6px). Transition: `color 0.2s ease-out, background-color 0.2s ease-out, border-color 0.2s ease-out`.

### Inputs

Cloudflare uses standard form inputs following Inter typography at regular weight. Focus states use `--color-accent-100` ring.

### Badges / Status

Secondary colors (Lemon, Blueberry, Raspberry) used in badges for diagrams and product status. Never use secondary colors as primary design elements or in the flare graphic system.

### Nav

- Height: 72px desktop, 54px mobile
- Fixed on desktop, absolute on mobile
- Blur backdrop when scrolled
- Logo fades wordmark on scroll (`html[data-nav-scrolled]`)
- "Start building" CTA appears sticky after deep scroll

---

## Signature Component: Firewall Rules Manager

Cloudflare's most iconic dashboard UI is the **Firewall Rules** (now Security Rules) table — a configuration interface for creating and managing rules that control traffic to a zone. It features:

- A zone/domain selector at the top
- Tabs for different security products (WAF, DDoS, Bots, Rate Limiting)
- A rules table with: rule name, expression, action (Allow / Challenge / Block / JS Challenge), enabled toggle, traffic hit count, and row actions
- An "Add a rule" primary CTA
- Empty state with orange "Create your first rule" prompt
- Bulk action checkboxes on each row

Interactive behaviors:
- Toggle switches enable/disable individual rules
- Row hover reveals edit/delete actions
- Clicking a rule expands an expression detail panel
- Adding a row at max (20) removes the oldest

---

## Guardrails

### Do

- Use Tangerine `#F6821F` as the primary accent in every layout — even if only a small hit
- Use ample white space to complement orange; the combination creates the bold, simple Cloudflare impression
- Use Inter (or Kunst Grotesk on the marketing site) as the only brand typeface
- Keep typography left-aligned in most layouts; center only when format demands it
- Use the Eyebrow role (all caps, semibold, +5% tracking) to introduce section topics
- Use the horizontal logo variant when vertical space is constrained
- Use black (`#000000`) only for type

### Don't

- Don't use secondary colors (Lemon, Blueberry, Raspberry, Blackberry, Cherry) as primary graphics or in the flare design system — diagrams and illustrations only
- Don't use black as a background color or as part of the flare graphic system
- Don't add colored backgrounds behind the logo — use sufficient clear space
- Don't stretch, recolor, or modify the cloud logomark shape
- Don't use secondary colors as button fills or hero backgrounds
- Don't use fonts other than Inter / Kunst Grotesk / Noto Sans CJK in brand communications
- Don't place the logo below the 75px (stacked) or 100px (horizontal) minimum size

---

## Real Copy (from cloudflare.com, June 2026)

**Page title:** "Cloudflare: Build for the agent era"

**Hero H1:** "Everything we learned from powering 20% of the Internet—yours by default"

**Hero subtitle:** "One platform for your apps, agents, and workforce. Build, secure, and scale without managing infrastructure."

**Section headings:**
- "Region: Earth"
- "Cloudflare powers 42% of the Fortune 500"
- "Why choose Cloudflare"
- "Everything needed to build secure, performant applications"
- "Pay only when your code runs"

**Feature headings:**
- "Run everywhere"
- "Run anywhere"
- "Run at massive scale"
- "Fighting infra with 'cloud'"
- "Shipping with Cloudflare"
- "Pay for clean traffic"
- "Tailored to your team"
- "Fits into your existing workflows"
- "One network for users, apps, and data"

**CTA labels (live nav):** "Start building", "Contact sales", "Login", "Start building for free"

**Products (from nav):** Workers, Durable Objects, Workers KV, AI Gateway, Workers AI, D1, R2, Cloudflare One, Zero trust network access, Secure web gateway, Web application firewall, Bot management, CDN, DNS, 1.1.1.1

**Workers tagline:** "Deploy serverless functions globally in seconds. Scale automatically from zero to millions of requests."
