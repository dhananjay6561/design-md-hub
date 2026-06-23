# Cursor Design System

**Cursor** is an AI-native code editor — a VS Code fork built around ambient intelligence, expressing technical precision through a warm, achromatic aesthetic.

---

## 1. Overview

Cursor's visual language is defined by two parallel design contexts:

1. **The App UI** — a dark, near-monochromatic IDE shell with a single chromatic accent (electric blue `#228df2`). Derived from the Anysphere Dark theme. Every surface sits in the `#141414`–`#1d1d1d` range; colour is reserved strictly for interactive states, status signals, and AI affordances.

2. **The Marketing Site** — a warm, off-white typographic system built around Cursor Gothic, a bespoke condensed grotesque commissioned from Kimera. Backgrounds are cream parchment (`#F7F7F4`), text is warm near-black (`#14120B`), and the single chromatic pop is ember orange (`#f54e00`).

**Design philosophy:** 95 %+ achromatic surface coverage. Colour communicates state, never decoration. Typography carries brand character; layout carries hierarchy. The editor and marketing site are distinct but share the same restraint — maximum signal, minimum noise.

---

## 2. Colors

### 2a. App UI — Dark Mode (Anysphere Dark)

| Token | Hex | Usage |
|-------|-----|-------|
| `editor.background` | `#181818` | Main editor canvas |
| `activityBar.background` | `#181818` | Left icon rail |
| `sideBar.background` | `#181818` | File explorer panel |
| `statusBar.background` | `#181818` | Bottom status strip |
| `titleBar.activeBackground` | `#181818` | Window title bar |
| `panel.background` | `#181818` | Terminal / output panels |
| `tab.activeBackground` | `#181818` | Active editor tab |
| `tab.inactiveBackground` | `#181818` | Inactive editor tabs |
| `dropdown.background` | `#1d1d1d` | Dropdowns, context menus |
| `editorSuggestWidget.background` | `#1d1d1d` | Autocomplete popup |
| `editorHoverWidget.background` | `#1d1d1d` | Hover tooltip |
| `notifications.background` | `#1d1d1d` | Toast notifications |
| `button.secondaryBackground` | `#1d1d1d` | Ghost / secondary button fill |
| `editor.lineHighlightBorder` (transparent) | `#181818` | Line highlight (no border) |
| `editor.selectionBackground` | `#163761` | Text selection highlight |
| `editorSuggestWidget.selectedBackground` | `#163761` | Selected autocomplete item |
| `foreground` | `#d6d6dd` | Default text / icons |
| `editor.foreground` | `#d6d6dd` | Editor text |
| `sideBar.foreground` | `#d1d1d1` | Sidebar file names |
| `activityBar.foreground` | `#e3e1e3` | Active activity-bar icon |
| `activityBar.inactiveForeground` | `#7a797a` | Inactive activity-bar icon |
| `editorLineNumber.foreground` | `#535353` | Dim line numbers |
| `editorLineNumber.activeForeground` | `#c2c2c2` | Active line number |
| `breadcrumb.foreground` | `#a6a6a6` | Breadcrumb path text |
| — | | — |
| **Accent Blue** | `#228df2` | Cursor caret, buttons, badges, links, info icons |
| `button.hoverBackground` | `#359dff` | Primary button hover |
| `activityBarBadge.background` | `#228df2` | Notification badge |
| `badge.background` | `#228df2` | General badge / pill |
| `textLink.foreground` | `#228df2` | Hyperlinks |
| `editorInfo.foreground` | `#228df2` | Info squiggle / gutter icon |
| `statusBarItem.remoteBackground` | `#5b51ec` | Remote indicator (purple-blue) |
| — | | — |
| **Borders / Dividers** | `#383838` | Panel borders, tab borders, widget borders |
| `tab.border` | `#292929` | Subtle tab separator |
| `sideBar.border` | `#383838` | Sidebar right edge |
| `editorGroup.border` | `#383838` | Split-editor divider |
| — | | — |
| **Semantic Status** | | |
| Error | `#f14c4c` | Errors, deleted git gutter |
| Warning | `#ea7620` | Warnings, debug bar |
| Success / Added | `#15ac91` | Git added, progress bar |
| Modified | `#e5b95c` | Git modified gutter |
| Git Conflict | `#aaa0fa` | Conflicting resource |

### 2b. App UI — Light Mode (Default Light Modern)

Cursor ships VS Code's Default Light Modern as the light option. Key values:

