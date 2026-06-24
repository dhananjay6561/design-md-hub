# Prisma – Design System Reference

> Values extracted from live CSS bundles at prisma.io on 2026-06-24.
> Sources: `/site-static/_next/static/chunks/e3ca8c55f5e05c9f.css` and `42fa0bd010237327.css`.
> Page title: "Agent Infrastructure for TypeScript"

---

## Fonts

Prisma uses three custom variable-font woff2 files served from their own CDN.

| Role | Family name | Variable axes |
|---|---|---|
| Display / headings | **Mona Sans VF** (`monaSans`) | `wdth`, `wght`, `opsz`, `ital` |
| Body / UI text | **Inter** | `wght` 100–900 |
| Code / mono | **Mona Sans Mono VF** (`monaSansMono`) | `wght` 200–900 |

### CSS font-stack variables (from `:root`)

```css
--font-sans-display: "Mona Sans VF", "Inter", "Helvetica Neue", "Arial Nova", sans-serif;
--font-sans:         "Inter", "Roboto", "Helvetica Neue", "Arial Nova", sans-serif;
--font-mono:         "Mona Sans Mono VF", ui-monospace, "Cascadia Code", "Source Code Pro", monospace;
```

### OpenType feature settings

```css
--font-sans-display-settings: "ss01" on, "ss02" on, "ss05" on, "ss06" on;
--font-sans-settings:         "cv01" on, "cv02" on, "cv06" on, "cv07" on, "cv08" on, "cv10" on;
--font-mono--settings:        "ss01" on, "ss02" on, "ss05" on, "ss06" on;
```

---

## Type Scale

Sourced from `--text-*` tokens in `:root`.

| Token | Size | Line-height |
|---|---|---|
| `--text-2xs` | 0.6875rem (11px) | 1rem |
| `--text-xs`  | 0.75rem (12px)   | 1rem |
| `--text-sm`  | 0.875rem (14px)  | 1.25rem |
| `--text-base` / `--text-md` | 1rem (16px) | 1.5rem |
| `--text-lg`  | 1.125rem (18px)  | 1.75rem |
| `--text-xl`  | 1.25rem (20px)   | 1.75rem |
| `--text-2xl` | 1.5rem (24px)    | 2rem |
| `--text-3xl` | 1.875rem (30px)  | 2.25rem |
| `--text-4xl` | 2.25rem (36px)   | 3rem |
| `--text-5xl` | 3rem (48px)      | 3.5rem |
| `--text-6xl` | 3.75rem (60px)   | 1 |
| `--text-7xl` | 4.5rem (72px)    | 1 |

Hero H1 uses `clamp(2rem, 6vw, 3.25rem)` at `line-height: 1.12` — extracted from inline style on `<h1>` in live HTML.

### Font weights

```
--font-weight-normal:    400
--font-weight-medium:    500
--font-weight-semibold:  600
--font-weight-bold:      700
--font-weight-extrabold: 800
--font-weight-black:     900
```

Primary CTA buttons use `font-weight: 650` with Mona Sans (confirmed from HTML class `font-[650]`).

---

## Colors

### Brand palette (static constants – same in both themes)

| Token | Hex | Semantic role |
|---|---|---|
| `--color-teal-400` | `#00d3bd` | PPG (Prisma Postgres) highlight |
| `--color-green-500` | `#00c758` | Success / `fd-success` |
| `--color-green-400` | `#05df72` | Success alt |
| `--color-indigo-400` | `#7d87ff` | ORM (Prisma ORM) highlight |
| `--color-indigo-300` | `#a4b3ff` | ORM light tint |
| `--color-blue-500` | `#3080ff` | Info / link / `fd-info` |
| `--color-red-500` | `#fb2c36` | Error / destructive |
| `--color-amber-400` | `#fcbb00` | Warning |
| `--color-gray-400` | `#99a1af` | Subtle UI text |
| `--color-gray-500` | `#6a7282` | Muted text |
| `--color-gray-600` | `#4a5565` | Disabled |
| `--color-black` | `#000000` | — |
| `--color-white` | `#ffffff` | — |

### Semantic tokens – Light theme

Sourced from `:root` blocks in `e3ca8c55f5e05c9f.css`.

