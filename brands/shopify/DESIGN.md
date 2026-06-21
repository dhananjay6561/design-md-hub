# Shopify Design System

## Brand Overview
Shopify powers commerce for millions of merchants. The design system (Polaris) prioritizes clarity and merchant trust — built on a confident green, clean surfaces, and a no-nonsense information hierarchy.

## Color Palette

### Primary
- **Green**: `#95BF47` — brand lime green, highlights
- **Commerce Green**: `#008060` — primary CTAs, success states
- **Green Hover**: `#006E52` — pressed/active

### Semantic
- **Success**: `#008060`
- **Warning**: `#FFC453`
- **Error**: `#D72C0D`
- **Info**: `#006FBB`

### Surfaces (Dark Mode)
- **Background**: `#1A1A1A`
- **Surface**: `#242424`
- **Elevated**: `#2E2E2E`
- **Border**: `#3D3D3D`

### Text
- **Primary**: `#F4F4F4`
- **Secondary**: `#ABABAB`
- **Muted**: `#6E6E6E`

## Typography

- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for order IDs, SKUs)

### Scale
| Token | Size | Weight | Use |
|-------|------|--------|-----|
| display | 34px | 700 | Hero |
| h1 | 24px | 700 | Page title |
| h2 | 18px | 600 | Section |
| body | 14px | 400 | Default |
| small | 12px | 400 | Metadata |
| code | 13px | 400 mono | Order IDs, SKUs |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 8px
- Badges: 4px
- Inputs: 6px

## Components

### Product Card
- Image placeholder at 16:9 or 1:1
- Product name in h2, price in commerce green
- Inventory badge: in stock (green), low (yellow), out (red)
- Quick-add button ghost on default, primary on hover

### Order Status Badge
- Unfulfilled: yellow/warning
- Fulfilled: green/success
- Cancelled: red/error
- Pending: muted

### Data Table
- Sticky header with bold labels
- Row hover: `#2A2A2A`
- Pagination at bottom right

## Guardrails
- Use `#008060` for commerce actions (buy, add, fulfill) — not `#95BF47`
- Lime green (`#95BF47`) is for brand accent only, not interactive elements
- Order IDs and SKUs always in monospace
- Keep tables scannable — no vertical borders, only horizontal separators
- Merchant-facing copy must be plain English — no jargon
