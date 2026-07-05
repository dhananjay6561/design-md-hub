# ElevenLabs — Design System

Design-token reference for **ElevenLabs** (elevenlabs.io), the AI audio research and deployment company. All values live-fetched from `elevenlabs.io` and its `_next/static/css` bundles (July 2026). ElevenLabs' identity is deliberately **monochrome** — near-black ink on an eggshell white, with a full color scale reserved for categorical tagging (voices, languages, model families), never as a single "brand accent."

---

## Brand voice

- Tagline (homepage hero): **"Generate ultra-realistic speech, videos, music, and sound effects."**
- Positioning line: research-driven — *"Showcasing the global impact of AI audio research."*
- Product surface names use plain, literal labels: **Text to Speech**, **Speech to Text**, **Voice Cloning**, **Voice Design**, **Studio**, **Dubbing**, **Music**, **Sound Effects**, **Conversational AI / Agents**.
- Primary CTAs on live site: **"Sign up"**, **"Get started free"**, **"Contact sales"**.

---

## Typography

Three real roles, all live-loaded from the site's own CDN (CORS-open, verified `access-control-allow-origin: *`).

| Role | Family | Source | Usage |
|------|--------|--------|-------|
| Display / UI | **Waldenburg** | `eleven-public-cdn.elevenlabs.io` woff2 (CORS ✅) | Hero H1, headings, body, buttons, all product UI |
| Mono | **Geist Mono** | Google Fonts (CORS ✅) | Model IDs, code, metadata, hex, spec chips |
| Body fallback | **Inter** | Google Fonts | Site also loads Inter as a UI fallback face |

Waldenburg is a proprietary grotesk by KMR/ElevenLabs. Real weights served: **300** (Buch), **400** (Normal), **700** (Fett), plus a condensed **WaldenburgFH** at 700. The CDN files are CORS-open so they are used directly (no `≈` fallback needed); `Waldenburg Fallback` maps to `local("Arial")` with metric overrides.

`@font-face` (real URLs from live CSS):
```
Waldenburg 300 → .../waldenburg/KMR-Waldenburg-Buch-latin.1f7863d3c4317f3d.woff2
Waldenburg 400 → .../waldenburg/KMR-Waldenburg-Normal-latin.47fcefe5bf77b4e5.woff2
Waldenburg 700 → .../waldenburg/KMR-Waldenburg-Fett-latin.e6b0db8ee0a63897.woff2
```

Type scale (from product/marketing surfaces): display 300–400 weight, tight tracking; headings 400/700; body 400; mono 400 for `eleven_multilingual_v2`-style identifiers.

---

## Color

ElevenLabs runs an **eggshell-white, ink-black** monochrome shell. There is **no single brand accent color** — the categorical scale (blue / cyan / green / magenta / orange / purple / red, each with a 50→950 ramp) tags voices, languages and states. Verify against live; do not invent a "brand teal/purple."

### Surfaces (light)
| Token | Hex | Usage |
|-------|-----|-------|
| `--eggshell` / `--page-background-color` | `#FDFCFC` | Page background |
| `--white-50` | `#FFFFFF` | Cards, panels |
| `--white-200` | `#F5F3F1` | Muted surface, marker background |
| `--neutral-50` | `#F2F2F2` | Subtle fill |
| `--neutral-100` | `#E5E5E5` | Hover fill |
| `--neutral-200` | `#DCDCDC` | Borders |

### Surfaces (dark)
| Token | Hex | Usage |
|-------|-----|-------|
| `.dark` background | `#0F1117` | Page background (live `rgb(15 17 23)`) |
| `--neutral-950` | `#1C1C1C` | Raised card / panel |
| `--neutral-900` | `#3D3D3D` | Dark-mode border (`.dark` sets `border-color:var(--neutral-900)`) |

### Text (neutral ramp)
| Token | Hex | Usage |
|-------|-----|-------|
| `--black` | `#000000` | Primary ink (light) |
| `--neutral-950` | `#1C1C1C` | Near-black text |
| `--neutral-500` | `#767676` | Secondary / muted text |
| `--neutral-400` | `#949494` | Tertiary / disabled |
| `--white-50` | `#FFFFFF` | Primary text (dark) |

### Categorical / semantic scale (ramp endpoints — real tokens)
| Family | 500 | Used for |
|--------|-----|----------|
| Blue | `#5D79DF` | Info / links |
| Cyan | `#19A2C1` | Audio / waveform accents |
| Green | `#10B978` | Success, "Ready" |
| Orange | `#F36F1C` | Warning, highlights |
| Red | `#EB524B` | Error, destructive |
| Purple | `#C47DE5` | Categorical tag |
| Magenta | `#D65CC8` | Categorical tag |

Each family has a full `50 / 100 / 200 / 300 / 400 / 500 / 600 / 700 / 800 / 900 / 950` ramp in the live CSS (e.g. green `#ECFDF4 → #022C20`, blue `#F2F5FC → #252846`).

---

## Models (real product identifiers)

From live copy and demo attributes:

| Model | Marketing name | Positioning (live copy) |
|-------|----------------|-------------------------|
| `eleven_v3` | Eleven v3 (alpha) | "The most expressive Text to Speech model ever released" |
| `eleven_multilingual_v2` | Eleven Multilingual v2 | "Our most consistent and lifelike Text to Speech model" |
| `eleven_turbo_v2_5` | Eleven Turbo v2.5 | "Our high-quality, low-latency Text to Speech model" |
| `eleven_flash_v2_5` | Eleven Flash v2.5 | "Our ultra-low latency Text to Speech model" |

Other real model IDs seen: `eleven_text_to_sound_v2`.

## Voices (real default library)

Current default voice-library names on the site: **Aria, Roger, Sarah, Laura, Charlie, George, Callum, River, Liam, Charlotte, Alice, Matilda, Will, Jessica, Eric, Chris, Brian, Daniel, Lily, Bill**. (Legacy v1 names Rachel/Adam/Antoni/Bella/Domi/Elli/Josh/Arnold/Sam still exist in the API but the site now surfaces the newer set above.)

Stability / Similarity / Style are the real Voice Settings sliders (0–1) in the TTS interface.

---

## Logo

Wordmark: lowercase-style "ElevenLabs" letterforms as a single `currentColor` SVG (viewBox `0 0 117 15`), real paths pulled from the live `<header>`. It inherits `currentColor`, so it flips ink→white between light and dark automatically. No standalone glyph mark is used in the site header.

---

## Guardrails

**DO**
- Keep the shell monochrome — ink `#000`/`#1C1C1C` on eggshell `#FDFCFC` (light) or `#0F1117` (dark).
- Use the categorical color ramps for tags, waveforms and states — not as a single brand accent.
- Use Waldenburg for all display and UI; Geist Mono only for model IDs, code and metadata.
- Use real model IDs (`eleven_multilingual_v2`, `eleven_turbo_v2_5`, `eleven_flash_v2_5`, `eleven_v3`) and real voice names.
- Let the logo inherit `currentColor` so it themes automatically.

**DON'T**
- Invent a single "ElevenLabs brand color" — the brand is monochrome; the scale is categorical.
- Use `#000` on the dark surface for text — flip to `#FFFFFF`.
- Over-saturate dark surfaces; step within the real neutral ramp (`#0F1117 → #1C1C1C → #3D3D3D`).
- Mix Waldenburg into code/metadata roles or Geist Mono into headings.
- Use `Math.random()` for the waveform — derive it deterministically from the input text.
