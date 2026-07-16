# Linear — Design System

> The system for product development.
> Purpose-built for planning and building products with AI agents.

Linear's identity is **dark-first, dense, and precise** — information density over whitespace, speed over decoration, keyboard-first. The aesthetic is technical and minimal, almost brutalist in its restraint, with a single **indigo-purple** accent as the only color statement. Color otherwise appears *only* as issue status, priority, and labels.

Dark is the primary experience; light is fully supported.

---

## Colors

### Accent (the one color statement)
| Token | Hex (dark) | Hex (light) | Usage |
|-------|------------|-------------|-------|
| `accent` | `#7170FF` | `#5E6AD2` | Selection, focus, primary button, active — **brightens on dark** |
| `accent-hover` | `#828FFF` | `#8989F0` | Hover on accent |
| `accent-tint` | `#18182F` | `#F1F1FF` | Subtle accent backgrounds (selected row) |
| `brand` | `#5E6AD2` | `#5E6AD2` | The classic "Linear plurple" brand mark |

> Re-audit note: Linear's accent **brightened to `#7170FF` on dark** (the old `#5E6AD2` is now the light-mode / brand value). Use the bright value on the dark app.

### Surfaces
| Token | Hex (dark) | Hex (light) | Usage |
|-------|------------|-------------|-------|
| `bg-primary` | `#08090A` | `#FFFFFF` | App background |
| `bg-secondary` | `#1C1C1F` | `#F9F8F9` | Panels, sidebar |
| `bg-tertiary` | `#232326` | `#F4F2F4` | Cards, dropdowns, rows |
| `bg-quaternary` | `#28282C` | `#EEEDEF` | Hover / raised |
| `bg-panel` | `#0F1011` | `#FFFFFF` | Marketing panels |
| `border` | `#23252A` | `#E9E8EA` | Dividers, subtle |
| `border-strong` | `#34343A` | `#E4E2E4` | Inputs, emphasized |

### Text
| Token | Hex (dark) | Hex (light) | Usage |
|-------|------------|-------------|-------|
| `fg-primary` | `#F7F8F8` | `#282A2F` | Primary |
| `fg-secondary` | `#D0D6E0` | `#3C4149` | Strong secondary |
| `fg-tertiary` | `#8A8F98` | `#6F6E77` | Metadata, muted |

### Status / priority / label spectrum (the only other color)
| Name | Hex | | Name | Hex |
|------|-----|--|------|-----|
| indigo (in-progress/done) | `#5E6AD2` | | orange | `#FC7840` |
| yellow (started) | `#F0BF00` | | red (urgent) | `#EB5757` |
| green (done) | `#27A644` | | teal | `#00B8CC` |
| blue | `#4EA7FC` | | grey (backlog/todo) | `#8A8F98` |

---

## Typography

- **Inter Variable** — the whole UI. Self-hosted at `static.linear.app/fonts/InterVariable.woff2`, **CORS-open** (`access-control-allow-origin: *`) — used directly. Linear enables the OpenType features **`cv01` + `ss03`** (`font-feature-settings:"cv01","ss03"`) — the detail that makes text look "Linear" (single-storey a, rounded g). Optical sizing `opsz auto`.
- **Berkeley Mono** — code, issue IDs, shortcuts (proprietary → documented ≈ **JetBrains Mono**, Google-hosted).

| Scale | Size | Weight | Notes |
|-------|------|--------|-------|
| heading-lg | 20px | 600 | `-0.02em` |
| heading | 16px | 600 | `-0.02em` |
| body | 14px | 400 | `-0.01em` |
| body-sm | 13px | 400 | list rows |
| label | 12px | 500 | badges, meta |

Letter-spacing `-0.01em` on body, `-0.02em` on headings. Tight, dense.

---

## Logo

The real **Linear wordmark** (mark + "Linear", `viewBox 0 0 400 100`, single path, `fill="currentColor"`), pulled verbatim from the live nav and themed via `--logo` (off-white on dark, near-black on light).

---

## Signature component — Issues (List ↔ Board) + ⌘K

Linear's two most iconic patterns in one frame:

- **Issues view** with a **List ↔ Board** toggle. List groups issues by status (In Progress / Todo / Backlog) with a status glyph + count per group; Board is a Kanban of the same issues in status columns.
- Each issue row/card = **priority glyph** (Linear's signal-bar icons: urgent/high/med/low/none) + **status glyph** (the circular progress rings: backlog dashed, todo empty, started yellow pie, done indigo check, canceled) + `ENG-###` id (mono) + title + label chips + assignee avatar.
- Click a status glyph to **cycle status** — the issue moves between groups (list) or columns (board), optimistically and instantly (no spinner — Linear's speed).
- **⌘K** opens the command palette overlay — borderless input + result rows with shortcut hints — the keyboard-first heart of Linear.

Deterministic — fixed issues, index-driven cycling, no `Math.random`.

---

## Guardrails

**Do**
- Default to dark; keep the UI dense — whitespace is earned, not default.
- Use the **bright `#7170FF`** accent on dark (not the old `#5E6AD2`); reserve it for selection, focus, and active only.
- Let color otherwise mean something — status, priority, label — never decoration.
- Set the UI in Inter with `cv01`+`ss03`; make hover transitions instant (~100ms).

**Don't**
- Use rounded corners larger than ~8px, or add decorative gradients, illustrations, or hero images.
- Use the accent as a fill for large areas — it's punctuation.
- Add loading spinners where optimistic UI is possible; prefer inline/toast over modals for confirmations.
- Use cold-neutral text on dark — Linear's greys are subtly cool but calibrated (`#8A8F98`), don't invent tints.
