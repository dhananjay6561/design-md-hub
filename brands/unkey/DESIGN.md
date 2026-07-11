# Unkey — Design System

> The Developer Platform for Modern APIs.
> API keys, rate limiting, and gateways — deploy in minutes, roll back in seconds.

Unkey's identity is **monochrome and precise**: a true near-black `#040406` canvas, a zinc neutral scale, and white as the primary action — no single brand hue. Color enters only as a **categorical accent spectrum** (blue, cyan, mint, lime, gold, red) used for data, state, and feature illustration. It reads like the product it is: a clean control plane for API infrastructure.

---

## Colors

### Neutral (the brand)
Unkey is monochrome. The "accent" is white on near-black; on light it inverts to near-black on white.

| Token | Hex | Usage |
|-------|-----|-------|
| `black` | `#040406` | App canvas (dark, default) |
| `zinc-950` | `#121317` | Panels / surfaces |
| `zinc-900` | `#18181B` | Raised surfaces / rows |
| `zinc-800` | `#27272A` | Borders / hairlines |
| `zinc-400` | `#A1A1AA` | Secondary text |
| `zinc-500` | `#71717A` | Meta / muted |
| `white` | `#FAFAFA` | Primary text (dark) · primary button |

### Accent spectrum (categorical — data & state only)
| Token | Hex | Typical role |
|-------|-----|--------------|
| blue | `#476CFF` | Links / info / primary data series |
| cyan | `#3DC5FA` | Secondary series |
| mint | `#3CEEAE` | **Valid** key · success · healthy |
| lime | `#DEF135` | Positive delta |
| gold | `#FFD55D` | **Rate-limited** / warning |
| red | `#FB1048` | **Invalid** / blocked / error |

These are a spectrum, not a brand color — never promote one to "the" accent. They carry meaning (key state) and chart series.

### Light theme
| Token | Hex | Usage |
|-------|-----|-------|
| canvas | `#FFFFFF` | Background |
| surface | `#FAFAFA` | Panels |
| border | `#E4E4E7` | Hairlines |
| ink | `#09090B` | Primary text · primary button |
| muted | `#52525B` | Secondary |

---

## Typography

- **Articulat CF** (`articulat-cf`) — display + UI + body. Articulat CF is an Adobe Typekit face (CORS-locked to Unkey's kit), so this showcase documents it as **≈ Inter** (Google) — a neutral grotesque of similar proportion.
- **JetBrains Mono** (`--font-jetbrains-mono`, the `.font-label` face) — keys, code, endpoints, request/response JSON, metrics, labels.

One role each: Articulat/Inter for human text, JetBrains Mono for anything that is a key, a number, or code.

| Role | Face | Spec |
|------|------|------|
| Display | Inter 600 | 52px, `-0.03em` |
| Heading | Inter 600 | 20px |
| Body | Inter 400 | 15px |
| Code / keys | JetBrains Mono 400 | 12–13px |

---

## Logo

The real Unkey **mark** — an abstract bracket/key glyph in two paths (from `favicon-dark.svg`, `viewBox 0 0 512 512`), themed via `--logo-mark` (white on dark, near-black on light). Pair it with the lowercase **"unkey"** wordmark set in Inter/Articulat.

---

## Signature component — API key control plane

Unkey's DNA in one panel: **create keys, then verify them under a rate limit.**

- A **keys list**: each row is a key (`sk_live_…` prefix in mono), a name, its rate limit (`100 / 60s`), request count, and an enabled dot. Selecting a key loads it into the console.
- A **verify console**: the real `unkey.keys.verify()` call beside its JSON response — `valid`, `code`, `permissions`, and `ratelimit: { limit, remaining, reset }`.
- A **rate-limit meter**. Each **Verify request** decrements `remaining` and returns `valid: true` (mint). When it hits zero, the response flips to `valid: false`, `code: "RATE_LIMITED"` (gold → red meter). **Reset window** restores it.

Deterministic — a counter drives the meter, fixed keys, no `Math.random`.

---

## Guardrails

**Do**
- Keep the canvas true near-black `#040406` with a zinc neutral scale; make white the primary action.
- Set every key, endpoint, and JSON value in JetBrains Mono — keys and data are always mono.
- Use the accent spectrum for **meaning**: mint = valid, gold = rate-limited, red = invalid/blocked.
- Show the core loop: a key list beside a live verify + rate-limit response.

**Don't**
- Promote one spectrum color to "the brand accent" — Unkey is monochrome; the colors are categorical.
- Add drop shadows or gradients to the primary button — it's a flat white (or near-black on light) surface.
- Render a raw API key in a proportional sans — keys are mono, and usually shown by prefix only.
- Invent a colored logo — the mark is monochrome (`--logo-mark`).
