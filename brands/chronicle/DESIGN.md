# Chronicle — Design System

> AI-powered presentations.

Chronicle is a modern presentation tool — an AI-assisted deck builder for professional, interactive slides. Its identity is deliberately **monochrome and editorial**: a warm off-white canvas, near-black ink, and one confident typeface — ABC Dinamo's **Diatype** — set large with tight negative tracking. The app chrome carries no brand color at all; the **color comes from the decks** — each slide theme (lime, cream, cobalt, orange, charcoal, white) paints the content while the interface stays quiet black-on-paper.

The result reads like a well-set magazine: restrained, typographic, and fast. The signature moment is switching a deck's **theme** and watching every slide re-skin instantly.

---

## Color

### Brand — monochrome ink
Chronicle's interface has **no accent color**. Identity is the ink scale on warm paper; the CTA is a solid black button.

| Token | Hex | Usage |
|---|---|---|
| ink | `#050505` | Primary text, logo, solid buttons (`solid-12`) |
| ink-800 | `#212121` | Strong text, headings on paper |
| ink-600 | `#484848` | Secondary text |
| ink-400 | `#7C7C7C` | Muted / captions |
| paper | `#F3F3F3` | Warm off-white canvas (`--color-bg`) |
| paper-line | `#E2E2E2` | Borders, hairlines |

### Deck themes (the color lives here)
Each slide theme is a `background + ink` pair; content is tonal within it. These skin the **slides**, never the chrome.

| Theme | Background | Ink | 
|---|---|---|
| Lime | `#E9FF66` | `#0A0A0A` |
| Cream | `#F1ECE1` | `#1A1A1A` |
| Cobalt | `#1B34C9` | `#FFFFFF` |
| Orange | `#FF6A2B` | `#1A1109` |
| Charcoal | `#191919` | `#F3F3F3` |
| White | `#FFFFFF` | `#0A0A0A` |

### Surfaces & text (chrome, dark-mode supported)
| Token | Light | Dark |
|---|---|---|
| canvas | `#F3F3F3` | `#0A0A0A` |
| panel | `#FFFFFF` | `#151515` |
| subtle | `#EAEAEA` | `#1C1C1C` |
| border | `#E2E2E2` | `#2A2A2A` |
| text primary | `#050505` | `#F3F3F3` |
| text secondary | `#484848` | `#B3B3B3` |
| text muted | `#7C7C7C` | `#7C7C7C` |

---

## Typography

Chronicle is a **single-typeface system** — Diatype does everything.

| Role | Family | Notes |
|---|---|---|
| Display | **Diatype** (`500`) | Oversized headlines with tight `-0.03em` tracking (`AI Powered Presentations.`). Self-hosted (Next font), CORS-open. |
| Headings | **Diatype** (`400 / 500`) | Slide titles & section heads, `-0.02em` tracking, generous size (`clamp` up to ~5rem on the site). |
| UI / body | **Diatype** (`400`) | Interface, body copy, slide content, labels. Fallback: Inter → system. |
| Emphasis | **Diatype** (`700`) + italic | Bold and true italics for pull quotes and callouts. |

Scale: display 44–64px (Diatype 500), slide title 30px, body 15px, caption/label 11px uppercase (`.06em`). Buttons: 14px / weight 500. No monospace — Chronicle stays in Diatype throughout.

---

## Shape, spacing & motion

- **Radius:** buttons & inputs `4px` (tight, editorial), thumbnails `6px`, slide canvas & panels `10px`, theme swatches `8px`. Small radii — this is a typographic tool, not a soft consumer app.
- **Spacing:** 8px grid; slides are 16:9; the thumbnail rail, canvas and theme row read as one calm workspace.
- **Elevation:** slides float on a single soft shadow; chrome is flat with hairline borders. The active slide/thumb gets an **ink ring**, not a colored one.
- **Motion:** quick and clean. Switching a deck **theme** re-skins every slide at once (`~0.2s` background/ink transition); selecting a thumbnail swaps the canvas content instantly. Deterministic — nothing random.

---

## Components

- **Slide canvas** — a 16:9 surface rendered in the active deck theme. Layouts: title, stats, chart, quote — content is tonal (ink at varying opacity), never multi-hued.
- **Thumbnail rail** — vertical list of numbered slide minis in the current theme; the active one carries an ink ring.
- **Theme switcher** — a row of `background/ink` swatches; clicking one re-skins the whole deck. This is the signature interaction.
- **Logo** — the ✦ four-point sparkle mark + `Chronicle` wordmark, in ink.
- **Buttons** — solid **ink** primary (`Present`, white text, radius 4px, weight 500); outline secondary with a paper border; plain/ghost for toolbar actions.

---

## Guardrails

**Do**
- Keep the interface **monochrome** — warm paper, near-black ink, one black button. No accent hue in the chrome.
- Let **deck themes** carry all the color, applied only to slide content.
- Set everything in **Diatype**; go large with tight negative tracking for display.
- Keep radii small (`4px` buttons) and borders hairline — editorial, not soft.
- Make theming the hero: switching a deck theme should re-skin every slide at once.
- Use an **ink ring** for selection, never a colored highlight.

**Don't**
- Introduce a brand accent color — Chronicle's chrome is black-on-paper; color belongs to the decks.
- Mix in a second typeface or a monospace — Diatype is the whole system.
- Use large pill radii or heavy drop shadows on the chrome — keep it flat and typographic.
- Render slide content in many hues at once — each theme is a tonal `background/ink` pair.
- Set the canvas on a cold pure-white app background — the brand paper is warm `#F3F3F3`.
