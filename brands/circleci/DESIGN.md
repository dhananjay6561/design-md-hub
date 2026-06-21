# CircleCI Design System

## Brand Overview
CircleCI is a CI/CD platform focused on speed and developer experience. The brand is sharp, technical, and confident — built on a near-black with a vivid green accent that signals passing builds.

## Color Palette

### Primary
- **Green**: `#04AA51` — primary brand, passing builds, CTAs
- **Green Hover**: `#038B42` — pressed states
- **Green Light**: `#06CC61` — highlights

### Build Status
- **Passed**: `#04AA51` — green
- **Failed**: `#E5483A` — red
- **Running**: `#FA7A14` — orange (animated)
- **On Hold**: `#9B9B9B` — grey
- **Cancelled**: `#676767` — dark grey

### Semantic
- **Success**: `#04AA51`
- **Warning**: `#FA7A14`
- **Error**: `#E5483A`

### Surfaces (Dark Mode)
- **Background**: `#161616`
- **Surface**: `#1E1E1E`
- **Elevated**: `#282828`
- **Border**: `#383838`

### Text
- **Primary**: `#F5F5F5`
- **Secondary**: `#9A9A9A`
- **Muted**: `#5A5A5A`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for job names, branch names, commit SHAs, config)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 8px
- Status badges: 4px
- Inputs: 6px

## Components

### Workflow Graph
- Jobs as nodes, dependencies as directed edges
- Node color reflects job status
- Parallel jobs shown on same horizontal level

### Pipeline Row
- Branch name in mono, commit SHA in mono
- Status icon left, duration right
- Expand to see individual jobs

### Job Card
- Job name, executor type, duration
- Step list with pass/fail indicators

## Guardrails
- Build status colors are semantic — never repurpose them
- Branch names and SHAs always in monospace
- Running builds should have a subtle pulse animation indicator
- Failed builds must be impossible to miss — red, prominent
- Duration always visible on completed jobs
