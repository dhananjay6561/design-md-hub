# Amplitude Design System

## Brand Overview
Amplitude is a product analytics platform. The design language reflects clarity in data, confident decision-making, and insight — built on a strong indigo with dark surfaces and sharp data visualizations.

## Color Palette

### Primary
- **Indigo**: `#1C57EB` — primary brand, CTAs, chart lines
- **Indigo Hover**: `#1648C9` — interactive states
- **Indigo Light**: `#5B8AF5` — secondary chart series, highlights

### Chart Colors
- **Series 1**: `#1C57EB`
- **Series 2**: `#9B59F5`
- **Series 3**: `#00BFA5`
- **Series 4**: `#F5A623`
- **Series 5**: `#E84393`

### Semantic
- **Success**: `#00BFA5`
- **Warning**: `#F5A623`
- **Error**: `#E03E3E`

### Surfaces (Dark Mode)
- **Background**: `#0D0F1A`
- **Surface**: `#161929`
- **Elevated**: `#1F2340`
- **Border**: `#2A3058`

### Text
- **Primary**: `#EEF0FA`
- **Secondary**: `#8B93C4`
- **Muted**: `#4A5280`

## Typography

- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for event properties, user IDs)

### Scale
| Token | Size | Weight | Use |
|-------|------|--------|-----|
| display | 36px | 700 | Hero |
- h1: 26px 700 — Page title
- h2: 20px 600 — Section
- body: 14px 400 — Default
- small: 12px 400 — Chart labels
- code: 13px mono — Event properties

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 10px
- Chart tooltips: 6px
- Inputs: 6px

## Components

### Metric Card
- Large number in display weight
- Trend indicator: green arrow up, red arrow down
- Comparison period in muted text
- Sparkline at card bottom

### Chart Area
- Grid lines: muted at 20% opacity
- Axis labels: 11px muted text
- Tooltip: elevated surface, border, all series values
- Zoom/brush selector at bottom

### Funnel Step
- Horizontal bars proportional to conversion
- Step name left, % right in bold
- Drop-off shown as lighter bar extension

### Event Property Tag
- Mono font
- Indigo bg at 10% opacity
- Border: indigo 25% opacity

## Guardrails
- Chart colors must be distinguishable at a glance — use the defined palette in order
- Always show absolute numbers alongside percentages
- Trend arrows must use red/green semantics — never indigo
- Event names and properties always in monospace
- Empty states for charts must include a call-to-action, not just "no data"