| Token | Hex | Usage |
|-------|-----|-------|
| `editor.background` | `#ffffff` | Editor canvas |
| `sideBar.background` | `#f3f3f3` | File explorer |
| `activityBar.background` | `#2c2c2c` | Left icon rail (stays dark) |
| `editor.foreground` | `#383a42` | Editor text |
| Accent Blue | `#0066bf` | Links, active states |
| Error | `#e51400` | Error squiggles |
| Added | `#587c0c` | Git added |

### 2c. Marketing Site — Light (Warm Parchment)

| Name | Hex | Usage |
|------|-----|-------|
| Canvas Parchment | `#F7F7F4` | Page background, card surfaces |
| Inkwell | `#14120B` | Primary text, headings |
| Espresso | `#26251E` | Body text, filled buttons |
| Deep Ink | `#26251E` | Navigation, button fills |
| Card Stone | `#E6E5E0` | Elevated card surfaces |
| Border Sand | `#D9D5CF` | Dividers, card / input borders |
| Muted Clay | `#7A7974` | Secondary text, placeholders |
| Ember Orange | `#f54e00` | Primary CTA, hover accents, link underlines |
| Brass Gold | `#C08532` | Icon strokes, decorative accents |
| Signal Green | `#4ADE80` | Tag outlines, focus edges |

---

## 3. Typography

### Font Families

| Role | Family | Weights | Notes |
|------|---------|---------|-------|
| **Brand / Display** | Cursor Gothic | 400 | Proprietary (Kimera, not publicly available). Preview fallback: system sans-serif stack (`'Helvetica Neue', Helvetica, Arial`) — no open-source font replicates its condensed grotesque cut closely enough. |
| **UI / Body** | `Geist, system-ui, sans-serif` | 400, 500 | App chrome. Geist is available via Vercel / Google Fonts. |
| **Code / Mono** | Berkeley Mono | 400, 500 | Proprietary (Berkeley Graphics, not publicly available). Preview fallback: `JetBrains Mono` (Google Fonts) — comparable monospace weight and code-legibility profile. |

> **Rule:** Code always renders in Berkeley Mono. Cursor Gothic never appears inside the code editor canvas.

### Type Scale (Marketing Site — Minor Third ratio, 15 px base)

| Role | Size | Weight | Line Height | Letter Spacing |
|------|------|--------|-------------|----------------|
| `display` | 72 px | 400 | 1.00 | −0.030 em |
| `heading-lg` | 36 px | 400 | 1.10 | −0.020 em |
| `heading` | 26 px | 400 | 1.20 | −0.012 em |
| `heading-sm` | 22 px | 400 | 1.30 | −0.005 em |
| `body-16` | 16 px | 400 | 1.50 | +0.005 em |
| `body-14` | 14 px | 400 | 1.50 | +0.010 em |
| `caption` | 13 px | 400 | 1.55 | +0.010 em |
| `small` | 12 px | 400 | 1.67 | — |

### App UI Type Scale

| Role | Size | Weight | Usage |
|------|------|--------|-------|
| Editor body | 13–14 px | 400 | Code, prose in chat panel |
| UI label | 11–12 px | 400 | Sidebar labels, tab titles |
| Status bar | 11 px | 400 | Bottom bar text |
| Badge | 10 px | 500 | Notification count |

---

## 4. Spacing

Base unit: **4 px**. All spacing tokens are multiples of 4, with additional fine-grained steps for dense IDE contexts.

| Token | Value | Usage |
|-------|-------|-------|
| `space-1` | 4 px | Icon padding, tight gaps |
| `space-2` | 8 px | Between list items, small element gaps |
| `space-3` | 12 px | Inner padding of compact components |
| `space-4` | 16 px | Default component padding, form field height rhythm |
| `space-5` | 20 px | Section sub-gaps |
| `space-6` | 24 px | Card padding, panel insets |
| `space-7` | 28 px | Taller section spacing |
| `space-8` | 32 px | Component group separation |
| `space-10` | 40 px | Panel header height |
| `space-12` | 48 px | Hero sub-sections |
| `section-gap` | 64 px | Marketing page section gaps |
| `max-width` | 1200 px | Content container max-width |

### App UI Fixed Dimensions

| Element | Value |
|---------|-------|
| Activity bar width | 48 px |
| Sidebar default width | 264 px (w-64) |
| Chat / AI panel width | 320 px (w-80) |
| Tab bar height | 35 px |
| Status bar height | 22 px |
| Editor line height | 1.5 (≈ 21 px at 14 px) |

---

## 5. Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `radius-none` | 0 px | Status bar, window chrome |
| `radius-sm` | 2 px | Inlay hints, micro-badges |
| `radius-base` | 4 px | Tags, inputs, icon buttons, dropdowns |
| `radius-md` | 6 px | Tooltips, hover widgets |
| `radius-lg` | 8 px | Cards, panels, modals, notification toasts |
| `radius-xl` | 12 px | Large modal / dialog |
| `radius-pill` | 9999 px | Marketing site primary buttons, badge pills |

