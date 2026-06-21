# Auth0 Design System

## Overview
Auth0 (now part of Okta) is a leading identity and authentication platform. The design language is clean, professional, and secure-feeling — the orange accent on dark backgrounds communicates warmth and trustworthiness. It's enterprise-ready but developer-accessible.

**Brand personality:** Secure, trustworthy, developer-friendly, enterprise-grade, clear.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--auth0-orange` | `#EB5424` | Primary brand, CTAs, highlights |
| `--auth0-orange-hover` | `#C9481E` | Hover states |
| `--auth0-orange-light` | `#FF7849` | Subtle highlights |
| `--auth0-blue` | `#16214D` | Deep accent surface |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0E1117` | Main background |
| `--bg-surface` | `#161D2E` | Cards, panels |
| `--bg-elevated` | `#1E2840` | Dropdowns, modals |
| `--border` | `#2A3650` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#F5F7FA` | Headings, body |
| `--text-secondary` | `#8FA3C0` | Labels, captions |
| `--text-muted` | `#546480` | Placeholders, disabled |
| `--text-orange` | `#EB5424` | Links, accent text |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#21A179` | Login successful, token valid |
| `--warning` | `#F5A623` | Token expiring, MFA required |
| `--danger` | `#E03E3E` | Auth failed, blocked user |
| `--info` | `#3B82F6` | Informational |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 36px | 700 | Hero, landing pages |
| Heading 1 | 26px | 600 | Page titles |
| Heading 2 | 20px | 600 | Section headers |
| Body | 14px | 400 | Default content |
| Small | 12px | 400 | Metadata, token previews |
| Mono | 13px | 400 | JWTs, client IDs, callback URLs |

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
| `--radius-md` | `8px` | Buttons, inputs |
| `--radius-lg` | `12px` | Cards, panels |
| `--radius-xl` | `16px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 4px rgba(0,0,0,0.4);
--shadow-md: 0 4px 16px rgba(0,0,0,0.5);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.6);
--shadow-orange: 0 0 0 3px rgba(235,84,36,0.25);
```

---

## Components

### Buttons
```
Primary:  bg #EB5424, text white, hover #C9481E, radius 8px, height 40px, font-weight 500
Ghost:    bg transparent, border #2A3650, text #8FA3C0, hover border #EB5424
Danger:   bg #E03E3E, text white
```

### Inputs
```
Background: #161D2E
Border:     #2A3650 default, #EB5424 focused
Text:       #F5F7FA
Placeholder: #546480
Radius:     8px, height: 40px
Font:       JetBrains Mono for client IDs, secrets, callback URLs
```

### User Status Badges
```
Active:  bg rgba(33,161,121,0.12), text #21A179
Blocked: bg rgba(224,62,62,0.12), text #E03E3E
Pending: bg rgba(245,166,35,0.12), text #F5A623
Invited: bg rgba(59,130,246,0.12), text #3B82F6
```

### JWT Viewer
```
Background: #0E1117
Border:     1px solid #2A3650
Radius:     8px
Header:     color #EB5424 (monospace)
Payload:    color #F5F7FA (monospace)
Signature:  color #8FA3C0 (monospace)
Section divider: · in #546480
```

---

## Layout

- Dashboard max-width: 1280px
- Left nav: 220px
- Content padding: 24px
- Application list: card grid (3-col)

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
- Use monospace for ALL tokens, client IDs, secrets, and callback URLs
- Color-code user status (Active/Blocked/Pending) consistently
- Show JWTs with section color-coding (header/payload/signature)
- Use the orange for primary CTAs — it must always feel actionable
- Mask sensitive values (client secrets) by default with a reveal toggle

### DON'T
- Don't show client secrets in plain text by default — always mask
- Don't use the orange for warnings — semantic colors must stay distinct
- Don't use rounded corners below 8px — Auth0 is security-focused, not playful
- Don't abbreviate tenant names or client IDs — security context requires full values
- Don't use thin fonts on dark backgrounds — critical auth data must be readable
