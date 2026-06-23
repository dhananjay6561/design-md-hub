# Upstash Design System

> Serverless Data Platform — dark-first, emerald-accented, data-dense UI built on Inter Tight display, Inter UI, and JetBrains Mono.

## Overview

Upstash is a serverless data platform offering Redis, Vector, QStash, Workflow, and Search as pay-per-request managed services. The design is dark-first, minimal, and performance-focused. The brand accent is **emerald** (#10b981) — it appears on CTAs, live indicators, and the logo's arc motif. Surfaces are near-black zinc tones; text uses a subtle emerald-50 tint rather than pure white. The aesthetic is clean and data-dense, reflecting the serverless-first product philosophy.

## Colors

### Dark (Primary)

| Token | Value | Usage |
|-------|-------|-------|
| `--bg` | `#09090b` | Page / app background |
| `--bg-mute` | `rgba(236,253,245,.06)` | Slightly lifted surface (cards, hover) |
| `--primary` | `#10b981` | Brand green — CTAs, active states, logo |
| `--primary-text` | `#34d399` | Emerald for text on dark bg (emerald-400) |
| `--text` | `#ecfdf5` | Primary text (emerald-50, near-white with green tint) |
| `--text-mute` | `#a1a1aa` | Secondary / muted text (zinc-400) |
| `--border` | `rgba(236,253,245,.08)` | Borders and dividers (subtle emerald tint) |
| `--pre-bg` | `#09090b` | Code block backgrounds |

### Light

| Token | Value | Usage |
|-------|-------|-------|
| `--bg` | `#f7f7f7` | Page background |
| `--bg-mute` | `rgba(4,120,87,.08)` | Subtle green-tinted surface |
| `--primary` | `#10b981` | Same emerald-500 |
| `--primary-text` | `#047857` | Emerald-700 for text on light bg |
| `--text` | `#022c22` | Primary text (very dark green, near black) |
| `--text-mute` | `#71717a` | Muted text (zinc-500) |

### Product Icon Colors

| Product | Color |
|---------|-------|
| Redis | `#DC2626` (red-600) |
| Vector | `#F97316` (orange-500) |
| QStash | `#2563EB` (blue-600) |
| Workflow | `#9333EA` (purple-600) |
| Search | `#10B981` (emerald-500) |

## Typography

All three fonts are loaded from Google Fonts.

- **Display**: `Inter Tight` (variable, wght 100–900) — headings, marketing, large numbers
- **Sans**: `Inter` (variable, wght 100–900) — UI labels, body, inputs
- **Mono**: `JetBrains Mono` (variable, wght 100–800) — connection strings, keys, code, commands

| Scale | Size | Weight | Font | Line Height |
|-------|------|--------|------|-------------|
| `display` | 96px | 700 | Inter Tight | 1.0 |
| `heading-lg` | 48px | 700 | Inter Tight | 1.1 |
| `heading-md` | 24px | 600 | Inter Tight | 1.25 |
| `heading-sm` | 18px | 600 | Inter Tight | 1.3 |
| `body` | 14px | 400 | Inter | 1.5 |
| `body-sm` | 13px | 400 | Inter | 1.5 |
| `caption` | 12px | 400 | Inter | 1.4 |
| `code` | 13px | 400 | JetBrains Mono | 1.6 |

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
| `radius-md` | 8px | Buttons, inputs |
| `radius-lg` | 12px | Cards, panels |
| `radius-xl` | 16px | Large cards |
| `radius-full` | 9999px | Pills, avatars |

## Shadows

Dark bg — shadows are very dark, nearly invisible on black:

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-sm` | `0 1px 3px rgba(0,0,0,.5)` | Subtle lift |
| `shadow-md` | `0 4px 16px rgba(0,0,0,.6)` | Dropdowns |
| `shadow-lg` | `0 8px 32px rgba(0,0,0,.7)` | Modals |
| `shadow-glow` | `0 0 24px rgba(16,185,129,.15)` | Emerald glow on CTA |

## Components

### Button

- **Primary**: `#10b981` bg, `#09090b` text, `8px` radius, `8px 20px` padding, 600 weight, glow shadow on hover
- **Secondary**: `rgba(236,253,245,.06)` bg, `rgba(236,253,245,.08)` border, `#ecfdf5` text, hover: `rgba(236,253,245,.10)` bg
- **Ghost**: transparent, `#a1a1aa` text, hover: `rgba(236,253,245,.06)` bg
- All: Inter, `13px`, `120ms ease`

### Database Card

- Background: `rgba(236,253,245,.04)` over `#09090b`
- Border: `1px solid rgba(236,253,245,.08)`
- Radius: `12px`
- Live indicator: pulsing `#10b981` dot
- Database name: Inter Tight 16px 600
- Region badge: JetBrains Mono 11px, pill
- Metric row: requests/sec, latency p99, data size — JetBrains Mono large numbers

### Redis Console

- Background: `#09090b`, border: `1px solid rgba(236,253,245,.08)`
- Prompt: `#10b981` `>` prefix, JetBrains Mono
- Command input: monospace, `#ecfdf5` text
- Response: `#34d399` for success, `#f87171` for errors, `#a1a1aa` for nil

### Input

- Background: `rgba(236,253,245,.04)`
- Border: `1px solid rgba(236,253,245,.08)` → `#10b981` on focus
- Radius: `8px`, height: `36px`
- Font: Inter 13px; connection strings use JetBrains Mono

### Badge

- Padding: `2px 8px`; Radius: `9999px`; Font: Inter 11px 500
- Active: `rgba(16,185,129,.15)` bg / `#34d399` text
- Paused: `rgba(161,161,170,.15)` bg / `#a1a1aa` text
- Error: `rgba(248,113,113,.15)` bg / `#f87171` text

## Layout

- **Sidebar**: `224px` fixed left — logo + product nav
- **Main**: fills remaining, `1200px` max content width
- **Dashboard**: 4-col stat row + database list grid
- **Console page**: full-width split — command history left, details right

## Tone & Guardrails

- DO: Use emerald only for brand CTAs and live/active status — never decoratively
- DO: Use JetBrains Mono for all connection strings, API keys, commands, and metrics
- DO: Use Inter Tight for all display headings and large numbers
- DO: Default to dark mode — it's the primary Upstash experience
- DO: Show latency and throughput metrics prominently — that's the product promise
- DON'T: Use pure white `#ffffff` for text — Upstash text has an emerald-50 tint (`#ecfdf5`)
- DON'T: Use decorative gradients on surfaces — gradients only appear on the H1 wordmark
- DON'T: Use placeholder connection strings — show realistic `redis://` or REST API URLs
- DON'T: Round corners above `16px` on cards; buttons use `8px`, not pills
- DON'T: Use light mode as default
