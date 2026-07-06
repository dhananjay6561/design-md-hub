# Cal.com — Design System

> The better way to schedule your meetings.

Cal.com is open-source scheduling infrastructure — a fully customizable booking platform for individuals, businesses, and developers. Its design language is confidently **monochrome**: near-black ink on white (and the clean inverse in dark mode), almost no chrome, and one signature typeface — **Cal Sans** — carrying every heading. The restraint is the point: a booking page should get out of the way so picking a time feels effortless.

Design principles: **black & white first** (color is opt-in, set per-user brand), **the booking flow is sacred** (event → date → time → confirm), and **type does the work** (Cal Sans headings, clean UI sans body).

---

## Color

Cal.com ships an intentionally neutral, near-monochrome palette. Brand color is configurable per user; the default and the identity is ink-on-white.

### Ink & surfaces
| Token | Light | Dark | Usage |
|---|---|---|---|
| ink (primary) | `#141414` | `#F4F4F4` | Text, primary buttons, selected states |
| ink-2 | `#242424` | `#E4E4E4` | Strong text, headings |
| canvas | `#FFFFFF` | `#0D0D0D` | Page background |
| subtle | `#F7F7F7` | `#171717` | Cards, hover, recessed |
| muted-fill | `#F4F4F4` | `#1F1F1F` | Slot / control backgrounds |
| border | `#E1E2E3` | `#2A2A2A` | Hairlines |
| border-strong | `#D4D4D4` | `#3A3A3A` | Emphasis borders |

### Text
| Token | Light | Dark |
|---|---|---|
| primary | `#141414` | `#F4F4F4` |
| secondary | `#4B4B4B` | `#B4B4B4` |
| muted | `#898989` | `#898989` |

### Semantic
| State | Hex | Usage |
|---|---|---|
| available | `#141414` (ink) | selectable date / open slot |
| success | `#0FA968` | meeting scheduled |
| busy / disabled | `#C4C4C4` | unavailable day |
| booking accent | `#6349EA` | optional brand color (user-configurable) |

---

## Typography

Three Google-hosted families — all used on cal.com today.

| Role | Family | Notes |
|---|---|---|
| Display / headings | **Cal Sans** | The signature typeface — event titles, hero, host names, section headers. Rounded, confident, unmistakably Cal. |
| UI / body | **Manrope** (`400 / 500 / 600 / 700`) | Body copy, labels, buttons, time slots, form fields. |
| Mono / meta | **Fragment Mono** | Timezone codes, duration, technical metadata, timestamps. |

Scale: hero 52–60px (Cal Sans), event title 24px (Cal Sans), section 15px `600`, body 14px, slot 14px `500`, meta 13px, mono 12px.

---

## Shape, spacing & motion

- **Radius:** cards `16px`, buttons & slots `8px`, inputs `8px`, avatars/pills `9999px`. Soft but tidy.
- **Spacing:** 4px grid; the booking card is a calm three-pane layout (event · calendar · times) with generous padding.
- **Elevation:** one soft border-plus-shadow on the booking card (`0 2px 8px rgba(0,0,0,.04)`, `1px` border). Inside, separation is by border and whitespace — no nested shadows.
- **Motion:** quick and subtle (120–180ms). Times fade/slide in when a date is picked; a chosen slot splits to reveal **Confirm** (the signature Cal interaction); the confirmation state settles calmly. No bounce.

---

## Components

- **Booking widget** — the atom of Cal.com: an event pane (avatar, host, title, duration, location, timezone), a month **calendar** (available days selectable), and a **time-slot** list.
- **Time slot** — a bordered ink-outline button; on select it splits into `[time] [Confirm]` side by side.
- **Primary button** — solid ink on light (white text); inverts to solid white on dark (ink text). Never a gradient.
- **Event-type card** — title (Cal Sans) + duration + location badges (`Cal Video`, `Google Meet`, `In person`).
- **12h / 24h toggle** — a small segmented control above the slots.

---

## Guardrails

**Do**
- Keep it monochrome — ink on white (and the clean inverse on dark). Let type and spacing carry the design.
- Set every heading and event title in **Cal Sans**; use Manrope for everything functional.
- Protect the booking flow: event → select a date → pick a time → confirm, in the fewest steps.
- Use real Cal vocabulary: `30 Min Meeting`, `Cal Video`, `Select a Date & Time`, timezone codes.

**Don't**
- Introduce brand color unless it's the user's configured accent — the default identity is black & white.
- Add decorative gradients, illustrations, or heavy shadows — Cal.com is quiet by design.
- Break the slot → Confirm interaction or bury the primary action.
- Mix type roles — Cal Sans is display only; body stays in Manrope.
