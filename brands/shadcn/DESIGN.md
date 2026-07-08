# shadcn/ui — Design System

*"The Foundation for your Design System."* Not a component library you install — a set of beautifully designed components you **copy into your codebase** and own. The aesthetic is deliberately quiet: monochrome zinc, generous whitespace, hairline borders, and a token system (CSS variables) that is the real product. **Open Source. Open Code.**

> **Source of truth:** traced from the live `ui.shadcn.com` markup + rendered homepage, plus the canonical shadcn/ui token names and default (`zinc`) palette. Where a value is a design-system convention rather than a scraped literal, it's noted.

---

## Brand foundations

shadcn/ui has no loud brand color — that's the point. The default theme is neutral **zinc**: white surfaces, near-black text, muted grays for secondary content. Color is something *you* add via a base-color preset. Everything is driven by semantic CSS variables (`--background`, `--foreground`, `--primary`, `--muted`, `--border`, `--ring`, …) so a theme is just a set of token values.

- Monochrome by default; a single accent (`--primary`) is user-chosen.
- Surfaces are white/near-black; separation comes from **1px zinc borders**, not shadows.
- The `--radius` token scales every corner in the system at once.

---

## Color — semantic tokens

The system is defined by token *roles*, not fixed hues. Default base = **Zinc**.

### Core (Zinc default)
| Token | Light | Dark | Usage |
|---|---|---|---|
| `--background` | `#FFFFFF` | `#09090B` | Page canvas |
| `--foreground` | `#09090B` | `#FAFAFA` | Primary text |
| `--card` | `#FFFFFF` | `#101013` | Card / popover surface |
| `--muted` | `#F4F4F5` | `#1C1C1F` | Subtle fills, wells |
| `--muted-foreground` | `#71717A` | `#A1A1AA` | Descriptions, meta |
| `--border` / `--input` | `#E4E4E7` | `#27272A` | Hairlines, field borders |
| `--ring` | `#A1A1AA` | `#52525B` | Focus ring (tracks primary in color themes) |

### Primary (Zinc default — flips with theme)
| Token | Light | Dark |
|---|---|---|
| `--primary` | `#18181B` | `#FAFAFA` |
| `--primary-foreground` | `#FAFAFA` | `#18181B` |
| `--secondary` | `#F4F4F5` | `#27272A` |
| `--destructive` | `#EF4444` | `#EF4444` |

### Base-color presets (`--primary` swap)
Picking a base color changes `--primary` (+ `--ring`); surfaces stay neutral.
| Preset | Primary | Foreground |
|---|---|---|
| **Zinc** | `#18181B` / `#FAFAFA` (theme-flip) | contrast |
| **Rose** | `#E11D48` | `#FFFFFF` |
| **Blue** | `#2563EB` | `#FFFFFF` |
| **Green** | `#16A34A` | `#FFFFFF` |
| **Orange** | `#F97316` | `#1A1A1A` |
| **Violet** | `#7C3AED` | `#FFFFFF` |

**Contrast trap:** never hardcode primary-button text — it's `--primary-foreground`. Zinc flips (dark text on light primary in dark mode); Orange needs a near-black foreground for legibility.

---

## Typography

| Family | Role | Notes |
|---|---|---|
| **Geist** | Everything — headings, body, UI, labels | Vercel's grotesque; weights 400 / 500 / 600 / 700 |
| **Geist Mono** | Code, CLI, token names, metadata | `npx shadcn@latest add …`, CSS variables |

Both are on Google Fonts (CORS-open) and used directly.

- **Hero H1:** Geist, ~48px, weight 600, tight tracking (`-0.02em`).
- **Card titles:** Geist 600, ~16px. **Descriptions:** `--muted-foreground`, 14px.
- **Code / tokens:** Geist Mono, 13px.

---

## Spacing, radius, shadow

- **Radius:** the `--radius` token (default `0.5rem`). Cards use `--radius`, buttons/inputs `calc(--radius - 2px)`, small chips `calc(--radius - 4px)`. Presets: `0`, `0.25`, `0.5`, `0.75`, `1.0rem`.
- **Shadow:** minimal. Cards are flat with a 1px border; popovers/dialogs get a soft `shadow-md`. Depth is borders, not drop shadows.
- **Spacing:** 4px base grid. Buttons `h-9` (36px), inputs `h-9`, comfortable card padding (24px).

---

## Components

- **Button** — variants: `default` (primary fill), `secondary`, `outline` (border + transparent), `ghost` (hover fill only), `destructive`, `link`. Height 36px, radius `calc(--radius - 2px)`, medium weight, 14px.
- **Badge** — `default`, `secondary`, `outline`, `destructive`. Small, pill-ish, 12px.
- **Input** — 1px `--input` border, `h-9`, focus = 2px `--ring`.
- **Card** — `--card` surface, 1px border, radius `--radius`; title + `--muted-foreground` description.
- **Switch / Checkbox** — checked state uses `--primary`.
- **Tabs** — active trigger sits on a `--background` pill inside a `--muted` track.

---

## Signature — the theme customizer

The single most shadcn artifact: pick a **base color** + **radius**, and a live preview of real components re-skins instantly — then **copy the CSS variables** into your project. It embodies *"customize, extend, and build on. Open Code."*

- **Controls:** base-color swatches (Zinc / Rose / Blue / Green / Orange / Violet) and radius steps (`0 → 1.0rem`).
- **Live preview:** a "Create an account" card, button variants, badges, tabs and a switch — all driven by scoped CSS variables on the preview root, so `--primary`, `--ring` and `--radius` update everywhere at once.
- **Copy output:** the generated `:root { --primary … --ring … --radius … }` block, in Geist Mono — the thing you actually paste.
- **Deterministic:** presets are fixed token sets, no `Math.random()`.

---

## Guardrails

**Do**
- Keep surfaces monochrome (zinc); let a single `--primary` carry any color.
- Drive *everything* from semantic tokens — never hardcode a hex on a component.
- Separate with 1px `--border`, not shadows; scale corners with one `--radius`.
- Use `--muted-foreground` for descriptions/meta, `--foreground` for content.
- Set the primary-button text to `--primary-foreground` (Zinc flips, Orange goes dark).

**Don't**
- Don't introduce a loud brand hue as the default — neutrality is the identity.
- Don't lean on drop shadows for hierarchy; borders and spacing do the work.
- Don't mix font roles — Geist for UI, Geist Mono for code/tokens only.
- Don't hardcode button text color or you'll break a theme in one mode.
- Don't use `Math.random()` in the customizer — presets are deterministic.
