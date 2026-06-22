# Postman Design System

## Brand Overview
Postman is the world's most popular API platform — used for building, testing, and documenting APIs. The visual identity is bold and warm — deep dark backgrounds, signature orange as the hero color, and request/response-centric layouts. UI feels like a powerful yet approachable developer workspace.

## Color Palette

### Primary
- Brand Orange: `#FF6C37`
- Orange Light: `#FF9068`
- Orange Dark: `#CC4F1E`

### Backgrounds
- Base: `#0C0D0E`
- Surface: `#161718`
- Elevated: `#1E2022`
- Border: `#2E3135`

### Semantic
- Success: `#27AE60`
- Warning: `#F2994A`
- Error: `#EB5757`
- Info: `#2F80ED`

### Text
- Primary: `#F5F5F5`
- Secondary: `#9E9E9E`
- Muted: `#616161`
- On-orange: `#FFFFFF`

### HTTP Method Colors
- GET: `#27AE60`
- POST: `#F2994A`
- PUT: `#2F80ED`
- PATCH: `#9B51E0`
- DELETE: `#EB5757`
- HEAD: `#27AE60`
- OPTIONS: `#9E9E9E`

## Typography

### Font Stack
- UI: `Space Grotesk, system-ui, sans-serif`
- Code/Body: `JetBrains Mono, monospace`

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

### Request Builder
- Method dropdown: color-coded pill (GET=green, POST=orange, etc.)
- URL bar: monospace input, full width
- Send button: orange filled
- Tabs below: Params / Auth / Headers / Body / Scripts

### Response Viewer
- Status badge: 200 (green), 4xx (orange), 5xx (red)
- Response time + size in muted text
- Body tab: JSON with syntax highlighting
- Pretty / Raw / Preview toggle

### Collection Sidebar
- Folder icon + collection name
- Nested request rows with method badge
- Active request: orange left border
- Search bar at top

### Environment Selector
- Dropdown in top-right of workspace
- Environment name + variable count
- Active variables shown as key-value list
- Add variable button: dashed border row

### Auth Config Panel
- Auth type dropdown (Bearer, Basic, OAuth2, API Key…)
- Token/key input masked
- "Use collection auth" inherit option

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
- Border radius: 4px (badges, method pills), 6px (inputs, cards), 8px (modals)
- Border: `1px solid #2E3135`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.5)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.6)`

## Guardrails

### DO
- Color-code HTTP methods consistently across all views
- Use orange only for the primary Send/submit action
- Show status codes prominently with color — they're the key signal
- Use mono for URLs, headers, request/response bodies
- Show response time on every request — performance is a core concern

### DON'T
- Don't use the same color for different HTTP methods
- Don't hide the response status code — it's the first thing devs look for
- Don't wrap URLs — keep them on one line with horizontal scroll
- Don't truncate JSON response bodies — show full payload with collapse
- Don't mix sans-serif and mono in the same code block
