# Shopify Design System

## Brand Overview

Shopify powers commerce for millions of merchants — "the all-in-one commerce platform to start, run, and grow a business." Two surfaces define the visual language, and both are captured here:

- **Marketing (shopify.com)** — a stark, editorial identity: coal-black `#02090a`, white, and a neutral zinc "shade" scale, set in **PolySans** display over **Neue Haas Grotesk** body. Confident, high-contrast, almost monochrome.
- **Admin (Polaris)** — the product merchants use daily: clean surfaces built around **commerce green** `#008060` for every action that moves money (Add product, Fulfill, Save) and for success/Paid states.

The one constant across every rebrand is the **green shopping bag**. Green is the brand; the neutrals are the canvas.

> Verified live from shopify.com (2026). The homepage has moved to a monochrome coal-black/zinc palette — do **not** assume the old green-black/mint marketing look, and do not use the legacy lime `#95BF47` as an interactive color.

## Color Palette

### Primary — commerce green
- **Green**: `#008060` — primary CTAs, success, Paid/Fulfilled, active states, the bag mark
- **Green Hover**: `#006E52` — hover/pressed
- **Green Deep**: `#004C3F` — deep accent, dark-surface green fills
- **Green Accent (text)**: `#008060` light / `#5EC49A` dark — green text/links (lighten on dark for contrast)

### Green tints (Polaris subdued backgrounds)
- **Aloe**: `#C1FBD4` — success badge background
- **Pistachio**: `#D4F9E0` — soft green fill
- **Legacy Lime**: `#95BF47` — heritage bag color only; **never** an interactive element

### Neutrals — "shade" scale (zinc)
- **Coal Black**: `#02090A` — dark page background (marketing hero)
- **Shade 90 / Header**: `#18181B` / `#0E0E10` — dark cards, header
- **Shade 70**: `#3F3F46` · **Shade 60**: `#52525B` · **Shade 50**: `#71717A` · **Shade 40**: `#A1A1AA`
- **Shade 30**: `#D4D4D8` · **Shade 20**: `#E4E4E7` · **Shade 10**: `#F4F4F5` · **White**: `#FFFFFF`

### Semantic (Polaris admin tones)
- **Success**: `#008060` (bg `#C1FBD4`)
- **Attention / Pending / Unfulfilled**: `#B98900` (bg `#FFF1D6`)
- **Critical / Error**: `#D82C0D` (bg `#FEE9E8`)
- **Info**: `#2C6ECB` (bg `#EBF1FC`)

## Typography

Three fonts, one role each — all served from Shopify's CDN (CORS-clean).

- **Display — PolySans** (500 Neutral, 600 Median, 700 Bulky): hero, page + section headings only
- **UI / Body — Neue Haas Grotesk** (400/500/600): all body, labels, nav, buttons, table cells
- **Mono — IBM Plex Mono** (400/500/600): order IDs, SKUs, CLI, metadata

### Scale
| Token | Size | Weight | Font | Use |
|-------|------|--------|------|-----|
| display | 56px | 700 | PolySans | Hero (`--font-size-dsp` scales 56→70→96px) |
| h1 | 34px | 600 | PolySans | Page title |
| h2 | 22px | 600 | PolySans | Section heading |
| body-lg | 17px | 400 | Neue Haas Grotesk | Lead paragraph |
| body | 14px | 400 | Neue Haas Grotesk | Default UI |
| small | 12px | 400 | Neue Haas Grotesk | Metadata |
| mono | 12px | 400 | IBM Plex Mono | Order IDs, SKUs, CLI |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons / inputs: 8px
- Cards / panels: 12px
- Badges: 9999px (pill) — Polaris uses fully-rounded status badges
- Base: 4px

## Components

### Button
- **Primary**: commerce green `#008060`, **white** text (works in both themes — never dark text). Labels: `Add product`, `Fulfill orders`, `Save`, `Start free trial`
- **Secondary**: transparent, `--border-strong` outline. Labels: `Export`, `More actions`
- **Marketing primary** (shopify.com): solid black on light / white on dark — reserved for the top-level site CTA, not admin actions

### Badge (Polaris status)
Fully-rounded, subdued fill + saturated text:
- Paid / Fulfilled: green (`#008060` on `#C1FBD4`)
- Pending / Unfulfilled: amber (`#B98900` on `#FFF1D6`)
- Refunded / archived: neutral shade
- Critical: red (`#D82C0D` on `#FEE9E8`)

### Data Table (Orders)
- Sticky header, **horizontal separators only** — no vertical borders
- Row hover one step darker than the surface
- Row selection checkboxes → bulk actions bar (Polaris pattern)
- Columns: Order · Date · Customer · Total (green) · Payment status · Fulfillment status · Items

## Signature — Shopify Admin Orders

The Polaris Orders index: filter tabs (All / Unfulfilled / Unpaid), selectable rows, and a **Mark as fulfilled** bulk action that flips selected Unfulfilled orders to Fulfilled. Green = money and success; amber = needs attention. Max 20 rows.

## Guardrails

**DO**
- Use commerce green `#008060` for primary actions and Paid/Fulfilled/success — white text on it in both themes
- Keep the shopping-bag mark green — it's the one constant across every rebrand
- Set headings in PolySans, UI/body in Neue Haas Grotesk, code in IBM Plex Mono — one role each
- Use amber for Pending/Unfulfilled and green for Paid/Fulfilled — never the reverse
- Follow Polaris: pill status badges, horizontal-only table separators, plain-English merchant copy

**DON'T**
- Don't use the legacy lime `#95BF47` for interactive elements — it's brand heritage, not a UI action color
- Don't put dark text on the green button — commerce green takes white text always
- Don't tint dark surfaces navy — Shopify's dark is coal-black `#02090A`, near-neutral
- Don't set body or UI in PolySans — it's display only; Neue Haas Grotesk owns the UI
- Don't invent order data — use real order numbers (#1001+), realistic totals, and Polaris badge tones
</content>
</invoke>
