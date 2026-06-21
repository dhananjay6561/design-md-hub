# Pinecone Design System

## Brand Overview
Pinecone is the leading vector database for AI applications. The visual identity is sleek and data-forward — dark surfaces, teal-green accents, and numerical precision everywhere. UI feels like a high-performance data infrastructure console built for ML engineers.

## Color Palette

### Primary
- Brand Teal: `#1ECA8A`
- Teal Light: `#5EDBB0`
- Teal Dark: `#0F9E6A`

### Backgrounds
- Base: `#0A0C10`
- Surface: `#111318`
- Elevated: `#181B22`
- Border: `#252A35`

### Semantic
- Success: `#1ECA8A`
- Warning: `#F59E0B`
- Error: `#EF4444`
- Info: `#3B82F6`

### Text
- Primary: `#F0F4FF`
- Secondary: `#8B95B0`
- Muted: `#5A6080`
- On-teal: `#0A0C10`

### Similarity Score
- High (>0.9): `#1ECA8A`
- Medium (0.7-0.9): `#3B82F6`
- Low (<0.7): `#94A3B8`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
- Numbers/IDs: `JetBrains Mono, monospace`

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

### Index Card
- Index name as title
- Dimension count badge (e.g. `1536 dims`)
- Metric badge: cosine / euclidean / dotproduct
- Vector count in large mono number
- Fullness bar (teal fill, proportional)
- Pod type / serverless badge

### Query Result Row
- Rank number in muted text (#1, #2…)
- Vector ID in mono
- Score displayed prominently in teal mono
- Metadata key-value pairs as tags
- Namespace badge on right

### Namespace Selector
- Dropdown with namespace names
- Vector count per namespace
- Default namespace marked with `(default)` suffix

### Upsert Form
- ID field: mono input
- Vector input: comma-separated floats in mono textarea
- Metadata: JSON key-value editor
- Namespace picker
- Submit: teal filled button

### Stats Panel
- Total vector count (large number)
- Dimension, metric, pod type in a small grid
- Index fullness: progress bar with percentage
- Namespaces listed with individual vector counts

### API Key Row
- Key name
- Masked key value in mono
- Environment: Production / Development badge
- Created date
- Copy + Delete actions

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

- Border radius: 4px (badges, mono chips), 6px (cards, inputs), 8px (modals)
- Border: `1px solid #252A35`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.4)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.5)`

## Iconography
- Line icons, 16px and 20px
- Database, search/magnify, nodes/graph for vector concepts
- Progress bars > icons for capacity visualization

## Motion
- Transitions: 150ms ease
- Query results: staggered fade-in (50ms delay per row)
- Score bar: width transition on load 300ms
- Fullness bar: fill transition 400ms ease-out

## Guardrails

### DO
- Always display similarity scores in teal mono
- Show dimension count on every index reference
- Use fullness bars to communicate capacity visually
- Display vector IDs in monospace always
- Color-code scores by range (high/medium/low)

### DON'T
- Don't show raw float vectors in UI unless debugging
- Don't omit the metric type (cosine/euclidean/dotproduct) — it changes search semantics
- Don't truncate vector IDs without a tooltip showing full value
- Don't use teal for anything other than primary actions and score highlights
- Don't show pod details for serverless indexes
