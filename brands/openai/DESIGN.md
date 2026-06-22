# OpenAI Design System

## Brand Overview
OpenAI is the leading AI research company and API provider. The visual identity is minimal and confident — near-black backgrounds, clean white as the primary expression, and a precision-engineered aesthetic. UI communicates cutting-edge capability through restraint: no noise, no decoration, just the model and the developer.

## Color Palette

### Primary
- Brand White: `#FFFFFF`
- Brand Green: `#10A37F`
- Green Light: `#19C37D`
- Green Dark: `#0D8C6C`

### Backgrounds
- Base: `#0D0D0D`
- Surface: `#141414`
- Elevated: `#1A1A1A`
- Border: `#2A2A2A`

### Semantic
- Success: `#10A37F`
- Warning: `#F59E0B`
- Error: `#EF4444`
- Info: `#6B7280`

### Text
- Primary: `#ECECEC`
- Secondary: `#8E8EA0`
- Muted: `#565869`
- On-green: `#FFFFFF`

### Model Colors
- GPT-4o: `#10A37F`
- GPT-4: `#AB68FF`
- GPT-3.5: `#19C37D`
- DALL·E: `#F59E0B`
- Whisper: `#60A5FA`
- TTS: `#FB923C`

## Typography

### Font Stack
- UI: `Söhne, Inter, system-ui, sans-serif`
- Code: `Söhne Mono, JetBrains Mono, monospace`

### Scale
- xs: 11px / 1.5
- sm: 13px / 1.6
- base: 14px / 1.6
- md: 16px / 1.5
- lg: 18px / 1.5
- xl: 22px / 1.3
- 2xl: 28px / 1.2

### Weights
- Regular: 400
- Medium: 500
- Semibold: 600
- Bold: 700

## Components

### Playground Message
- User: right-aligned, grey bubble
- Assistant: left-aligned, surface bg, green left accent line
- System: top-pinned, muted text with tag
- Streaming: blinking cursor at end of output

### Model Selector
- Dropdown with model name + capability tags
- Model icon/color dot beside name
- Context window shown in muted text
- Capability badges: Vision, Functions, JSON mode

### Token Counter
- Input / Output / Total shown as three columns
- Progress bar filling toward context limit
- Color: green → orange → red as limit approaches

### API Key Row
- Key name + masked value (`sk-...XXXX`)
- Created date + last used
- Copy / Delete actions
- Usage stats sparkline

### Usage Dashboard
- Bar chart per day: input tokens (light) / output tokens (dark)
- Model breakdown as stacked or grouped bars
- Cost estimate below chart
- Date range picker: 7d / 30d / 90d

### Response Format Toggle
- Text / JSON object / JSON schema tabs
- JSON schema: inline editor with type validation
- Active: green underline tab

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
- Border radius: 4px (tags, pills), 6px (inputs, cards), 12px (chat bubbles, modals)
- Border: `1px solid #2A2A2A`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.4)`
- Shadow md: `0 4px 20px rgba(0,0,0,0.5)`

## Guardrails

### DO
- Use green exclusively for the brand accent and success states
- Keep the UI minimal — the model output is the hero
- Show token counts always — developers are cost-conscious
- Use monospace for all prompts, completions, and code
- Show model name and version on every completion context

### DON'T
- Don't use color for decoration — every color must carry meaning
- Don't truncate streaming output — show it as it arrives
- Don't omit finish_reason — it tells devs why the model stopped
- Don't round token costs — show 4 decimal places minimum
- Don't mix model colors in a single response thread