---

## 6. Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-widget` | `0 2px 8px rgba(0,0,0,0.32)` | Autocomplete popup, hover widget (dark mode) |
| `shadow-subtle` | `oklab(0.263 -0.002 0.012 / 0.1) 0px 0px 0px 1px, rgba(0,0,0,0.28) 0px 18px 36px -18px` | Floating cards, marketing site panels |
| `shadow-xl` | `rgba(0,0,0,0.14) 0px 28px 70px 0px, rgba(0,0,0,0.10) 0px 14px 32px 0px, oklab(0.263 -0.002 0.012 / 0.1) 0px 0px 0px 1px` | Hero product screenshots, large marketing cards |
| `shadow-xl-2` | `rgba(0,0,0,0.25) 0px 25px 50px -12px, rgba(0,0,0,0.15) 0px 12px 24px -8px, oklab(0.263 -0.002 0.012 / 0.1) 0px 0px 0px 0.5px` | Modals, dialogs, layered panels |
| `shadow-widget-dark` | `#111111eb spread, 0 2px 12px` | `widget.shadow` in app UI |

> Marketing site shadows use OKLab-encoded border rings (instead of `box-shadow: 0 0 0 1px`) to ensure perceptual colour consistency across monitors.

---

## 7. Components

### Button

#### Primary (App UI)
- Background: `#228df2`
- Foreground: `#e6e6ed`
- Hover: `#359dff`
- Border radius: `4px`
- Padding: `6px 14px`
- Font: 13 px / 400

#### Secondary (App UI)
- Background: `#1d1d1d`
- Foreground: `#d6d6dd`
- Hover: `#303030`
- Border radius: `4px`
- Padding: `6px 14px`

#### Primary (Marketing Site)
- Background: `#26251E` (Espresso Ink)
- Foreground: `#F7F7F4`
- Hover: shifts text to `#cf2d56` (crimson)
- Border radius: `9999px` (pill)
- Padding: `10px 22px`
- Font: Cursor Gothic, 14–15 px

#### Ghost / Outline (Marketing Site)
- Background: transparent
- Border: 1 px solid `#D9D5CF`
- Foreground: `#26251E`
- Hover border: `#26251E`
- Border radius: `9999px`

---

### Input / Text Field

| Property | App UI (Dark) | Marketing Site |
|----------|--------------|----------------|
| Background | `#1d1d1d` | `#F7F7F4` |
| Border | 1 px `#383838` | 1 px `#D9D5CF` |
| Focus border | `#228df2` | `#14120B` |
| Foreground | `#d6d6dd` | `#26251E` |
| Placeholder | `#7a797a` | `#7A7974` |
| Border radius | `4px` | `4px` |
| Padding | `5px 10px` | `8px 12px` |
| Font size | 13 px | 14 px |

---

### Card

| Property | App UI | Marketing Site |
|----------|--------|----------------|
| Background | `#1d1d1d` | `#F7F7F4` / `#E6E5E0` |
| Border | 1 px `#383838` | 1 px `#D9D5CF` |
| Border radius | `8px` | `8px` |
| Padding | `16px` | `24px` |
| Shadow | `shadow-widget` | `shadow-subtle` or `shadow-xl` |
| Heading color | `#d6d6dd` | `#14120B` |
| Body color | `#a6a6a6` | `#7A7974` |

---

### Sidebar (App UI)

- Background: `#181818`
- Right border: 1 px `#383838`
- Default width: 264 px
- Section header: transparent bg, foreground `#d1d1d1`, font 11 px uppercase + tracked
- File item height: 22 px
- Active item: `#163761` background, `#d6d6dd` text
- Hover item: `#2a2a2a` background
- Icon color: `#d1d1d1`; modified git: `#1981ef`; added: `#5a964d`; deleted: `#f14c4c`

---

### Chat Panel (AI Panel)

- Background: matches `sideBar.background` → `#181818`
- Right-side panel, default width: 320 px
- Border left: 1 px `#383838`
- User message bubble: `#1d1d1d` fill, `#383838` border, radius `8px`, padding `12px 16px`
- AI response: no fill bubble, rendered inline with `#d6d6dd` text
- Code blocks inside chat: `#141414` bg, Berkeley Mono, radius `4px`, 1 px `#383838` border
- Input box at bottom: `#1d1d1d` bg, `#383838` border, radius `6px`, padding `8px 12px`
- Send button: `#228df2` accent when active, `#383838` when empty
- Inline diff accept: `#15ac91` (green); reject: `#f14c4c` (red)

