# Terraform Design System

## Brand Overview
Terraform is HashiCorp's infrastructure-as-code tool. The design language reflects precision, structure, and infrastructure thinking — built on a deep purple with dark surfaces and monospace-heavy UI.

## Color Palette

### Primary
- **Purple**: `#844FBA` — primary brand, CTAs
- **Purple Dark**: `#6B3FA0` — hover, pressed
- **Purple Light**: `#A678D4` — highlights, icons

### Semantic
- **Apply / Success**: `#27AE60`
- **Plan / Info**: `#3498DB`
- **Destroy / Danger**: `#E74C3C`
- **Warning**: `#F39C12`
- **No-change**: `#7F8C8D`

### Terraform Plan Colors
- `+` Add: `#27AE60` — green
- `~` Change: `#F39C12` — yellow
- `-` Destroy: `#E74C3C` — red
- `=` No-op: `#7F8C8D` — grey

### Surfaces (Dark Mode)
- **Background**: `#1A1625`
- **Surface**: `#231E32`
- **Elevated**: `#2D2740`
- **Border**: `#3D3558`

### Text
- **Primary**: `#EDE8F8`
- **Secondary**: `#9A8FC0`
- **Muted**: `#5A5078`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for HCL code, resource addresses, plan output)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 10px
- Code blocks: 8px
- Inputs: 6px

## Components

### Plan Output Block
- Monospace, dark bg (#0D0A15)
- Color-coded add/change/destroy lines
- Summary line at bottom: X to add, Y to change, Z to destroy

### Resource Card
- Resource address in mono with provider prefix
- Status chip (planned / applied / tainted / destroyed)
- Attribute list in two-column key-value layout

### Provider Badge
- Provider name in mono (aws, google, azurerm)
- Purple tinted background

## Guardrails
- All resource addresses must be in monospace
- Plan diff colors (+/-/~) must match exactly — they're semantic
- Never abbreviate resource addresses
- Code blocks need sufficient contrast — minimum HCL syntax coloring
- Apply button should always confirm the plan count before proceeding
