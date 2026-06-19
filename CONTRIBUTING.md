# Contributing to design-md-hub

Thank you for helping grow this collection!

## How to Add a DESIGN.md

1. **Fork** this repository
2. **Create** a new file at `design-md/<brand-name>.md` (lowercase, hyphenated)
3. **Follow** the template below
4. **Open a Pull Request** with the title `Add: <Brand Name> DESIGN.md`

## DESIGN.md Template

```markdown
# <Brand Name> DESIGN.md

> One-line description of the brand's visual identity.

## Overview

Brief summary of the design philosophy.

## Colors

| Token | Hex | Usage |
|-------|-----|-------|
| primary | #000000 | Primary actions, CTAs |
| background | #ffffff | Page background |

## Typography

- **Font family**: ...
- **Heading scale**: ...
- **Body size**: ...
- **Line height**: ...

## Spacing

Base unit: `4px`

| Token | Value | Usage |
|-------|-------|-------|
| xs | 4px | Tight gaps |
| sm | 8px | Component padding |
| md | 16px | Section spacing |
| lg | 32px | Layout gaps |

## Border Radius

| Token | Value |
|-------|-------|
| sm | 4px |
| md | 8px |
| full | 9999px |

## Shadows

...

## Components

### Button
...

### Card
...

### Input
...

## Layout

...

## Tone & Guardrails

- DO: ...
- DON'T: ...
```

## Quality Bar

- Colors must include hex values
- Typography must name the actual font(s) used
- At least 3 core components documented
- Guardrails section is required
- No placeholder text — every field should have real values

## Naming Convention

| Brand | Filename |
|-------|----------|
| OpenAI | `openai.md` |
| Hugging Face | `hugging-face.md` |
| GitHub Copilot | `github-copilot.md` |