| Token | Light value |
|---|---|
| `--background` | `#ffffff` |
| `--foreground` | `#1d242f` |
| `--card` | `#ffffff` |
| `--primary` | `#16a394` |
| `--primary-foreground` | `#ffffff` |
| `--secondary` | `#f7fafc` |
| `--muted` | `#edf2f7` |
| `--muted-foreground` | `#718096` |
| `--accent` | `#d9f9f6` |
| `--accent-foreground` | `#154f47` |
| `--border` | `#e2e8f0` |
| `--ring` | `#16a394` |
| `--color-background-default` | `#ffffff` |
| `--color-background-neutral` | `#f3f4f6` |
| `--color-background-neutral-weak` | `#f9fafb` |
| `--color-background-neutral-weaker` | `#fcfdfd` |
| `--color-background-ppg` | `#f0fdfa` |
| `--color-background-ppg-strong` | `#ccfbf1` |
| `--color-background-ppg-reverse` | `#14b8a6` |
| `--color-background-ppg-reverse-strong` | `#0d9488` |
| `--color-background-orm` | `#eef2ff` |
| `--color-background-orm-reverse` | `#6366f1` |
| `--color-foreground-neutral` | `#111827` |
| `--color-foreground-neutral-weak` | `#6b7280` |
| `--color-foreground-ppg` | `#0d9488` |
| `--color-foreground-ppg-strong` | `#0f766e` |
| `--color-foreground-orm` | `#4f46e5` |
| `--color-foreground-orm-strong` | `#4338ca` |
| `--color-stroke-neutral-strong` | `#d1d5db` |
| `--color-stroke-neutral` | `#e5e7eb` |
| `--color-stroke-ppg` | `#0d9488` |
| `--color-stroke-orm` | `#4f46e5` |

### Semantic tokens – Dark theme

Sourced from `.dark { ... }` block in `e3ca8c55f5e05c9f.css`.

| Token | Dark value |
|---|---|
| `--background` | `#131420` |
| `--foreground` | `#f7fafc` |
| `--card` | `#1a202c` |
| `--primary` | `#16a394` |
| `--muted` | `#1d242f` |
| `--muted-foreground` | `#a0aec0` |
| `--accent` | `#0d3a38` |
| `--accent-foreground` | `#71e8df` |
| `--border` | `#1d242f` |
| `--color-background-default` | `#030712` |
| `--color-background-neutral-weaker` | `#0a101d` |
| `--color-background-neutral-weak` | `#111827` |
| `--color-background-neutral` | `#1f2937` |
| `--color-background-neutral-strong` | `#374151` |
| `--color-background-ppg` | `#042f2e` |
| `--color-background-ppg-strong` | `#134e4a` |
| `--color-background-ppg-reverse` | `#14b8a6` |
| `--color-background-ppg-reverse-strong` | `#2dd4bf` |
| `--color-background-orm` | `#1e1b4b` |
| `--color-background-orm-reverse` | `#6366f1` |
| `--color-foreground-neutral` | `#f9fafb` |
| `--color-foreground-neutral-weak` | `#9ca3af` |
| `--color-foreground-ppg` | `#14b8a6` |
| `--color-foreground-ppg-strong` | `#2dd4bf` |
| `--color-foreground-orm` | `#6366f1` |
| `--color-foreground-orm-strong` | `#818cf8` |
| `--color-stroke-neutral-strong` | `#374151` |
| `--color-stroke-neutral` | `#1f2937` |
| `--color-stroke-ppg` | `#14b8a6` |
| `--color-stroke-orm` | `#6366f1` |

---

## Spacing

Base unit: `--spacing: 0.25rem`. Named element-spacing tokens:

| Token | Value |
|---|---|
| `--spacing-element-2xs` | `0.75rem` (12px) |
| `--spacing-element-xs` | `1rem` (16px) |
| `--spacing-element-sm` | `1.25rem` (20px) |
| `--spacing-element-md` | `1.5rem` (24px) |
| `--spacing-element-lg` | `1.75rem` (28px) |
| `--spacing-element-xl` | `2rem` (32px) |
| `--spacing-element-2xl` | `2.25rem` (36px) |
| `--spacing-element-3xl` | `2.5rem` (40px) |
| `--spacing-element-4xl` | `3rem` (48px) |
| `--spacing-element-5xl` | `4rem` (64px) |

---

## Border Radius

| Token | Value |
|---|---|
| `--radius-square-low` | `0.1875rem` (3px) – inline badges |
| `--radius-square` | `0.375rem` (6px) – buttons, inputs |
| `--radius-square-high` | `0.75rem` (12px) – cards, nav container |
| `--radius` | `0.5rem` (8px) – base radius |
| `--radius-md` | `6px` (calc) |
| `--radius-lg` | `8px` = `var(--radius)` |
| `--radius-circle` | `999px` – pills |

---

## Shadows & Blur

Nav wrapper: `shadow-box-high` with `backdrop-filter: blur(3px)` and `bg-background-default/50` (50% opacity).

```css
--blur-surface-low: 1rem;
--blur-xs: 4px;
--blur-sm: 8px;
--blur-md: 12px;
--blur-lg: 16px;
```

---

## Components

### Buttons

