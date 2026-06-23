# Clerk DESIGN.md

> Auth that just works — a developer authentication platform with a polished, trust-first UI.

## Overview

Clerk's design is clean, professional, and conversion-optimized. The dashboard is light-first with a violet accent, communicating security and reliability without feeling sterile. The UI components (SignIn, UserButton, etc.) are designed to embed seamlessly into any product — minimal opinionation, maximum polish. The aesthetic is modern SaaS: card-heavy, well-spaced, and accessible.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#6C47FF` | CTAs, active states, links |
| `primary-hover` | `#5A38E8` | Hover on primary |
| `background` | `#FFFFFF` | Page background |
| `surface` | `#FAFAFA` | Cards, panels |
| `surface-secondary` | `#F4F4F5` | Hover states, subtle fills |
| `text-primary` | `#09090B` | Body text, headings |
| `text-secondary` | `#71717A` | Supporting text |
| `text-muted` | `#A1A1AA` | Placeholders, disabled |
| `border` | `#E4E4E7` | Dividers, input borders |
| `border-strong` | `#D4D4D8` | Emphasized borders |
| `error` | `#EF4444` | Error states |
| `success` | `#22C543` | Success states |
| `warning` | `#F36B16` | Warnings |
| `purple-dim` | `rgba(108,71,255,0.08)` | Subtle primary fills |
| `cyan` | `#5DE3FF` | Secondary accent, highlights |
| `cyan-dim` | `rgba(93,227,255,0.12)` | Subtle cyan backgrounds |

### Dark Mode

| Token | Hex |
|-------|-----|
| `background` | `#131316` |
| `surface` | `#212126` |
| `surface-secondary` | `#2F3037` |
| `text-primary` | `#FAFAFA` |
| `text-secondary` | `#A1A1AA` |
| `border` | `#3F3F46` |
| `border-strong` | `#52525B` |
| `primary` | `#7C5CFF` |
| `primary-hover` | `#9171FF` |

## Typography

- **Font family**: `Suisse Intl` — proprietary (Schick Toikka foundry, not publicly available). Preview fallback: `Geist` (Vercel / Google Fonts) — Clerk's own fallback in production; closest match in proportions and weight range.
- **Mono font**: System monospace stack (`ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace`) — Clerk components use the system stack, not a custom mono font. Preview uses `JetBrains Mono` as a visible stand-in.
- **Numbers**: `Geist` (numerals only) — available via Vercel / Google Fonts.

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `heading-xl` | 28px | 700 | 1.2 |
| `heading-lg` | 22px | 600 | 1.3 |
| `heading-md` | 16px | 600 | 1.4 |
| `body` | 14px | 400 | 1.5 |
| `body-sm` | 13px | 400 | 1.5 |
| `caption` | 12px | 400 | 1.4 |
| `label` | 12px | 500 | 1.3 |
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
| `radius-sm` | 4px | Tags, badges |
| `radius-md` | 8px | Inputs, buttons |
| `radius-lg` | 12px | Cards, modals |
| `radius-xl` | 16px | Auth components |
| `radius-full` | 9999px | Avatars, pills |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.06), 0 1px 2px rgba(0,0,0,0.04)` | Cards |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.08)` | Dropdowns, popovers |
| `shadow-lg` | `0 8px 24px rgba(0,0,0,0.10)` | Modals, dialogs |

## Components

### Button

- **Primary**: `primary` background, white text, `8px` radius, `10px 18px` padding, 500 weight
- **Secondary**: `surface` background, `border` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover fills `surface-secondary`
- **Destructive**: `error` background, white text
- All: `14px`, `150ms ease`

### Auth Card (SignIn / SignUp)

- Background: `surface`
- Border: `1px solid border`
- Radius: `radius-xl`
- Padding: `space-8`
- Shadow: `shadow-lg`
- Max-width: `400px`, centered
- Social OAuth buttons: full-width, secondary style, icon + label

### Input

- Background: `background`
- Border: `1px solid border` → `primary` on focus
- Radius: `radius-md`
- Padding: `10px 14px`
- Height: `40px`
- Label: `label` scale, above input
- Error state: `error` border + error message below

### User Button (Avatar dropdown)

- Avatar: `32px`, `radius-full`, `primary` background initials fallback
- Dropdown: `surface`, `radius-lg`, `shadow-md`, `200px` min-width
- User row: avatar + name + email
- Menu items: `body-sm`, `text-primary`, hover fills `surface-secondary`

### Badge / Role Tag

- Padding: `2px 8px`
- Radius: `radius-sm`
- Font: `label`
- Variants: admin (purple-dim), member (surface-secondary), pending (warning-dim)

## Layout

- **Dashboard**: sidebar `240px` + main content area
- **Auth pages**: centered card, `min-height: 100vh`, subtle background
- **Max content width**: `1100px`
- **Settings pages**: two-column — nav list left, form right

## Responsive

- Auth card goes full-width on mobile with reduced padding
- Sidebar collapses to hamburger on mobile
- UserButton dropdown repositions to bottom-sheet on mobile

## Tone & Guardrails

- DO: Prioritize trust signals — use consistent borders, clean spacing, accessible contrast
- DO: Use violet only for the primary action per view
- DO: Keep auth components tight and focused — no distractions during sign-in flows
- DO: Show clear error states with actionable messages
- DON'T: Use more than one primary button per screen
- DON'T: Add decorative backgrounds to auth pages — plain white or subtle gray only
- DON'T: Show technical error codes to end users
- DON'T: Use animations that delay the form becoming interactive
- DON'T: Use all-caps labels or uppercase text
