# Algolia Design System

## Brand Overview
Algolia is a search-as-a-service platform. The design language conveys instant, precise, and intelligent search — built around a vivid blue with dark, focused surfaces and crisp typography.

## Color Palette

### Primary
- **Blue**: `#003DFF` — primary brand color, CTAs, links
- **Blue Medium**: `#5468FF` — hover, interactive highlights
- **Blue Light**: `#8594FF` — focus rings, subtle accents

### Semantic
- **Success**: `#18981D`
- **Warning**: `#F59E0B`
- **Error**: `#EF4444`
- **Hit Highlight**: `#FFE000` — search result highlights

### Surfaces (Dark Mode)
- **Background**: `#1C1E21`
- **Surface**: `#26292D`
- **Elevated**: `#303439`
- **Border**: `#3C4148`

### Text
- **Primary**: `#F0F0F0`
- **Secondary**: `#9BA1A6`
- **Muted**: `#5C6370`

## Typography

- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for index names, API keys)

### Scale
| Token | Size | Weight | Use |
|-------|------|--------|-----|
| display | 36px | 700 | Hero |
| h1 | 26px | 700 | Page title |
| h2 | 20px | 600 | Section |
| body | 14px | 400 | Default |
| small | 12px | 400 | Metadata |
| code | 13px | 400 mono | Index names, keys |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Search box: 8px
- Cards: 10px
- Hit rows: 6px
- Buttons: 6px

## Components

### Search Box
- Full-width, prominent border that glows blue on focus
- Search icon left, clear (×) right when populated
- Instant result dropdown below, max 6 visible items

### Hit Row
- Matched terms highlighted in `#FFE000` with dark text
- Breadcrumb path in muted text above result title
- Category badge right-aligned

### Index Badge
- Mono font, blue bg at 12% opacity
- Border: blue 30% opacity

### Stats Bar
- X results in Y ms — muted text, small size
- Speed always displayed — it's a core feature

## Guardrails
- Always highlight matched query terms — never show raw results without highlighting
- Search must feel instant — use skeleton loaders, never empty states during load
- Index names always in monospace
- API keys must always be partially masked
- Blue on dark only — never blue text on light backgrounds without contrast check
