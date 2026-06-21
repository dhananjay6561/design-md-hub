# Hugging Face Design System

## Brand Overview
Hugging Face is the AI community platform — home to models, datasets, and Spaces. The visual identity is warm and community-driven — dark surfaces, golden-yellow as the hero color, and a playful-meets-technical aesthetic. UI feels like a collaborative developer hub for the ML ecosystem.

## Color Palette

### Primary
- Brand Yellow: `#FFD21E`
- Yellow Light: `#FFE566`
- Yellow Dark: `#C9A800`

### Backgrounds
- Base: `#0F0F0F`
- Surface: `#1A1A1A`
- Elevated: `#242424`
- Border: `#333333`

### Semantic
- Success: `#22C55E`
- Warning: `#FFD21E`
- Error: `#EF4444`
- Info: `#3B82F6`

### Text
- Primary: `#F5F5F5`
- Secondary: `#A0A0A0`
- Muted: `#666666`
- On-yellow: `#0F0F0F`

### Task Colors
- NLP: `#3B82F6`
- Vision: `#8B5CF6`
- Audio: `#EC4899`
- Multimodal: `#F97316`
- Tabular: `#22C55E`
- RL: `#EAB308`

## Typography

### Font Stack
- UI: `Source Sans Pro, Inter, sans-serif`
- Code: `JetBrains Mono, monospace`

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

### Model Card
- Model name + org prefix (`org/model-name`)
- Task badge (NLP / Vision / Audio etc.) with color
- Like count + download count in meta row
- Tags: framework (PyTorch, JAX), language, license
- Last updated in muted text
- Avatar/logo for org

### Dataset Card
- Same pattern as model card
- Size badge: rows count, file size
- Modality tag
- License badge

### Inference Playground
- Input textarea with placeholder
- Model selector dropdown
- Parameters panel: temperature, max tokens, top-p
- Run button: yellow filled
- Output area: monospace, streaming cursor

### Space Preview Card
- App screenshot thumbnail
- Space name + author
- Running/Building/Error status dot
- Like count
- SDK badge: Gradio / Streamlit / Static / Docker

### Download / Like Counter
- Number formatted with K/M suffix
- Download icon (arrow down) or heart icon
- Icon in muted, number in secondary text
- Yellow heart when liked

### Organization Avatar
- Circular crop
- Fallback: initials on yellow bg
- Size variants: 24px, 32px, 40px, 64px

### Tag Chip
- Small pill, outlined
- Framework: PyTorch (orange), TensorFlow (yellow), JAX (purple)
- License: MIT (green), Apache (blue), CC (grey)
- Language: flag emoji + language name

## Spacing

```
4px   — icon gap
8px   — tight padding
12px  — component padding sm
16px  — base padding
20px  — card padding
24px  — section gap
32px  — major section gap
48px  — page section spacing
```

## Elevation & Borders

- Border radius: 6px (tags, cards), 8px (modals, panels), 12px (feature cards)
- Border: `1px solid #333333`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.3)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.4)`

## Iconography
- Mix of line and filled icons
- Emoji used contextually (🤗 as brand mascot only)
- Download, heart, star, eye for community metrics
- Wand/sparkle for inference/generation actions

## Motion
- Transitions: 150ms ease
- Card hover: border color lighten
- Like button: heart pulse animation on click
- Inference output: typewriter streaming effect

## Guardrails

### DO
- Use yellow exclusively for primary actions and brand moments
- Show download + like counts on every model/dataset card
- Color-code task types consistently (NLP=blue, Vision=purple, etc.)
- Use `org/model-name` format for all model references
- Keep inference playground outputs in monospace

### DON'T
- Don't use emoji in data-dense tables or metric rows
- Don't use yellow text on white/light backgrounds
- Don't omit license information on model cards — it's critical
- Don't use bright colors for muted/secondary metadata
- Don't auto-run inference without user trigger
