# Netlify Design System

## Brand Overview
Netlify is a cloud platform for web deployment and serverless functions. The brand is built around speed, simplicity, and developer joy — reflected in a clean teal palette with dark, focused surfaces.

## Color Palette

### Primary
- **Teal**: `#00C7B7` — primary brand color, CTAs, active states
- **Teal Dark**: `#009E91` — hover, pressed states
- **Teal Light**: `#33D6C9` — highlights, focus rings

### Semantic
- **Success**: `#28B487`
- **Warning**: `#FFCC00`
- **Error**: `#FF4949`
- **Info**: `#0097FF`

### Surfaces (Dark Mode)
- **Background**: `#0E1E25`
- **Surface**: `#1B2E36`
- **Elevated**: `#243D48`
- **Border**: `#2E4D5C`

### Text
- **Primary**: `#EEF5F7`
- **Secondary**: `#7FA8B8`
- **Muted**: `#4A7080`

## Typography

- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for deploy logs, branch names, hashes)

### Scale
| Token | Size | Weight | Use |
|-------|------|--------|-----|
| display | 36px | 700 | Hero |
| h1 | 26px | 700 | Page title |
| h2 | 20px | 600 | Section |
| body | 14px | 400 | Default |
| small | 12px | 400 | Meta |
| code | 13px | 400 mono | Logs, hashes |

## Spacing
4px base grid — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons: 6px
- Cards: 10px
- Badges: 4px
- Inputs: 6px

## Components

### Deploy Card
- Status dot: green (success), yellow (building), red (failed)
- Branch label in mono with `#` prefix
- Commit hash in muted mono
- Timestamp right-aligned

### Branch Badge
- Background: teal at 12% opacity
- Text: teal
- Border: teal at 30% opacity

### Log Output
- Dark bg `#060F14`
- Monospace text, muted color
- Green for success lines, red for errors

### Site Status Banner
- Full-width, borderless
- Color-coded left border

## Guardrails
- Always monospace for hashes, deploy IDs, branch names
- Deploy status must be immediately visible — lead with the dot, not text
- Teal on dark only — avoid teal on light without sufficient contrast check
- No gradients on functional UI elements
- Keep deploy card information density high but scannable
