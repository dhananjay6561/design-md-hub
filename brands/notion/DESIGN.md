# Notion Design System

**Notion** — a calm, newspaper-like productivity workspace where structured content always takes center stage.

---

## Overview

Notion's design philosophy is **warm minimalism**. Every decision points away from itself and toward the content. The interface is sparse but never cold — off-white surfaces, ink-dark text, and generous whitespace evoke a well-typeset document rather than a software product. There is no chrome for its own sake; borders, shadows, and decoration are deployed only when they carry meaning (hierarchy, grouping, interactivity).

Key principles:

- **Content supremacy.** The page is a blank sheet; UI recedes to the margins.
- **Warmth through neutrals.** Pure black is avoided in favor of near-black `#37352F`; pure white gives way to warm off-whites like `#F7F6F3`.
- **Functional color.** Color is used to communicate state and content type, never for decorative flourish.
- **Incremental disclosure.** Toolbars, menus, and options appear on hover or focus, not as persistent clutter.
- **Consistent rhythm.** An 8px base grid governs every spacing decision without exception.

---

## Colors

### Brand Identity

| Role | Name | Hex |
|---|---|---|
| Brand Black | Ink | `#000000` |
| Brand White | Paper | `#FFFFFF` |
| Brand Cream | Off-white | `#E3E2DE` |

### Light Mode — UI Surfaces

| Token | Hex | Usage |
|---|---|---|
| `bg-primary` | `#FFFFFF` | Main page canvas |
| `bg-sidebar` | `#F7F6F3` | Left sidebar background |
| `bg-hover` | `#EFEFEF` | Sidebar / list item hover |
| `bg-selected` | `#E8E8E5` | Active / selected item in sidebar |
| `bg-callout` | `#F1F1EF` | Callout block, gray background |
| `border-default` | `#E9E9E7` | Dividers, cell borders |
| `border-input` | `#DFDCD9` | Input field border |

### Light Mode — Text

| Token | Hex | Usage |
|---|---|---|
| `text-primary` | `#37352F` | All body text, headings |
| `text-secondary` | `#787774` | Placeholder, metadata, captions |
| `text-tertiary` | `#9B9A97` | Disabled labels, very soft hints |
| `text-link` | `#337EA9` | Hyperlinks, interactive blue |

### Light Mode — Content Colors (Text / Background pairs)

| Color | Text | Background |
|---|---|---|
| Gray | `#787774` | `#F1F1EF` |
| Brown | `#9F6B53` | `#F4EEEE` |
| Orange | `#D9730D` | `#FAEBDD` |
| Yellow | `#CB912F` | `#FBF3DB` |
| Green | `#448361` | `#EDF3EC` |
| Blue | `#487CA5` | `#E9F3F7` |
| Purple | `#8A67AB` | `#F6F3F8` |
| Pink | `#B35488` | `#F9F2F5` |
| Red | `#C4554D` | `#FAECEC` |

### Light Mode — Content Icon Colors

| Color | Hex |
|---|---|
| Gray | `#A6A299` |
| Brown | `#9F6B53` |
| Orange | `#D87620` |
| Yellow | `#CB912F` |
| Green | `#448361` |
| Blue | `#337EA9` |
| Purple | `#9065B0` |
| Pink | `#C14C8A` |
| Red | `#D44C47` |

### Dark Mode — UI Surfaces

| Token | Hex | Usage |
|---|---|---|
| `bg-primary` | `#191919` | Main page canvas |
| `bg-sidebar` | `#2F3438` | Left sidebar background |
| `bg-hover` | `#3F4448` | Sidebar / list item hover |
| `bg-selected` | `#373C3F` | Active / selected item |
| `bg-callout` | `#252525` | Callout block, gray background |
| `border-default` | `#373737` | Dividers, cell borders |
| `border-input` | `#4A4A4A` | Input field border |

### Dark Mode — Text

| Token | Hex | Usage |
|---|---|---|
| `text-primary` | `#D4D4D4` | All body text, headings |
| `text-secondary` | `#9B9B9B` | Placeholder, metadata, captions |
| `text-tertiary` | `#7F7F7F` | Disabled, very soft hints |
| `text-link` | `#2E7CD1` | Hyperlinks, interactive blue |

### Dark Mode — Content Colors (Text / Background pairs)

| Color | Text | Background |
|---|---|---|
| Gray | `#9B9B9B` | `#252525` |
| Brown | `#A27763` | `#2E2724` |
| Orange | `#CB7B37` | `#36291F` |
| Yellow | `#C19138` | `#372E20` |
| Green | `#4F9768` | `#242B26` |
| Blue | `#447ACB` | `#1F282D` |
| Purple | `#865DBB` | `#2A2430` |
| Pink | `#BA4A78` | `#2E2328` |
| Red | `#BE524B` | `#332523` |

