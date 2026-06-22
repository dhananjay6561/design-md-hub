# Temporal Design System

## Brand Overview
Temporal is a workflow orchestration platform for durable execution. The visual identity is precise and systematic — near-black backgrounds, blue accents, and timeline/graph-centric layouts. UI communicates reliability, tracing, and long-running process visibility.

## Color Palette

### Primary
- Brand Blue: `#438AFF`
- Blue Light: `#76AAFF`
- Blue Dark: `#2060CC`

### Backgrounds
- Base: `#0D0D0F`
- Surface: `#161618`
- Elevated: `#1E1E22`
- Border: `#2A2A30`

### Semantic
- Running: `#438AFF`
- Completed: `#22C55E`
- Failed: `#EF4444`
- TimedOut: `#F97316`
- Canceled: `#94A3B8`
- Terminated: `#A855F7`

### Text
- Primary: `#F4F4F6`
- Secondary: `#8B8B9E`
- Muted: `#5C5C70`
- On-blue: `#FFFFFF`

### Workflow States
- Activity: `#438AFF`
- Timer: `#A78BFA`
- Signal: `#FB923C`
- Child Workflow: `#34D399`

## Typography

### Font Stack
- UI: `Space Grotesk, system-ui, sans-serif`
- Code/IDs: `JetBrains Mono, monospace`

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

### Workflow Timeline
- Horizontal event chain with connecting lines
- Node types: activity (circle), timer (clock), signal (bolt), child workflow (nested)
- Node color maps to event type
- Duration labels below each node
- Hover: tooltip with full event details

### Workflow List Row
- Workflow ID in monospace, truncated
- Type name in secondary text
- Status badge (left-colored pill)
- Start time, duration, run ID
- Click to drill into event history

### Event History
- Vertical list of events, newest at bottom
- Event type tag: EventType color-coded
- Timestamp in mono, relative + absolute on hover
- Expandable JSON payload per event
- Search/filter bar at top

### Activity Card
- Activity name as title
- Attempt count badge (orange if >1)
- Schedule-to-start, start-to-close timing bars
- Worker identity in muted mono text
- Retry policy shown as small config block

### Namespace Selector
- Current namespace pill in header
- Dropdown with namespace list + task queue count
- Environment indicators: prod / staging / dev

### Status Badge
- Running: blue filled
- Completed: green filled
- Failed: red filled
- Timed Out: orange filled
- Canceled: grey outline
- Terminated: purple filled

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

- Border radius: 4px (badges, mono tags), 6px (cards, inputs), 8px (modals)
- Border: `1px solid #2A2A30`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.5)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.6)`

## Iconography
- Line icons, 16px and 20px
- Clock, activity, bolt, fork/branch for workflow concepts
- Status icons: checkmark, x, spinner, pause

## Motion
- Transitions: 150ms ease
- Timeline node hover: 100ms scale
- Workflow list load: staggered fade-in rows
- Event history scroll: smooth momentum

## Guardrails

### DO
- Use status colors consistently across all workflow states
- Always show workflow/run IDs in monospace
- Show timing information prominently — duration is key context
- Use the timeline view for active workflows, list for history
- Color-code event types to aid quick scanning

### DON'T
- Don't abbreviate workflow IDs — they're the primary identifier
- Don't use blue (Running) for completed states
- Don't show raw protobuf — always deserialize to JSON
- Don't collapse event history by default for failed workflows
- Don't use animation heavier than 200ms in the event list
