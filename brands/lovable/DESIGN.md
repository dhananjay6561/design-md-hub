# Lovable — Design System

> Build something Lovable — create apps and websites by chatting with AI.

Lovable is an AI app builder: describe what you want in plain language and it generates a real, working app — "vibe coding." The identity is warm, optimistic and unmistakable: a soft **cream** canvas and a giant, blurred **heart-shaped gradient** that blooms from **periwinkle-blue → hot magenta → orange**. The name is the brand — the heart *is* the logo, and love is the feeling. Type is clean and modern (Inter) so the warmth comes entirely from the gradient and the friendly, plain-spoken copy. The core interaction — a single prompt box that turns a sentence into software — sits calmly in the middle of that glow.

---

## Color

### Brand — the heart gradient
| Token | Hex | Usage |
|---|---|---|
| blue | `#5681FE` | Gradient outer — periwinkle |
| magenta | `#FB3598` | Gradient mid · primary accent · links · the "Lovable pink" |
| orange | `#FF6D1B` | Gradient core · warm highlight |
| heart gradient | `#5681FE → #FB3598 → #FF6D1B` | The heart mark, hero glow, AI/generating states, gradient CTAs |
| ink | `#1A1815` | Primary buttons ("Get started"), headings |

The **heart gradient** is the whole brand. Magenta (`#FB3598`) is the single flat accent when one color is needed (links, active); the primary action button is warm near-black **ink**.

### Surfaces (light-first — Lovable is warm & bright; the builder app is dark)
| Token | Light | Dark | Usage |
|---|---|---|---|
| canvas | `#FCFBF8` | `#0E0D0C` | App background (warm cream) |
| panel | `#FFFFFF` | `#1B1917` | Cards, prompt box, preview |
| subtle | `#F5F2EC` | `#231F1C` | Wells, chat, muted rows |
| raised | `#EEE9E0` | `#2C2723` | Hover / selected |
| border | `#E9E4DA` | `#332E29` | Hairlines |

### Text
| Token | Light | Dark |
|---|---|---|
| ink | `#1A1815` | `#F7F4EF` |
| secondary | `#6B645C` | `#B5AEA4` |
| muted | `#9B9389` | `#7E766C` |
| link | `#FB3598` | `#FF6FB4` |

### Functional signals (the builder — not brand)
| Token | Hex | Meaning |
|---|---|---|
| generating | heart gradient | AI thinking / building a step |
| done | `#22A06B` | Step complete · file written |
| file | `#6B645C` | Generated file chip |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / UI / body | **Inter** (`400 / 500 / 600 / 700`) | Lovable's clean, modern workhorse — headings ("Build something Lovable"), UI, chat and body. The warmth comes from the gradient, not the type. |
| Code / build log | **JetBrains Mono** (`400 / 500`) | Generated file names, code snippets and the streaming build log in the builder. |

Scale: hero 52px (Inter 700, tight tracking), section 26px, prompt 15px, body 15px, chat 13px, code 12px. Keep type quiet and legible; let the heart glow carry the feeling.

---

## Shape, spacing & motion

- **Radius:** the prompt box & cards `16px`, buttons `9999px` (fully rounded pills) and `12px` for panels, chips `9999px`. Soft, friendly, pill-forward.
- **Spacing:** the marketing hero is centered and airy — the prompt box floats in the heart glow. The builder is a **two-pane** app: chat/build log on the left, live app preview on the right.
- **Elevation:** the prompt box and cards float on a soft shadow (`0 12px 40px rgba(120,40,90,.12)`); the heart gradient is a large, heavily-blurred radial bloom behind everything.
- **Motion:** the signature moment is **generation** — you send a prompt and the app *assembles itself*: build steps stream into the chat (spinner → ✓), and the preview fills in section by section (nav → hero → cards). Warm and lively, **deterministic** — a fixed build sequence per prompt; no randomness.

---

## Components

- **Heart mark** — a rounded heart filled with the blue→magenta→orange gradient; pairs with the `Lovable` wordmark in Inter. The heart is the logo.
- **Prompt box** — the hero interaction: a rounded input ("Ask Lovable to build…") with model/attach controls and a send button; the front door to everything.
- **Builder** — a two-pane workspace: a **chat / build log** (user prompt bubble + streaming AI steps with file chips) and a **live preview** that assembles the generated app in real time.
- **Suggestion chips** — rounded pills offering starter prompts (Landing page, Dashboard, Todo app).
- **Buttons** — near-black **ink** primary pill ("Get started"), gradient pill for AI actions ("Build"), quiet ghost secondary.
- **Heart-gradient bloom** — the big blurred background glow; the brand's atmosphere.

---

## Guardrails

**Do**
- Anchor on a warm **cream canvas** with the blurred **heart gradient** (blue→magenta→orange) as the atmosphere.
- Treat the **heart** as the logo and the brand's soul; the gradient carries AI/generating states and CTAs.
- Keep type in **Inter** (code in JetBrains Mono) and copy plain-spoken and friendly — warmth comes from the gradient, not the font.
- Make the **prompt → app** flow the centerpiece: a calm prompt box, then an app that assembles itself section by section.
- Use fully **rounded pill** buttons and soft, floating cards.

**Don't**
- Put the gradient on everything — it's a big soft *bloom*, not a fill for buttons and text everywhere.
- Introduce a competing brand hue; the blue→magenta→orange heart is the whole palette (magenta is the single flat accent).
- Make the gradient harsh or banded — it's heavily blurred and dreamy.
- Use sharp corners or a cold/dark marketing canvas — Lovable is warm and rounded (the *builder app* is dark; marketing is cream).
- Replace the heart with a generic sparkle/bot icon — the heart is non-negotiable.