---

### Badge / Pill

| Property | App UI | Marketing Site |
|----------|--------|----------------|
| Background | `#228df2` | transparent or `#E6E5E0` |
| Foreground | `#d6d6dd` | `#26251E` or accent color |
| Border radius | `9999px` | `9999px` |
| Padding | `2px 6px` | `3px 10px` |
| Font size | 10–11 px / 500 | 12 px / 400 |
| Outline variant | — | 1 px `#4ADE80` or `#D9D5CF` border, transparent bg |

---

## 8. Layout Principles

1. **Tri-zone IDE shell.** Activity bar (48 px, far left) → Sidebar (264 px) → Editor group (flex-fill) → AI/Chat panel (320 px, far right). Every zone has a hard 1 px `#383838` border at its edge.

2. **Editor maximalism.** The editor canvas takes all remaining horizontal space. Secondary panels collapse by default; no panel overlaps the editor unless explicitly invoked (e.g., Command Palette floats centered at 34 % viewport width).

3. **Marketing: single-column long-form.** Sections stack vertically with `64 px` gaps. Content width caps at `1200 px`. Text blocks and hero images share a single centered column — no persistent sidebars. White space conveys quality over density.

4. **Floating surfaces are always dark in app, warm-light on marketing.** Dropdowns, tooltips, autocomplete popups, and modals follow the host surface's mode (never mix light popup on dark bg in the app).

5. **Grid alignment.** All measurements snap to the 4 px grid. The 8 px double-unit is the standard element gap. The 16 px quad-unit is the standard inset.

6. **Status bar is always full-bleed.** It spans 100 % viewport width with no internal gaps. Remote indicator uses `#5b51ec` (purple-blue) to distinguish it from the primary `#228df2` accent.

---

## 9. Responsive Behavior

### App UI
- The app targets **desktop only** (minimum 1024 px wide). No mobile layout exists.
- Sidebar collapses to 0 px on narrow splits; activity bar remains visible.
- AI panel can be undocked to a floating window or collapsed; width is user-resizable with a minimum of 200 px.
- Editor tabs switch to a scroll mode below ~600 px panel width; breadcrumbs are hidden below 400 px.

### Marketing Site
- **≥ 1200 px** — Full layout; hero with side-by-side text + product screenshot.
- **768–1199 px** — Hero stacks vertically; pricing cards reflow to 2-column grid.
- **< 768 px** — Single-column; navigation collapses to hamburger menu; hero image hidden; font size scales down (`display` → 40 px, `heading-lg` → 28 px).
- Touch targets: minimum 44 × 44 px on all interactive elements in responsive breakpoints.
- Preferred breakpoints: `640 px`, `768 px`, `1024 px`, `1280 px`.

---

## 10. Tone & Guardrails

### DO

- Use `#228df2` as the **one and only** chromatic colour in the app UI. All other colour is reserved for semantic status (error / warning / success).
- Keep all app surfaces within the `#141414`–`#1d1d1d` range. Never introduce mid-grey or coloured backgrounds.
- Render all code — in editor, chat bubbles, tooltips, and inline diffs — in **Berkeley Mono**.
- Use **Cursor Gothic** exclusively for brand and marketing text. Never set it inside the editor canvas or code-adjacent contexts.
- Maintain 95 %+ achromatic coverage on any surface. Chromatic colours are states, not backgrounds.
- Apply `#14120B` / `#26251E` for text on marketing pages — never pure `#000000`.
- Use pill (`9999px`) radius for marketing buttons and strict `4px` / `8px` for IDE UI elements.
- Preserve the `64 px` section gap rhythm on marketing pages for breathing room and editorial quality.
- Treat the AI panel as a sidebar peer — same background as the sidebar, not the editor.

### DON'T

- Don't use gradients, drop shadows, or coloured glows in the app UI. Depth is implied by background value alone.
- Don't add decorative illustrations or icons to the editor shell. Iconography is functional and monochromatic.
- Don't use orange (`#f54e00`) inside the IDE — that accent is marketing-only.
- Don't mix light UI widgets into a dark theme context or vice versa.
- Don't use `#000000` pure black for any text — always warm it (Espresso `#26251E` on marketing, near-black `#141414` for UI rails).
- Don't reduce the Activity Bar below 48 px or the AI panel below 200 px.
- Don't use EB Garamond outside editorial / marketing long-form contexts.
- Don't place more than one chromatic accent per screen in the IDE. Blue is for primary action; everything else must use neutrals.
- Don't animate layout transitions in the editor. Micro-animations are permitted only in the chat stream and diff application.
- Don't refer to the product as "Cursor AI" or "Cursor Code" — it is simply **Cursor**.
