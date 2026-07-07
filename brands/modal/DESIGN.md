# Modal — Design System

> High-performance AI infrastructure — the serverless platform for AI and data teams.

Modal lets you bring your own Python code and run CPU, GPU, and data-intensive workloads at scale, serverlessly — you decorate a function with `@app.function(gpu="A100")`, and Modal builds the image, cold-starts containers, and autoscales them out (and back to zero) in seconds. No clusters, no YAML.

The identity is a **warm near-black canvas lit by neon green** — a glowing, isometric **cube-M** and floating green cubes are the motif, echoing containers spinning up in the dark. Type is a friendly geometric display face (**Goga**) over Inter body and Fira Mono for code. It reads as serious infrastructure that's also fast, modern, and a little playful.

---

## Color

### Brand
| Token | Hex | Usage |
|---|---|---|
| green | `#7FEE64` | Primary — CTAs, links, active state, the signal color (`c-green-100`) |
| green-deep | `#09AF58` | Cube shadow face, deep end of the brand gradient |
| green-light | `#BFF9B4` | Cube highlight face, soft tint |
| cube gradient | `#80EE64 → 09AF58` | The logomark's lit face; glowing containers |
| green-ink (light mode) | `#10A550` | Readable green for text/links on white |

### Green scale (containers, fills, states)
`#1D231C` · `#222D20` · `#273823` · `#2D4327` · `#37582F` · `#416E36` · `#4C833E` · `#569846` · `#60AE4D` · `#6AC355` · `#75D95C` · `#7FEE64` — dark (`green-5`) to bright (`green-100`).

### Secondary accents (sparingly)
| Token | Hex | Usage |
|---|---|---|
| orange | `#FFAB5E` | Warm accent, warnings (`c-orange-100`) |
| pink | `#FF8DE6` | Accent / dataviz (`c-pink-100`) |
| dataviz | `#ADEAAB` `#D9866B` `#FFC1F7` `#4AA19D` `#DECB6C` `#648FE0` | Chart series |

### Surfaces & text (dark-first)
| Token | Dark | Light | Usage |
|---|---|---|---|
| canvas | `#131513` | `#FFFFFF` | App background (warm near-black) |
| panel | `#1A1C1A` | `#FFFFFF` | Cards |
| raised | `#252825` | `#EEF1EE` | Hover / elevated |
| border | `#2C2F2C` | `#E4E7E4` | Hairlines |
| text primary | `#F5F6F5` | `#131513` | `c-gray-100/0` |
| text secondary | `#B0B4B0` | `#4A4E4A` | Body (`c-gray-80` = `#D1D1D1`) |
| text muted | `#7D827D` | `#7D827D` | Meta / captions |

The **run console** stays dark in both themes (`#0E100E`) — it's a terminal.

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / headings | **Goga** (`medium 500`) | Modal's brand face (self-hosted variable font). **CORS-locked** off `modal-cdn.com`, so this preview uses **≈ Hanken Grotesk** (Google) as a close geometric-grotesque stand-in. All `h1–h5` / `.marketing-h*` use Goga with `ss01` on. |
| UI / body | **Inter** (Inter Variable, `400 / 500`) | The default body face (`--font-sans`). Labels, paragraphs, UI. |
| Code / mono | **Fira Mono** (`400 / 500`) | SDK source, CLI output, GPU labels, metrics — everything in the run console. |

Scale: hero 56–64px (Goga 500), section 40px, h3 30px, body 16px (Inter), code 12.5px (Fira Mono), labels 11px uppercase.

---

## Shape, spacing & motion

- **Radius:** buttons `8px` (`radius-lg`), cards & panels `10px`, container cubes `4px`, chips/pills `9999px`. Rounded but businesslike.
- **Spacing:** 8px grid. The run view reads left-to-right: your code → the containers it spins up → the metrics they produce.
- **Elevation:** flat panels with hairline borders on the warm canvas; green elements get a soft **glow** (`0 0 18px rgba(127,238,100,.45)`) rather than a drop shadow — light, like a lit cube.
- **Motion:** things **scale**. On a run, containers cold-start and light up one by one (autoscale 0→N), a progress bar fills as outputs complete, a throughput counter climbs, then containers wink out (scale to zero). Deterministic — no randomness.

---

## Components

- **Logomark** — the isometric **cube-M**: three faces, a bright `#80EE64→#09AF58` gradient front, a `#BFF9B4` highlight, deep-green sides. Pairs with the `Modal` wordmark.
- **Container cube** — a small green-gradient cube representing one running container (labeled `A100`); idle cubes are dim outlines, active ones glow.
- **Run console** — a dark terminal: `modal run app.py` streaming build → cold-start → autoscale → complete logs, with a live container grid and metrics (containers, outputs, throughput).
- **Buttons** — solid **green** primary (`#7FEE64`, dark ink text); ghost secondary with a green ring; mono for CLI-style actions.
- **GPU pill** — a mono chip (`A100` / `H100` / `T4`) in the green family.

---

## Guardrails

**Do**
- Anchor on a **warm near-black** canvas and let **neon green** (`#7FEE64`) be the single signal color.
- Use the **cube** motif — glowing green cubes as containers, the isometric cube-M as the mark.
- Show the serverless story: containers **cold-start, autoscale out, and scale to zero** — motion is scaling.
- Set headings in Goga (or a geometric-grotesque stand-in), body in Inter, all code/CLI/metrics in Fira Mono.
- Use real SDK vocabulary: `modal.App`, `@app.function(gpu="A100")`, `.map()`, `modal run`, `@app.local_entrypoint()`.
- Give green a soft **glow**, not a heavy shadow.

**Don't**
- Put green on a light/white canvas as the primary identity — Modal is dark-first, warm-black.
- Introduce a second bright brand hue; orange/pink are sparing accents, not co-leads.
- Use flat gray boxes for containers — they're lit green cubes.
- Set code or metrics in the body/display font — the console is Fira Mono.
- Render green as pure `#00FF00`; it's the specific warm lime `#7FEE64`.
