# Runway — Design System

Reference documentation for Runway's visual identity, distilled from the live site (runwayml.com, fetched 2026-07-05). Runway builds AI to simulate the world — generative video models (Gen-4.5, Gen-4, Gen-4 Turbo), Act-Two, Aleph, and General World Models research. The brand system is deliberately monochrome and editorial: warm off-white paper, near-black ink, a serif display face paired with a neutral grotesque, and almost no chromatic accent. Restraint is the identity.

> Ground-truth note: every color, font name, and string below was pulled from the live site's compiled CSS/HTML. Where the site exposes no confirmable value (e.g. no published semantic error/success palette), that is stated explicitly rather than guessed.

---

## Brand foundation

- **Tagline (hero H1):** "Building AI to Simulate the World"
- **Mission line:** "We are building AI to simulate the world through merging art and science."
- **Positioning line:** "Runway is being used by the world's leading organizations across industries."
- **Primary CTAs (verbatim):** `Try Runway`, `Get Started`, `Try now`, `Learn more`, `Explore the Research`, `Login`
- **Voice:** research-lab editorial. Sentence case, matter-of-fact, no exclamation. Product and model names are proper nouns (Gen-4.5, Act-Two, Aleph, GWM).

---

## Color

Runway's palette is intentionally monochrome. The two load-bearing brand tokens in the compiled CSS are `offBlack` and `offWhite` — note that neither is a pure `#000`/`#fff`; the off-white carries a warm paper tint that is part of the identity.

### Primary (brand ink + paper)
| Token | Hex | rgb | Usage |
|---|---|---|---|
| `offBlack` | `#0C0C0C` | `12 12 12` | Primary ink, dark surfaces, primary button bg |
| `offWhite` | `#EFEEE6` | `239 238 230` | Warm paper background (the signature off-white) |
| `black` | `#000000` | `0 0 0` | Pure black — used sparingly for max-contrast fills |
| `white` | `#FFFFFF` | `255 255 255` | Pure white surfaces, media frames |

### Surfaces
| Token | Hex | Usage |
|---|---|---|
| `offWhiteAlt` | `#F6F6F6` | Alternate light surface, cards, panels |
| `surface-100` | `#F7F7F7` | Muted light fill |
| `surface-line` | `#E5E5E5` | Hairline borders / dividers (light) |
| `surface-line-strong` | `#D4D4D4` | Stronger borders, control outlines (light) |
| `dark-800` | `#1A1A1A` | Elevated surface on dark |
| `dark-700` | `#3A3A3A` | Control / border on dark |

### Text
| Token | Hex | Usage |
|---|---|---|
| `ink` | `#0C0C0C` | Primary text on light |
| `ink-muted` | `#7C7C7C` | Secondary / caption text |
| `on-dark` | `#EFEEE6` | Primary text on dark (paper on ink) |
| `on-dark-muted` | `#9CA3AF` | Secondary text on dark |

### Semantic
Runway does **not** publish a chromatic semantic palette (no brand green/red for success/error is exposed in the compiled tokens — the product UI communicates state through neutrals, motion, and copy). For documentation-only status affordances in this system, states are expressed monochromatically:

| State | Treatment |
|---|---|
| Queued / neutral | `ink-muted` `#7C7C7C` on `offWhiteAlt` |
| Generating / active | `offBlack` fill + animated shimmer |
| Done / complete | `offBlack` text, solid ink border |

If a genuine positive/negative accent is ever required, borrow from the product-surface neutrals rather than introducing a new hue — Runway avoids brand color entirely.

---

## Typography

Two typefaces, both self-hosted by Runway and served CORS-open (`access-control-allow-origin: *` confirmed on the woff2 assets):

- **abcNormal** (ABC Normal, by Dinamo) — the neutral grotesque. Body, UI, labels, nav, buttons, metadata. CSS var `--abcNormal`, fallback stack `abcNormal, "abcNormal Fallback", Arial`.
- **timesNow** (Times Now, by Sharp Type) — high-contrast serif display. Reserved for hero headlines and large editorial statements only. CSS var `--timesNow`.

> Fallbacks for this showcase: ABC Normal and Times Now are proprietary. Runway's own woff2 files are CORS-open, so this system links ABC Normal directly where possible. Times Now has no free equivalent; the nearest documented fallback is a high-contrast serif — here **≈ "PT Serif" / Georgia** for the display role. These are marked "≈" wherever substituted.

### Scale
| Role | Family | Size | Weight | Notes |
|---|---|---|---|---|
| display / hero | timesNow (≈ serif) | 56px | 400 | Serif, tight leading, sentence case |
| headline | abcNormal | 32px | 500 | Section headlines |
| title | abcNormal | 20px | 500 | Card / product titles |
| body | abcNormal | 16px | 400 | Paragraph copy |
| ui / label | abcNormal | 14px | 400 | Controls, nav |
| caption / meta | abcNormal | 12px | 400 | Timestamps, metadata, mono-style chips |

---

## Logo

The Runway wordmark is a lowercase custom logotype "runway" (viewBox `0 0 84 19`), rendered with `fill-current` so it inherits ink color — black on paper, paper on ink. Real path data is embedded in `preview.html`. Do not recolor the mark; it is monochrome by design and adapts only between `offBlack` and `offWhite`.

---

## Product & model lexicon (real, verify before use)

- **Models:** Gen-4.5, Gen-4, Gen-4 Turbo, Gen-3 Alpha, Gen-3 Alpha Turbo, Aleph, Aleph 2.0
- **Tools / features:** Act-One, Act-Two, Motion Brush, Frames, Text to Video, Image to Video, Video to Video
- **Research:** General World Models (GWM), GWM Worlds, GWM Avatars, GWM Robotics
- **Programs:** Runway Studios, AI Film Festival, Gen:48, Creative Partners Program
- **Aspect ratios / output:** 16:9, 9:16, 1:1 · 720p / 1080p · 5s and 10s clips

---

## Spacing & radius

- Spacing scale (Tailwind-derived): 4 · 8 · 12 · 16 · 24 · 32 · 48 · 64px
- Radius: controls and cards use small radii (`6–8px`); media frames are near-square (`2–4px`). The brand leans rectilinear, not pill-heavy.
- Layout container max-width: `1600px` (`.rw-container`).

---

## Guardrails

**DO**
- Keep surfaces monochrome — warm off-white `#EFEEE6` paper and off-black `#0C0C0C` ink carry the brand.
- Reserve the serif (Times Now ≈) for hero/display only; everything functional is ABC Normal.
- Preserve the warm off-white tint `#EFEEE6` — do not flatten it to pure `#FFFFFF`.
- Let generated media (video frames) supply all the color; the chrome stays neutral.
- Use real model/tool names exactly (Gen-4.5, Act-Two, Aleph) — proper nouns, hyphenated.

**DON'T**
- Introduce a brand accent color — Runway has no green/blue/orange brand hue; adding one breaks the identity.
- Recolor the wordmark or add a gradient to it.
- Use the serif for body, labels, or UI text.
- Use pure `#000`/`#fff` as the default background when the branded off-black/off-white tokens apply.
- Communicate state with saturated color chips — Runway expresses status through neutrals, motion, and copy.
