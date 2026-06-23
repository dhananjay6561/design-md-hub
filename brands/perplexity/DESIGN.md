# Perplexity DESIGN.md

> Clean, answer-first — an AI search interface that gets out of the way and lets the content breathe.

## Overview

Perplexity's design is minimal and editorial. It prioritizes the answer above everything — no decorative chrome, no heavy branding. The aesthetic is light-first with a calm teal/cyan accent, generous whitespace, and a strong focus on typography. It feels closer to a reading app than a search engine.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#1FB8CD` | CTAs, links, active states |
| `primary-hover` | `#1A9FB0` | Hover on primary |
| `background` | `#FFFFFF` | Page background |
| `surface` | `#F9F9F9` | Cards, input backgrounds |
| `surface-secondary` | `#F2F2F2` | Hover states, subtle fills |
| `text-primary` | `#1C1C1C` | Body text, headings |
| `text-secondary` | `#666666` | Supporting text, metadata |
| `text-muted` | `#999999` | Placeholders, disabled |
| `border` | `#E5E5E5` | Dividers, input borders |
| `border-strong` | `#CCCCCC` | Emphasized borders |
| `error` | `#E53935` | Error states |
| `success` | `#2E7D32` | Success states |

### Dark Mode

| Token | Hex |
|-------|-----|
| `background` | `#131313` |
| `surface` | `#1C1C1C` |
| `surface-secondary` | `#242424` |
| `text-primary` | `#F0F0F0` |
| `text-secondary` | `#A0A0A0` |
| `border` | `#2E2E2E` |
| `primary` | `#1FB8CD` |

## Typography

- **Font family**: `Inter`, `ui-sans-serif`, `system-ui`, `sans-serif`
- **Mono font**: `JetBrains Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `display` | 28px | 600 | 1.2 |
| `heading-lg` | 20px | 600 | 1.3 |
| `heading-md` | 16px | 600 | 1.4 |
| `body` | 15px | 400 | 1.65 |
| `body-sm` | 13px | 400 | 1.5 |
| `caption` | 12px | 400 | 1.4 |
| `code` | 13px | 400 | 1.6 |

## Spacing

Base unit: `4px`

| Token | Value |
|-------|-------|
| `space-1` | 4px |
| `space-2` | 8px |
| `space-3` | 12px |
| `space-4` | 16px |
| `space-5` | 20px |
| `space-6` | 24px |
| `space-8` | 32px |
| `space-10` | 40px |
| `space-12` | 48px |

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-sm` | 4px | Tags, inline badges |
| `radius-md` | 8px | Buttons, inputs |
| `radius-lg` | 12px | Cards, panels |
| `radius-xl` | 16px | Search bar, modals |
| `radius-full` | 9999px | Pills, avatars |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.06)` | Subtle lift |
| `shadow-md` | `0 4px 16px rgba(0,0,0,0.08)` | Cards, dropdowns |
| `shadow-lg` | `0 8px 32px rgba(0,0,0,0.10)` | Modals |

## Components

### Button

- **Primary**: `primary` background, white text, `8px` radius, `10px 20px` padding, 500 weight
- **Secondary**: `surface` background, `border` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover fills `surface-secondary`
- All: `14px`, `150ms ease` transition

### Search Bar

- Height: `52px`, `radius-xl`, `surface` background
- Border: `1px solid border` → `primary` on focus
- Left icon: search glyph, `text-muted`
- Right: submit arrow button, `primary` color
- Font: `body`, `text-primary`
- Prominent — center of the page, generous padding

### Source Card

- Background: `surface`
- Border: `1px solid border`
- Radius: `radius-lg`
- Padding: `space-3 space-4`
- Favicon + domain + title layout
- Hover: `shadow-md`, border → `border-strong`

### Answer Block

- Max width: `720px`, centered
- Body text: `body` scale, `text-primary`, `line-height: 1.65`
- Inline citations: superscript numbers, `primary` color
- Code blocks: `surface-secondary`, `radius-md`, monospace

### Badge / Citation

- Padding: `2px 8px`
- Radius: `radius-sm`
- Font: `caption`, 500 weight
- Citation style: numbered, `primary` tint background

## Layout

- **Max content width**: `720px` centered
- **Search bar**: full width up to `640px`, centered
- **Sources grid**: horizontal scroll row above answer
- **Single column**: answer dominates the page
- **Sticky header**: minimal, just logo + account

## Responsive

- Search bar goes full-width on mobile
- Sources collapse into a count badge on mobile
- Typography scales down ~5% on mobile

## Tone & Guardrails

- DO: Let the answer be the hero — minimize surrounding UI chrome
- DO: Use teal accent sparingly — links and one CTA max per view
- DO: Keep line lengths under 75 characters for readability
- DO: Show source citations prominently — trust is the product
- DON'T: Add decorative gradients or background textures
- DON'T: Use heavy shadows — keep the UI flat and clean
- DON'T: Use more than 2 font weights on a single screen
- DON'T: Add animations that delay showing the answer
- DON'T: Use colored backgrounds for content sections
