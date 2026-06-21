# Expo Design System

## Overview
Expo is an open-source platform for building universal React Native apps. The design language is modern, developer-focused, and approachable — it signals that mobile development can be fast and enjoyable. The deep indigo/blue anchors a clean dark aesthetic.

**Brand personality:** Approachable, modern, cross-platform, developer-first.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--expo-blue` | `#4630EB` | Primary brand, CTAs, links |
| `--expo-blue-light` | `#6B5CE7` | Hover states |
| `--expo-white` | `#FFFFFF` | High-contrast text on dark |
| `--expo-teal` | `#00B4D8` | Secondary accent, highlights |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0E0E14` | Main background |
| `--bg-surface` | `#161622` | Cards, panels |
| `--bg-elevated` | `#20202E` | Dropdowns, modals |
| `--border` | `#2E2E44` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#FFFFFF` | Headings, primary content |
| `--text-secondary` | `#9898B0` | Labels, descriptions |
| `--text-muted` | `#5C5C78` | Placeholders, disabled |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#22C55E` | Build passed, published |
| `--warning` | `#F59E0B` | Deprecation, slow build |
| `--danger` | `#EF4444` | Build failed, crash |
| `--info` | `#4630EB` | SDK updates, info |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 36px | 700 | Hero, marketing |
| Heading 1 | 28px | 600 | Page titles |
| Heading 2 | 20px | 600 | Section headers |
| Body | 15px | 400 | Default content |
| Small | 13px | 400 | Labels, metadata |
| Mono | 13px | 400 | CLI output, config |

---

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | `4px` | Micro gaps |
| `--space-2` | `8px` | Inline spacing |
| `--space-3` | `12px` | Tight padding |
| `--space-4` | `16px` | Standard gap |
| `--space-6` | `24px` | Card padding |
| `--space-8` | `32px` | Section gap |
| `--space-12` | `48px` | Page sections |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `6px` | Badges, tags |
| `--radius-md` | `8px` | Buttons, inputs |
| `--radius-lg` | `12px` | Cards |
| `--radius-xl` | `16px` | Modals |
| `--radius-full` | `9999px` | Pills |

---

## Shadows

```css
--shadow-sm: 0 1px 4px rgba(0,0,0,0.5);
--shadow-md: 0 4px 16px rgba(0,0,0,0.6);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.7);
--shadow-blue: 0 0 0 3px rgba(70,48,235,0.3);
```

---

## Components

### Buttons
```
Primary:  bg #4630EB, text white, hover #6B5CE7, radius 8px, height 40px
Ghost:    bg transparent, border #2E2E44, text #9898B0, hover border #4630EB
Height:   40px, font-weight 600
```

### Inputs
```
Background: #161622
Border:     #2E2E44 default, #4630EB focused
Text:       #FFFFFF
Placeholder: #5C5C78
Radius:     8px, height: 40px
Font:       JetBrains Mono for SDK version/config fields
```

### Build Status Badges
```
Success: bg rgba(34,197,94,0.12), text #22C55E
Warning: bg rgba(245,158,11,0.12), text #F59E0B
Error:   bg rgba(239,68,68,0.12), text #EF4444
Running: bg rgba(70,48,235,0.12), text #4630EB
```

### Platform Pill
```
iOS:     bg rgba(70,48,235,0.15), text #6B5CE7, border rgba(70,48,235,0.3)
Android: bg rgba(34,197,94,0.12), text #22C55E, border rgba(34,197,94,0.3)
Web:     bg rgba(0,180,216,0.12), text #00B4D8, border rgba(0,180,216,0.3)
```

---

## Layout

- Docs max-width: 1200px
- Sidebar: 260px
- Content area: 720px
- Code block ratio in docs: ~35%

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
- Use platform pills (iOS/Android/Web) to indicate cross-platform compatibility
- Lead code examples with `npx create-expo-app` — onboarding matters
- Use monospace for all CLI commands, SDK versions, and config snippets
- Keep the blue accent on primary actions only — it must always feel tappable
- Show build logs in monospace with proper status color-coding

### DON'T
- Don't use the teal accent as a primary CTA — it's a secondary highlight
- Don't forget mobile context — Expo users think in terms of devices, not browsers
- Don't use thin font weights — they disappear against dark backgrounds
- Don't use rounded corners below 8px — Expo's aesthetic is friendly, not corporate
- Don't mix platform colors in a single non-platform-specific context
