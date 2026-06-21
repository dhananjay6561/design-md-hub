# Deno Design System

## Overview
Deno is a secure JavaScript/TypeScript runtime. The design language is stark, minimal, and confident — black and white with a single teal/mint accent. It communicates precision and security without unnecessary decoration. The dinosaur mascot (Deno) is friendly but the UI around it is serious.

**Brand personality:** Minimal, secure, precise, opinionated, modern.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--deno-teal` | `#70FFAF` | Primary accent, links, highlights |
| `--deno-black` | `#000000` | Primary background, hero |
| `--deno-white` | `#FFFFFF` | Primary text on dark |
| `--deno-teal-dim` | `#3DD68C` | Hover on teal elements |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0A0A0A` | App background |
| `--bg-surface` | `#141414` | Cards, panels |
| `--bg-elevated` | `#1E1E1E` | Dropdowns, modals |
| `--border` | `#2E2E2E` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#FFFFFF` | Headings, body |
| `--text-secondary` | `#888888` | Labels, captions |
| `--text-muted` | `#555555` | Placeholders, disabled |
| `--text-teal` | `#70FFAF` | Links, accent text |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#70FFAF` | Tests passing, deploy OK |
| `--warning` | `#F5A623` | Deprecated API, slow |
| `--danger` | `#FF4444` | Runtime error, failed |
| `--info` | `#60A5FA` | Informational notes |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 48px | 800 | Hero only |
| Heading 1 | 32px | 700 | Page titles |
| Heading 2 | 22px | 600 | Section headers |
| Body | 15px | 400 | Default prose |
| Small | 13px | 400 | Captions, metadata |
| Mono | 14px | 400 | All code |

Deno documentation uses generous line-heights (1.7) and short line lengths for readability.

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
| `--space-16` | `64px` | Page sections |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `4px` | Badges, chips |
| `--radius-md` | `6px` | Buttons, inputs |
| `--radius-lg` | `8px` | Cards |
| `--radius-xl` | `12px` | Modals |

Deno uses sharp corners — this is a runtime for engineers, not a consumer app.

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.6);
--shadow-md: 0 4px 16px rgba(0,0,0,0.8);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.9);
--shadow-teal: 0 0 0 2px rgba(112,255,175,0.4);
```

---

## Components

### Buttons
```
Primary:  bg #70FFAF, text #000000, hover bg #3DD68C, radius 6px, height 38px, font-weight 700
Ghost:    bg transparent, border #2E2E2E, text #888888, hover border #70FFAF, hover text #70FFAF
Height:   38px, padding 0 18px
```

### Inputs
```
Background: #141414
Border:     #2E2E2E default, #70FFAF focused
Text:       #FFFFFF
Placeholder: #555555
Radius:     6px, height: 38px
Font:       JetBrains Mono
```

### Code Block
```
Background: #0A0A0A (same as page — flush)
Border:     1px solid #2E2E2E
Radius:     6px
Padding:    16px
Font:       JetBrains Mono 14px
Keyword:    #70FFAF
String:     #F5A623
Type:       #60A5FA
Comment:    #555555
```

### Badges
```
Success: bg rgba(112,255,175,0.1), text #70FFAF, border rgba(112,255,175,0.3)
Warning: bg rgba(245,166,35,0.1), text #F5A623, border rgba(245,166,35,0.3)
Error:   bg rgba(255,68,68,0.1), text #FF4444, border rgba(255,68,68,0.3)
```

---

## Layout

- Docs max-width: 1200px
- Sidebar: 240px
- Content prose width: 680px
- No sidebar on marketing pages

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
- Use the teal only as an accent — it should feel like a highlight, not a fill
- Black text on teal buttons — never white; the contrast ratio demands it
- Use `JetBrains Mono` for all code, imports, and CLI commands
- Let whitespace breathe — Deno's minimalism is a feature, not laziness
- Show security context (permissions, `--allow-net`) in a distinct visual style

### DON'T
- Don't add color variety — one teal accent is the entire palette
- Don't use gradients — Deno is flat and binary (black/white/teal)
- Don't round corners more than 8px — sharp edges signal precision
- Don't use animation on documentation content — distraction is the enemy of focus
- Don't use the teal for error or warning states — semantic colors must remain separate
