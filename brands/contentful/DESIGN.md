# Contentful Design System

## Brand Overview
Contentful is the leading headless CMS platform. The visual identity is clean and editorial — deep navy backgrounds, vivid blue accents, and structured content hierarchy. UI feels like a professional editorial workspace for content teams and developers alike.

## Color Palette

### Primary
- Brand Blue: `#2536CC`
- Blue Light: `#4C62F5`
- Blue Dark: `#1A2799`

### Backgrounds
- Base: `#0B0E1A`
- Surface: `#141828`
- Elevated: `#1E2438`
- Border: `#2A3050`

### Semantic
- Success: `#2EA44F`
- Warning: `#F5A623`
- Error: `#E34850`
- Info: `#2536CC`

### Text
- Primary: `#F0F2FF`
- Secondary: `#8B95C4`
- Muted: `#5A6490`
- On-blue: `#FFFFFF`

### Content Status
- Published: `#2EA44F`
- Draft: `#F5A623`
- Changed: `#2536CC`
- Archived: `#5A6490`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
- Code: `JetBrains Mono, monospace`

### Scale
- xs: 11px / 1.5
- sm: 13px / 1.5
- base: 14px / 1.6
- md: 16px / 1.5
- lg: 20px / 1.4
- xl: 24px / 1.3
- 2xl: 32px / 1.2

### Weights
- Regular: 400
- Medium: 500
- Semibold: 600
- Bold: 700

## Components

### Entry List
- Row: entry name, content type badge, status dot, last updated
- Status dot: green (published), orange (draft), blue (changed), grey (archived)
- Hover: slight surface elevation
- Bulk select: checkbox on left

### Content Type Editor
- Field rows with drag handle, field name, field type icon
- Field type shown as colored badge (Text=blue, Media=purple, Reference=teal)
- Validation indicators: required asterisk, unique lock icon
- Add field button: dashed border row at bottom

### Entry Editor
- Two-panel: left content fields, right sidebar (info, links, references)
- Rich text editor with toolbar (bold, italic, headings, embeds)
- Field labels in secondary text, values in primary
- Save/publish action bar: fixed bottom

### Asset Preview Card
- Image thumbnail with aspect-ratio preserve
- File name, type badge, file size
- Processing state: skeleton + spinner overlay
- Hover: action overlay (edit, delete, download)

### Status Badges
- Published: green filled pill
- Draft: orange outline pill
- Changed: blue filled pill
- Archived: grey outline pill

### Space Selector
- Logo + space name dropdown
- Environment indicator below (master / staging / development)
- Color-coded environment: prod=red dot, staging=yellow, dev=green

## Spacing

```
4px   — icon gap
8px   — tight padding
12px  — component padding sm
16px  — base padding
20px  — card padding
24px  — section gap
32px  — major section gap
48px  — page section spacing
64px  — hero/top spacing
```

## Elevation & Borders

- Border radius: 4px (badges, chips), 6px (inputs, cards), 8px (modals, panels)
- Border: `1px solid #2A3050`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.4)`
- Shadow md: `0 4px 20px rgba(0,0,0,0.5)`

## Iconography
- Line icons, 16px and 20px
- Content type icons: distinct per field type (text, number, media, reference, etc.)
- Entry status represented by dots, not icons

## Motion
- Transitions: 150ms ease
- Entry row expand: 200ms ease-out
- Status change: color transition 300ms
- Modal open: fade + scale-up 200ms

## Guardrails

### DO
- Use status dots consistently — green/orange/blue/grey only
- Keep the entry list scannable — name, type, status at a glance
- Use blue for primary actions (Save, Publish)
- Distinguish environments visually with color-coded dots
- Show content types with icons in every context where entries appear

### DON'T
- Don't use green for anything except "published" state
- Don't mix content type colors across contexts
- Don't show raw API responses in the editor view
- Don't use more than 2 actions visible on hover (keep it clean)
- Don't render rich text as plain text — always preserve formatting
