# GitBook — Design System

> The knowledge layer for AI.
> AI made docs easy to write. Not easy to trust — GitBook is the docs infrastructure that does both.

GitBook's identity is **warm and monochrome-first**: a warm off-white canvas, warm near-black (stone) ink, and a near-black primary button — with one signature **GitBook green** (`#1D7253`) for links, AI, and active state, and an **orange** (`#FE551B`) reserved for "New" badges and decoration. It reads like a documentation product: quiet chrome, legible type, color used to mean something.

---

## Colors

### Brand
| Token | Hex | Usage |
|-------|-----|-------|
| `green-600` | `#1D7253` | The brand green — links, Ask/AI, active nav, success |
| `green-tint` | `#E1F8EC` | Mint wash behind AI answers / highlights |
| `green-deep` | `#0F5C40` | Hover / pressed |
| `orange-500` | `#FE551B` | "New" badges, decorative blobs (secondary only) |

### Surfaces
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `bg` | `#FAFAF9` | `#1C1917` | App canvas (warm) |
| `card` | `#FFFFFF` | `#262322` | Cards / doc surface |
| `subtle` | `#F5F4F2` | `#2A2725` | Nav / wells |
| `border` | `#E7E5E3` | `#33302E` | Hairlines |

### Text (warm stone)
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `ink` | `#1C1917` | `#FAFAF9` | Primary · primary button |
| `muted` | `#57534D` | `#B8B2AC` | Secondary |
| `subtle` | `#79716B` | `#8A827B` | Meta / captions |

The warm stone neutrals (`#57534D`, `#79716B`) are part of the identity — never swap them for cold grey.

---

## Typography

- **Inter** (`--font-family`) — UI, body, headings, doc content. Google-hosted, used directly.
- **Geist Mono** — code blocks, inline code, API paths, metadata. (GitBook's site also loads Space Mono; Geist Mono is used here.)

| Role | Face | Spec |
|------|------|------|
| Display | Inter 600 | 52px, `-0.03em` |
| Heading | Inter 600 | 20px |
| Body | Inter 400 | 15px |
| Code | Geist Mono 400 | 12–13px |

---

## Logo

The real GitBook **mark** — the stacked/layered glyph (`viewBox 0 0 24 24`, single path) — themed via `--logo-mark` (warm near-black on light, warm white on dark). Pair it with the **"GitBook"** wordmark in Inter.

---

## Signature component — The docs, with Ask AI

GitBook is a docs platform that is now "the knowledge layer for AI." The signature shows both:

- A **published docs site**: a left page tree (`Getting Started → Welcome / Quickstart / Authentication`), a center doc page (heading, prose, a code block, a hint callout), and a right "On this page" TOC. Selecting a page in the tree loads it in the center.
- An **Ask** bar (GitBook green). Choosing a question opens an **AI answer** on a mint surface that streams a response and cites its **sources** — chips that link back to the exact doc pages. That is the "knowledge layer": trustworthy answers, grounded in the docs.

Deterministic — fixed pages and answers, index-driven streaming, no `Math.random`.

---

## Guardrails

**Do**
- Keep the canvas warm off-white `#FAFAF9` (or stone `#1C1917`) with warm near-black text and a near-black primary button.
- Use **GitBook green** for links, active nav, and the Ask/AI surface; keep orange for "New" badges only.
- Ground AI answers in **cited sources** — the trust story is the point.
- Set code, API paths, and metadata in Geist Mono.

**Don't**
- Use cold grey neutrals — GitBook's greys are warm stone.
- Promote orange to the primary action — the primary button is monochrome near-black.
- Show an AI answer without citations — "not easy to trust" is the problem GitBook solves.
- Recolor the mark — it's monochrome (`--logo-mark`).
