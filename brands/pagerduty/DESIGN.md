# PagerDuty Design System

## Brand Overview
PagerDuty is an incident management and on-call scheduling platform. The design language is urgent, reliable, and action-oriented — built on a bold green with dark surfaces that communicate operational awareness.

## Color Palette

### Primary
- **Green**: `#06AC38` — brand green, active/healthy states
- **Green Dark**: `#059030` — hover, pressed
- **Green Light**: `#3DC65F` — highlights

### Alert Severity
- **Critical**: `#E8001C` — P1, immediate action
- **High**: `#FF6B00` — P2, urgent
- **Medium**: `#F5A623` — P3, warning
- **Low**: `#2D9CDB` — P4, informational
- **Info**: `#828282` — P5, no action needed

### Status
- **Triggered**: `#E8001C` — red
- **Acknowledged**: `#F5A623` — yellow
- **Resolved**: `#06AC38` — green
- **Silenced**: `#828282` — grey

### Surfaces (Dark Mode)
- **Background**: `#0B0B0E`
- **Surface**: `#14151A`
- **Elevated**: `#1E1F26`
- **Border**: `#2C2E38`

### Text
- **Primary**: `#F0F1F5`
- **Secondary**: `#8A8FA8`
- **Muted**: `#4A4E62`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for incident IDs, alert keys, runbook URLs)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Alert cards: 8px
- Status badges: 4px
- Buttons: 6px

## Components

### Incident Alert Card
- Severity color left border (4px)
- Incident title, service name, triggered time
- Status badge top right
- Acknowledge / Resolve actions inline

### On-Call Schedule Row
- User avatar + name, shift time range
- Escalation policy name muted below
- Active shift: green left border

### Status Badge
- Background at 12% severity color
- Text full severity color
- Border at 30% severity color

## Guardrails
- Severity colors are life-safety semantics — never repurpose them
- Critical incidents must have visual urgency: red, prominent
- Incident IDs always in monospace
- Resolved state must feel calming — use green, not grey
- Never hide the acknowledge button behind a hover
