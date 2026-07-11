# v0 — Design System

> What do you want to create?

v0 by Vercel is a collaborative AI assistant that designs, iterates, and ships full-stack web apps. You describe what you want; v0 generates real React + Tailwind (shadcn/ui) components you can preview, read as code, and deploy.

The identity is pure **Vercel monochrome** — near-white canvas, near-black ink, Geist everywhere, no brand hue. The interface gets out of the way so the *generated* work carries the color. A **Preview / Code** split is the whole product.

---

## Color

### Brand — monochrome (no accent hue; foreground *is* the accent)
| Token | Light | Dark | Usage |
|---|---|---|---|
| foreground | `#171717` | `#FAFAFA` | Text, primary button, logo |
| background | `#FFFFFF` | `#0A0A0A` | App background |
| subtle | `#FAFAFA` | `#111111` | Page tint / secondary surface |
| card | `#FFFFFF` | `#0E0E0E` | Cards, panels |
| muted | `#F5F5F5` | `#1A1A1A` | Muted fills |
| muted-fg | `#737373` | `#A1A1A1` | Secondary text |
| border | `#E5E5E5` | `#262626` | Hairlines |
| input | `#E5E5E5` | `#2A2A2A` | Inputs, dividers |

> v0 has **no brand color** by design — like Vercel and shadcn/ui, the surface is neutral and the generated UI provides any color. The reds/blues/ambers on the homepage are template thumbnails, not the brand.

### Functional only
| Token | Hex | Usage |
|---|---|---|
| success | `#16A34A` | Generation complete |
| streaming | `#171717` | Building indicator (mono) |

---

## Typography

| Role | Font | Notes |
|---|---|---|
| Display / UI / body | **Geist** | Vercel's grotesque — headings + product UI |
| Code / generated source | **Geist Mono** | The Code tab, model name, tokens |

Both are Vercel's own faces, self-hosted CORS-open and also on Google Fonts (used here). Hierarchy is weight and size, not typeface — Geist carries everything visible; Geist Mono is reserved for generated code and metadata.

---

## Logo

The `v0` mark (viewBox `0 0 147 70`) — two paths forming a slanted `v` and `0` — filled `currentColor` (`--logo-fg`): ink on light, near-white on dark. No wordmark needed; the mark *is* the wordmark.

---

## Signature component — v0 generate

If you saw only this, you'd know it was v0: a prompt bar (**Ask v0 to build…**, model set to **v0 Max**) that generates a real component into a **Preview / Code** panel. Pick a prompt — a pricing table, a contact form, a stats dashboard — and v0 streams its build steps, then renders the live component; flip to **Code** for the actual React + Tailwind (shadcn/ui) source. Regenerate to replay.

- Prompt bar + preset chips + `v0 Max` model selector
- Build-step stream (Thinking → Generating → Styling → Done)
- **Preview / Code** tabbed result — live shadcn component ↔ real JSX
- Deterministic presets (no `Math.random`)

---

## Guardrails

**Do**
- Keep the surface monochrome — near-white / near-black, Geist; let the *generated* UI carry color.
- Make **Preview ↔ Code** the core interaction — v0's value is real, readable component source.
- Generate real shadcn/ui + Tailwind patterns (cards, tiers, form fields), not lorem boxes.
- Set the Code tab and model name in Geist Mono; everything else in Geist.

**Don't**
- Add a v0 brand hue — the neutral surface is the point.
- Set body or UI copy in the mono — Geist carries sentences; mono is code only.
- Show only a preview or only code — the split is the identity.
- Invent fake component output — mirror what v0 actually generates.
