# Hugging Face Design System

## Brand Overview

Hugging Face is "the AI community building the future" — the platform where the machine
learning community collaborates on models, datasets, and applications. The identity is warm
and playful on top of a precise, developer-dense product: the golden 🤗 Hugging Face emoji is
the whole brand, everything else is a neutral Tailwind-gray canvas that lets model cards,
tags, and metrics breathe. Light-first — the homepage and hub are white.

> "We're on a journey to advance and democratize artificial intelligence through open source
> and open science."

## Typography

- **Source Sans Pro** — all UI, body, headings, nav, buttons (Google Fonts: *Source Sans 3*).
- **IBM Plex Mono** — code, model IDs, tensors, CLI, metadata (Google Fonts).
- **Charter** — serif reserved for long-form prose (blog / papers); not a UI font.

Roles are strict: Source Sans for everything interface, IBM Plex Mono for anything a machine
would read (model ids like `bert-base-uncased`, shapes, token counts).

## Color Palette

### Primary — the 🤗 mark
- Brand Yellow: `#FFD21E` (the face)
- Orange: `#FF9D0B` (outline, hands)
- Face Dark: `#3A3B45` (eyes, mouth outline)
- Red: `#FF323D` (mouth, blush)

### Accent & Category (from the gradient set)
- Blue: `#3080FF` (links, interactive)
- Green: `#21DE75`
- Purple: `#861FFF`
- Pink: `#FF3270`

### Surfaces — Light
- Page: `#FFFFFF`
- Surface: `#F9FAFB` (gray-50 — cards, sidebar)
- Elevated: `#F3F4F6` (gray-100)
- Border: `#E5E7EB` (gray-200)

### Surfaces — Dark (real Tailwind navy-grays)
- Page: `#030712` (gray-950)
- Surface: `#101828` (gray-900)
- Elevated: `#1E2939` (gray-800)
- Border: `#364153` (gray-700)

### Text
- Primary (light `#101828` / dark `#F3F4F6`)
- Secondary: `#6A7282` (gray-500)
- Muted: `#99A1AF` (gray-400)

### Semantic
- Success: `#21DE75`
- Error: `#FB2C36`
- Warning: `#FF9D0B`

## Logo

The official **Hugging Face emoji** (🤗) — a smiling face with open hands. viewBox `0 0 95 88`,
seven fixed-color paths: face `#FFD21E`, outline/hands `#FF9D0B`, eyes + mouth outline `#3A3B45`,
mouth/blush `#FF323D`. The mark is **always full-color** — never flattened to a single fill or
recolored. It carries the brand on its own; no separate wordmark is required beside it.

## Signature Component — Model page & Inference Widget

A model page mirroring `huggingface.co/bert-base-uncased`: the 🤗 mark, model id in mono, a
**Fill-Mask** task pill, and like/download counts — above the **Hosted inference API** widget.
The widget takes a masked sentence (`The goal of life is [MASK].`), and **Compute** streams the
ranked token predictions with confidence scores and filling score bars — the single most
recognizable Hugging Face interaction.

## Guardrails

**DO**
- Keep the 🤗 mark full-color and unmodified — it is the entire brand.
- Keep the canvas neutral gray so model cards, tags, and metrics lead.
- Use IBM Plex Mono for every model id, shape, count, and code token.
- Use colored pills for tasks/libraries; keep them legible in both themes.
- Reserve yellow/orange for the mark and highlights, not large fills.

**DON'T**
- Don't flatten, recolor, or add effects to the Hugging Face emoji.
- Don't make yellow a page background — it's an accent, not a surface.
- Don't invent dark surfaces; anchor on the real Tailwind navy-gray scale.
- Don't set model ids or metrics in a proportional font.
- Don't crowd out the inference widget — it's the core value moment.
