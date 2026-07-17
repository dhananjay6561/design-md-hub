# Ramp — Design System

Time is money. Save both. Ramp is the all-in-one finance platform — corporate cards, expense management, bill payments, travel, procurement, and accounting automation. The design language is confident and editorial: a warm off-white canvas, near-black ink set in **TWK Lausanne**, and one unmistakable **Ramp yellow** reserved for action.

Tokens are lifted from the live site (`ramp.com`) — TWK Lausanne is self-hosted there (CORS-open); the signature yellow and blue were sampled from live surfaces.

---

## Colors

Ramp is near-monochrome — warm paper, warm near-black — punctuated by a single electric **yellow** for every primary action, and a **blue** used for data, links, and the product surface. Green marks money saved.

| Token | Hex | Use |
|---|---|---|
| yellow | `#e4f222` | **Ramp yellow** — primary CTA fill, highlights (black text on it) |
| blue | `#0066ff` | Links · data-viz · product accents |
| ink | `#1a1918` | Primary text (warm near-black) |
| paper | `#f4f2ef` | Canvas (warm off-white) |
| white | `#ffffff` | Cards · raised surfaces |
| surface | `#eeebe7` | Wells · subtle fills |
| green | `#1f7a46` | Money saved · in-policy · positive |
| red | `#d4443a` | Out of policy · declined |

### Semantic mapping

| Role | Light | Dark |
|---|---|---|
| background | paper `#f4f2ef` | warm black `#141310` |
| card / raised | white `#ffffff` | `#1d1b17` |
| surface / well | `#eeebe7` | `#242118` |
| text primary | ink `#1a1918` | `#f4f2ef` |
| text muted | `#5c5a54` | `#a8a49b` |
| text faint | `#93908a` | `#77736b` |
| border | `#e4e0db` | `rgba(255,255,255,.10)` |
| accent (CTA) | yellow `#e4f222` | yellow `#e4f222` |
| link / data | blue `#0066ff` | `#5b92ff` |

> The yellow is theme-invariant — it carries the brand across light and dark. Text on yellow is **always** ink, never white.

---

## Typography

One superfamily does almost everything: **TWK Lausanne** (Weltkern), a warm neo-grotesque. Ramp runs it light for body, near-regular for UI, and bold for display. There is no serif and no brand monospace; numeric metadata falls back to the system mono stack with tabular figures.

| Role | Family / weight | Notes |
|---|---|---|
| Display / hero | TWK Lausanne 700 | Tight tracking (`-0.03em`), large — "Time is money. Save both." |
| Heading | TWK Lausanne 400–700 | Section titles |
| Body / UI | TWK Lausanne 350 | The workhorse — light, calm, editorial |
| Emphasis | TWK Lausanne 400 Italic | Rare inline emphasis |
| Numerals / meta | system mono | `ui-monospace, SFMono-Regular, Menlo` · tabular-nums for money |

> Weights self-hosted from `ramp.com` (CORS-open): TWK Lausanne 300 / 350 / 400 / 700 + italics.

---

## Type scale

| Step | Size | Weight | Tracking |
|---|---|---|---|
| Display | 72px | 700 | -0.03em |
| Heading-lg | 40px | 700 | -0.02em |
| Heading-md | 24px | 400 | -0.015em |
| Title | 17px | 400 | -0.01em |
| Body | 15px | 350 | 0 |
| Caption | 13px | 350 | 0 |
| Amount / meta | 13px | mono | tabular-nums |

---

## Radius, spacing, elevation

- **Radius:** 8px (chips / inputs) · 10px (buttons) · 14px (cards) · 18px (panels) · full (pills / avatars).
- **Borders:** 1px warm hairlines (`#e4e0db`); surfaces read on borders + generous whitespace, not heavy shadow.
- **Elevation:** soft, low shadows on floating cards only (`0 12px 40px rgba(26,25,24,.08)`).
- **Density:** editorial and roomy in marketing; dense tabular rows (`~52px`) in the product feed.

---

## Components

- **Buttons:** primary = **Ramp yellow** fill with **ink** text (`Get a demo`); secondary = white with a hairline border; ghost = text-only. Blue is a link color, never a button fill.
- **Corporate card:** the iconic Ramp card — warm-black slab, yellow ramp mark, mono card number. A brand object, not just a component.
- **Ramp Intelligence — the savings engine (signature):** a live spend panel — a big green **Saved this year** counter, **auto-categorized** spend bars (mono, tabular amounts), and stacked yellow **savings insights** (duplicate subscription, unused seats, cheaper annual price). Each carries an **Apply** action that books the savings straight into the counter. This is the product's whole promise in one component: *time is money — save both*.
- **Status pills:** green in-policy / approved, yellow needs-review, red out-of-policy.
- **Inputs:** white fill, hairline border, ink text; focus ring in yellow.

---

## Guardrails

**Do**
- Keep the canvas warm off-white `#f4f2ef` with warm near-black ink — the warmth is the brand.
- Reserve **Ramp yellow** `#e4f222` for primary actions and highlights; put **ink** text on it, never white.
- Set everything in **TWK Lausanne** — light `350` for body, `700` for display.
- Use **green** to celebrate money and time saved; that's Ramp's whole story.
- Let money read in **tabular mono** so columns align.

**Don't**
- Don't tint the yellow toward gold or orange, or use it as a large background wash.
- Don't put white text on the yellow, or use yellow for body text.
- Don't swap the warm paper for a cold pure-grey — it flattens the identity.
- Don't turn the blue into a primary button; it's for links and data.
- Don't reach for a second display typeface — Lausanne carries the whole system.
