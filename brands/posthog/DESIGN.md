# PostHog – Design System Reference

> **Brand:** PostHog  
> **Tagline:** We make dev tools for product engineers  
> **Description:** All your developer tools in one place. PostHog gives engineers everything to build, test, measure, and ship successful products faster.  
> **Source:** Live CSS extracted from `posthog.com/styles.ea523234e42160aa985c.css` on 2026-06-24

---

## Typography

### Font Families

| Role | Family | Source |
|------|--------|--------|
| Display / Hero | **Squeak** (Bold 700) | `/fonts/squeak-bold-webfont.woff2` — PostHog's own CDN |
| UI Body | **IBM Plex Sans Variable** | `posthog.com/static/ibm-plex-sans-latin-wght-normal-*.woff2` (variable, 100–700) |
| Code / Mono | **Source Code Pro** | Inlined base64 data URI in CSS bundle |

```css
@font-face {
  font-family: Squeak;
  font-style: normal;
  font-weight: 700;
  src: url(/fonts/squeak-bold-webfont.woff2) format("woff2"),
       url(/fonts/squeak-bold-webfont.woff) format("woff");
}

@font-face {
  font-display: swap;
  font-family: IBM Plex Sans Variable;
  font-style: normal;
  font-weight: 100 700;
  src: url(/static/ibm-plex-sans-latin-wght-normal-57bde7cafd4d43a2790a7240a25ea948.woff2)
       format("woff2-variations");
}
```

### Type Scale (Tailwind)

| Token | Size | Usage |
|-------|------|-------|
| `text-2xs` | 0.625rem / 10px | Micro labels, timestamps |
| `text-xs` | 0.75rem / 12px | Captions, meta text |
| `text-sm` | 0.875rem / 14px | Secondary body, table cells |
| `text-base` | 1rem / 16px | Primary body copy |
| `text-lg` | 1.125rem / 18px | Lead text, card headings |
| `text-xl` | 1.25rem / 20px | Section headings |
| `text-2xl` | 1.5rem / 24px | Page subheadings |
| `text-3xl` | 1.875rem / 30px | Page headings |
| `text-4xl` | 2.25rem / 36px | Hero sub |
| `text-5xl` | 3rem / 48px | Hero headings |
| `text-6xl` | 3.75rem / 60px | Display |
| `text-7xl` | 4.5rem / 72px | Display XL |

---

## Color System

PostHog uses a dual-scheme system. The app UI (LemonUI) uses CSS custom properties as **raw RGB triplets** so Tailwind can compose opacity variants (`rgb(var(--bg) / 0.5)`). The marketing site uses named utility classes from a custom Tailwind config.

### Brand & Named Colors

Extracted from `fill-*` / `bg-*` utility classes in the live CSS bundle:

| Name | Hex | Usage |
|------|-----|-------|
| `red` (primary) | `#F54E00` | Brand orange-red; CTAs, highlights, swiper active |
| `yellow` | `#F7A501` | Secondary accent; dark-mode swiper, charts |
| `orange` | `#EB9D2A` | Charts, callouts |
| `green` | `#6AA84F` | Success states, data |
| `teal` | `#29DBBB` | Analytics charts |
| `teal-2` | `#6BC0B3` | Chart series variant |
| `seagreen` | `#30ABC6` | Charts, info badges |
| `sky-blue` | `#2EA2D3` | Info |
| `blue` | `#2F80FA` | Links, focus rings |
| `blue-2` | `#589DF8` | Chart series 2 |
| `light-blue` | `#9FC4FF` | Pale blue accent |
| `lilac` | `#8567FF` | Feature flags |
| `purple` | `#B62AD9` | Session replay |
| `purple-2` | `#40396E` | Dark purple surface |
| `light-purple` | `#E2D6FF` | Light purple background |
| `pink` | `#E34C6F` | Error/alert |
| `salmon` | `#F35454` | Error red |
| `gold` | `#FFBA53` | Warning highlight |
| `lime-green` | `#96E5B6` | Light success |
| `tan` | `#EEEFE9` | Light page background |
| `navy` | `#1E2F46` | Dark surface |
| `dark` | `#1E1F23` | Dark page background |
| `brown` | `#3B2B26` | Warm dark surface |
| `gray` | `#8F8F8C` | Neutral text |
| `burnt-orange` | `#DF6133` | Charts alt |
| `creamsicle` | `#FFD699` | Warm highlight |
| `fuchsia` | `#A621C8` | Purple accent |

### Dark Color Variants

