# Snowflake Design System

## Brand Overview
Snowflake is the cloud data platform — data warehouse, data lake, and data sharing in one. The visual identity is clean and data-forward — deep dark backgrounds, icy blue as the signature color, and query/warehouse-centric layouts. UI communicates enterprise-grade scale with developer-friendly precision.

## Color Palette

### Primary
- Brand Blue: `#29B5E8`
- Blue Light: `#63CFF1`
- Blue Dark: `#1A8FC0`

### Backgrounds
- Base: `#0A0F14`
- Surface: `#111820`
- Elevated: `#182030`
- Border: `#263040`

### Semantic
- Success: `#22C55E`
- Warning: `#F59E0B`
- Error: `#EF4444`
- Info: `#29B5E8`

### Text
- Primary: `#E8F0FF`
- Secondary: `#8098B8`
- Muted: `#506080`
- On-blue: `#FFFFFF`

### SQL Syntax
- Keyword: `#29B5E8`
- Function: `#A78BFA`
- String: `#86EFAC`
- Number: `#FCA5A5`
- Comment: `#506080`
- Table/Column: `#E8F0FF`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
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

### SQL Editor
- Dark surface with line numbers
- Syntax-highlighted SQL
- Run button: blue filled, top-right
- Keyboard shortcut hint: Cmd+Enter
- Error underline: red squiggle

### Query Results Grid
- Column headers: sortable, resizable
- Cell values: type-aware formatting (dates, numbers right-aligned)
- Row count in footer
- Export button: CSV / JSON

### Warehouse Card
- Name + size badge (XS / S / M / L / XL)
- Status: Running (green) / Suspended (grey) / Starting (blue animated)
- Credits/hour + estimated cost
- Suspend / Resume button
- Auto-suspend timer shown

### Database/Schema Tree
- Hierarchical: Account → Database → Schema → Table/View
- Icons: cylinder (DB), folder (schema), grid (table), eye (view)
- Row count badge on tables
- Search at top

### Query History Row
- Query preview (first 60 chars of SQL)
- Status badge: Success / Failed / Running
- Duration in mono
- Warehouse used
- Timestamp

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
- Use blue exclusively for primary actions and active states
- Show warehouse status prominently — it affects cost directly
- Use monospace for all SQL, column names, and row values
- Show query duration on every result — performance is key
- Color-code SQL syntax tokens consistently

### DON'T
- Don't hide credit consumption — it's the core billing signal
- Don't auto-resume warehouses silently — always confirm
- Don't truncate query results — paginate with explicit row count
- Don't use sans-serif for SQL — mono only
- Don't collapse the schema tree by default — context is critical
