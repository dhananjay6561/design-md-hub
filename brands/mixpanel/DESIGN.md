# Mixpanel Design System

## Brand Overview
Mixpanel is a product analytics platform focused on event-based tracking. The brand is dark, bold, and data-forward — built on a deep violet/purple with sharp data visualizations.

## Color Palette

### Primary
- **Violet**: `#7856FF` — primary brand, CTAs, chart series 1
- **Violet Dark**: `#5D3FD3` — hover, pressed
- **Violet Light**: `#A08AFF` — highlights, secondary series

### Chart Series
- **Series 1**: `#7856FF` — violet
- **Series 2**: `#FF6B6B` — coral
- **Series 3**: `#4ECDC4` — teal
- **Series 4**: `#FFE66D` — yellow
- **Series 5**: `#A8E6CF` — mint

### Semantic
- **Success**: `#4ECDC4`
- **Warning**: `#FFD166`
- **Error**: `#FF6B6B`

### Surfaces (Dark Mode)
- **Background**: `#0A0A14`
- **Surface**: `#13131F`
- **Elevated**: `#1C1C2E`
- **Border**: `#2A2A42`

### Text
- **Primary**: `#EEEEFF`
- **Secondary**: `#8888BB`
- **Muted**: `#4A4A6A`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for event names, property keys)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 8px
- Cards: 12px
- Inputs: 8px

## Components

### Funnel Chart
- Horizontal bar per step, proportional width
- Step name left, conversion % right in bold violet
- Drop-off delta between steps in red

### Retention Grid
- Row = cohort week, columns = week N retention
- Color intensity: deeper violet = higher retention
- Header row and column with dates

### Event Property Tag
- Mono, violet bg at 10% opacity

## Guardrails
- Event names always in monospace
- Chart series colors must be used in order
- Always show both absolute numbers and percentages
- Retention grid cells must be readable — don't go below 40% opacity
- Empty chart states need a guide, not just "no data"
