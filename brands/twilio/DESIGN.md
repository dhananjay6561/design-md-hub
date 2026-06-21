# Twilio Design System

## Overview
Twilio is the leading cloud communications platform — SMS, voice, video, and email APIs. The design language is bold and confident, anchored by a distinctive red that communicates urgency and reliability. The UI is developer-first with an enterprise finish.

**Brand personality:** Bold, reliable, communication-first, developer-grade, enterprise-ready.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--twilio-red` | `#F22F46` | Primary brand, CTAs |
| `--twilio-red-dark` | `#C82333` | Hover states |
| `--twilio-red-light` | `#FF6B7A` | Highlights, subtle accents |
| `--twilio-blue` | `#0263E0` | Secondary actions, links |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#06080D` | Main background |
| `--bg-surface` | `#0F1623` | Cards, panels |
| `--bg-elevated` | `#172030` | Dropdowns, modals |
| `--border` | `#1F2D42` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#F4F6FA` | Headings, body |
| `--text-secondary` | `#8896AD` | Labels, captions |
| `--text-muted` | `#4E5F78` | Placeholders, disabled |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#07BB8B` | Message delivered, call connected |
| `--warning` | `#E8A800` | Rate limited, queue growing |
| `--danger` | `#F22F46` | Failed delivery, error code |
| `--info` | `#0263E0` | Informational |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 36px | 700 | Marketing, hero |
| Heading 1 | 26px | 600 | Page titles |
| Heading 2 | 20px | 600 | Section headers |
| Body | 14px | 400 | Default content |
| Small | 12px | 400 | Metadata, timestamps |
| Mono | 13px | 400 | Phone numbers, SIDs, webhook payloads |

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
| `--radius-sm` | `4px` | Tags, badges |
| `--radius-md` | `6px` | Buttons, inputs |
| `--radius-lg` | `8px` | Cards, panels |
| `--radius-xl` | `12px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.5);
--shadow-md: 0 4px 16px rgba(0,0,0,0.6);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.7);
--shadow-red: 0 0 0 3px rgba(242,47,70,0.3);
```

---

## Components

### Buttons
```
Primary:  bg #F22F46, text white, hover #C82333, radius 6px, height 38px, font-weight 500
Ghost:    bg transparent, border #1F2D42, text #8896AD, hover border #F22F46
Blue:     bg #0263E0, text white — for secondary actions
```

### Inputs
```
Background: #0F1623
Border:     #1F2D42 default, #F22F46 focused
Text:       #F4F6FA
Placeholder: #4E5F78
Radius:     6px, height: 38px
Font:       JetBrains Mono for phone numbers, SIDs, webhook URLs
```

### Message Status Badges
```
Delivered: bg rgba(7,187,139,0.12), text #07BB8B
Sent:      bg rgba(2,99,224,0.12), text #0263E0
Queued:    bg rgba(232,168,0,0.12), text #E8A800
Failed:    bg rgba(242,47,70,0.12), text #F22F46
```

### Error Code Block
```
Background: #06080D
Border:     left 3px solid #F22F46
Radius:     6px
Code:       JetBrains Mono 13px
Error code: color #F22F46, font-weight 600
Message:    color #8896AD
```

---

## Layout

- Console max-width: 1280px
- Left sidebar: 220px
- Content padding: 24px
- Phone number tables use monospace throughout

---

## Responsive Breakpoints

| Name | Width |
|------|-------|
| Mobile | < 768px |
| Tablet | 768px – 1280px |
| Desktop | > 1280px |

---

## Tone & Guardrails

### DO
- Use monospace for ALL phone numbers, SIDs, account IDs, and webhook payloads
- Color-code message status consistently (Delivered/Sent/Queued/Failed)
- Show error codes prominently — developers debugging failed messages need them fast
- Use the red confidently — it's a brand color here, not just a warning signal
- Display delivery receipts with timestamps in relative time

### DON'T
- Don't confuse brand red with danger red — Twilio red IS the primary action color
- Don't use light mode for the console — developers prefer dark for long sessions
- Don't truncate phone numbers — always show the full E.164 format (+12025551234)
- Don't use soft corners beyond 8px — Twilio is enterprise-grade, not a consumer app
- Don't skip error code details — a vague "failed" message is useless for debugging
