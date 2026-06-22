# Canva Design System

## Brand Overview
Canva is the visual communication platform — design tools for everyone. The visual identity is vibrant and creative — dark surfaces, signature purple as the hero color with teal as an accent, and template/canvas-centric layouts. UI communicates creative empowerment: approachable, polished, and feature-rich without feeling overwhelming.

## Color Palette

### Primary
- Brand Purple: `#7D2AE8`
- Purple Light: `#9B59F5`
- Purple Dark: `#5C1DB3`

### Accent
- Teal: `#00C4CC`
- Teal Light: `#40D9DF`
- Teal Dark: `#009BA1`

### Backgrounds
- Base: `#1A1A2E`
- Surface: `#22223A`
- Elevated: `#2C2C48`
- Border: `#3C3C58`

### Semantic
- Success: `#22C55E`
- Warning: `#F59E0B`
- Error: `#EF4444`
- Info: `#00C4CC`

### Text
- Primary: `#F0F0FF`
- Secondary: `#9898B8`
- Muted: `#6060808`
- On-purple: `#FFFFFF`
- On-teal: `#0A1A1A`

### Element Categories
- Photos: `#FF6B6B`
- Graphics: `#7D2AE8`
- Text: `#00C4CC`
- Video: `#F59E0B`
- Audio: `#22C55E`
- Charts: `#3B82F6`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
- Brand wordmark: Display/custom weight

### Scale
- xs: 11px / 1.5
- sm: 13px / 1.5
- base: 14px / 1.6
- md: 16px / 1.5
- lg: 18px / 1.4
- xl: 22px / 1.3
- 2xl: 28px / 1.2
- 3xl: 36px / 1.1

### Weights
- Regular: 400
- Medium: 500
- Semibold: 600
- Bold: 700

## Components

### Template Card
- Thumbnail preview (aspect ratio preserved)
- Template name on hover overlay
- Category tag below
- "Use template" CTA on hover: purple filled
- Pro badge: gold star top-right if premium

### Editor Canvas
- Canvas area on dark bg
- Selected element: purple outline with resize handles
- Multi-select: blue outline
- Snap guides: teal lines on snap
- Page indicator: dots at bottom

### Left Panel (Elements)
- Search bar at top with teal focus ring
- Category filters: horizontal pill row
- Grid of element thumbnails
- Hover: slight lift shadow + "Add" overlay

### Color Picker
- Swatch grid: brand + document colors
- Hex input in mono
- Opacity slider
- Gradient option toggle
- Recently used row at bottom

### Layer Panel
- List of elements: drag handle, name, lock/hide icons
- Indented for groups
- Selected: purple bg row
- Hidden: text muted + eye-off icon

### Brand Kit Card
- Logo thumbnail
- Color swatches row (circular, 24px each)
- Font pair display
- "Brand Pro" badge if applicable

## Spacing

```
4px   — tight element gaps
8px   — panel padding xs
12px  — panel padding sm
16px  — base padding
20px  — card padding
24px  — section gap
32px  — major section gap
48px  — page section spacing
```

## Elevation & Borders

- Border radius: 6px (thumbnails, cards), 8px (panels), 12px (modals, popovers)
- Border: `1px solid #3C3C58`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.4)`
- Shadow md: `0 4px 20px rgba(0,0,0,0.5)`
- Canvas shadow: `0 8px 40px rgba(0,0,0,0.6)`

## Iconography
- Line icons with slightly heavier stroke (1.8px)
- Creative category icons: photos, graphics, text, shapes, elements
- Editor actions: align, group, lock, flip, crop

## Motion
- Template card hover: 200ms lift
- Canvas selection handles: instant (no delay)
- Panel slide-in: 200ms ease-out
- Element add: 150ms scale-in from click origin
- Snap guides: instant appear/disappear

## Guardrails

### DO
- Use purple as the single primary action color
- Keep canvas bg darker than canvas surface — focus on content
- Show template previews at true aspect ratio — no cropping
- Use teal for interactive affordances (snap, focus, info)
- Keep the toolbar minimal — surface contextual tools only

### DON'T
- Don't use more than 2 accent colors simultaneously
- Don't animate canvas elements on selection — instant handles only
- Don't truncate template names in the grid — use tooltip on hover
- Don't use filled icons in the toolbar — line only for clarity
- Don't show more than 3 layers of panel nesting (panel → group → element)
