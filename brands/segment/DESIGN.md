# Segment Design System

## Brand Overview
Segment is a customer data platform — collect, clean, and route data to every tool. The design language reflects trust, data clarity, and pipeline thinking: a clean teal-green on deep navy surfaces.

## Color Palette

### Primary
- **Green**: `#52BD94` — primary brand, CTAs, active states
- **Green Dark**: `#3D9E7A` — hover, pressed
- **Green Light**: `#7ED4B3` — highlights, icons

### Semantic
- **Success**: `#52BD94`
- **Warning**: `#F5A623`
- **Error**: `#E03E3E`
- **Info**: `#3D8EF0`

### Surfaces (Dark Mode)
- **Background**: `#0D1B2A`
- **Surface**: `#162336`
- **Elevated**: `#1E3048`
- **Border**: `#2A4060`

### Text
- **Primary**: `#E8F0F8`
- **Secondary**: `#7A9BBB`
- **Muted**: `#3D5A78`

## Typography

- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for event names, write keys, JSON payloads)

### Scale
| Token | Size | Weight | Use |
|-------|------|--------|-----|
| display | 36px | 700 | Hero |
| h1 | 26px | 700 | Page title |
| h2 | 20px | 600 | Section |
| body | 14px | 400 | Default |
| small | 12px | 400 | Metadata |
| code | 13px | 400 mono | Event names, payloads |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 10px
- Event rows: 6px
- Inputs: 6px

## Components

### Event Stream
- Scrolling live feed of track/identify/page calls
- Event type badge (track/identify/page/screen/group) color-coded
- Timestamp in muted mono, right-aligned
- Payload expandable on click

### Source Badge
- Green accent, source name in mono
- Icon: dot indicator (green = live, grey = disconnected)

### Destination Card
- Integration logo + name
- Status toggle (enabled/disabled)
- Event volume sparkline

### Write Key Input
- Mono font, masked by default
- Copy-to-clipboard button

## Guardrails
- Event names always in monospace — they are identifiers, not prose
- Write keys must be masked by default — reveal on explicit toggle
- Data flow direction must be visually clear (source → destination)
- Never truncate event payloads without an expand affordance
- Use green for data-flowing/healthy states only
