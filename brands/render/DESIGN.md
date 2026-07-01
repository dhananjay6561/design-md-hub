# Render Design System

## Overview

Render is the cloud platform for deploying apps and databases without DevOps overhead. The design language is technical and vivid — deep purple dark mode backgrounds, an electric purple primary accent, and green reserved exclusively for live/success states. Dark-first.

**Brand positioning:** "Your fastest path to production" / "Deploy apps and agents with zero ops"

---

## Colors

### Purple Scale (Primary Brand)
| Token | Hex | Usage |
|-------|-----|-------|
| `--color-purple-25` | `#fbfaff` | Lightest tint |
| `--color-purple-50` | `#f4f0ff` | Light hover bg |
| `--color-purple-100` | `#e7dbff` | Badge bg, light chips |
| `--color-purple-200` | `#d1b8ff` | Dark mode secondary text |
| `--color-purple-300` | `#c29eff` | Dark mode muted text |
| `--color-purple-500` | `#9b52fb` | Hover purple |
| `--color-purple-600` | `#8a05ff` | **Primary brand — CTAs, links, active elements** |
| `--color-purple-700` | `#48008c` | Dark mode card/section bg |
| `--color-purple-800` | `#2a0052` | Deep dark surface |
| `--color-purple-900` | `#1c0037` | Deepest dark, hero bg gradient end |

### Green Scale (Success / Live States Only)
| Token | Hex | Usage |
|-------|-----|-------|
| `--color-green-100` | `#b8ffd7` | Light success chip bg |
| `--color-green-300` | `#1efe9d` | Dark mode hero gradient accent |
| `--color-green-400` | `#00db7c` | **Live badge text, success state** |
| `--color-green-500` | `#009e7a` | Success text on light bg |
| `--color-green-800` | `#001f16` | Dark green bg (hero gradient start) |

Green is semantic — not a decorative accent. Never use it outside live/success/deploy contexts.

### Gray Scale (Neutral)
| Token | Hex | Usage |
|-------|-----|-------|
| `--color-gray-100` | `#e3e3e3` | Light mode border |
| `--color-gray-200` | `#c7c7c7` | Light mode input border |
| `--color-gray-600` | `#4d4d4d` | Light mode secondary text |
| `--color-gray-700` | `#272727` | Dark mode border |
| `--color-gray-800` | `#141414` | Dark mode raised surface |
| `--color-gray-900` | `#0d0d0d` | Dark mode page background |

### Semantic Tokens
| Token | Light | Dark |
|-------|-------|------|
| `--color-background` | `#ffffff` | `#0d0d0d` |
| `--color-border` | `#e3e3e3` | `#272727` |
| `--color-border-input` | `#c7c7c7` | `#4d4d4d` |
| `--color-text-primary` | `#0d0d0d` | `#ffffff` |
| `--color-text-secondary` | `#4d4d4d` | `#e3e3e3` |

### Hero Gradients
- **Light mode H1 text:** `linear-gradient(to right, #8a05ff → orange-400 #d67f2e)`
- **Dark mode hero bg:** `linear-gradient(177deg, #001f16 56.49%, #1c0037 12.68%)`

---

## Typography

### Font Stack
Render uses three proprietary fonts — Roobert (display) from Self-Host Studio, PPNeueMontreal and PPNeueMontrealMono from Pangram Pangram Foundry. All are served from `render.com/_next/static/media/` without `Access-Control-Allow-Origin` headers, which blocks loading from any non-Render origin.

**Live font files (no public CORS — cannot use from file://):**
- Roobert: `c7e359b9e8a1a81c` (300), `36de5d5a6fde5419` (400), `b134c96c03a76fa5` (600)
- PPNeueMontreal: `dc03e58dafb0f94e` (400), `eb0b6447daad5399` (500), `614210d7392d1f42` (600)
- PPNeueMontrealMono: `a02a323226559df3` (400), `772d87814c6d4363` (500)

**Google Fonts substitutes used in preview.html:**
- Roobert → `DM Sans` (700–800 at display sizes, closest geometric grotesque)
- PPNeueMontreal → `DM Sans` (400–600 at body/UI sizes)
- PPNeueMontrealMono → `JetBrains Mono`

### Type Scale
| Role | Font | Size | Weight | Line Height |
|------|------|------|--------|-------------|
| Display (hero H1) | Roobert | 56px | 600 | 1.05 |
| H1 | Roobert | 32px | 600 | 1.2 |
| H2 | PPNeueMontreal | 20px | 600 | 1.3 |
| Body | PPNeueMontreal | 16px | 400 | 1.65 |
| Small / label | PPNeueMontreal | 13px | 400–500 | 1.5 |
| Code | PPNeueMontrealMono | 13px | 400 | 1.6 |

---

## Logo

Two components:

**Mark** (`viewBox="0 0 12 20"`, `fill="currentColor"`) — 5 rectangles in a diagonal staircase:
```
(0,0,4,4)   top-left
(4,4,4,4)   middle
(8,8,4,4)   middle-right (shifts right)
(4,12,4,4)  lower
(0,16,4,4)  bottom
```

**Wordmark** (`viewBox="0 0 110 21"`, `class="fill-current"`) — 6 letter paths for "Render".

Both adapt to dark/light automatically via `fill="currentColor"` / `color: var(--text)`.

---

## Spacing & Shape

| Property | Value |
|----------|-------|
| Border radius — buttons | 6px |
| Border radius — cards | 8–12px |
| Border radius — badges | 100px (pill) |
| Elevation | Border-based — no heavy shadows |

---

## Components

### Buttons
- **Primary:** `background: #8a05ff`, white text, radius 6px, padding `10px 20px`, weight 500.
- **Outline:** transparent, `border: 1px solid var(--color-border)`, hover tinted purple.

CTAs used on site: "Get started", "Apply now", "Deploy to Render", "Sign in".

### Service Status Badges (pill)
- **Live** — `#00db7c` text on green-tinted bg
- **Building** — `#8a05ff` text on purple-tinted bg
- **Failed** — red text on red-tinted bg
- **Suspended** — gray text on gray bg

### Service Type Chips (small, mono, pill)
Web Service · PostgreSQL · Redis · Cron Job · Static Site · Background Worker

---

## Signature Component — Services Dashboard

The most recognizable Render UI: a project's resource list showing multiple service types together, each with status, region, and plan.

**Columns:** Service (type chip + name) · Status · Region · Plan · Last Deploy

**Row types shown:** Web Service, PostgreSQL, Cron Job, Static Site, Background Worker — the variety of types is what makes it immediately feel like Render, not a generic CI table.

**Interaction:** Click a service row to expand a deploy log panel.

---

## Guardrails

### DO
- Use `#8a05ff` as the sole primary brand color — all interactive elements key from this one value
- Reserve green (`#00db7c`) strictly for live/success/deploy states — it is semantic, not decorative
- Use dark purple (`#1c0037`, `#48008c`) for dark mode feature cards and hero sections
- Keep `fill="currentColor"` on both mark and wordmark — they adapt to dark/light automatically
- Use `#0d0d0d` (gray-900) as the dark mode page background — purple backgrounds are for cards/sections

### DON'T
- Use green as a decorative accent — it signals "live" and nothing else
- Use orange (`#d67f2e`) anywhere except the hero H1 gradient
- Place bright purple `#8a05ff` as a background color — it's for foreground elements only
- Add extra box-shadows — Render uses subtle borders, not elevation hierarchy
- Mix the three font roles: Roobert is heading-only, PPNeueMontreal is UI-only, Mono is code-only
