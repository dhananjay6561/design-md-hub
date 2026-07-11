# Devin — Design System

> Devin, the AI software engineer.

Devin (by Cognition) is an AI coding agent and software engineer — **parallel cloud agents for serious engineering teams**. You plan, delegate, review, and ship without leaving your editor; Devin Desktop is the surface for managing fleets of local and cloud agents. *(Windsurf is now part of Cognition — windsurf.com redirects to Devin Desktop.)*

The identity is **Swiss and monochrome**: a warm paper canvas, near-black ink, NB International Pro set tight, and one electric **ultramarine** (`#2200FF`) used sparingly. The product surface (Devin Desktop) flips to a true-black console.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| ultramarine | `#2200FF` | The accent — links, active state, key highlights (used sparingly) |
| ink | `#191919` | Primary text, buttons |
| orange | `#EC5D40` | Secondary accent |
| blue-illus | `#317CFF` | Illustration / diff blues |

### Surfaces
| Token | Light (marketing) | Dark (Devin Desktop) | Usage |
|---|---|---|---|
| canvas | `#F7F6F5` | `#0E0E0E` | Background (warm paper / true console) |
| panel | `#FFFFFF` | `#191919` | Cards, panels |
| raised | `#EFEFEF` | `#1F1F1F` | Session cards / bento |
| border | `#E7E7E7` | `#2A2A2A` | Hairlines |
| border-strong | `#D9D9D9` | `#3A3A3A` | Inputs, dividers |

### Text
| Token | Light | Dark |
|---|---|---|
| primary | `#191919` | `#E7E7E7` |
| secondary | `#626870` | `#A7A6A6` |
| muted | `#7D7D7D` | `#6D6D6D` |

### Session state
| Token | Hex | Meaning |
|---|---|---|
| running | `#2200FF` | Agent working |
| review | `#EC5D40` | Waiting for review |
| done | `#20A56A` | Merged / done |
| error | `#FF1A1A` | Failed |

---

## Typography

| Role | Font | Notes |
|---|---|---|
| Display / UI / body | **NB International Pro** | Swiss neo-grotesque — self-hosted on devin.ai, **CORS-open**, used directly (weights 400–500) |
| Code / session meta | **Geist Mono** | Diffs, IDs, timestamps, branch names |

NB International Pro carries everything visible — headings set at 500, tight tracking, sentence case. Keep code, IDs and branch names in Geist Mono.

---

## Logo

The Cognition/Devin **prism mark** — a single interlocking path (viewBox `0 0 425 425`) filled `--logo-mark` — followed by the `Devin` wordmark in NB International Pro. Ink on paper, light on console.

---

## Signature component — the agent-fleet board

If you saw only this, you'd know it was Devin Desktop: a **session board** for managing a fleet of parallel agents — columns for **Running**, **Waiting for review**, and **Done**, each holding session cards where a Devin agent works a real engineering task (`Widen the model hidden dimension`, `Switch the MLP activation to GELU`). **Delegate a task** and a new agent spawns into Running (*Working…*) while a finished one advances to review with a PR ready. This is "plan, delegate, review, ship" made literal.

- Slim Spaces sidebar + Agent/Editor toggle + Board/List
- Three columns with live session cards (status, PR/branch, timestamp)
- Delegate input spawns a running agent; deterministic advancement (no `Math.random`)

---

## Guardrails

**Do**
- Keep marketing on warm paper `#F7F6F5` with near-black ink; flip the product surface to true-black `#0E0E0E`.
- Use **ultramarine** sparingly — links, active session, one highlight; it's a punctuation color, not a fill.
- Set everything visible in NB International Pro (500 for headings); code & branches in Geist Mono.
- Treat agents as a **fleet** — parallel sessions across Running / Review / Done.

**Don't**
- Reintroduce a Windsurf teal/green identity — the brand is Cognition/Devin monochrome now.
- Flood the UI with ultramarine or add a second bright accent — orange is the only secondary.
- Set body copy in a mono — NB International Pro carries sentences.
- Show a single agent — the many-agent fleet is the whole surface.
