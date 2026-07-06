# Family — Design System

> Your favorite crypto wallet.

Family is a beautiful, self-custody Ethereum wallet designed to make crypto easy for everyone. It is built for iOS and is known for having some of the best UI, UX, and micro-interactions in the entire web3 space. The design language is warm, tactile, and unmistakably native-feeling — soft beige surfaces, one confident blue, generously rounded corners, and motion that springs.

Design principles: **flawless essentials** (send, receive, swap in the fewest taps), **see everything clearly** (real-time balances, animated price charts), and **truly yours** (fully self-custodial — only you hold the keys). Every screen is designed so that something as complex as a crypto wallet feels approachable for "normies."

---

## Color

Family's palette is a single, confident **blue** on a soft **warm-beige** canvas, with an iOS-flavored semantic set. All values are from the live product CSS (both `#hex` and `color(display-p3 …)` are shipped; the hex is the sRGB fallback).

### Brand blue
| Token | Hex | Usage |
|---|---|---|
| `--app-blue` | `#018DFF` | The iconic Family blue — primary actions, the app icon, links |
| `--blue` | `#3784F4` | Secondary blue for fills and charts |
| `--color-anchor` | `#6187FE` | Inline text links / anchors |
| `--graphic-blue` | `#7DC4FF` | Illustration blue |
| `--graphic-blue-alt` | `#4DAFFF` | Brighter illustration blue (also the dark-mode accent) |
| `--graphic-blue-pale` | `#8ECCFF` | Palest graphic blue |
| `--blue-light` | `#EEFBFD` | Tinted blue surface / info background |

### Surfaces (warm neutral)
| Token | Hex | Usage |
|---|---|---|
| `--beige` | `#FBFAF9` | App background (light) |
| `--beige-dark` | `#EAEAEA` | Recessed surface / dividers (light) |
| Ink 900 | `#171717` | App background (dark) |
| Ink 950 | `#121212` | Deepest surface (dark) |
| `--color-border` | `#E8E8E8` | Hairline borders (light) |

### Text
| Token | Hex | Usage |
|---|---|---|
| `--color-text` / `--color-primary` | `#343433` | Primary text |
| `--body` | `#494340` | Body copy (P3 `0.286 0.267 0.251`) |
| `--body-muted` | `#848281` | Muted / secondary text |

### Semantic (iOS-flavored)
| Token | Hex | Usage |
|---|---|---|
| `--app-green` | `#34C759` | Positive / receive / success |
| `--color-valid` | `#00C454` | Valid input |
| `--color-invalid` | `#FF4E4E` | Error / destructive |
| `--color-warning` | `#F6C30F` | Warning |
| `--gold` / graphic-gold | `#FEBE44` | Highlight / rewards |
| `--graphic-orange` | `#FF5310` | Send / outgoing accent |
| `--app-pink` | `#F966AC` | Playful accent |

**Asset chip colors** (for token logos): ETH `#627EEA`, USDC `#2775CA`, Base `#0052FF`, Optimism `#FF0420`, Polygon `#8247E5`, Arbitrum `#12AAFF`.

---

## Typography

Family self-hosts two proprietary typefaces (both served CORS-open from `family.co/fonts`) plus a mono for addresses.

| Role | Family | Notes |
|---|---|---|
| Display + UI | **Family** (`Regular 400 / Medium 500 / SemiBold 600`) | The namesake typeface — the primary stack is `"Family", -apple-system, BlinkMacSystemFont, …`. Used for hero, headings, body, labels, buttons. |
| Numerals / metrics | **LFESans** (`Regular / Medium / SemiBold / Bold`) | Secondary Family cut, used here for large tabular balances and price figures. |
| Addresses / hex | **JetBrains Mono** | Wallet addresses, ENS, token amounts, hex codes. |

Type scale: hero 44–52px, section headings 22px, balance display 40–56px (tabular-nums), body 14–15px, labels 11px uppercase `letter-spacing:.06em`, mono chips 11–12px.

---

## Shape, spacing & motion

- **Radius (iOS-flavored, generous):** cards `20px`, inner tiles `16px`, buttons/pills `9999px` (fully round) or `14px`, inputs `12px`. Family leans rounder than most dev-tool brands.
- **Spacing:** 8px base grid. Cards padded `18–22px`. Comfortable, airy — never cramped.
- **Elevation:** soft, low, warm shadows — `0 12px 40px rgba(0,0,0,.10)`. No hard borders on the primary card; it floats on the beige canvas.
- **Motion is the brand.** Interactions spring rather than fade — balances count up, price charts scrub with the numbers animating in real time, sheets slide with overshoot. Use spring-like easing (`cubic-bezier(.34,1.56,.64,1)`) for entrances; keep durations short (150–300ms). Motion should feel *physical*, never linear.

---

## Components

- **Balance header** — a large tabular numeral (LFESans) with an animated up/down `%` change chip in green/red, sitting above a scrubbable price sparkline.
- **Token rows** — round asset chip (brand color) + name + secondary network label, right-aligned balance + fiat value. Fewest possible taps.
- **Primary button** — full-width, fully rounded, `--app-blue` fill, white text, springs on press.
- **Segmented tab bar** — Wallet / Swap / Activity, iOS-style, pill selector slides between segments.
- **Watch-only chip** — enter an address or ENS to follow any wallet in view-only mode.

---

## Guardrails

**Do**
- Lead with one blue (`#018DFF`) on the warm beige canvas — restraint is the look.
- Make every number animate — balances count, charts scrub. Motion is the product.
- Round generously; keep surfaces soft and shadows warm and low.
- Use real tokens, networks, and ENS names — Ethereum mainnet + L2s (Optimism, Base, Arbitrum, Polygon, zkSync).
- Keep flows to the fewest taps — send, receive, swap should feel effortless.

**Don't**
- Introduce a second brand hue — no rainbow gradients competing with the blue.
- Use hard, cold borders or pure `#000`/`#fff` — the canvas is warm (`#FBFAF9`).
- Ship linear, abrupt transitions — everything should spring.
- Imply custody of user funds — Family is fully self-custodial; only the user holds the keys.
- Use sharp corners or dense, cramped layouts — the app breathes.