### Interactive / Semantic Colors

| Role | Light Mode | Dark Mode |
|---|---|---|
| Primary action (CTA) | `#097FE8` | `#097FE8` |
| Primary action pressed | `#005BAB` | `#005BAB` |
| Focus ring | `rgba(9, 127, 232, 0.35)` | `rgba(9, 127, 232, 0.35)` |
| Danger | `#D44C47` | `#CD4945` |
| Selection highlight | `rgba(46, 170, 220, 0.15)` | `rgba(46, 170, 220, 0.20)` |

---

## Typography

Notion uses its own distribution of **Inter** (called *Notion Inter*) as the exclusive UI typeface. Users may switch the page body between three editorial faces:

| Face | Stack |
|---|---|
| Default | `"Notion Inter", Inter, -apple-system, BlinkMacSystemFont, sans-serif` |
| Serif | `"Notion Serif", Georgia, "Times New Roman", serif` |
| Mono | `"Notion Mono", "SFMono-Regular", Consolas, "Liberation Mono", Courier, monospace` |

### Type Scale

| Token | Size | Weight | Line Height | Usage |
|---|---|---|---|---|
| `display` | 54px | 700 | 1.15 | Marketing hero text |
| `heading-xl` | 40px | 700 | 1.2 | H1 page title (full size) |
| `heading-lg` | 30px | 600 | 1.3 | H1 page title (small text mode) / H2 |
| `heading-md` | 24px | 600 | 1.35 | H2 / H3 |
| `heading-sm` | 20px | 600 | 1.4 | H3 / section titles |
| `body-lg` | 16px | 400 | 1.5 | Default body text |
| `body-sm` | 14px | 400 | 1.5 | Small text mode body / sidebar items |
| `label` | 14px | 500 | 1.4 | UI labels, button text, property names |
| `caption` | 12px | 400 | 1.4 | Timestamps, helper text, footnotes |
| `code-inline` | 14px | 400 | 1.5 | Inline `code` spans |
| `code-block` | 13px | 400 | 1.6 | Fenced code blocks |

> The "Small text" page toggle reduces all content text by ~15% (body 16px → ~13.5px, H1 40px → 30px).

### Font Weight Reference

| Weight | Name | Usage |
|---|---|---|
| 400 | Regular | Body text, captions, metadata |
| 500 | Medium | UI labels, buttons, sidebar nav items |
| 600 | SemiBold | Subheadings, H2–H3 |
| 700 | Bold | Page titles (H1), display text |

---

## Spacing

Base unit: **8px**. All spacing values are multiples of 4px (half-unit) at small scales and multiples of 8px at larger scales.

| Token | px | Usage |
|---|---|---|
| `space-1` | 4px | Icon to label gap, inline badge padding |
| `space-2` | 8px | Internal padding (icon containers, chips), section gap in sidebar |
| `space-3` | 12px | Button vertical padding, input vertical padding |
| `space-4` | 16px | Card padding (compact), horizontal button padding |
| `space-5` | 20px | Card padding (standard), list item horizontal padding |
| `space-6` | 24px | Section separation (small), form row gap |
| `space-8` | 32px | Page content padding-inline (narrow) |
| `space-10` | 40px | Section separation (large), page top padding |
| `space-12` | 48px | Major section break |
| `space-16` | 64px | Hero / full-bleed section padding |
| `space-24` | 96px | Top-level page section spacing |

### Layout Widths

| Token | Value | Usage |
|---|---|---|
| `sidebar-width` | 224px | Default left sidebar |
| `content-max-width` | 720px | Default page body max-width |
| `content-max-width-full` | 1200px | Full-width page max-width |
| `header-height` | 45px | Top bar / breadcrumb row |

---

## Border Radius

| Token | Value | Usage |
|---|---|---|
| `radius-none` | 0px | Table cells, full-bleed images |
| `radius-sm` | 3px | Inline code, text highlights, small chips |
| `radius-md` | 4px | Buttons, inputs, select dropdowns |
| `radius-lg` | 8px | Cards, modals, sidebar items, callout blocks |
| `radius-xl` | 12px | Large modals, dialogs, floating panels |
| `radius-full` | 9999px | Pills, avatar images, toggle handles |

---

## Shadows

Notion uses extremely restrained elevation. Shadows are near-transparent and rely on layering rather than depth drama.