| Name | Hex |
|------|-----|
| `burnt-orange-dark` | `#8E2600` |
| `creamsicle-dark` | `#E38907` |
| `gold-dark` | `#E38907` |
| `pink-dark` | `#8C0D3B` |
| `pale-blue-dark` | `#648DC2` |
| `teal-2-dark` | `#34796F` |
| `red-2-dark` | `#C03300` |
| `light-yellow-dark` | `#C7982B` |
| `fuchsia-dark` | `#74108D` |
| `light-blue-dark` | `#1E2F46` |
| `purple-2-dark` | `#3C3154` |

### LemonUI App Theme Tokens

CSS custom properties as raw `R G B` triplets — used with Tailwind's `rgb(var(--token) / opacity)` pattern:

#### Light Mode (`.light [data-scheme=primary]`)

```css
--bg:             253 253 248;   /* #FDFDF8 warm white */
--accent:         229 231 224;   /* #E5E7E0 light gray-green */
--border:         191 193 183;   /* #BFC1B7 */
--input-bg:       238 239 233;   /* #EEEFE9 (= tan) */
--input-bg-hover: 238 239 233;
--input-border:   210 211 204;   /* #D2D3CC */
--text-primary:   77 79 70;      /* #4D4F46 dark olive */
--text-secondary: 101 103 94;    /* #65675E */
--text-muted:     158 160 150;   /* #9EA096 */
```

#### Dark Mode (`.dark [data-scheme=primary]`)

```css
--bg:              30 31 35;     /* #1E1F23 */
--accent:          45 46 55;     /* #2D2E37 */
--border:          62 66 79;     /* #3E424F */
--input-bg:        37 38 43;     /* #25262B */
--input-bg-hover:  34 35 32;     /* #222320 */
--input-border:    50 52 63;     /* #32343F */
--input-border-hover: 176 180 196; /* #B0B4C4 */
--text-primary:    234 236 246;  /* #EAECF6 */
--text-secondary:  174 179 194;  /* #AEB3C2 */
--text-muted:      98 102 116;   /* #626674 */
```

#### Marketing Site Themes

```css
/* Light page background */
theme-color: #E5E7E0;

/* .dark background */
background-color: #1d1f27;

/* Squeak chat widget vars */
--squeak-primary-color: 0,0,0;        /* light */
--squeak-button-color: 245,78,0;      /* brand orange */
--squeak-primary-color: 255,255,255;  /* dark */
--swiper-pagination-color: #f7a501;   /* dark mode swiper */
```

---

## Spacing

PostHog uses Tailwind's default 4px base spacing scale.

| Token | Value |
|-------|-------|
| `space-1` | 4px |
| `space-2` | 8px |
| `space-3` | 12px |
| `space-4` | 16px |
| `space-5` | 20px |
| `space-6` | 24px |
| `space-8` | 32px |
| `space-10` | 40px |
| `space-12` | 48px |
| `space-16` | 64px |

---

## Border Radius

PostHog customizes Tailwind's radius scale. The standout value is `rounded-lg` = **20px**, much larger than Tailwind's default — it's PostHog's signature card radius.

| Tailwind class | Value | Usage |
|----------------|-------|-------|
| `rounded-xs` | 2px | Micro inline tags |
| `rounded-sm` | 4px | Buttons, inputs, small chips |
| `rounded` | 0.25rem / 4px | Generic |
| `rounded-md` | 0.375rem / 6px | Menus, tooltips |
| `rounded-lg` | **20px** | Cards, modals, insight panels (PostHog signature) |
| `rounded-xl` | 0.75rem / 12px | Feature cards |
| `rounded-2xl` | 1rem / 16px | Hero blocks |
| `rounded-full` | 9999px | Pills, badges, avatars |

---

## Shadows

PostHog's LemonUI relies on borders for separation, with minimal shadow depth:

```css
/* Focus ring — primary orange */
box-shadow: 0 0 0 3px rgba(245, 78, 0, 0.25);

/* Slider focus */
box-shadow: 0 0 0 5px #96dbfa;

/* Light-mode card lift */
box-shadow: 0 0 4px #d9d9d9;

/* Dark scrollbar thumb */
background-color: hsla(0, 0%, 100%, 0.2);   /* hover: 0.3 */
```

---

## Components

### Buttons (LemonButton)

```css
/* Primary / CTA — "Get started – free" */
background: #F54E00;
color: #ffffff;
border-radius: 4px;
font-weight: 600;
height: 34px;
padding: 0 16px;

/* Secondary / Ghost */
background: transparent;
border: 1px solid rgb(var(--border));
color: rgb(var(--text-primary));

/* Danger / Highlight */
background: rgba(245, 78, 0, 0.1);
color: #F54E00;
border: 1px solid rgba(245, 78, 0, 0.3);
```

**Real button labels from posthog.com:**
- "Get started – free"
- "Talk to a human"
- "Sign up ↗"
- "Ask a question"

### Inputs

