# Weights & Biases Design System

## Brand Overview
Weights & Biases (wandb) is the ML experiment tracking and model management platform. The visual identity is bold and data-rich — very dark backgrounds, golden-yellow as the signature accent, and chart/metric-centric layouts. UI feels like a high-density research dashboard built for ML practitioners.

## Color Palette

### Primary
- Brand Gold: `#FFCC00`
- Gold Light: `#FFE066`
- Gold Dark: `#CC9F00`

### Backgrounds
- Base: `#0F0F0F`
- Surface: `#181818`
- Elevated: `#222222`
- Border: `#333333`

### Semantic
- Success: `#34D399`
- Warning: `#FFCC00`
- Error: `#F87171`
- Info: `#60A5FA`

### Text
- Primary: `#F0F0F0`
- Secondary: `#A0A0A0`
- Muted: `#666666`
- On-gold: `#0F0F0F`

### Chart Colors (Run Lines)
- Run 1: `#FFCC00`
- Run 2: `#60A5FA`
- Run 3: `#34D399`
- Run 4: `#F87171`
- Run 5: `#A78BFA`
- Run 6: `#FB923C`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
- Code/Metrics: `JetBrains Mono, monospace`

### Scale
- xs: 11px / 1.5
- sm: 13px / 1.5
- base: 14px / 1.6
- md: 16px / 1.5
- lg: 18px / 1.4
- xl: 22px / 1.3
- 2xl: 28px / 1.2

### Weights
- Regular: 400
- Medium: 500
- Semibold: 600
- Bold: 700

## Components

### Run Row
- Colored left dot (run color)
- Run name in bold
- Status badge: running (animated), finished, crashed, killed
- Key metrics inline: `val_loss: 0.234 · accuracy: 94.2%`
- Duration + GPU hours in muted text

### Metric Chart
- Dark background `#181818`
- Axis labels in muted text
- Grid lines: `#2A2A2A`
- Multiple run lines in chart colors
- Hover tooltip: all runs at that step
- Smooth curves (cubic interpolation)

### Config / Summary Table
- Two-column: key | value
- Key in secondary text
- Value in primary or mono for numbers
- Nested expandable sections

### Artifact Card
- Artifact name + version (`v3`)
- Type badge: dataset / model / code
- Size in muted text
- Aliases as tags (`:latest`, `:best`)

### Project Card
- Project name + entity
- Run count, last active date
- Team avatars if shared
- Hover: quick-access to latest run

### Status Badges
- Running: gold animated dot
- Finished: green
- Crashed: red
- Killed: grey
- Failed: red

## Spacing

```
4px   — tight inline gaps
8px   — component padding xs
12px  — component padding sm
16px  — base padding
20px  — card padding
24px  — section gap
32px  — major section gap
48px  — page section spacing
```

## Elevation & Borders

- Border radius: 4px (badges, tags), 6px (cards, inputs), 8px (modals, panels)
- Border: `1px solid #333333`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.4)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.5)`

## Iconography
- Line icons, 16px and 20px
- Chart/graph iconography dominant
- Run, artifact, sweep, project icons

## Motion
- Chart line draw: 400ms ease-out on load
- Run status pulse: 1.5s ease-in-out infinite for "running"
- Metric card value update: 200ms fade
- Panel expand: 200ms ease-out

## Guardrails

### DO
- Use gold exclusively for primary actions and highlighted runs
- Show step/epoch on x-axis of all charts — time is ambiguous
- Use run colors consistently across all charts in a workspace
- Display metric values with consistent decimal precision
- Show system metrics (GPU util, memory) alongside model metrics

### DON'T
- Don't use rounded corners > 8px on chart containers
- Don't smooth out NaN gaps — show them as breaks in the line
- Don't default to showing all runs — default to top-5 by primary metric
- Don't use gold for anything other than primary CTA and active run
- Don't hide crashed/failed runs by default — researchers need them