| Token | Value | Usage |
|---|---|---|
| `shadow-none` | `none` | Flat surfaces, sidebar panels |
| `shadow-xs` | `0 1px 2px rgba(0,0,0,0.06)` | Subtle card lift |
| `shadow-sm` | `0 1px 3px rgba(0,0,0,0.08), 0 1px 2px rgba(0,0,0,0.06)` | Default card, input focus backdrop |
| `shadow-md` | `0 4px 6px rgba(0,0,0,0.07), 0 2px 4px rgba(0,0,0,0.05)` | Hovering over a card, inline menu |
| `shadow-lg` | `0 10px 15px rgba(0,0,0,0.08), 0 4px 6px rgba(0,0,0,0.05)` | Modal dialogs, context menus, floating toolbar |
| `shadow-xl` | `0 20px 25px rgba(0,0,0,0.10), 0 10px 10px rgba(0,0,0,0.04)` | Full-screen overlays, command palette |
| `shadow-focus` | `0 0 0 2px rgba(9,127,232,0.35)` | Keyboard focus ring on interactive elements |

> Dark mode applies the same shadow tokens but reduces all alpha values by ~30% since the dark surface provides its own visual separation.

---

## Components

### Button

Notion has three button variants: **Primary**, **Secondary (outline)**, and **Ghost (text)**.

**Primary Button**

| Property | Value |
|---|---|
| Background | `#097FE8` |
| Background (hover) | `#0069C6` |
| Background (active/pressed) | `#005BAB` |
| Text color | `#FFFFFF` |
| Font | 14px / 500 (Medium) |
| Padding | `6px 12px` |
| Border radius | `4px` |
| Border | none |
| Min height | 32px |
| Focus ring | `shadow-focus` |

**Secondary Button**

| Property | Value |
|---|---|
| Background | `transparent` |
| Background (hover) | `rgba(55,53,47,0.08)` |
| Text color | `#37352F` |
| Font | 14px / 500 |
| Padding | `6px 12px` |
| Border radius | `4px` |
| Border | `1px solid rgba(55,53,47,0.16)` |
| Min height | 32px |

**Ghost / Text Button**

| Property | Value |
|---|---|
| Background | `transparent` |
| Background (hover) | `rgba(55,53,47,0.06)` |
| Text color | `#37352F` |
| Font | 14px / 400 |
| Padding | `4px 8px` |
| Border radius | `4px` |
| Border | none |

---

### Input

All text inputs share a consistent form anatomy.

| Property | Value |
|---|---|
| Background | `#FFFFFF` (light) / `#252525` (dark) |
| Border | `1px solid #DFDCD9` (light) / `1px solid #4A4A4A` (dark) |
| Border (focus) | `1px solid #097FE8` |
| Box shadow (focus) | `shadow-focus` |
| Text color | `text-primary` |
| Placeholder color | `text-secondary` |
| Font | 14px / 400 |
| Padding | `8px 12px` |
| Border radius | `4px` |
| Min height | 32px |

---

### Card

Notion cards (database gallery tiles, link previews, inline page references) follow a common template.

| Property | Value |
|---|---|
| Background | `#FFFFFF` (light) / `#2F2F2F` (dark) |
| Border | `1px solid #E9E9E7` (light) / `1px solid #373737` (dark) |
| Border radius | `8px` |
| Padding | `16px` |
| Shadow (default) | `shadow-sm` |
| Shadow (hover) | `shadow-md` |
| Hover transform | `translateY(-2px)` |
| Transition | `box-shadow 120ms ease, transform 120ms ease` |

---

### Navigation (Sidebar)

The left sidebar is Notion's primary navigation surface.

| Property | Value |
|---|---|
| Sidebar background | `#F7F6F3` (light) / `#2F3438` (dark) |
| Sidebar width | `224px` |
| Item padding | `4px 8px` |
| Item border radius | `8px` |
| Item font | 14px / 500 |
| Item text color | `#37352F` (light) / `#CFCFCD` (dark) |
| Item icon size | `22px` container, `16px` icon |
| Item hover background | `rgba(55,53,47,0.08)` (light) / `rgba(255,255,255,0.06)` (dark) |
| Item selected background | `rgba(55,53,47,0.12)` (light) / `rgba(255,255,255,0.10)` (dark) |
| Section gap | `6px` |
| Indent per level | `20px` |

---

### Badge

Badges are small, pill-shaped or chip-shaped labels used for tags, statuses, and property values in database views.

| Property | Value |
|---|---|
| Font | 12px / 400 |
| Padding | `2px 8px` |
| Border radius | `3px` (flat chip) or `9999px` (pill) |
| Background | Matches the content color background tokens (e.g., blue: `#E9F3F7`) |
| Text color | Matches the content color text tokens (e.g., blue: `#487CA5`) |
| Height | 20px |

The "New" / primary badge uses `#097FE8` background with `#FFFFFF` text.

---

### Table (Database Table View)

