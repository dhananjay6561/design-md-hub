# Hasura Design System

## Brand Overview
Hasura is a GraphQL engine that gives instant, realtime APIs on databases. The visual identity is technical and precise — dark surfaces, cyan-teal accents, and monospace code everywhere. UI feels like a high-performance developer console.

## Color Palette

### Primary
- Brand Teal: `#1EB4D4`
- Teal Light: `#5ECFE7`
- Teal Dark: `#0F8BA6`

### Backgrounds
- Base: `#0F1117`
- Surface: `#1A1D27`
- Elevated: `#242837`
- Border: `#2E3347`

### Semantic
- Success: `#27AE60`
- Warning: `#F2994A`
- Error: `#EB5757`
- Info: `#1EB4D4`

### Text
- Primary: `#F8FAFC`
- Secondary: `#94A3B8`
- Muted: `#64748B`
- On-teal: `#0F1117`

### GraphQL Syntax
- Field: `#1EB4D4`
- Type: `#A78BFA`
- String: `#86EFAC`
- Keyword: `#FB923C`
- Comment: `#64748B`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
- Code/Query: `JetBrains Mono, Fira Code, monospace`

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

### Query Editor
- Dark surface `#1A1D27`
- Monospace font, syntax highlighted
- Line numbers in muted text
- Run button: teal filled, top-right
- Results pane below with JSON output

### Schema Browser
- Left sidebar: table/view list with icons
- Expandable rows showing columns with type badges
- Relationship arrows shown as `→` links
- Search field at top with teal focus ring

### Table Selector
- Dropdown with search
- Database icon prefix
- Schema grouping (public / custom)
- Active item: teal left border

### Status Badges
- Tracked: teal pill
- Untracked: grey outline
- Error: red filled
- Deprecated: orange outline

### Relationship Cards
- Object relationship: single arrow icon
- Array relationship: stacked arrow icon
- Source/target table names in mono
- Edit/delete actions on hover

### Permission Matrix
- Grid: roles × operations (insert/select/update/delete)
- Cell: checkmark (full), partial circle (custom), dash (none)
- Row header: role name
- Hover: highlight entire row/column

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

- Border radius: 4px (inputs, badges), 6px (cards), 8px (modals)
- Border: `1px solid #2E3347`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.4)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.5)`

## Iconography
- Line icons, 16px and 20px
- Stroke weight: 1.5px
- Database, table, column, relationship, permissions themes
- No filled icons except status indicators

## Motion
- Transitions: 150ms ease
- Panel expand: 200ms ease-out
- Query run: spinner in button, no page jump
- Toast notifications: slide in from top-right

## Guardrails

### DO
- Use monospace for all query text, table names, column names
- Use teal exclusively for primary actions and active states
- Keep backgrounds layered: base → surface → elevated
- Show relationship directions clearly with arrows
- Use type badges on every column (Int, String, Boolean, etc.)

### DON'T
- Don't use rounded corners > 8px — feels too soft for a DB tool
- Don't color-code unrelated elements teal — it signals "action"
- Don't show raw SQL unless explicitly toggled — keep GraphQL first
- Don't use animations > 250ms in query workflows
- Don't mix UI font and mono in the same sentence/label
