# Docker Design System

## Overview

Docker is the platform developers use to build, share, and run container applications — "we handle the tedious setup, so you can focus on the code." The visual language is built around one confident, unmistakable blue and the Moby Dock whale. It reads as infrastructure you can trust: clean, technical, enterprise-grade, but still developer-first and approachable.

**Brand personality:** Reliable, universal, developer-first, the container standard.

**Positioning (live copy):** "91% of the Fortune 100 already run on Docker · 20B+ pulls a month on Docker Hub · 20M+ developers build on Docker every day."

---

## Colors

Docker is **light-first** on the marketing surface (white panels on a cool `#f4f6f9` page) with a navy-tinted dark mode. The one non-negotiable is Docker Blue `#1d63ed`.

### Primary
| Token | Hex | Usage |
|-------|-----|-------|
| `--docker-blue` | `#1D63ED` | Primary brand, buttons, links, the whale mark |
| `--blue-bright` | `#2560FF` | Link hover, focus, brighter accent (dark mode brand) |
| `--navy` | `#00153C` | Deep navy — headings on light, logo default fill |
| `--blue-soft` | `#5B9CF0` | Soft accent, illustrations, secondary highlights |

### Surfaces — Light
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#FFFFFF` | Cards, panels, primary surface |
| `--bg2` | `#F4F6F9` | Page background |
| `--bg3` | `#E6EBF2` | Fills, hover, tertiary surface |
| `--border` | `#E3E6EA` | Default borders, dividers |
| `--term-bg` | `#0C1424` | Terminal / code surface (always dark) |

### Surfaces — Dark
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#0F1A2E` | Cards, panels |
| `--bg2` | `#0B1220` | Page background |
| `--bg3` | `#14233D` | Elevated, hover |
| `--border` | `#1F3350` | Borders, dividers |

### Text
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `--text` | `#00153C` | `#E6EBF2` | Headings, body |
| `--text2` | `#475569` | `#8AA1C5` | Labels, secondary |
| `--text3` | `#94A3B8` | `#5B7398` | Muted, placeholder |

### Semantic
| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#27C93F` | Container running, healthy, build succeeded |
| `--warning` | `#FFBD2E` | Restarting, image outdated |
| `--danger` | `#FF5F56` | Container exited, error, failed pull |

---

## Typography

Three fonts, three strict roles.

| Role | Font | Notes |
|------|------|-------|
| Display / headings | **Repro** (≈ Space Grotesk) | Docker's headings use ABC Repro; Space Grotesk is the CORS-safe free substitute |
| UI / body | **Inter** | All body, labels, nav, buttons, table cells |
| Mono / code | **JetBrains Mono** | Terminal, CLI specimens, image tags, metadata |

### Scale
| Token | Size | Weight | Sample |
|-------|------|--------|--------|
| `display-2xl` | 52px | 700 | Docker |
| `display-xl` | 34px | 700 | Build better, together |
| `display-md` | 22px | 600 | Start local. Scale anywhere. |
| `text-lg` | 16px | 400 | Body / lead copy |
| `text-sm` | 13px | 400 | UI copy, table cells |
| `ui-mono` | 12px | 400 | `docker run -d -p 80:80 nginx` |

---

## Components

- **Buttons:** solid Docker-blue primary (`#1D63ED`, white text — safe in both themes), outline secondary, ghost link. Radius `8px`.
- **Containers table:** the Docker Desktop pattern — name, image, status dot, port mapping, CPU. Green dot = running, gray = exited.
- **Badges:** status (`Running`, `Exited`, `Paused`) and image tags (`nginx:latest`, `redis:7-alpine`) in mono.
- **Terminal:** dark `#0C1424` surface with macOS traffic-light dots, mono body, blue prompt.
- **Inputs:** 1px border, `#1D63ED` focus ring at 3px / 30% alpha.

### Radius & elevation
| Token | Value |
|-------|-------|
| `radius-sm` | 6px |
| `radius-md` | 8px |
| `radius-lg` | 12px |
| `shadow-card` | `0 1px 2px rgba(0,21,60,.06), 0 4px 16px rgba(0,21,60,.06)` |

---

## Signature component

**Docker CLI terminal.** The universal Docker moment: type a command, watch it run. Supports real commands — `docker run`, `docker ps`, `docker images`, `docker pull`, `docker build`, `docker compose up`, `docker --version` — with realistic layer-pull and build output. Output history is capped at 20 lines.

If you saw only this terminal with no branding, the `docker run` / layer-pull output would be unmistakable.

---

## Guardrails

**DO**
- Use Docker Blue `#1D63ED` as the single primary — one confident blue, not a rainbow.
- Keep the whale mark blue; render it on white or navy, never on a busy photo.
- Keep surfaces neutral (white / `#f4f6f9`) and let the blue carry emphasis.
- Use green only for genuine "running / healthy / succeeded" states.
- Pair status color with a label or dot — never color alone.

**DON'T**
- Don't use the old cyan `#2496ED` — the current brand blue is `#1D63ED`.
- Don't recolor the whale into gradients or off-brand hues.
- Don't use pure black `#000` for dark surfaces — Docker's dark is navy-tinted (`#0B1220`).
- Don't use the macOS traffic-light trio as decorative UI accents — they're terminal chrome / status only.
- Don't set display headings in the mono or body font — Repro/Space Grotesk owns headings.
