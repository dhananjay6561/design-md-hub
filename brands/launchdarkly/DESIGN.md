# LaunchDarkly Design System

## Brand Overview
LaunchDarkly is a feature flag management platform. The brand is technical, confident, and precise — built on a deep navy with a vivid blue accent, reflecting controlled, deliberate software releases.

## Color Palette

### Primary
- **Blue**: `#405BFF` — primary brand, CTAs, active flags
- **Blue Hover**: `#3048E8` — pressed states
- **Blue Light**: `#6B82FF` — highlights

### Flag States
- **On**: `#1DB954` — green, flag enabled
- **Off**: `#6B7280` — grey, flag disabled
- **Targeting On**: `#405BFF` — blue, with rules active

### Semantic
- **Success**: `#1DB954`
- **Warning**: `#F59E0B`
- **Error**: `#EF4444`

### Surfaces (Dark Mode)
- **Background**: `#0A0E1A`
- **Surface**: `#111827`
- **Elevated**: `#1A2438`
- **Border**: `#243250`

### Text
- **Primary**: `#F0F4FF`
- **Secondary**: `#8899CC`
- **Muted**: `#445577`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for flag keys, variation values, targeting rules)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 10px
- Toggle: 9999px (pill)
- Inputs: 6px

## Components

### Flag Toggle
- Large pill toggle: green = on, grey = off
- Flag key in monospace below name
- Targeting indicator when rules are active

### Flag Row
- Toggle left, flag name + key, environment badges right
- Tags inline with name
- Last modified timestamp muted right

### Targeting Rule
- Condition blocks with operator (if/and/else)
- Variation served shown as colored chip
- Percentage rollout bar

### Environment Badge
- Short env name (Production/Staging/Dev)
- Color-coded per environment

## Guardrails
- Flag keys always in monospace — they're identifiers
- Toggle state must be unmistakable — on/off must be obvious at a glance
- Never show flag keys truncated
- Production environment always visually distinct (often red-bordered)
- Targeting rules need clear if/then structure
