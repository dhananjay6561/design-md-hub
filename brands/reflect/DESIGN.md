# Reflect — Design System

> A beautifully minimalist note-taking app designed to mirror the way you think.

Reflect is a networked note-taking app: notes link to each other with `[[wiki-links]]`, every note surfaces its **backlinks**, and the whole knowledge base forms a **graph** — with a native AI integration on top. The idea is *networked thought*: ideas connected like neurons, not filed in folders.

The identity is dreamy and nocturnal: a near-black indigo canvas (`#030014`) fading up into a **glowing purple horizon**, one luminous **indigo→purple→magenta** gradient, and a signature mark of a **networked sphere** — glowing nodes and edges, the graph made literal. Type is Aeonik Pro for display over Inter for body. It feels calm, focused, and a little cosmic.

---

## Color

### Brand — the purple gradient
| Token | Hex | Usage |
|---|---|---|
| indigo | `#787BFF` | Gradient start, links |
| purple | `#A479FF` | Primary accent, active node, focus |
| magenta | `#FA5FFF` | Gradient end, glow highlights |
| lavender | `#C9B1FF` | Soft accent, secondary nodes |
| pink | `#E59CFF` | Tint / secondary glow |
| brand gradient | `#787BFF → #A479FF → #FA5FFF` | Logo tile, CTAs, the horizon glow |

### Surfaces (dark-first — the app is nocturnal)
| Token | Dark | Light | Usage |
|---|---|---|---|
| canvas | `#030014` | `#FBFAFF` | App background (dark fades to a purple horizon) |
| panel | `#0B0918` | `#FFFFFF` | Cards, editor |
| subtle | `#100D22` | `#F3EEFF` | Muted rows, backlink cards |
| raised | `#181430` | `#EFEDFD` | Hover / selected |
| border | `#241F3D` | `#E7E1FA` | Hairlines |

### Text
| Token | Dark | Light |
|---|---|---|
| primary | `#F4F2FF` | `#12102A` |
| secondary | `#B9B4D6` | `#54506E` |
| muted | `#7C7799` | `#8B86A6` |
| link | `#BF97FF` | `#7C4DFF` |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / headings | **Aeonik Pro** (`medium 500`) | CoType's geometric grotesque — the brand face (wordmark, note titles, headings). Self-hosted at `site.reflect.app/home/fonts/AeonikPro`, CORS-open. Ships medium only. |
| UI / body | **Inter** (Inter Variable, `400 / 500`) | Note body, UI, labels. Self-hosted `InterV`, CORS-open. |
| Meta / mono | **JetBrains Mono** | Timestamps, node ids, small meta — used sparingly. |

Scale: hero 56px (Aeonik 500), note title 30px, section 20px, body 15px (Inter), backlink 13px, meta 11px. Generous line-height (1.6) in the editor — it's for reading and thinking.

---

## Shape, spacing & motion

- **Radius:** cards & editor `14px`, the logo tile `22%` (superellipse app-icon), buttons `10px`, graph nodes are circles, chips/pills `9999px`. Soft and rounded.
- **Spacing:** 8px grid; the editor is roomy and centered; the graph and backlinks sit alongside as a calm secondary column.
- **Elevation:** panels float on deep shadows over the dark canvas; accent elements carry a soft purple **glow** (`0 0 24px rgba(164,121,255,.4)`), never a hard shadow. The horizon gradient glows up from the bottom.
- **Motion:** gentle and fluid. Selecting a note eases the graph to re-center on it; the active node grows and brightens; links fade in. Nothing snaps. Deterministic — no randomness.

---

## Components

- **Logo mark** — a superellipse tile with the indigo→magenta gradient, holding a glowing **networked sphere**: white nodes joined by thin edges. Pairs with the `Reflect` wordmark in Aeonik.
- **Note editor** — a titled note (Aeonik title, Inter body) with inline `[[wiki-links]]` rendered as purple links; roomy line-height.
- **Backlinks panel** — cards listing the notes that link *to* the current note, with a snippet of context.
- **Graph view** — nodes (notes) and edges (links) as a glowing constellation; the active note is the bright center. Clicking a node navigates to that note (the signature echo of the logo).
- **Buttons** — gradient primary (indigo→magenta, light text) with a glow on hover; ghost secondary with a purple border.

---

## Guardrails

**Do**
- Anchor on a **near-black indigo** canvas that fades up to a glowing **purple horizon**.
- Use the one **indigo→purple→magenta** gradient for the mark, CTAs, and glows — purple is the single accent family.
- Make the **network** literal: `[[backlinks]]`, a backlinks panel, and a node-and-edge graph that echoes the logo.
- Set titles/wordmark in Aeonik Pro; body in Inter; give the editor generous line-height for reading.
- Give accents a soft **glow**, not a hard drop shadow.

**Don't**
- Use a flat white/light canvas as the primary identity — Reflect is dark and nocturnal (light mode is secondary).
- Introduce a competing brand hue — stay within the indigo→magenta purple family.
- Render notes as isolated cards with no links — the whole point is the network.
- Set body text in the display face, or crowd the editor — it's minimalist and calm.
- Make the gradient garish; it's a soft luminous glow, not neon.
