# New Relic Design System

## Brand Overview
New Relic is the observability platform — APM, infrastructure monitoring, logs, and alerts in one. The visual identity is bold and data-dense — very dark backgrounds, vivid teal-green as the signature accent, and chart/metric-centric layouts. UI communicates full-stack visibility with precision and speed.

## Color Palette

### Primary
- Brand Green: `#00AC69`
- Green Light: `#00D188`
- Green Dark: `#008050`

### Backgrounds
- Base: `#0B0C0E`
- Surface: `#131416`
- Elevated: `#1B1D20`
- Border: `#2B2D32`

### Semantic
- Critical: `#DF2D24`
- Warning: `#F0B400`
- Success: `#00AC69`
- Info: `#0079BF`

### Alert Severity
- Critical: `#DF2D24`
- High: `#F0B400`
- Medium: `#8B5CF6`
- Low: `#60A5FA`
- Info: `#94A3B8`

### Text
- Primary: `#EDEDED`
- Secondary: `#8E9096`
- Muted: `#5C5F66`
- On-green: `#000000`

### Chart Colors
- Series 1: `#00AC69`
- Series 2: `#00B3D7`
- Series 3: `#A855F7`
- Series 4: `#F97316`
- Series 5: `#EAB308`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
- Code/Queries: `JetBrains Mono, monospace`

### Scale
- xs: 11px / 1.5
- sm: 13px / 1.5
- base: 14px / 1.6
- md: 16px / 1.5
- lg: 18px / 1.4
- xl: 22px / 1.3
- 2xl: 28px / 1.2

## Components

### APM Service Card
- Service name + language icon
- Response time sparkline
- Throughput (rpm) + Error rate
- Apdex score with color indicator
- Last deploy marker on chart

### Alert Incident Row
- Severity left border (critical=red, warning=yellow)
- Alert name + condition
- Entity affected
- Duration open
- Acknowledge / Close buttons

### NRQL Query Bar
- Full-width monospace input
- Run button: green filled
- Query history dropdown
- Time picker: 30m / 1h / 3h / 1d / custom

### Chart Widget
- Title + NRQL query in tooltip
- Line / Area / Bar / Billboard / Table types
- Threshold lines (warning=yellow, critical=red)
- Legend below with series toggles
- Hover: crosshair + tooltip all series

### Infrastructure Host Row
- Hostname in mono
- CPU % + Memory % + Disk I/O as mini bars
- OS badge
- Status: Reporting (green) / Not reporting (red) / Warning (yellow)

### Log Line
- Timestamp in mono
- Log level tag: INFO / WARN / ERROR / DEBUG
- Service name badge
- Message text
- Expandable JSON attributes on click

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

## Guardrails

### DO
- Use alert severity colors consistently — critical=red, warning=yellow
- Always show time range on every chart — context-free metrics are useless
- Use green exclusively for healthy/success states and primary actions
- Show error rate and response time together — they tell the full story
- Use mono for all NRQL queries, hostnames, and log output

### DON'T
- Don't hide resolved incidents — history is critical for postmortems
- Don't autoscale charts silently — show the y-axis range clearly
- Don't use the same color for different severity levels
- Don't collapse log attributes by default on error logs
- Don't round response times below 1ms — show full precision
