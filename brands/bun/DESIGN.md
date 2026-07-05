# Bun — Design System

Design-token reference for **Bun** (bun.sh), the fast all-in-one JavaScript runtime & toolkit. All values live-fetched from `bun.sh` and its `/_assets/site-*.css` bundle (July 2026). Bun's identity is the warm **cream canvas** (`#fbf0df`), the full-color **bun mascot**, and a **Dracula-style terminal** — speed is the message, and the visual language stays deliberately simple and system-native.

---

## Brand voice

- Hero H1 (rotating word): **"Bun is a _fast_ JavaScript all-in-one toolkit"** (rotates: fast · all-in-one toolkit · incrementally adoptable).
- Positioning: *"Develop, test, run, and bundle JavaScript & TypeScript projects — all with Bun."*
- Everything is about **speed** and **all-in-one** (runtime + package manager + bundler + test runner + Node-compatible).
- Real install: `curl -fsSL https://bun.sh/install | bash`. Real commands: `bun install`, `bun run`, `bun test`, `bun build`, `bunx`.
- Sign-off in copy: **"Bun good 🧅"**.

---

## Typography

Bun ships **no custom webfont** — the site uses the native system stack, paired with JetBrains Mono for code (the real `--monospace-font`).

| Role | Family | Source | Usage |
|------|--------|--------|-------|
| Display / UI / body | **system-ui** (`-apple-system, BlinkMacSystemFont, "Segoe UI", …`) | native | Hero, headings, body, buttons |
| Mono | **JetBrains Mono** (then Fira Code / Hack / Source Code Pro) | Google Fonts (CORS ✅) | Terminal, code, commands, metrics |

Real `--monospace-font: "JetBrains Mono", "Fira Code", "Hack", "Source Code Pro", …`. Headings are heavy system-ui (700–800), tight tracking; the mascot supplies the personality, not a display face.

---

## Color

Bun's shell is a **warm cream** in light and a **near-black** in dark. The pink/coral comes from the mascot; code blocks use a **Dracula** palette.

### Surfaces
| Token | Hex | Usage |
|-------|-----|-------|
| `cream` | `#FBF0DF` | Page background (light) — the signature Bun cream |
| `cream-2` | `#F9F1E1` | Cards, raised surfaces (light) |
| `cream-3` | `#F6DECE` | Fills, hover, mascot bottom-shadow |
| `ink` | `#14151A` | Page background (dark) — real `#14151a` |
| `ink-2` | `#1C1D24` | Raised surface (dark) |
| `ink-3` | `#24252E` | Fill / border (dark) |

### Text
| Token | Hex | Usage |
|-------|-----|-------|
| `text` (light) | `#14151A` | Primary ink |
| `text-2` | `#374151` | Secondary (gray-700) |
| `text-3` | `#6B7280` | Muted (gray-500) |
| `text` (dark) | `#F9FAFB` | Primary on ink |

### Accent & semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `bun-coral` | `#FF6164` | Brand accent — buttons, links, highlights (the mascot mouth) |
| `bun-pink` | `#F472B6` | Secondary pink accent (from live CSS) |
| `blush` | `#FEBBD0` | Mascot blush (fixed logo color) |
| `green` | `#28C840` | Success / macOS traffic-light green |
| `yellow` | `#FEBC2E` | Warning / traffic-light yellow |
| `red` | `#FF5F57` | Error / traffic-light red |

### Code (Dracula — terminal & code blocks only)
Background `#282A36`; syntax: pink `#FF79C6` · green `#50FA7B` · cyan `#8BE9FD` · purple `#BD93F9` · yellow `#F1FA8C` · comment `#6272A4`.

---

## Logo

Full-color **bun mascot** (`/logo.svg`, viewBox `0 0 80 70`) — a cream bun with pink blush `#FEBBD0`, coral mouth `#FF6164`, deep-red gum `#B71422`, and white eye highlights. Colors are **fixed** — never flatten to a single hue or recolor. Paired with a heavy system-ui **"Bun"** wordmark in ink (light) / cream (dark).

---

## Guardrails

**DO**
- Anchor the light UI on the cream `#FBF0DF` — the warm canvas is the brand, not white.
- Keep the mascot full-color with its fixed cream / blush / coral / red palette.
- Use JetBrains Mono for every command, metric and terminal line; system-ui for everything else.
- Style code blocks and the terminal with the Dracula palette on `#282A36`.
- Show real commands (`bun install`, `bun run`, `bunx`) and lead with speed.

**DON'T**
- Use pure white as the light page — it loses the cream identity.
- Recolor or flatten the mascot, or drop its blush/mouth colors.
- Introduce a bespoke display font — Bun is system-native by design.
- Use `#000` on the dark surface for text — flip to `#F9FAFB`.
- Fabricate benchmark numbers — use Bun's published relative speeds, computed deterministically.
