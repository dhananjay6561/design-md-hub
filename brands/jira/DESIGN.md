# Jira Design System

## Brand Overview
Jira is Atlassian's project tracking tool used by millions of engineering teams. The design language is professional, information-dense, and systematic — built on a confident blue with clear status semantics.

## Color Palette

### Primary
- **Blue**: `#0052CC` — primary brand, CTAs, links
- **Blue Light**: `#0065FF` — hover states
- **Blue Subtle**: `#DEEBFF` — tinted backgrounds (light mode)

### Issue Priority Colors
- **Highest**: `#CD1316` — red
- **High**: `#E97F33` — orange
- **Medium**: `#E2B203` — yellow
- **Low**: `#2D8738` — green
- **Lowest**: `#57A3EF` — blue

### Status Colors
- **To Do**: `#42526E` — grey
- **In Progress**: `#0052CC` — blue
- **Done**: `#00875A` — green
- **Blocked**: `#DE350B` — red

### Surfaces (Dark Mode)
- **Background**: `#161618`
- **Surface**: `#1D1E20`
- **Elevated**: `#27282B`
- **Border**: `#373A3F`

### Text
- **Primary**: `#E6E8EC`
- **Secondary**: `#8C96A4`
- **Muted**: `#596068`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for issue keys, commit hashes)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 4px (Jira uses tight radius)
- Cards: 8px
- Status badges: 3px
- Inputs: 4px

## Components

### Issue Row
- Priority icon left, issue key in mono, summary text, assignee avatar right
- Status badge color-coded
- Story points badge muted right-aligned

### Sprint Board Column
- Column header with count badge
- Cards draggable, shadow on hover
- Assignee avatar bottom-right of card

### Status Badge
- Pill shape, background at 15% opacity of status color
- Text in full status color

## Guardrails
- Issue keys (e.g. ENG-1234) always in monospace
- Priority and status must always be visually distinct
- Dense layout — Jira users expect information density
- Avoid decorative elements — utility first
- Status transitions should be explicit, never implied
