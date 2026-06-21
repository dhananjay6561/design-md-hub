# DigitalOcean Design System

## Brand Overview
DigitalOcean is a developer-friendly cloud platform. The brand is approachable, clean, and optimistic — built on a vivid ocean blue with clear, uncluttered surfaces.

## Color Palette

### Primary
- **Blue**: `#0080FF` — primary brand, CTAs, links
- **Blue Hover**: `#0064CC` — pressed states
- **Blue Light**: `#4DA6FF` — highlights, icons

### Semantic
- **Success**: `#00B27A`
- **Warning**: `#FFB020`
- **Error**: `#FF4040`
- **Info**: `#0080FF`

### Surfaces (Dark Mode)
- **Background**: `#0B1624`
- **Surface**: `#131F2E`
- **Elevated**: `#1C2D40`
- **Border**: `#273D54`

### Text
- **Primary**: `#EBF4FF`
- **Secondary**: `#6B9BBB`
- **Muted**: `#3A5A78`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for IP addresses, droplet names, commands)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 10px
- Badges: 4px
- Inputs: 6px

## Components

### Droplet Card
- Droplet name + OS icon + region
- vCPU / RAM / Disk specs in a row
- IP address in monospace
- Status dot: green = active, grey = off, yellow = provisioning

### Resource Usage Bar
- Label left, percentage right
- Bar proportional to usage
- Color: green < 60%, yellow 60-80%, red > 80%

### Region Badge
- Flag emoji + region name
- Surface bg, muted border

## Guardrails
- IP addresses always in monospace
- Resource specs (vCPU/RAM/disk) always shown together
- Status dots must always be visible
- Blue CTAs on dark surfaces only
- Keep pricing visible alongside specs — it's a key decision factor
