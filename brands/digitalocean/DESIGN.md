# DigitalOcean Design System

## Brand Overview

DigitalOcean is the developer-friendly cloud — simple, predictable infrastructure for builders.
The identity is optimistic and clean: the iconic **ocean blue `#0069FF`**, deep navy surfaces,
and a green for healthy resources. The product is the Control Panel — Droplets, databases, and
apps managed without ceremony. Light-first, on a cool off-white canvas.

> "AI-Native Cloud."

## Typography

- **Plus Jakarta Sans** — display / headings (real DO brand font, Google Fonts).
- **Inter** — body / UI (real, Google Fonts).
- **JetBrains Mono** — IP addresses, Droplet sizes, regions, commands (real, Google Fonts).

All three are the fonts DigitalOcean actually ships — used directly.

## Color Palette

### Primary
- Ocean Blue: `#0069FF` — brand, CTAs, links
- Blue Deep: `#1633FF` (hover)
- Navy: `#000C79`
- Ink: `#080B2D`

### Accent & Semantic
- Green (active): `#15CD72`
- Lime: `#80D34A`
- Warning: `#FFB020`
- Error: `#FF4747`

### Surfaces — Light
- Page: `#F9FAFE`
- Card: `#FFFFFF`
- Sunken: `#F1F3FB`
- Border: `#E1E5F0`

### Surfaces — Dark (real DO navy)
- Page: `#080B2D`
- Surface: `#11192E`
- Elevated: `#1A2444`
- Border: `#24335A`

### Text
- Primary (light `#080B2D` / dark `#EAEEFB`)
- Secondary: `#8690A9`
- Muted: `#BCC2C2`

## Logo

The **DigitalOcean mark** — the wave-in-circle "O" droplet (viewBox `0 0 24 24`, single path),
rendered in ocean blue `#0069FF` (or `currentColor` in monochrome contexts). Pairs with the
"DigitalOcean" wordmark set in Plus Jakarta Sans.

## Signature Component — Droplets

The Control Panel Droplets view: a list of Droplets with name, status (Active / powered off),
region (`NYC3`, `SFO3`…), size (`s-2vcpu-4gb`), public IP, and a CPU sparkline. A **Create
Droplet** action spins up a new Droplet that animates New → Booting → Active with an assigned
IP — the core DigitalOcean provisioning moment.

## Guardrails

**DO**
- Use ocean blue `#0069FF` for brand, CTAs, and links.
- Use green `#15CD72` only for healthy/active resources.
- Set IPs, regions, sizes, and commands in the mono stack.
- Keep the canvas cool off-white / navy so status colors read.
- Show region and size on every Droplet — developers scan for them.

**DON'T**
- Don't drift the blue lighter — the brand blue is `#0069FF`, not `#0080FF`.
- Don't invent dark surfaces; anchor on the real DO navy `#080B2D`.
- Don't use green for anything but healthy/active state.
- Don't set IPs or resource sizes in a proportional font.
- Don't hide a Droplet's status while it's provisioning.
