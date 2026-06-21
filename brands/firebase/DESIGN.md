# Firebase Design System

## Overview
Firebase is Google's app development platform — real-time database, auth, hosting, and more. The design language uses a warm amber/orange flame that signals energy and speed. It's approachable and colorful compared to most developer tools, reflecting its appeal to indie devs and teams alike.

**Brand personality:** Fast, warm, full-stack, approachable, Google-backed.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--fb-amber` | `#FFCA28` | Primary brand, highlights |
| `--fb-orange` | `#FF6F00` | CTA buttons, hover states |
| `--fb-orange-light` | `#FFA000` | Mid-tone accent |
| `--fb-red` | `#DD2C00` | Danger, delete actions |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#111827` | Main background |
| `--bg-surface` | `#1A2332` | Cards, panels |
| `--bg-elevated` | `#222D40` | Dropdowns, modals |
| `--border` | `#2E3F58` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#F9FAFB` | Headings, body |
| `--text-secondary` | `#9CA3AF` | Labels, captions |
| `--text-muted` | `#6B7280` | Placeholders, disabled |
| `--text-amber` | `#FFCA28` | Links, highlighted values |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#34D399` | Rules matched, deploy OK |
| `--warning` | `#FFCA28` | Quota approaching, slow |
| `--danger` | `#DD2C00` | Security rule violation, error |
| `--info` | `#60A5FA` | Informational |

---

## Typography

**Primary Font:** `Google Sans` (fallback: `Inter`, Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 36px | 700 | Hero, product pages |
| Heading 1 | 26px | 600 | Page titles |
| Heading 2 | 20px | 600 | Section headers |
| Body | 14px | 400 | Default content |
| Small | 12px | 400 | Metadata, timestamps |
| Mono | 13px | 400 | Security rules, JSON, paths |

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Micro gaps |
| `--space-2` | `8px` | Inline spacing |
| `--space-3` | `12px` | Compact padding |
| `--space-4` | `16px` | Standard gap |
| `--space-6` | `24px` | Card padding |
| `--space-8` | `32px` | Section gap |
| `--space-12` | `48px` | Page sections |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `4px` | Tags, small badges |
| `--radius-md` | `8px` | Buttons, inputs |
| `--radius-lg` | `12px` | Cards, panels |
| `--radius-xl` | `16px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 4px rgba(0,0,0,0.4);
--shadow-md: 0 4px 16px rgba(0,0,0,0.5);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.6);
--shadow-amber: 0 0 0 3px rgba(255,202,40,0.25);
```

---

## Components

### Buttons
```
Primary:  bg #FF6F00, text white, hover #E65100, radius 8px, height 40px, font-weight 500
Amber:    bg #FFCA28, text #111827, hover #FFB300 — for featured/hero CTAs only
Ghost:    bg transparent, border #2E3F58, text #9CA3AF, hover border #FFA000
```

### Inputs
```
Background: #1A2332
Border:     #2E3F58 default, #FFCA28 focused
Text:       #F9FAFB
Placeholder: #6B7280
Radius:     8px, height: 40px
Font:       JetBrains Mono for document paths, security rules
```

### Product Badges (Firebase services)
```
Firestore:   bg rgba(255,202,40,0.12), text #FFCA28
Auth:        bg rgba(66,133,244,0.12), text #4285F4
Hosting:     bg rgba(52,211,153,0.12), text #34D399
Functions:   bg rgba(255,111,0,0.12), text #FF6F00
Storage:     bg rgba(96,165,250,0.12), text #60A5FA
```

### Security Rule Block
```
Background: #0D1117
Border:     1px solid #2E3F58
Radius:     8px
Font:       JetBrains Mono 12px
Keyword:    #FFCA28
String:     #34D399
Comment:    #6B7280
```

---

## Layout

- Console max-width: 1280px
- Left nav: 220px (product switcher)
- Content padding: 24px
- Data tables for Firestore documents

---

## Responsive Breakpoints

| Name | Width |
|------|-------|
| Mobile | < 768px |
| Tablet | 768px – 1024px |
| Desktop | > 1024px |

---

## Tone & Guardrails

### DO
- Use the flame gradient (amber → orange) in hero/marketing contexts only
- Color-code Firebase products consistently (Firestore=amber, Auth=blue, etc.)
- Use monospace for security rules, document paths, and JSON data
- Show quota usage with visual progress bars — Firebase devs monitor limits closely
- Use amber `#FFCA28` as a warning color — it's both brand and semantic here

### DON'T
- Don't use the amber/orange as a generic background fill — it's an accent
- Don't mix multiple product accent colors in a single non-console view
- Don't use sharp corners — Firebase is more approachable than enterprise infra tools
- Don't use the red (#DD2C00) for anything except delete and critical security errors
- Don't use small font sizes for security rules — they're complex enough to need breathing room