```css
background: rgb(var(--input-bg));
border: 1px solid rgb(var(--input-border));
border-radius: 4px;
height: 34px;
font-family: IBM Plex Sans Variable;
font-size: 0.875rem;
transition: border-color 0.15s, box-shadow 0.15s;

/* Focus */
border-color: rgb(var(--input-border-hover));
box-shadow: 0 0 0 3px rgba(245, 78, 0, 0.2);
```

### Tags / Badges (LemonTag)

From live CSS — `.lemon-tag`:

```css
background: rgba(0, 0, 0, 0.15);
border-radius: 4px;
color: #2d2d2d;
display: inline;
font-size: 0.75em;
font-weight: 700;
line-height: 1rem;
padding: 2px 6px;
text-transform: uppercase;
```

Semantic badge colors map to PostHog's named palette:
- **Success:** `#6AA84F` / `lime-green` bg at 15% opacity
- **Warning:** `#F7A501` / `gold` bg at 15% opacity
- **Error:** `#F35454` / `salmon` bg at 15% opacity
- **Info:** `#2F80FA` / `blue` bg at 15% opacity

### Cards (LemonCard)

```css
background: rgb(var(--accent));       /* slightly off-bg */
border: 1px solid rgb(var(--border));
border-radius: 20px;                  /* rounded-lg — PostHog signature */
padding: 24px;
```

---

## Signature Component — Product Analytics Dashboard

**The Events stream and Funnel chart** are PostHog's most recognizable UI patterns:

### Events Table

Real-time stream of captured events per user:

```css
/* Table header */
background: rgb(var(--accent));
border-bottom: 1px solid rgb(var(--border));
font-size: 0.75rem;
font-weight: 600;
text-transform: uppercase;
letter-spacing: 0.06em;
color: rgb(var(--text-muted));

/* Row */
border-bottom: 1px solid rgb(var(--border));
transition: background 0.1s;

/* Row hover */
background: rgb(var(--accent) / 0.5);

/* Cell */
font-size: 0.875rem;
padding: 8px 12px;

/* Event name pill */
font-family: Source Code Pro, monospace;
font-size: 0.75rem;
background: rgba(245, 78, 0, 0.12);
color: #F54E00;
border-radius: 4px;
padding: 2px 8px;
```

### Funnel Bars

```css
/* Funnel bar container */
border-radius: 4px;
overflow: hidden;
height: 32px;

/* Converted fill */
background: #F54E00;        /* primary orange-red */

/* Dropped fill */
background: rgb(var(--border));
opacity: 0.4;
```

### Person Chips

User identifiers shown as pill links:

```css
display: inline-flex;
align-items: center;
gap: 6px;
padding: 2px 8px;
border-radius: 9999px;     /* rounded-full */
background: rgb(var(--accent));
border: 1px solid rgb(var(--border));
font-family: Source Code Pro, monospace;
font-size: 0.75rem;
```

---

## Guardrails

### Do

- Use **Squeak** only for hero/display headings — never body copy or UI text
- Use **IBM Plex Sans Variable** for all UI text, including headings below `text-3xl`
- Use `#F54E00` (red) as the primary CTA color — this is PostHog's brand orange-red
- Use **`rounded-lg` (20px)** for product cards, modals, and insight panels — PostHog's signature radius
- Pair warm `tan` (`#EEEFE9`) background with dark-olive text (`#4D4F46`) in light mode — PostHog's palette has olive/green undertones, not cool gray
- Use the **RGB triplet** CSS var pattern (`rgb(var(--bg) / 0.5)`) when composing transparent colors in LemonUI
- Keep data-dense: PostHog UIs pack information tightly — use 8px padding in table cells
- Use `Source Code Pro` for user IDs, event names, and raw identifier strings in data tables

### Don't

- Don't use `#F54E00` for error states — PostHog uses `salmon` (`#F35454`) or `pink` (`#E34C6F`) for errors, not the brand orange
- Don't use pure black (`#000`) or pure dark gray for backgrounds — dark mode bg is `#1E1F23`, a warm dark charcoal with slight olive undertone
- Don't apply `rounded-lg` (20px) to small buttons or inputs — those use `rounded-sm` (4px)
- Don't mix **Squeak** with **IBM Plex Sans** in the same heading hierarchy — Squeak is for hero display only
- Don't use `rgba(#hex)` syntax in CSS vars — the RGB triplet pattern (`R G B`) is required for Tailwind opacity composition
- Don't put more than one primary orange CTA per view — `#F54E00` is high-energy and must anchor one clear action
- Don't use cool gray neutrals — PostHog's neutral scale has warm olive/green undertones throughout
- Don't use `blue` (`#2F80FA`) as the brand primary — PostHog's primary action color is orange-red, not blue
