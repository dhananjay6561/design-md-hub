# Zed — Design System

> Your last next editor.

Zed is a high-performance, multiplayer code editor from the creators of Atom and Tree-sitter — written from scratch in Rust to leverage multiple CPU cores and the GPU. Its identity is a **warm graph-paper canvas** with one confident **cobalt blue** accent and an editorial, IBM-Plex-driven voice: a serif *italic* headline over a crisp mono editor.

The look is engineered, not decorative — a light paper marketing surface, a One-dark editor, and blue reserved for the moments that matter (the headline, the primary action, an active state).

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| accent-blue | `#1348DC` | Primary accent — headline (light), primary button, links, active state |
| blue-bright | `#3080FF` | Secondary blue / hover |
| blue-300 | `#90C5FF` | Dark-mode headline & accent (blue is lightened on the dark canvas) |
| dithering | `#0751CF` | Deep-blue motif — the marketing dithering / gradient wash |
| motif-blue | `#1E69F6` | Ambient motif accent |

### Surfaces (light-first — the marketing canvas is warm paper)
| Token | Light | Dark | Usage |
|---|---|---|---|
| canvas | `#F7F7F2` | `#121417` | App background (warm paper / near-black nav) |
| panel | `#FFFFFF` | `#1A1D21` | Cards, panels |
| raised | `#EFF1F0` | `#22262B` | Hover / secondary surface |
| border | `#DADDE2` | `#27272A` | Hairlines |
| border-strong | `#C4C8CE` | `#3A3E44` | Inputs, stronger dividers |

### Text
| Token | Light | Dark |
|---|---|---|
| primary | `#101828` | `#F7F7F2` |
| secondary | `#4A5565` | `#D1D5DC` |
| faint (offgray) | `#727A89` | `#727A89` |

`offgray` `#727A89` is a real Zed token used identically in both themes for meta text.

### Editor — the "One" theme (always dark, ships with Zed)
| Token | Hex | Usage |
|---|---|---|
| editor-bg | `#282C34` | Buffer background |
| gutter | `#21252B` | Line-number gutter / panels |
| editor-text | `#ABB2BF` | Default foreground |
| keyword | `#C678DD` | Keywords (`fn`, `let`, `pub`, `impl`) |
| string | `#98C379` | String literals |
| function | `#61AFEF` | Function names / methods |
| type | `#E5C07B` | Types, structs, enums |
| number | `#D19A66` | Numbers, constants |
| operator | `#56B6C2` | Operators, punctuation accents |
| variable | `#E06C75` | Variables / tags |
| comment | `#5C6370` | Comments (italic) |

### Collaboration — player cursors
Zed assigns each collaborator a distinct player color for real-time multiplayer cursors and selections.
| Player | Hex |
|---|---|
| blue | `#54A2FF` |
| green | `#7BF1A8` |
| yellow | `#FFE02A` |
| red | `#E06C75` |

---

## Typography

Zed self-hosts its faces (CORS-locked); the equivalents below are Google-hosted.

| Role | Font | Notes |
|---|---|---|
| Display | **IBM Plex Serif** *italic* | The headline voice — "Your last next editor" |
| UI / body | **IBM Plex Sans** | Nav, labels, prose |
| Code | **Lilex** ≈ **JetBrains Mono** | Zed's default editor font; documented fallback for `file://` |

Lilex is Zed's own coding face (a JetBrains-Mono-family ligature font). It is served CORS-locked from `zed.dev/_next/…`, so this showcase renders the editor in **JetBrains Mono** as a faithful stand-in (`≈`).

**Hierarchy — one role each:** Serif italic = the hero headline only. Sans = all UI and prose. Mono = the editor buffer, file tree, terminal, and metadata.

---

## Logo

The Zed mark is a single spiral-bracket glyph (a recursive `[` labyrinth) rendered in `accent-blue`, followed by the `Zed` wordmark. On the dark canvas the mark shifts toward `blue-300` via `color-mix`.

---

## Signature component — the editor

If you saw only this and no branding, you'd know it was Zed: a One-dark buffer with **live multiplayer cursors** (named collaborator flags) and an **agent panel** on the right. Type or pick a prompt, send it, and the agent streams its reasoning and applies an edit directly into the buffer — added lines flag green in the gutter. This is Zed's whole thesis in one frame: fast native editing, real-time collaboration, and agents that edit alongside you.

- Project panel (file tree) · tab bar · line-numbered buffer with One syntax highlighting
- Remote collaborator cursors with name labels (real Zed founders: Nathan, Max)
- Agent panel: prompt → deterministic streamed steps → applied diff
- Deterministic (no `Math.random`) so screenshots are stable

---

## Guardrails

**Do**
- Keep the marketing canvas warm paper `#F7F7F2`; reserve `accent-blue` for the headline, primary action, and active state.
- Set the hero headline in IBM Plex **Serif italic** — it's the brand's voice.
- Lighten blue to `blue-300` on the dark canvas so it stays legible.
- Render code in the One theme with real Rust — Zed is written in Rust and dogfoods it.

**Don't**
- Flood the UI with blue — it's an accent, not a fill.
- Set body or UI text in the serif — that face is display-only.
- Invent editor syntax colors; use the shipped One palette.
- Drop the graph-paper grid — the engineered-paper motif is part of the identity.
