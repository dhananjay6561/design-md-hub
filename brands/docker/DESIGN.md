# Docker Design System

## Overview
Docker is the de-facto standard for containerization. The design language centers on a clear, confident blue — it's technical but accessible, enterprise-grade but not sterile. The whale logo and blue palette are among the most recognized in the developer world.

**Brand personality:** Reliable, universal, developer-first, infrastructure backbone.

---

## Colors

### Primary Palette
| Token | Hex | Usage |
|-------|-----|-------|
| `--docker-blue` | `#2496ED` | Primary brand, CTAs, links |
| `--docker-blue-dark` | `#1A7BC4` | Hover on blue elements |
| `--docker-navy` | `#003F8A` | Deep accent, gradients |
| `--docker-teal` | `#00ADB5` | Secondary accent |

### Surface Palette (Dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0D1117` | Main background |
| `--bg-surface` | `#131D2B` | Cards, panels |
| `--bg-elevated` | `#1A2840` | Dropdowns, modals |
| `--border` | `#243550` | Dividers, borders |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `--text-primary` | `#F0F6FF` | Headings, body |
| `--text-secondary` | `#8BA5C4` | Labels, captions |
| `--text-muted` | `#506580` | Placeholders, disabled |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#26A269` | Container running, healthy |
| `--warning` | `#E5A50A` | Image outdated, restarting |
| `--danger` | `#E01E37` | Container stopped, error |
| `--info` | `#2496ED` | Pull in progress |

---

## Typography

**Primary Font:** `Inter` (Google Fonts)
**Monospace Font:** `JetBrains Mono`

| Scale | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 36px | 700 | Hero, marketing |
| Heading 1 | 26px | 600 | Page titles |
| Heading 2 | 18px | 600 | Section headers |
| Body | 14px | 400 | Default content |
| Small | 12px | 400 | Metadata, timestamps |
| Mono | 13px | 400 | Commands, image names, IDs |

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
| `--radius-sm` | `4px` | Tags, labels |
| `--radius-md` | `6px` | Buttons, inputs |
| `--radius-lg` | `8px` | Cards, panels |
| `--radius-xl` | `12px` | Modals |

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0,0,0,0.5);
--shadow-md: 0 4px 16px rgba(0,0,0,0.6);
--shadow-lg: 0 8px 32px rgba(0,0,0,0.7);
--shadow-blue: 0 0 0 3px rgba(36,150,237,0.3);
```

---

## Components

### Buttons
```
Primary:  bg #2496ED, text white, hover #1A7BC4, radius 6px, height 36px
Ghost:    bg transparent, border #243550, text #8BA5C4, hover border #2496ED
Danger:   bg #E01E37, text white
```

### Inputs
```
Background: #131D2B
Border:     #243550 default, #2496ED focused
Text:       #F0F6FF
Placeholder: #506580
Radius:     6px, height: 36px
Font:       JetBrains Mono for image names, tags
```

### Container Status Badges
```
Running:    bg rgba(38,162,105,0.12), text #26A269
Stopped:    bg rgba(224,30,55,0.12), text #E01E37
Restarting: bg rgba(229,165,10,0.12), text #E5A50A
Pulling:    bg rgba(36,150,237,0.12), text #2496ED
```

### Terminal Block
```
Background: #000000
Border:     1px solid #243550
Radius:     6px
Font:       JetBrains Mono 12px
Prompt:     color #2496ED
Output:     color #8BA5C4
Success:    color #26A269
Error:      color #E01E37
```

---

## Layout

- Dashboard max-width: 1280px
- Sidebar: 220px
- Content padding: 24px
- Container list: table layout preferred

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
- Use monospace for all image names, container IDs, tags, and CLI commands
- Color-code container status consistently across all views
- Show container logs in a dark terminal block — black, not navy
- Use the blue anchor sparingly for primary actions — it must feel clickable
- Show resource usage (CPU/RAM) with progress bars, not just numbers

### DON'T
- Don't use light mode for container dashboards — operators work in dim conditions
- Don't use rounded corners beyond 8px — Docker is infrastructure, not consumer
- Don't mix the teal accent with blue in the same component
- Don't show partial image names — always show full registry/repo:tag
- Don't use color alone to indicate status — pair with text labels too
