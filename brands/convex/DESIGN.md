# Convex Design System

## Brand Overview
Convex is the reactive backend platform — real-time database, functions, and file storage in one. The visual identity is warm and modern — very dark backgrounds, amber-orange accents, and reactive/live UI patterns. UI communicates backend-as-a-product: the dashboard is the developer's lens into a living system.

## Color Palette

### Primary
- Brand Amber: `#F5A623`
- Amber Light: `#FFBE5C`
- Amber Dark: `#C07D0F`

### Backgrounds
- Base: `#0A0A0A`
- Surface: `#111111`
- Elevated: `#1A1A1A`
- Border: `#2A2A2A`

### Semantic
- Success: `#22C55E`
- Warning: `#F5A623`
- Error: `#EF4444`
- Info: `#60A5FA`

### Text
- Primary: `#F5F5F5`
- Secondary: `#A0A0A0`
- Muted: `#666666`
- On-amber: `#0A0A0A`

### Function Types
- Query: `#60A5FA`
- Mutation: `#F5A623`
- Action: `#A78BFA`
- HTTP Action: `#34D399`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
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

### Function Log Row
- Function name in mono
- Type badge: Query / Mutation / Action (color per type)
- Duration in mono
- Status: success (green check) / error (red x)
- Timestamp right-aligned in muted text
- Expand: shows arguments and return value as JSON

### Data Browser Table
- Column headers: field name + type badge
- Row hover: subtle surface highlight
- ID column: always first, monospace, truncated
- Reactive indicator: amber pulse dot when live

### Document Viewer
- JSON tree with expand/collapse
- Key names in secondary text
- String values in green mono
- Number values in amber mono
- Null in muted text
- Edit inline: click value to edit

### Deployment Card
- Deployment name + URL
- Status dot: live (green) / paused (grey) / error (red)
- Function count badge
- Last deploy timestamp
- Environment: Production / Preview / Development

### Metrics Sparkline
- Small inline chart (48px tall)
- Amber line on dark bg
- No axes — relative trend only
- Current value displayed next to sparkline

### Environment Variable Row
- Key in mono
- Value masked: `••••••••`
- Reveal toggle button
- Copy button
- Edit / Delete in overflow

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

- Border radius: 4px (badges, tags), 6px (cards, inputs), 8px (modals)
- Border: `1px solid #2A2A2A`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.5)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.6)`

## Iconography
- Line icons, 16px and 20px
- Function, database, file, deployment icons
- Reactive indicator: animated amber pulse dot

## Motion
- Log stream: smooth append, no layout shift
- Reactive data pulse: amber glow on change
- Document edit: inline transition 150ms
- Status badge: instant color change

## Guardrails

### DO
- Color-code function types consistently across all views
- Show real-time reactivity — pulse on live data changes
- Always mask env variable values by default
- Use mono for all function names, IDs, and document fields
- Show duration on every function call — performance matters

### DON'T
- Don't use amber for anything other than primary actions and Mutations
- Don't show full document contents in list views — truncate arrays/objects
- Don't hide error stack traces — show them fully in log rows
- Don't paginate realtime logs — stream them
- Don't omit function type from any context where functions appear