| Property | Value |
|---|---|
| Header background | `#F7F6F3` (light) / `#2F3438` (dark) |
| Header font | 12px / 500 / `text-secondary` color |
| Row background | `#FFFFFF` (light) / `#191919` (dark) |
| Row hover background | `#F7F6F3` (light) / `#252525` (dark) |
| Row height | 34px (compact) / 46px (default) |
| Cell padding | `8px 12px` |
| Cell font | 14px / 400 |
| Border color | `#E9E9E7` (light) / `#373737` (dark) |
| Border style | `1px solid` on all cell edges |
| Column resize handle | 2px wide, appears on header hover |
| Checkbox column width | 32px |
| Add-row button | Ghost style, full row width, bottom of table |

---

## Layout Principles

1. **Single-column page body.** Content flows in one centered column, respecting a `max-width` of `720px` (standard) or `1200px` (full-width). Side-by-side columns exist only when explicitly created with column blocks.

2. **8px grid.** Every margin, padding, gap, and positional offset is a multiple of 8px (with 4px half-steps permitted at the tightest scales only).

3. **Sidebar + content split.** The sidebar occupies a fixed `224px` on the left; the remaining viewport is the content area. The sidebar can be collapsed to `0px` via the hide/show toggle or overlay on smaller viewports.

4. **Hierarchy through size and weight, not color.** H1 > H2 > H3 > body is achieved purely by scale and weight. Color is never used as the sole differentiator of content hierarchy.

5. **Hover to reveal.** Secondary controls (inline menus, block handles, property icons) are hidden at `opacity: 0` and transition to `opacity: 1` on hover. This reduces visual noise while keeping controls accessible.

6. **Generous line length.** At `720px` content width and `16px` body text, the ideal 60–80 character line length is naturally maintained without further constraint.

7. **Block-based layout.** All content is composed of discrete blocks (paragraph, heading, list, callout, database, etc.). Each block respects consistent vertical rhythm via `margin-block-end: 2px` (tight) up to `8px` (between block types).

---

## Responsive Behavior

| Breakpoint | Behavior |
|---|---|
| `< 480px` (mobile-sm) | Sidebar hidden; full-width single column; font sizes reduced 10–15%; touch tap targets minimum 44px |
| `480px – 767px` (mobile-lg) | Sidebar accessible as slide-in overlay; content full-width with `16px` horizontal padding |
| `768px – 1023px` (tablet) | Sidebar optional overlay or persistent at `200px`; content max-width `680px` |
| `1024px – 1439px` (desktop-sm) | Full sidebar at `224px`; content max-width `720px` |
| `≥ 1440px` (desktop-lg) | Full sidebar; full-width pages can expand up to `1200px`; standard pages remain `720px` |

- Heading font sizes scale down ~15–20% on mobile to preserve vertical rhythm.
- Database views switch from table → gallery or list on small viewports.
- The top navigation bar collapses to a compact header with a hamburger toggle below `768px`.
- Touch targets (tap areas) are always at least `44×44px`, with `8px` minimum gap between adjacent targets.

---

## Tone & Guardrails

### DO

- Use `text-primary` (`#37352F` / `#D4D4D4`) for all reading text — never pure black or pure white.
- Use warm off-white (`#F7F6F3`) for sidebar and secondary surfaces instead of pure gray.
- Apply the 8px grid strictly; every spacing value must be a multiple of 4px.
- Rely on Inter at weight 500 for all UI labels and interactive element text.
- Use the 10-color content palette for semantic tagging (status badges, callouts, highlights).
- Keep shadows extremely subtle — less than you think is needed; Notion's elevation is nearly flat.
- Use `border-radius: 8px` on all card-like containers and `4px` on form controls.
- Hide secondary actions behind hover/focus states to preserve the calm reading experience.
- Maintain a content max-width of 720px on standard pages to honor the document metaphor.
- Use `transition: 120ms ease` for hover state changes — fast but not jarring.

### DON'T

- Don't use pure `#000000` black for text; Notion's ink is always the warm near-black `#37352F`.
- Don't apply aggressive drop shadows or heavy borders — they break the paper-document illusion.
- Don't use more than two typefaces; stick to Inter (sans), Georgia (serif), and system mono only.
- Don't use color as decoration; every color application must signal a content type or interactive state.
- Don't introduce new brand colors outside the established 10-color palette plus the CTA blue `#097FE8`.
- Don't use font weights above 700 or below 400.
- Don't make interactive controls permanently visible if they are secondary to the reading experience.
- Don't use border-radius values not in the token table (e.g., avoid `6px`, `10px`, `16px`).
- Don't use spacing values that are not multiples of 4px.
- Don't add motion or animation beyond simple opacity/transform transitions at ≤ 200ms.
- Don't center-align body text; all prose is left-aligned to support long-form reading.
- Don't use color-only status indicators — always pair color with an icon or text label for accessibility.
