# Airtable Design System

## Brand Overview
Airtable is a flexible database-spreadsheet hybrid. The brand is colorful, approachable, and structured — a multi-color palette reflecting different field types, base types, and workspace variety.

## Color Palette

### Primary
- **Blue**: `#2D7FF9` — primary brand, CTAs, links
- **Blue Hover**: `#1D6FE9` — pressed states
- **Yellow**: `#FCB400` — brand accent, highlights

### Field Type Colors
- **Text**: `#666666`
- **Number**: `#2D7FF9` — blue
- **Date**: `#20C933` — green
- **Attachment**: `#FF6F2C` — orange
- **Checkbox**: `#20C933` — green
- **Select**: `#8B46FF` — purple
- **Link**: `#F82B60` — pink/red
- **Formula**: `#FCB400` — yellow

### Surfaces (Dark Mode)
- **Background**: `#18191A`
- **Surface**: `#242526`
- **Elevated**: `#2E2F30`
- **Border**: `#3E3F40`

### Text
- **Primary**: `#F0F0F0`
- **Secondary**: `#A0A0A0`
- **Muted**: `#606060`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for formulas, field IDs)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards/Records: 8px
- Field badges: 4px
- Select options: 9999px (pill)

## Components

### Grid Row
- Row number muted left, fields in columns
- Row hover: elevated bg
- Expand icon on row hover to open record

### Select Field Chip
- Colored pill per option — each option has its own color
- Text white or dark based on bg color

### Field Type Badge
- Icon + type name, color-coded by field type
- Used in field configuration dropdown

### Base Card
- Colored icon/emoji, base name, collaborator avatars
- Workspace label below

## Guardrails
- Each select option must have a distinct color — never two identical
- Field type colors are semantic — don't repurpose them
- Grid density should allow at least 20 rows visible without scroll
- Formulas and field IDs in monospace
- Record expand modal should not lose grid context behind it
