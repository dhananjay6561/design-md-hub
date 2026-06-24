# Lemon Squeezy — Design System

Payments, tax & subscriptions for software companies. Lemon Squeezy is the all-in-one platform for running your SaaS business — handling payments, subscriptions, global tax compliance, fraud prevention, multi-currency support, and failed payment recovery.

---

## Colors

### Brand

| Token | Hex | Usage |
|---|---|---|
| lemon | `#FFC233` | Brand icon mark — decorative only, never for text or interactive |
| purple-500 | `#7047EB` | Primary actions, CTAs, links |
| purple-600 | `#5423E7` | Primary hover state |
| pink-500 | `#F75FDE` | Gradient accents, marketing highlights |
| plum | `#CF75FF` | Gradient endpoints, decorative badges |

### Purple Scale

| Step | Hex |
|---|---|
| 50 | `#F4F1FD` |
| 100 | `#E2DAFB` |
| 200 | `#C6B6F7` |
| 300 | `#A991F3` |
| 400 | `#8D6CEF` |
| 500 | `#7047EB` |
| 600 | `#5423E7` |
| 700 | `#4316CA` |
| 900 | `#2B0E81` |

### Yellow / Lemon Scale

| Step | Hex |
|---|---|
| 50 | `#FFF9EB` |
| 100 | `#FFF3D6` |
| 200 | `#FFE7AD` |
| 300 | `#FFDA85` |
| 400 | `#FFCE5C` |
| 500 | `#FFC233` |
| 700 | `#C28800` |

### Supporting Palettes

Green: `#EEFBF4` → `#DFF8EA` → `#84E4AE` → `#2DCA72` → `#26A95F` → `#1E874C`

Blue: `#F0FAFF` → `#DBF3FF` → `#70D1FF` → `#00ACFF` → `#0090D6` → `#0075AD`

Orange: `#FFF2EE` → `#FFB399` → `#FF7D52` → `#FF571F` → `#EB3A00`

Red: `#FEF0F4` → `#FDD8E1` → `#FBB1C4` → `#F76489` → `#F53D6B` → `#D50B3E`

Pink: `#FEECFB` → `#FCC5F3` → `#FA99EA` → `#F75FDE` → `#F42AD3` → `#DB0BB9`

### Semantic Colors

| Role | Light bg | Light text | Dark bg | Dark text |
|---|---|---|---|---|
| Success | `#EEFBF4` | `#1E874C` | `rgba(45,202,114,.12)` | `#84E4AE` |
| Warning | `#FFF9EB` | `#C28800` | `rgba(255,194,51,.12)` | `#FFCE5C` |
| Error | `#FEF0F4` | `#D50B3E` | `rgba(245,61,107,.12)` | `#F76489` |
| Info | `#F0FAFF` | `#0075AD` | `rgba(0,172,255,.12)` | `#70D1FF` |

### Surfaces

| Token | Light | Dark |
|---|---|---|
| bg | `#FFFFFF` | `#121217` |
| surface | `#F7F7F8` | `#1C1C28` |
| elevated | `#EEEEF2` | `#252535` |
| border | `#D1D1DB` | `#2D2D42` |
| text | `#121217` | `#F7F7F8` |
| text-2 | `#3F3F50` | `#C8C8DA` |
| text-3 | `#6C6C89` | `#6C6C89` |
| text-4 | `#A9A9BC` | `#3F3F50` |

---

## Typography

### Font Families

| Role | Family | Source |
|---|---|---|
| Display / Headings | Circular XX | `cdn.prod.website-files.com` (OTF) |
| Body / UI | Inter | `cdn.prod.website-files.com` (TTF) |
| Code / Mono | JetBrains Mono | `cdn.prod.website-files.com` (TTF) |

### Type Scale

| Level | Size | Weight | Line Height | Font |
|---|---|---|---|---|
| h1 | 48px | 700 | 1.1 | Circular XX |
| h2 | 36px | 700 | 1.15 | Circular XX |
| h3 | 24px | 600 | 1.3 | Circular XX |
| body-lg | 16px | 400 | 1.6 | Inter |
| body | 14px | 400 | 1.5 | Inter |
| label | 11px | 600 | 1 | Inter |
| code | 13px | 400 | 1.6 | JetBrains Mono |

---

## Spacing & Radius

Base unit: 4px

| Token | Value |
|---|---|
| radius-sm | 6px |
| radius-md | 10px |
| radius-lg | 16px |
| radius-xl | 24px |
| radius-full | 9999px |

---

## Components

### Buttons

| Variant | Background | Text | Border |
|---|---|---|---|
| Primary | `#7047EB` | `#FFF` | — |
| Primary hover | `#5423E7` | `#FFF` | — |
| Secondary | transparent | `#7047EB` | `1.5px #7047EB` |
| Ghost | transparent | `#3F3F50` | `1px var(--border)` |
| Danger | `#F53D6B` | `#FFF` | — |

### Status Badges

| Status | Background | Text | Border |
|---|---|---|---|
| Active | `#EEFBF4` | `#1E874C` | `#B2EECC` |
| Trialing | `#F0FAFF` | `#0075AD` | `#ADE4FF` |
| Cancelled | `#FEF0F4` | `#D50B3E` | `#FDD8E1` |
| Paused | `var(--elevated)` | `#6C6C89` | `var(--border)` |
| New | `#F4F1FD` | `#5423E7` | `#C6B6F7` |

---

## Guardrails

**DO**
- Use purple (#7047EB) as the single primary action color — never blue or green for CTAs
- Use Circular XX for all headings; Inter for all UI and body text
- Keep cards at #F7F7F8 in light mode — the subtle contrast from #FFF creates depth
- Use the lemon yellow (#FFC233) only for the brand icon mark and decorative accents
- Dark bg is #121217 — a near-black with purple-blue undertone, never pure black

**DON'T**
- Don't use lemon yellow as a button, link, or interactive element color
- Don't set Circular XX below 16px — use Inter for small/label text
- Don't use pure #000000 for text — always #121217
- Don't use green or blue as CTA colors — purple owns that role
- Don't stack pink, plum, and yellow gradients in a single UI region
