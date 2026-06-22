# dbt Design System

## Brand Overview
dbt (data build tool) is the transformation layer of the modern data stack — SQL-first data modeling, testing, and documentation. The visual identity is warm and developer-centric — near-black backgrounds, coral-orange as the signature accent, and lineage/model-centric layouts. UI communicates data engineering as software engineering.

## Color Palette

### Primary
- Brand Orange: `#FF694A`
- Orange Light: `#FF8F76`
- Orange Dark: `#CC4A2E`

### Backgrounds
- Base: `#0E0E10`
- Surface: `#161618`
- Elevated: `#1E1E22`
- Border: `#2C2C32`

### Semantic
- Success: `#22C55E`
- Warning: `#F59E0B`
- Error: `#EF4444`
- Skipped: `#94A3B8`

### Text
- Primary: `#F2F2F4`
- Secondary: `#9090A0`
- Muted: `#606070`
- On-orange: `#FFFFFF`

### Node Types
- Model: `#FF694A`
- Source: `#22C55E`
- Seed: `#F59E0B`
- Snapshot: `#A78BFA`
- Exposure: `#60A5FA`
- Metric: `#34D399`

### Test Status
- Pass: `#22C55E`
- Fail: `#EF4444`
- Warn: `#F59E0B`
- Error: `#EF4444`
- Skipped: `#94A3B8`

## Typography

### Font Stack
- UI: `IBM Plex Sans, system-ui, sans-serif`
- Code/SQL: `JetBrains Mono, monospace`

### Scale
- xs: 11px / 1.5
- sm: 13px / 1.5
- base: 14px / 1.6
- md: 16px / 1.5
- lg: 18px / 1.4
- xl: 22px / 1.3
- 2xl: 28px / 1.2

## Components

### Lineage Graph
- DAG of nodes: models, sources, seeds, exposures
- Node color per type
- Selected node: orange outline
- Upstream/downstream highlighted on hover
- Zoom controls + fit-to-screen

### Model Node
- Node name in bold
- Type badge: model / source / seed
- Materialization badge: table / view / incremental / ephemeral
- Status dot: pass / fail / warn / skipped

### Run Results
- Model name + file path in mono
- Status: ✓ Pass / ✕ Fail / ⚠ Warn
- Duration in mono
- Row count affected
- Expandable log output below

### Test Row
- Test name (unique, not_null, accepted_values, etc.)
- Column name in mono
- Status badge
- Failures count (red if > 0)

### SQL Model Preview
- Dark code block, syntax-highlighted SQL
- `{{ ref() }}` and `{{ source() }}` highlighted in orange
- Jinja expressions in purple
- Line numbers

### Job Run Card
- Job name
- Triggered by: schedule / API / manual
- Status + duration
- Models passed / failed / skipped counts
- Last run time

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
- Color-code node types consistently — lineage is the core mental model
- Show test failure counts prominently — zero failures is the goal
- Use mono for all model names, column names, and SQL
- Show materialization type on every model reference
- Highlight `ref()` and `source()` in SQL — they define the DAG

### DON'T
- Don't hide skipped tests — they're as important as failures
- Don't flatten the lineage graph — depth is meaningful
- Don't use orange for anything other than models and primary actions
- Don't truncate run logs — developers debug from them
- Don't auto-run on save without confirmation
