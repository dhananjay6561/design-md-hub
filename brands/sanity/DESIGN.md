# Sanity Design System

## Brand Overview
Sanity is a headless CMS with a real-time, structured content platform. The brand is bold and editorial — built on a striking red with near-black surfaces and a strong typographic hierarchy.

## Color Palette

### Primary
- **Red**: `#F03E2F` — primary brand, CTAs, active states
- **Red Hover**: `#D43020` — pressed states
- **Red Light**: `#FF6B5B` — highlights

### Semantic
- **Success**: `#43BF8F`
- **Warning**: `#F5A623`
- **Error**: `#F03E2F`
- **Info**: `#2276FC`

### Surfaces (Dark Mode)
- **Background**: `#101112`
- **Surface**: `#1A1B1D`
- **Elevated**: `#232428`
- **Border**: `#313238`

### Text
- **Primary**: `#F5F5F5`
- **Secondary**: `#9898A6`
- **Muted**: `#565660`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for GROQ queries, field names, document IDs)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 10px
- Input fields: 6px
- Document preview: 8px

## Components

### Document List Row
- Document title, type badge, last edited
- Published indicator: green dot = live, grey = draft
- Preview thumbnail left when available

### Portable Text Editor
- Block-level formatting toolbar
- Inline annotations underlined in red
- Focus mode hides surrounding UI

### GROQ Query Block
- Dark bg, monospace throughout
- Field names in red, strings in green, operators in grey

### Document Type Badge
- Type name, subtle bg tinted by type color
- Consistent across list and detail views

## Guardrails
- GROQ queries always in monospace
- Published vs draft state must always be visible
- Document IDs in monospace
- Red is for brand CTAs — don't use it for warnings
- Portable text toolbar appears on selection only — don't always-show
