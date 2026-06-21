# Doppler DESIGN.md

> Secrets management for teams — a polished, light-first platform that makes environment variables feel organized and secure.

## Overview

Doppler's design is clean, professional, and more polished than most dev tool dashboards. It's light-first (unusual in the secrets space), uses a distinctive royal blue accent, and prioritizes clarity for team workflows. The aesthetic is modern SaaS — structured, accessible, and trustworthy — designed for both developers and non-technical team members.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `primary` | `#4F46E5` | CTAs, active states, links |
| `primary-hover` | `#4338CA` | Hover on primary |
| `background` | `#FFFFFF` | Page background |
| `surface` | `#F9FAFB` | Cards, panels |
| `surface-secondary` | `#F3F4F6` | Hover states, subtle fills |
| `text-primary` | `#111827` | Body text, headings |
| `text-secondary` | `#6B7280` | Supporting text |
| `text-muted` | `#9CA3AF` | Placeholders, disabled |
| `border` | `#E5E7EB` | Dividers, input borders |
| `border-strong` | `#D1D5DB` | Emphasized borders |
| `error` | `#EF4444` | Errors |
| `success` | `#10B981` | Success, synced |
| `warning` | `#F59E0B` | Warnings |
| `indigo-dim` | `rgba(79,70,229,0.08)` | Subtle primary backgrounds |

### Dark Mode

| Token | Hex |
|-------|-----|
| `background` | `#111827` |
| `surface` | `#1F2937` |
| `surface-secondary` | `#374151` |
| `text-primary` | `#F9FAFB` |
| `text-secondary` | `#9CA3AF` |
| `border` | `#374151` |
| `primary` | `#6366F1` |

## Typography

- **Font family**: `Inter`, `ui-sans-serif`, `system-ui`, `sans-serif`
- **Mono font**: `JetBrains Mono`, `ui-monospace`, `monospace`

| Scale | Size | Weight | Line Height |
|-------|------|--------|-------------|
| `heading-lg` | 22px | 700 | 1.3 |
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

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-sm` | 4px | Tags, badges |
| `radius-md` | 6px | Buttons, inputs |
| `radius-lg` | 8px | Cards, modals |
| `radius-full` | 9999px | Pills, avatars |

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 2px rgba(0,0,0,0.05)` | Subtle |
| `shadow-md` | `0 4px 12px rgba(0,0,0,0.08)` | Cards, dropdowns |
| `shadow-lg` | `0 8px 24px rgba(0,0,0,0.10)` | Modals |

## Components

### Button

- **Primary**: `primary` background, white text, `6px` radius, `8px 16px` padding, 500 weight
- **Secondary**: `surface` background, `border` border, `text-primary`
- **Ghost**: transparent, `text-secondary`, hover fills `surface-secondary`
- **Danger**: `error` background, white text
- All: `14px`, `150ms ease`

### Secret Row

- Height: `44px`
- Layout: checkbox + key name (monospace) + masked value + environment badge + sync status + actions
- Reveal: eye icon on hover, `text-muted` default
- Copy: clipboard icon on hover
- Selected: `indigo-dim` background + `primary` left border
- Border-bottom: `1px solid border`

### Config / Project Card

- Background: `surface`
- Border: `1px solid border`
- Radius: `radius-lg`
- Padding: `space-5 space-6`
- Shadow: `shadow-sm`
- Hover: `shadow-md`

### Input

- Background: `background`
- Border: `1px solid border` → `primary` on focus with `0 0 0 3px rgba(79,70,229,0.12)` ring
- Radius: `radius-md`, height: `38px`
- Secret value: monospace font, masked by default

### Badge / Environment Tag

- Padding: `2px 8px`
- Radius: `radius-full`
- Font: `label`
- Development: indigo-dim; Production: red-dim; Staging: yellow-dim; Synced: green-dim

## Layout

- **Sidebar**: `240px` fixed — workspace + project tree
- **Main**: fills remaining, max `1000px`
- **Secrets table**: full-width with sticky header
- **Header**: `56px`, project name + env switcher + actions

## Responsive

- Sidebar collapses on mobile
- Secrets table horizontally scrollable on small screens
- Light mode default suits non-technical team members

## Tone & Guardrails

- DO: Light mode first — Doppler serves whole teams, not just engineers
- DO: Use indigo accent for selection, focus, and primary CTA
- DO: Mask all secret values by default
- DO: Use environment color-coding consistently throughout
- DON'T: Use more than one primary button per view
- DON'T: Show unmasked values in audit logs or notifications
- DON'T: Use yellow/orange for anything other than staging environment
- DON'T: Add heavy shadows — keep the UI light and airy
- DON'T: Use monospace for non-technical UI text
