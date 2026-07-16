# Suno — Design System

> AI Music Generator.
> Create stunning original music for free in seconds. Start with a simple prompt or dive into pro editing tools — your next track is just a step away.

Suno's identity is a **dark warm studio**: a near-black canvas washed with a colorful orange→pink→purple **aura**, an editorial serif for the big statements, a neutral grotesque for everything else, and a signature **orange→pink gradient** on the one button that matters — *Create*. Color is generous — a full categorical spectrum carries song variety, genre tags, and album art.

Dark-default (the marketing hero and the music-making app are both dark); light is fully supported.

---

## Colors

### Brand
| Token | Hex | Usage |
|-------|-----|-------|
| `strawberry-600` | `#FD429C` | Brand pink (dark) — accent, "Join Suno" CTA, active |
| `strawberry-500` | `#DE1677` | Brand pink (light) — deeper for contrast on paper |
| `create-gradient` | `#E14C1E → #DD2C5D` | The *Create* button — orange→pink, top→bottom |
| `aura` | `#E14C1E · #DD2C5D · #AC4BFF` | Blurred radial bloom behind the hero |

### Neutral (Suno calls the scale "dumbo") — warm
| Token | Hex (dark) | Hex (light) | Usage |
|-------|------------|-------------|-------|
| `bg-primary` | `#101012` | `#F7F4EF` | Canvas |
| `bg-secondary` | `#1C1C1F` | `#EDEAE4` | Cards / panels |
| `bg-raised` | `#252529` | `#FCFBF9` | Wells / inputs |
| `fg-primary` | `#F7F4EF` | `#101012` | Primary text |
| `fg-secondary` | `#C2C2C1` | `#5B5B62` | Secondary text |
| `fg-tertiary` | `#A3A3A3` | `#7D7C83` | Meta |
| `border` | `rgba(255,255,255,.10)` | `rgba(0,0,0,.10)` | Hairlines (translucent) |

### Accent spectrum (song / genre / album variety)
| Name | Hex | | Name | Hex |
|------|-----|--|------|-----|
| pink (strawberry) | `#FD429C` | | green (slime) | `#02D95C` |
| orange (pumpkin) | `#FF6A00` | | blue (dodger) | `#1F8BFF` |
| red (vermilion) | `#F8441B` | | purple | `#AC4BFF` |

### Semantic
| State | Hex | Meaning |
|-------|-----|---------|
| success | `#02D95C` | Done / ready |
| generating | `#FF6A00` | Composing |
| error | `#F8441B` | Failed |

---

## Typography

All three faces below are Suno's real self-hosted fonts, **CORS-open** (`access-control-allow-origin: *`) — used directly from `suno.com/static-p/`.

- **PP Editorial New** — editorial display serif for the hero statement ("Make a house song about quitting your job"). Weights Light 300 / Regular 400.
- **PP Neue Montreal** — neutral grotesque for UI, body, nav, buttons, labels. Weights Regular 400 / Medium 500 / SemiBold 600.
- **JetBrains Mono** — durations, counts, IDs (Suno ships Input Mono / SFMono; JetBrains Mono is the Google-hosted stand-in for the same role).

| Role | Face | Spec |
|------|------|------|
| Display | PP Editorial New 400 | 56px, `-0.02em`, tight leading |
| Heading | PP Neue Montreal 600 | 20px |
| Body | PP Neue Montreal 400 | 15px |
| Meta / duration | JetBrains Mono | 12px, tabular-nums |

---

## Logo

The Suno **mark** — two interlocking teardrop/wave shapes (`viewBox 0 0 24 24`, single path, Simple Icons `suno`) — recolored via `--logo` (off-white on dark, near-black on light), beside a **Suno** wordmark set in PP Neue Montreal SemiBold. (The live site's `SUNO` wordmark is an animated morphing SVG — the clean mark reads more reliably.)

---

## Signature component — The song generator

Suno's whole product: **a prompt becomes a finished song in seconds.**

- A **"Chat to make music"** prompt bar + style chips (House · Lo-fi · Folk · Synthwave) — pick a preset or keep the default.
- **Create** (the orange→pink gradient button) runs a deterministic generation sequence — *Composing → Adding vocals → Mastering* — with a progress bar in Suno orange.
- Two versions land as **song cards** (Suno always returns 2): each with a **procedural album-art** gradient mesh, a title derived from the prompt, colored **genre tags** from the accent spectrum, a **waveform** bar visualization, a play/pause toggle, and a duration.
- **Play** animates the waveform (an equalizer bounce) and sweeps a progress scrubber; the album art gently pulses.

Each preset produces a genuinely different song — its own album-art palette, genre tags, title, and deterministic waveform shape (index/hash-based bar heights). No `Math.random`.

---

## Guardrails

**Do**
- Keep the canvas dark warm `#101012` (light = warm paper `#F7F4EF`); the neutrals are *warm* ("dumbo"), never cold grey.
- Reserve the **orange→pink gradient** (`#E14C1E → #DD2C5D`) for the one *Create* action; use strawberry pink `#FD429C` for other accents.
- Let the accent **spectrum** carry song/genre/album variety — this is a colorful brand, color is welcome in the *content*.
- Set the hero statement in **PP Editorial New** serif; everything else in PP Neue Montreal.

**Don't**
- Use cold grey neutrals — the dumbo scale is warm.
- Put the Create gradient on secondary buttons, or use more than one gradient button per view.
- Set body or UI in the serif — the serif is display-only (hero + big song titles).
- Invent album-art or waveforms with `Math.random` — keep them deterministic per prompt.
