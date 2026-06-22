# Replicate Design System

## Brand Overview
Replicate is the cloud platform for running AI models via API. The visual identity is minimal and technical — near-black backgrounds, electric blue accents, and code-first layouts. UI feels like a precision tool for ML engineers: clean, fast, and unapologetic about complexity.

## Color Palette

### Primary
- Brand Blue: `#0066FF`
- Blue Light: `#4D94FF`
- Blue Dark: `#0047B3`

### Backgrounds
- Base: `#0D0D0D`
- Surface: `#161616`
- Elevated: `#1E1E1E`
- Border: `#2A2A2A`

### Semantic
- Success: `#22C55E`
- Warning: `#F59E0B`
- Error: `#EF4444`
- Processing: `#0066FF`

### Text
- Primary: `#F5F5F5`
- Secondary: `#A0A0A0`
- Muted: `#666666`
- On-blue: `#FFFFFF`

### Prediction Status
- Starting: `#666666`
- Processing: `#0066FF`
- Succeeded: `#22C55E`
- Failed: `#EF4444`
- Canceled: `#94A3B8`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
- Code/IDs: `JetBrains Mono, monospace`

### Scale
- xs: 11px / 1.5
- sm: 13px / 1.5
- base: 14px / 1.6
- md: 16px / 1.5
- lg: 18px / 1.4
- xl: 22px / 1.3
- 2xl: 28px / 1.2

### Weights
- Regular: 400
- Medium: 500
- Semibold: 600
- Bold: 700

## Components

### Prediction Card
- Model name + version in mono
- Input params shown as key-value
- Output preview: image thumbnail or text block
- Status badge with timing (e.g. "Succeeded · 3.2s")
- Prediction ID in muted mono

### Model Card
- Model name + owner (`owner/model-name`)
- Cover image or gradient placeholder
- Run count badge (e.g. "1.2M runs")
- Description truncated to 2 lines
- Tags: task type, hardware, license

### API Playground
- Input fields generated from model schema
- Run button: blue filled, full-width
- Output area: image or text with copy button
- Cost estimate in muted text below Run

### Version List
- Version hash in mono, truncated
- Created date
- Run count
- Diff indicator if schema changed

### Hardware Badges
- CPU: grey
- T4: green
- A40: blue
- A100: purple
- H100: orange

## Spacing

```
4px   — tight inline gaps
8px   — component padding xs
12px  — component padding sm
16px  — base padding
20px  — card padding
24px  — section gap
32px  — major section gap
48px  — page section spacing
```

## Elevation & Borders

- Border radius: 4px (badges, mono tags), 6px (cards, inputs), 8px (modals)
- Border: `1px solid #2A2A2A`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.5)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.6)`

## Iconography
- Line icons, 16px and 20px
- Minimal set: run, model, version, API, hardware
- No decorative icons

## Motion
- Transitions: 150ms ease
- Prediction processing: pulsing blue border
- Output reveal: fade-in 200ms
- Status change: instant (no animation for status)

## Guardrails

### DO
- Use `owner/model-name` format consistently
- Show prediction timing always (speed is a key value prop)
- Use mono for all IDs, hashes, and version strings
- Blue only for the primary Run/Submit action
- Show cost/time estimates before running

### DON'T
- Don't hide model versions — they're critical for reproducibility
- Don't animate prediction status changes — instant feedback only
- Don't use rounded corners > 8px — the aesthetic is technical, not playful
- Don't omit hardware type — it affects both cost and latency
- Don't truncate output without a "show more" affordance
