# Webflow Design System

## Brand Overview
Webflow is a visual web development platform — design, build, and launch sites without writing code. The brand is bold, creative, and premium, built on a deep blue-indigo with dark surfaces.

## Color Palette

### Primary
- **Indigo**: `#4353FF` — primary brand, CTAs, active states
- **Indigo Hover**: `#3343EE` — pressed states
- **Indigo Light**: `#6B7AFF` — highlights, focus rings

### Semantic
- **Success**: `#12A150`
- **Warning**: `#F5A623`
- **Error**: `#E03E3E`

### Surfaces (Dark Mode)
- **Background**: `#0E0E10`
- **Surface**: `#1A1A1F`
- **Elevated**: `#242429`
- **Border**: `#34343C`

### Text
- **Primary**: `#F2F2F5`
- **Secondary**: `#9090A0`
- **Muted**: `#55556A`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for CSS values, class names, breakpoints)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 8px
- Cards: 12px
- Canvas elements: 4px
- Inputs: 8px

## Components

### Canvas Element
- Dashed border when selected, indigo when active
- Resize handles on corners
- Label chip top-left with element type

### Breakpoint Pills
- Desktop / Tablet / Mobile — horizontal switcher
- Active breakpoint highlighted in indigo

### Class Badge
- Indigo bg at 10% opacity, indigo text
- Mono font for class names

### Style Panel
- Property name left, value right in mono
- Hover reveals edit affordance

## Guardrails
- CSS values and class names always in monospace
- Canvas selection state must be unmistakably visible
- Breakpoint indicators must be persistent — never hidden
- Don't use indigo for warnings — keep semantics clean
- Keep panels information-dense but scannable
