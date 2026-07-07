# Bolt — Design System

> Prompt, run, edit and deploy full-stack web apps — right in the browser.

Bolt (bolt.new, by StackBlitz) is an AI web app builder with a twist: it doesn't just generate code, it **runs** it — a full dev environment (npm install, dev server, terminal, editor and live preview) lives in the browser via WebContainers. The identity is fast and electric: a **near-black** canvas with a subtle blue aurora, one **electric blue** (`#1488FC`), and a signature **light-streak** — a bright horizontal flare across the prompt box, like a bolt of energy. Type is Inter, with a heavy **bold-italic** `bolt` wordmark that leans forward like it's moving. It feels like a developer tool that's genuinely quick.

---

## Color

### Brand — electric blue on black
| Token | Hex | Usage |
|---|---|---|
| bolt-blue | `#1488FC` | Primary accent — buttons, links, active, the card glow |
| blue-hover | `#1172E2` | Hover / pressed |
| blue-deep | `#03305D` | Deep tint, borders in glow |
| streak | `#EAF2FF → #1488FC` | The bright horizontal light-flare across the prompt box |
| aurora | `radial #1488FC @ ~14%` | Faint blue bloom in the top corner of the canvas |

Blue is the single brand hue; on a near-black canvas it reads as electric. The bright white **streak** is the signature energy accent.

### Surfaces (dark-first — Bolt is a dark product; light is a secondary courtesy)
| Token | Dark | Light | Usage |
|---|---|---|---|
| canvas | `#08090C` | `#FFFFFF` | App background (dark has a faint blue tint) |
| panel | `#101216` | `#FFFFFF` | Cards, workbench, prompt box |
| subtle | `#16181D` | `#F5F6F8` | Wells, chat, sidebars |
| raised | `#1E2127` | `#EDEEF1` | Hover / active rows, editor gutter |
| border | `#23262D` | `#E4E6EB` | Hairlines |
| code-bg | `#0B0C0F` | `#0B0C0F` | Editor + terminal (always dark) |

### Text
| Token | Dark | Light |
|---|---|---|
| primary | `#EDEEF2` | `#0D0E12` |
| secondary | `#9BA1AD` | `#5A5F6B` |
| muted | `#6A707C` | `#8A8F99` |
| link | `#1488FC` | `#1172E2` |

### Functional signals (workbench — not brand)
| Token | Hex | Meaning |
|---|---|---|
| success | `#3FB950` | Command done · dev server ready |
| running | `#1488FC` | Installing / building |
| warn | `#D29922` | Notice |
| syntax | keyword `#FF7B72` · string `#7EE787` · fn `#D2A8FF` · var `#79C0FF` · comment `#6A737D` | Code editor tokens |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / UI / body | **Inter** (`400 / 500 / 600 / 700`) | Bolt's workhorse — headings, prompt, chat and UI. |
| Wordmark | **Inter** `800 italic` | The `bolt` logotype is a heavy, forward-leaning **bold italic**; `.new` follows in a lighter, muted weight. |
| Code / terminal | **JetBrains Mono** (`400 / 500`) | The editor, file names, and the streaming terminal (npm install / dev). |

Scale: hero 52px (Inter 700, tight), prompt 16px, section 24px, body 15px, code 12.5px (JetBrains Mono). The wordmark's italic lean is the one expressive move — keep everything else calm and legible.

---

## Shape, spacing & motion

- **Radius:** the prompt box & cards `16px`, buttons `10px`, workbench panels `12px`, chips/pills `9999px`, editor/terminal `10px`. Rounded but businesslike.
- **Spacing:** the hero centers a single prompt box in a dark field; the app is the **workbench** — chat/terminal on the left, a **Code / Preview** tabbed pane on the right.
- **Elevation:** the prompt box carries a **blue border-glow** and a bright **light-streak** across its top edge; panels sit on soft dark shadows.
- **Motion:** the signature is **run** — you prompt, files stream in, then a **terminal actually runs** (`npm install` → `npm run dev`) and the pane flips to a live **Preview** when the dev server is ready. Quick, sequential, **deterministic** — fixed file writes, fixed install/boot; no randomness.

---

## Components

- **Wordmark** — heavy bold-italic `bolt` + muted `.new`; leans forward like motion.
- **Prompt box** — the hero + workbench entry: a dark rounded card, blue border-glow, a bright **light-streak** on the top edge, "What do you want to build?", with attach / enhance controls and a blue send button.
- **Workbench** — the product: a **chat / build log** with a live **terminal** (streaming npm install & dev), beside a **Code / Preview** tabbed pane (file tree + syntax-highlighted editor, then the running app).
- **Terminal** — a mono console that streams real commands with a success (`✓`) and the dev-server URL.
- **Code editor** — dark editor with GitHub-style syntax tokens + a file tree.
- **Buttons** — electric-blue primary, quiet ghost secondary; pill chips for suggested prompts.

---

## Guardrails

**Do**
- Anchor on a **near-black canvas** with one **electric blue** (`#1488FC`) and a faint blue aurora — dark is the identity.
- Give the prompt box its **blue glow** and bright **light-streak** — the signature energy.
- Make the flow **prompt → run → preview**: stream files, then actually **run a terminal** (npm install / dev) and flip to a live preview.
- Set the `bolt` wordmark in **bold italic**; keep the rest of the UI in calm Inter, code in JetBrains Mono.
- Keep the editor & terminal **always dark**, with GitHub-style syntax colors.

**Don't**
- Use a bright/light canvas as the primary identity — Bolt is dark and electric (light mode is secondary).
- Introduce a second brand hue; blue is the only accent (syntax + status colors are functional).
- Present Bolt as just a code generator — the point is that it **runs and deploys** in-browser (show the terminal).
- Over-glow everything — the streak + card glow are focal; the rest stays matte.
- Set the wordmark upright or light — the forward **italic** lean is the character.
