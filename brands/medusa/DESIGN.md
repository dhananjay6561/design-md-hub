# Medusa — Design System

> The best commerce platform for agents and developers.
> #1 open-source commerce platform on GitHub. Extend, customize, and own every commerce workflow.

Medusa's identity is **monochrome and engineering-first**: a clean white canvas, near-black ink, and a near-black primary button — no brand hue in the chrome. It reads like a developer framework (because it is): the interest lives in the **code** and the **Admin**, not in decoration. Color appears only as syntax highlighting, order state, and an occasional illustrative coral gradient.

---

## Colors

### Neutral (the brand)
Medusa is monochrome — the Simple Icons brand color is `#000000`. The "accent" is near-black on white; it inverts on dark.

| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `bg` | `#FFFFFF` | `#18181B` | App canvas |
| `bg-subtle` | `#FAFAFA` | `#1C1C1F` | Panels / cards |
| `bg-field` | `#F4F4F5` | `#232327` | Rows / inputs |
| `border` | `#EAEAEA` | `#2E2E32` | Hairlines |
| `fg` | `#18181B` | `#FAFAFA` | Primary text · primary button |
| `fg-muted` | `#71717A` | `#A1A1AA` | Secondary text |
| `fg-subtle` | `#9CA3AF` | `#71717A` | Meta / captions |

The deepest ink `#030712` anchors always-dark surfaces (the code panel).

### Order & commerce state (semantic)
| State | Hex | Meaning |
|-------|-----|---------|
| authorized | `#3B82F6` | Payment authorized |
| captured / paid | `#10B981` | Payment captured · fulfilled |
| pending | `#E9A23B` | Awaiting action |
| canceled | `#FB1048` | Canceled / error |

### Illustrative (marketing only)
A warm coral→peach gradient — `#FF5A77` → `#FF774C` → `#FFBA71` → `#FED7AA` — and a periwinkle `#9290FE` appear in hero art. **Never** the UI accent; the chrome stays monochrome.

---

## Typography

- **Inter** (`--font-inter`) — display, UI, body. Google-hosted, used directly.
- **Roboto Mono** (`--font-roboto-mono`) — code, module calls, IDs, money, order numbers. Google-hosted.

One role each: Inter for everything human-readable, Roboto Mono for code and commerce data.

| Role | Face | Spec |
|------|------|------|
| Display | Inter 600 | 52px, `-0.03em` |
| Heading | Inter 600 | 20px |
| Body | Inter 400 | 15px |
| Code / data | Roboto Mono 400 | 12–13px |

---

## Logo

The real Medusa **mark** — a rounded hexagon shield enclosing a ring (`viewBox 0 0 64 64`, single path), pulled verbatim from the live site and themed via `--logo-mark` (black on light, white on dark). Pair it with the **"Medusa"** wordmark in Inter.

---

## Signature component — Modules → Admin order

Medusa's whole model in one frame: **commerce modules power the Admin.**

- A left **code panel** (always-dark) with the real Medusa module call — `paymentModule.capturePayment()`, `fulfillmentModule.createFulfillment()` — in Roboto Mono, syntax-highlighted.
- A right **Admin order** (`Order #2456 · Acme, Inc.`): customer, line items (`Medusa Sweatshirt`, `Medusa Coffee Mug`), a money summary (subtotal / shipping `FREE_SHIPPING` / tax / total), and two status badges — **Payment** and **Fulfillment**.
- **Capture payment** flips the payment badge Authorized → Captured (green) and streams the matching module call. **Create fulfillment** flips fulfillment Not fulfilled → Fulfilled and prints the shipment. An activity log records each action.

Deterministic — fixed order, index-driven actions, no `Math.random`.

---

## Guardrails

**Do**
- Keep the chrome monochrome: white (or near-black) canvas, near-black (or white) primary button.
- Set every module call, ID, and money value in Roboto Mono.
- Show the core model — **module code beside the Admin it drives**.
- Color order state by meaning: blue authorized, green captured/fulfilled, amber pending.

**Don't**
- Use the coral gradient or periwinkle as the UI accent — they're illustrative only.
- Add a brand hue to buttons — the primary action is flat near-black / white.
- Render code or money in a proportional sans — it's mono.
- Recolor the hexagon mark — it's monochrome (`--logo-mark`).
