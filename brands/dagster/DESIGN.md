# Dagster Design System

## Brand Overview
Dagster is the data orchestration platform for building data pipelines and software-defined assets. The visual identity is clean and graph-centric — dark surfaces, vivid purple accents, and asset lineage as the central UI metaphor. UI feels like a thoughtful engineering tool for data teams.

## Color Palette

### Primary
- Brand Purple: `#7B61FF`
- Purple Light: `#A594FF`
- Purple Dark: `#5A44CC`

### Backgrounds
- Base: `#0A0A0F`
- Surface: `#12121A`
- Elevated: `#1A1A26`
- Border: `#2A2A3A`

### Semantic
- Success: `#22C55E`
- Warning: `#F59E0B`
- Error: `#EF4444`
- Skipped: `#94A3B8`

### Run Status
- Success: `#22C55E`
- Failure: `#EF4444`
- In Progress: `#7B61FF`
- Queued: `#60A5FA`
- Canceled: `#94A3B8`
- Skipped: `#71717A`

### Asset Status
- Materialized: `#22C55E`
- Failed: `#EF4444`
- Stale: `#F59E0B`
- Missing: `#94A3B8`
- Materializing: `#7B61FF`

### Text
- Primary: `#F0F0FF`
- Secondary: `#8B8BAA`
- Muted: `#5C5C70`
- On-purple: `#FFFFFF`

## Typography

### Font Stack
- UI: `Space Grotesk, system-ui, sans-serif`
- Code: `JetBrains Mono, monospace`

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

### Asset Graph Node
- Rectangle with rounded corners (6px)
- Asset key as title in bold
- Status dot top-right (color per status)
- Group/repository badge below name
- Dependency arrows: thin lines, directional
- Selected: purple outline 2px

### Job Run Row
- Run ID in mono, truncated
- Job name + tags
- Status badge (color per status)
- Start time + duration
- Asset count materialized
- Click to drill into step logs

### Partition Status Grid
- Grid of colored cells per partition
- Colors: green (success), red (failed), orange (stale), grey (missing)
- X-axis: partitions, Y-axis: runs or time
- Hover: partition key + last run timestamp

### Step Logs
- Timestamp in muted mono
- Log level tag (INFO/WARNING/ERROR)
- Message in primary text
- Step name as collapsible group header

### Asset Catalog Row
- Asset key (hierarchical: `schema/table`)
- Last materialized timestamp
- Owner tag
- Freshness policy indicator
- Compute kind badge (SQL, Python, dbt)

### Sensor / Schedule Card
- Name + cron expression
- Status toggle: Running / Stopped
- Last tick time + result
- Target jobs as tags

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

- Border radius: 4px (tags, badges), 6px (nodes, cards), 8px (modals)
- Border: `1px solid #2A2A3A`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.4)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.5)`

## Iconography
- Line icons, 16px and 20px
- Asset, job, schedule, sensor, partition iconography
- Graph/dag icons for pipeline visualization

## Motion
- Asset graph pan/zoom: 60fps GPU-composited
- Node status change: 200ms color transition
- Run log stream: append-only, no re-render flicker
- Partition grid load: staggered 20ms per row

## Guardrails

### DO
- Use asset key hierarchy (`schema/table`) consistently
- Color-code all statuses — users scan by color first
- Show freshness policy violations prominently (orange/stale)
- Always surface the last materialization timestamp
- Use purple only for selected state and primary actions

### DON'T
- Don't flatten asset key hierarchies — nesting is intentional
- Don't collapse failed run logs by default — visibility is critical
- Don't use green for anything other than "Success/Materialized"
- Don't hide partition count — it's key context for data assets
- Don't auto-refresh the asset graph during materialization — it interrupts inspection
