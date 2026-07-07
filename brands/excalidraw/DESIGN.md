# Excalidraw — Design System

> A virtual whiteboard for sketching hand-drawn-feel diagrams.

Excalidraw is an open-source virtual whiteboard: you draw boxes, arrows, ellipses and text, and everything renders with a **hand-drawn, sketchy feel** (wobbly strokes, hachure fills) as if scrawled on a napkin. The identity is playful and disarmingly simple — a clean white (or near-black) canvas, floating rounded UI **islands**, one friendly **violet** (`#6965DB`), and hand-drawn typography (Excalifont/Virgil) throughout. Diagrams look intentionally imperfect, which makes them feel approachable and low-stakes. The magic is the **roughness**: nothing is a crisp vector; every shape looks sketched, and a *sloppiness* control dials how wobbly.

---

## Color

### Brand — one friendly violet
| Token | Hex | Usage |
|---|---|---|
| violet | `#6965DB` | Primary accent — active tool, buttons, links, selection |
| violet-deep | `#5B57D1` | Hover / pressed |
| indigo-ink | `#030064` | Active-tool icon on the light violet chip |
| selected | `#E0DFFF` | Selected tool / row background (light) |
| hover | `#F1F0FF` | Hover background (light) |

Violet is the single brand hue; it marks the active tool, selection and CTAs. Everything else is the neutral canvas or the sketch itself.

### Surfaces (light-first; a true dark canvas is a first-class mode)
| Token | Light | Dark | Usage |
|---|---|---|---|
| canvas | `#FFFFFF` | `#121212` | The infinite drawing canvas |
| panel | `#FFFFFF` | `#232329` | Floating UI islands (toolbar, panels) |
| subtle | `#F1F0FF` | `#2E2D3A` | Hover, wells |
| raised | `#ECECF4` | `#363442` | Rows, secondary fills |
| border | `#E9E9EE` | `#33333A` | Island hairlines / dividers |

### Text
| Token | Light | Dark |
|---|---|---|
| ink | `#1B1B1F` | `#E3E3E8` |
| secondary | `#6B6B75` | `#A8A8B3` |
| muted | `#9B9BA5` | `#6E6E78` |
| link | `#6965DB` | `#A8A5FF` |

### Sketch palette (the drawing — functional, not brand chrome)
| Role | Stroke | Background fill |
|---|---|---|
| ink | `#1E1E1E` | transparent |
| red | `#E03131` | `#FFC9C9` |
| green | `#2F9E44` | `#B2F2BB` |
| blue | `#1971C2` | `#A5D8FF` |
| orange | `#F08C00` | `#FFEC99` |

These are Excalidraw's default stroke + background swatches. Fills are drawn as **hachure** (parallel sketch lines), **cross-hatch**, or **solid**.

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Hand-drawn — sketch text, labels, display | **Excalifont** (the successor to *Virgil*) | The soul of the brand: neat, monoline, wobbly hand-print. Used for canvas text, diagram labels and playful headings. Self-hosted but **CORS-locked** → documented fallback **≈ Shantell Sans** (Google), a modern hand-drawn face with the same casual sketch feel. |
| UI / body | **Assistant** (`400 / 500 / 600 / 700`) | Excalidraw's real interface font — a clean, quiet humanist sans for menus, panels and body. Available on Google Fonts. |
| Wordmark | **Nunito** (`800`) | The chunky, rounded `EXCALIDRAW` lockup. |

Rule of thumb: **hand-drawn font for the drawing and playful copy; Assistant for the UI.** Keep the interface text crisp and legible so the sketchiness stays where it belongs — on the canvas.

---

## Shape, spacing & motion

- **Radius:** UI islands & panels `12px`, buttons/tool tiles `10px`, swatches `6px`, pills `9999px`. On the canvas, shapes have a **round-edges** option (sketchy rounded corners) vs sharp.
- **Spacing:** the app is a full-bleed **infinite canvas** with **floating islands** — a centered top toolbar, a left properties panel when something's selected, zoom bottom-left. Chrome floats; the canvas is king.
- **Elevation:** islands rest on a soft shadow (`0 2px 12px rgba(0,0,0,.10)`) over the canvas; selection is a dashed violet bounding box with small square handles.
- **Motion:** minimal and functional — tools highlight on pick, selection snaps, panels appear on select. The signature motion is **re-roughening**: changing *sloppiness* (Architect → Artist → Cartoonist) re-draws every shape with more wobble. **Deterministic** — a seeded roughness, so a given drawing always looks the same.

---

## Components

- **Logo** — a violet sketch-pencil mark + the rounded `EXCALIDRAW` wordmark (Nunito).
- **Toolbar island** — a floating, rounded, centered bar of tools (selection, rectangle, diamond, ellipse, arrow, line, draw, text, image, eraser) with number shortcuts; the active tool sits on a `#E0DFFF` violet chip.
- **Hand-drawn shapes** — rectangles, ellipses, diamonds, arrows and freedraw rendered with **rough**, double-pass wobbly strokes and hachure fills. This *is* the product.
- **Properties panel** — a left-floating island shown on selection: Stroke color, Background, Fill style (hachure / cross-hatch / solid), Stroke width, Sloppiness (Architect / Artist / Cartoonist), Edges (sharp / round).
- **Selection** — dashed violet bounding box + square handles.
- **Buttons** — violet primary (Share), quiet ghost/icon buttons in the islands.

---

## Guardrails

**Do**
- Render diagram shapes with the **hand-drawn, rough** look — wobbly double strokes and hachure fills; imperfect on purpose.
- Keep one friendly **violet** (`#6965DB`) for active tool, selection and CTAs; let the canvas stay neutral.
- Use **hand-drawn type** (Excalifont ≈ Shantell Sans) for canvas text & playful copy; keep **UI text in Assistant** and legible.
- Float the UI as **rounded islands** over a full-bleed canvas; support a true dark canvas.
- Offer the **sloppiness** control — the roughness is the whole point; keep it deterministic per drawing.

**Don't**
- Render shapes as crisp, precise vectors — that kills the hand-drawn identity.
- Introduce a second brand hue; violet is the only chrome accent (sketch stroke colors are content, not brand).
- Set dense UI or long body copy in the hand-drawn font — it belongs on the canvas.
- Crowd the canvas with heavy chrome — the islands float; the drawing leads.
- Make the violet loud or gradient-y — it's one flat, friendly indigo-violet.
