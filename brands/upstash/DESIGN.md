# Upstash DESIGN.md

> Serverless data for the edge — a Redis and Kafka platform with a clean dark UI and a signature green accent.

## Overview

Upstash's design is minimal, dark-first, and data-centric. The UI is clean and uncluttered, reflecting the simplicity of the product itself — serverless, pay-per-request, zero management. The green accent communicates speed and liveness. Dashboards prioritize metrics and connection details over decorative elements.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#00E9A3` | CTAs, active states, live indicators |
| `primary-hover` | `#00CC8E` | Hover on primary |
| `background` | `#0A0A0A` | App background |
| `surface` | `#141414` | Cards, panels |
| `surface-raised` | `#1C1C1C` | Elevated surfaces |
| `surface-overlay` | `#242424` | Dropdowns, modals |
| `text-primary` | `#F5F5F5` | Primary text |
| `text-secondary` | `#888888` | Supporting text |
| `text-muted` | `#555555` | Placeholders, disabled |
| `border` | `#202020` | Dividers |
| `border-strong` | `#2E2E2E` | Input borders |
| `error` | `#F87171` | Errors |
| `success` | `#00E9A3` | Success (same as primary) |
| `warning` | `#FBBF24` | Warnings |
| `green-dim` | `rgba(0,233,163,0.10)` | Subtle primary fills |

### Light Mode

| Token | Hex |
|-------|-----|
| `background` | `#FFFFFF` |
| `surface` | `#F9FAFB` |
| `surface-raised` | `#F3F4F6` |
| `text-primary` | `#111827` |
| `text-secondary` | `#6B7280` |
| `border` | `#E5E7EB` |

## Typography

- **Font family**: `Inter`, `ui-sans-serif`, `system-ui`, `sans-serif`
- **Mono font**: `JetBrains Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `heading-lg` | 20px | 600 | 1.3 |
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
| `shadow-sm` | `0 1px 4px rgba(0,0,0,0.5)` | Subtle |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.6)` | Dropdowns |
| `shadow-lg` | `0 8px 24px rgba(0,0,0,0.7)` | Modals |

## Components

### Button

- **Primary**: `primary` background, `#0A0A0A` text, `6px` radius, `8px 16px` padding, 600 weight
- **Secondary**: `surface-raised` background, `border-strong` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover fills `surface-raised`
- All: `13px`, `120ms ease`

### Database Card

- Background: `surface`
- Border: `1px solid border-strong`
- Radius: `radius-lg`
- Padding: `space-4 space-5`
- Live indicator: pulsing green dot
- Connection string: monospace, `caption`, copyable
- Metric row: requests/day, latency, data size in large mono numbers

### Metric Card

- Large stat in `20px`, 600 weight, `text-primary`
- Label: `caption`, `text-secondary`
- Sparkline: thin `primary` colored line

### Input

- Background: `surface-raised`
- Border: `1px solid border-strong` → `primary` on focus
- Radius: `radius-md`, height: `36px`
- Connection strings and keys: monospace

### Badge

- Padding: `2px 8px`
- Radius: `radius-full`
- Font: `caption`, 500 weight
- Active: green-dim; Paused: gray; Error: red-dim

## Layout

- **Sidebar**: `200px` fixed
- **Main**: fills remaining, max `960px`
- **Dashboard**: 3-col metric cards + database list

## Responsive

- Sidebar collapses on mobile
- Metric cards stack on small screens
- Desktop-first developer tool

## Tone & Guardrails

- DO: Use green accent only for live status and primary CTAs
- DO: Use monospace for all connection strings, keys, and metrics
- DO: Keep the UI data-dense but uncluttered
- DO: Show latency and request counts prominently — they're the product
- DON'T: Use decorative gradients or animations
- DON'T: Use light mode as default
- DON'T: Round corners above `8px`
- DON'T: Hide connection details behind extra clicks
