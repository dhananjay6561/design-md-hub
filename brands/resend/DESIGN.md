# Resend DESIGN.md

> Email for developers — a clean, minimal email API platform with an elegant dark-first dashboard.

## Overview

Resend's design is sharp, modern, and developer-focused. It uses a near-black background with a clean white primary and subtle gray accents. The aesthetic is confident minimalism — almost no color, letting content hierarchy do all the work. It borrows from Vercel's visual language but feels warmer and more approachable.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#FFFFFF` | CTAs, primary text, active states |
| `primary-hover` | `#E4E4E7` | Hover on primary buttons |
| `background` | `#08090A` | App background |
| `surface` | `#111111` | Cards, panels |
| `surface-raised` | `#1A1A1A` | Elevated surfaces, dropdowns |
| `surface-overlay` | `#232323` | Modals, tooltips |
| `text-primary` | `#EDEDED` | Primary text |
| `text-secondary` | `#888888` | Supporting text, metadata |
| `text-muted` | `#555555` | Placeholders, disabled |
| `border` | `#1F1F1F` | Dividers, subtle borders |
| `border-strong` | `#2E2E2E` | Input borders, cards |
| `accent` | `#F97316` | Email open rates, highlights (orange) |
| `error` | `#EF4444` | Errors |
| `success` | `#22C55E` | Delivered, success |
| `warning` | `#EAB308` | Warnings, bounced |

### Light Mode

| Token | Hex |
|-------|-----|
| `background` | `#FFFFFF` |
| `surface` | `#FAFAFA` |
| `surface-raised` | `#F4F4F5` |
| `text-primary` | `#09090B` |
| `text-secondary` | `#71717A` |
| `border` | `#E4E4E7` |

## Typography

- **Font family**: `Inter`, `ui-sans-serif`, `system-ui`, `sans-serif`
- **Mono font**: `JetBrains Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `heading-lg` | 22px | 600 | 1.3 |
| `heading-md` | 16px | 600 | 1.4 |
| `body` | 14px | 400 | 1.5 |
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

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-sm` | 4px | Tags, badges |
| `radius-md` | 6px | Buttons, inputs |
| `radius-lg` | 8px | Cards, panels |
| `radius-full` | 9999px | Pills, avatars |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.5)` | Subtle lift |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.6)` | Dropdowns |
| `shadow-lg` | `0 8px 24px rgba(0,0,0,0.7)` | Modals |

## Components

### Button

- **Primary**: white background, `#09090B` text, `6px` radius, `8px 16px` padding, 500 weight
- **Secondary**: `surface-raised` background, `border-strong` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover fills `surface-raised`
- **Danger**: `error` background, white text
- All: `13px`, `120ms ease`

### Email Log Row

- Height: `44px`
- Layout: status dot + recipient + subject + timestamp + open indicator
- Status dot: green (delivered), red (bounced), yellow (pending)
- Font: `body-sm`, monospace for email addresses
- Hover: `surface-raised` background
- Border-bottom: `1px solid border`

### Metric Card

- Background: `surface`
- Border: `1px solid border-strong`
- Radius: `radius-lg`
- Padding: `space-5 space-6`
- Large number: `28px`, 600 weight, `text-primary`
- Label: `caption`, `text-secondary`
- Delta: green/red with arrow icon

### Input

- Background: `surface-raised`
- Border: `1px solid border-strong` → white ring on focus
- Radius: `radius-md`, height: `36px`
- Font: `body-sm`
- API key inputs: monospace font

### Badge

- Padding: `2px 8px`
- Radius: `radius-full`
- Font: `caption`, 500 weight
- Delivered: green-dim; Bounced: red-dim; Pending: yellow-dim; Opened: orange-dim

## Layout

- **Sidebar**: `200px` fixed, minimal — logo + nav items only
- **Main**: fills remaining width, max `960px`
- **Dashboard**: metric cards grid (2-4 cols) + email log table
- **API section**: two-column — docs left, code right

## Responsive

- Sidebar collapses to icon-only on narrow screens
- Metric cards stack to 2-col on tablet, 1-col on mobile
- Email log hides metadata columns on mobile

## Tone & Guardrails

- DO: Keep the UI near-monochrome — color only for status signals
- DO: Use orange accent for engagement metrics (opens, clicks)
- DO: Use monospace for all email addresses, IDs, API keys
- DO: Prioritize delivery status visibility — it's the core product metric
- DON'T: Add decorative gradients or illustrations
- DON'T: Use more than 3 colors on a single screen
- DON'T: Use light mode as the default — dark is the primary experience
- DON'T: Round corners above `8px`
- DON'T: Show raw SMTP errors — translate to human-readable messages
