# GitLab Design System

## Brand Overview
GitLab is an all-in-one DevOps platform — from code to deploy. The brand is bold and energetic, built around a distinctive orange that communicates speed and openness.

## Color Palette

### Primary
- **Orange**: `#FC6D26` — primary brand, CTAs, highlights
- **Orange Dark**: `#E24329` — hover, pressed states
- **Orange Light**: `#FCA326` — secondary accents

### Semantic
- **Success**: `#108548`
- **Warning**: `#C17D10`
- **Error**: `#AE1800`
- **Info**: `#0F5986`

### Pipeline Status
- **Passed**: `#108548` — green
- **Failed**: `#AE1800` — red
- **Running**: `#FC6D26` — orange
- **Pending**: `#756FA3` — purple
- **Cancelled**: `#737278` — grey
- **Skipped**: `#737278` — grey

### Surfaces (Dark Mode)
- **Background**: `#1F1F1F`
- **Surface**: `#2B2B2B`
- **Elevated**: `#363636`
- **Border**: `#4A4A4A`

### Text
- **Primary**: `#FAFAFA`
- **Secondary**: `#ACACAC`
- **Muted**: `#737373`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for branch names, commit SHAs, pipeline IDs)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 8px
- Pipeline badges: 4px
- Inputs: 6px

## Components

### Pipeline Stage
- Horizontal stage chain with connecting lines
- Each job: status icon + name, tooltip on hover
- Stage header shows passed/total count

### Merge Request Row
- MR title, branch (mono), author avatar
- Pipeline status dot left of title
- Approvals badge right-aligned

### Branch Badge
- Mono font, bg at 10% primary opacity
- Truncate long names with tooltip

## Guardrails
- Branch names and commit SHAs always in monospace
- Pipeline status colors must match the defined set exactly
- Don't use orange for error states — it belongs to brand/running
- MR titles should not be truncated on desktop
- Keep pipeline stage chains horizontal — never vertical