**PPG Primary** – main CTA ("Try Prisma Postgres", "Get started"):
```css
background:    var(--color-background-ppg-reverse);   /* teal */
color:         var(--color-foreground-ppg-reverse);   /* #fff */
border-radius: var(--radius-square);                  /* 6px */
height:        var(--spacing-element-4xl);             /* 48px */
font-family:   var(--font-sans-display);
font-weight:   650;
```
Hover: `--color-background-ppg-reverse-strong` (`#0d9488` light / `#2dd4bf` dark).

**ORM Secondary** – indigo for ORM product CTA:
```css
background:    var(--color-background-orm-reverse);
color:         var(--color-foreground-orm-reverse);
```

**Ghost / Outline**:
```css
background:    transparent;
border:        1px solid var(--color-stroke-neutral-strong);
color:         var(--color-foreground-neutral);
border-radius: var(--radius-square);
```

### Inputs

```css
background:    var(--color-background-neutral-weak);
border:        1px solid var(--color-stroke-neutral-strong);
border-radius: var(--radius-square);
height:        var(--spacing-element-4xl);
padding:       0 0.75rem;
font-size:     var(--text-sm);
color:         var(--color-foreground-neutral);
```
Focus: `box-shadow: 0 0 0 3px rgba(22,163,148,0.25)` + `border-color: var(--ring)`.

### Badges

**PPG (Postgres)** – teal:
```css
background:    var(--color-background-ppg);
color:         var(--color-foreground-ppg);
border:        1px solid var(--color-stroke-ppg);
border-radius: var(--radius-square-low);
font-size:     var(--text-xs);
font-weight:   600;
```

**ORM** – indigo:
```css
background:    var(--color-background-orm);
color:         var(--color-foreground-orm);
border:        1px solid var(--color-stroke-orm);
```

**Error** – red, **Success** – teal, **Warning** – amber follow same pattern with their respective `--color-background-*` / `--color-foreground-*` / `--color-stroke-*` tokens.

### Cards

```css
background:    var(--card);
border:        1px solid var(--border);
border-radius: var(--radius-square-high);  /* 12px */
padding:       1.5rem;
```

---

## Signature Component – Prisma Studio Table View

Prisma's most iconic UI pattern is **Prisma Studio** — the visual database browser bundled with Prisma ORM. It renders model records as a spreadsheet with typed column headers, relation chip links, and toolbar filters.

Visual traits:
- Dense table with monospace column values
- Column headers show Prisma model field name + scalar type (`Int`, `String`, `DateTime`, `Boolean`)
- Relation columns shown as teal-tinted chip links using `@relation`
- Row selection checkboxes
- Toolbar: model name dropdown + "Add record" button + filter bar
- Type badges follow PPG/ORM color system

Prisma schema behind the showcase table:
```prisma
model User {
  id        Int      @id @default(autoincrement())
  email     String   @unique
  name      String?
  role      String   @default("user")
  createdAt DateTime @default(now())
  posts     Post[]
}

model Post {
  id        Int      @id @default(autoincrement())
  title     String
  published Boolean  @default(false)
  authorId  Int
  author    User     @relation(fields: [authorId], references: [id])
}
```

Query that populates the table view:
```typescript
const users = await prisma.user.findMany({
  include: { posts: true },
  orderBy: { createdAt: 'desc' },
  take: 20,
});
```

---

## Guardrails

### Do
- Use **Mona Sans** for all headings and display text; use **Inter** for dense body/UI strings.
- Use teal (`#16a394`, `--primary`) for Postgres/PPG-branded interactions; use indigo (`#4f46e5`) exclusively for ORM-branded elements.
- Use `rounded-square-high` (12px) for cards and modal containers; `rounded-square` (6px) for buttons and inputs.
- Default to **dark** theme (`data-theme="dark"`) — Prisma's own site reads `prefers-color-scheme` but falls back to dark.
- Apply `font-weight: 650` with Mona Sans on primary CTA buttons — this is a confirmed value from live HTML (`font-[650]` class).
- Render all Prisma schema syntax and query code in **Mona Sans Mono** at `font-size: 0.875rem`.
- Keep `--blur-surface-low: 1rem` frosted-glass blur on overlapping nav surfaces.

### Don't
- Don't mix PPG teal and ORM indigo in the same interactive element — they are distinct product pillars with separate color systems.
- Don't use teal as a generic accent color; inside Prisma it is specifically the Postgres/PPG product identity.
- Don't use `border-radius` below 3px (`--radius-square-low`) except for small inline type badges.
- Don't use `font-weight > 700` with Inter — heavier weights require Mona Sans.
- Don't render Prisma schema keywords (`model`, `datasource`, `generator`, `@id`, `@default`) in proportional fonts.
- Don't abbreviate Prisma Client method chains — full paths like `prisma.user.findMany()` are part of the brand's "type-safe" positioning and should always appear in full.
- Don't use the teal primary button color for destructive or warning actions — use red (`--color-background-error-reverse`) or amber (`--color-amber-400`) instead.
