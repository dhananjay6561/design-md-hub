# Warp — Design System

> The Agentic Development Environment.

Warp is a modern, Rust-built terminal reimagined for coding with AI agents — run Oz, Claude Code, Codex, and Gemini CLI with fine-grained control, locally or in the cloud. Its defining idea is **Blocks**: every command and its output are grouped into a distinct, selectable card instead of an endless scrollback stream.

The identity is a deep, near-black canvas with a soft **lavender-purple** accent, sharp monospace output, and one characterful display typeface — **The Future**. It reads as a developer tool that's fast and modern, not retro.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| lavender | `#C7AEFF` | Primary accent — active block, prompt, links |
| purple | `#BDA6F7` | Secondary accent / gradient partner |
| brand gradient | `#BDA6F7 → #C7AEFF` | Logo mark, marquee CTA |
| purple-surface | `#1C1A26` | Accent-tinted panels |
| purple-line | `#373245` | Accent-tinted borders |

### Surfaces (dark-first)
| Token | Dark | Light | Usage |
|---|---|---|---|
| canvas | `#0B0B0B` | `#FFFFFF` | App background |
| terminal | `#111111` | `#F6F5FA` | Terminal / panel body |
| block | `#16151D` | `#FFFFFF` | Command block |
| raised | `#1C1A26` | `#EFEDF6` | Selected / hover block |
| border | `#2A2833` | `#E6E3F0` | Hairlines |

### Text
| Token | Dark | Light |
|---|---|---|
| primary | `#F5F4F8` | `#1C1A26` |
| secondary | `#B5B2C2` | `#55516A` |
| faint | `#7C7890` | `#8B87A0` |

### Terminal / agent semantics
| Token | Hex | Usage |
|---|---|---|
| success | `#5CD98A` | passing tests, clean exit |
| error | `#FF6B6B` | failures, non-zero exit |
| warning | `#E8C15F` | warnings |
| agent | `#C7AEFF` | agent (Oz) blocks & steps |
| info / dir | `#5AA6F2` | directories, info output |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / headings | **The Future** (`Regular / Medium`) | Warp's signature display face (self-hosted, CORS-open). Hero, headings, big numbers. |
| UI / body | **Inter** (`400 / 500 / 600`) | Product UI, body, labels, buttons, block metadata. |
| Terminal / code | **JetBrains Mono** | Command input, block output, prompts, agent steps — everything inside a block. |

Scale: hero 52–60px (The Future), section 22px, block command 13px mono, output 12.5px mono, body 14px, labels 11px uppercase.

---

## Shape, spacing & motion

- **Radius:** blocks `10px`, terminal window `14px`, buttons `8px`, chips/pills `9999px`. Rounded but tight.
- **Spacing:** 8px grid; blocks stack with a small gap (`6–8px`) so each reads as its own unit.
- **Elevation:** the terminal floats on a soft shadow; inside, blocks are flat and separated by a hairline. A **selected block** gets a lavender left-accent and a raised tint — no shadow.
- **Motion:** fast and mechanical. Agent steps stream in line by line; a running block shows a subtle pulse on its accent bar; block selection is instant. Nothing bounces.

---

## Components

- **Block** — the atom of Warp: a prompt row (`user  ~/dir ❯ command`) plus its output, as one selectable card. Hover raises it; click selects it (lavender left-accent).
- **Agent block** — an Oz/agent run: a natural-language prompt (`▸`) that expands into streamed steps (reading files, editing, running commands) ending in a result.
- **Input bar** — a bottom command line with a mode switch (Terminal `❯` / Agent `▸`) and a `⌘P` command-palette hint.
- **Prompt** — `user` + working dir + a lavender `❯` glyph.
- **Buttons / chips** — solid lavender primary (dark text); ghost chips for quick actions.

---

## Guardrails

**Do**
- Group commands and output into **blocks** — never a flat, undifferentiated scrollback.
- Keep the canvas near-black with one lavender-purple accent for state (active block, prompt, agent).
- Use JetBrains Mono for everything inside a block; The Future only for display headings.
- Color output by meaning — green pass, red fail, lavender for agent steps.
- Show real agent vocabulary: Oz, Claude Code, Codex, Gemini CLI; `❯` prompt, `▸` agent.

**Don't**
- Render a classic uninterrupted terminal stream — blocks are the whole point.
- Introduce a second bright accent — lavender carries the brand; agent colors are opt-in tints.
- Use heavy shadows between blocks or large consumer radii — Warp is tight and technical.
- Set body or terminal text in a display font — The Future is headings only.
