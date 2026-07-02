# Postman Design System

## Brand Overview

Postman is "the world's leading API platform" — now "the AI-native API Platform." The identity is warm and confident: the iconic **Postman orange `#FF6C37`** and the Postmanaut planet mark, near-black ink `#212121`, and a clean neutral canvas. The product's soul is the **request builder** — a method, a URL, Send, and a color-coded response — and HTTP-method color (GET green, POST amber, PUT blue, PATCH purple, DELETE red) is a first-class part of the system.

Light-first marketing; the app itself ships light and dark.

> Verified live from postman.com (2026). Orange `#FF6C37` confirmed 96× in the production CSS. Fonts are Degular (display) + Inter + IBM Plex Mono via next/font (Degular self-hosted, not CORS-open) — so this reference uses **Figtree** (≈ Degular) + **Inter** + the real **IBM Plex Mono**.

## Color Palette

### Primary
- **Orange**: `#FF6C37` — brand, Send, the mark, primary CTAs
- **Orange Hover**: `#EF5B25` — hover/pressed
- **Ink**: `#212121` — headings, body, dark UI chrome
- **Dark Plum**: `#140B1E` — deep brand dark, tinted dark surfaces

### HTTP methods (semantic — the core)
- **GET**: `#0CBB52` green · **POST**: `#B07800` amber · **PUT**: `#0265D2` blue · **PATCH**: `#7C3FBF` purple · **DELETE**: `#D92D20` red

### Neutrals
- **Grey**: `#5C5C5C` · **Muted**: `#6B6B6B`
- **Border**: `#E6E6E6` · **Fill**: `#EFEFEF` · **Off-white**: `#F9F8F7` · **White**: `#FFFFFF`

### Response syntax
- **Key**: `#C15B28` · **String**: `#0A8F40` · **Number**: `#0265D2` · **Boolean/null**: `#7C3FBF`

## Typography

Three fonts, one role each. Degular is CORS-locked, so this reference approximates it; IBM Plex Mono is the real, Google-Fonts-hosted face.

- **Display — Figtree** (≈ Degular) (500/600/700): hero, page + section headings
- **UI / Body — Inter** (400/500/600): all body, labels, nav, buttons, UI
- **Mono — IBM Plex Mono** (400/500): URLs, JSON, code, method labels

### Scale
| Token | Size | Weight | Font | Use |
|-------|------|--------|------|-----|
| display | 54px | 700 | Figtree | Hero |
| h1 | 32px | 700 | Figtree | Page title |
| h2 | 22px | 600 | Figtree | Section heading |
| body-lg | 17px | 400 | Inter | Lead paragraph |
| body | 14px | 400 | Inter | Default UI |
| small | 12px | 400 | Inter | Metadata |
| mono | 12.5px | 400 | IBM Plex Mono | URLs, JSON |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons / inputs: 6px
- Cards / panels: 8px
- Method / status pills: 4px
- Base: 4px

## Components

### Button
- **Primary**: orange `#FF6C37`, white text ("Send"). Labels: `Send`, `Sign Up for Free`, `Save`
- **Secondary**: transparent, `--border-strong` outline. Labels: `Import`, `Docs`
- The Send button is the hero action — always orange

### Method tag
Bold mono label colored by verb: GET green, POST amber, PUT blue, PATCH purple, DELETE red. Appears in the request bar and on every saved request.

### Status pill
`200 OK` green, `201 Created` green, `204 No Content` grey-green, `4xx/5xx` red — beside response time and size.

### Response viewer
Monospace JSON with syntax highlighting (key / string / number / boolean colors), status + time + size header.

## Signature — API Request Builder

Postman's defining view: `[method] [URL] [Send]`. Pick a verb — the method tag recolors — enter the endpoint, and **Send** runs it: a status pill (`200 OK` / `201 Created` / `204 No Content`), response time, size, and a syntax-highlighted JSON body appear. Each method returns its own realistic response against `api.getpostman.com`. Deterministic timings, real API shapes.

## Guardrails

**DO**
- Use orange `#FF6C37` for the Send button and primary CTAs — it is the brand
- Color HTTP methods semantically: GET green, POST amber, PUT blue, PATCH purple, DELETE red
- Set URLs, JSON, and method labels in IBM Plex Mono — the request/response is code
- Set headings in Degular (≈ Figtree), UI in Inter
- Show status + time + size on every response — that triad is the Postman readout

**DON'T**
- Don't recolor the Postmanaut mark — it's fixed orange + white
- Don't use a method's color for a different verb — GET is green, never orange
- Don't set JSON or URLs in a sans — mono carries the payload
- Don't render response bodies without a status pill — status is always shown
- Don't fabricate responses — use realistic API shapes and correct status codes
</content>
