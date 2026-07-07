# Apidog — Design System

> Design, Build, and Test APIs — all in one place.

Apidog is an all-in-one API platform: API **design**, **debugging**, automated **testing**, **docs** and **mocking** in a single tool (it pitches itself as "Postman + Swagger + Stoplight + Mock… combined"). The identity is bright, friendly and technical — a clean white-to-pale-blue canvas, a deep **navy ink** (`#1D2447`), and one vivid **blue→cyan gradient** (`#1A66FF → #00AAFF`) carrying every brand moment. Display type is **Poppins** (geometric, rounded, approachable) over a neutral Inter UI. The defining idea — and the thing that separates it from a plain API client — is **design-first**: every response is validated against the endpoint's designed schema, so docs, tests and reality stay in sync.

---

## Color

### Brand — the blue→cyan gradient
| Token | Hex | Usage |
|---|---|---|
| blue | `#1A66FF` | Primary accent, gradient start, links |
| azure | `#2B6EF6` | Solid primary buttons |
| cyan | `#00AAFF` | Gradient end, highlights |
| sky | `#7CB2FF` | Soft tint, secondary marks |
| brand gradient | `#1A66FF → #00AAFF` | Logo mark, hero, Send button, active states |

Blue is the single brand hue. Everything else is navy/neutral; other colors appear only as functional **HTTP-method** and **status** signals inside the client.

### Surfaces (light-first — Apidog is a bright product)
| Token | Light | Dark | Usage |
|---|---|---|---|
| canvas | `#FFFFFF` | `#0E1220` | App background (light has a pale-blue wash) |
| panel | `#FFFFFF` | `#161B2E` | Cards, request/response panels |
| subtle | `#F5F8FC` | `#1B2136` | Sidebar, wells, muted rows |
| raised | `#EAF1FB` | `#232A42` | Hover / selected |
| border | `#E4EAF2` | `#2C3350` | Hairlines |
| code | `#141A2E` | `#0A0E1A` | Dark code / response console (always dark) |

### Text
| Token | Light | Dark |
|---|---|---|
| ink (navy) | `#1D2447` | `#EEF2FB` |
| secondary | `#5B6478` | `#A6AEC6` |
| muted | `#8A93A8` | `#6C7492` |
| link | `#1A66FF` | `#5B9BFF` |

### Functional signals (product only — not brand)
| Token | Hex | Meaning |
|---|---|---|
| GET green | `#16A34A` | GET method · schema match |
| POST amber | `#E8863A` | POST method |
| PUT blue | `#2B6EF6` | PUT method |
| DELETE red | `#E5484D` | DELETE method · schema mismatch |
| PATCH purple | `#8B5CF6` | PATCH method |
| status 2xx | `#16A34A` | Success response |
| status 4xx/5xx | `#E5484D` | Error response |

---

## Typography

| Role | Family | Notes |
|---|---|---|
| Display / headings | **Poppins** (`600 / 700`) | The brand face — geometric, rounded, friendly. Hero, section headings, wordmark. Google Fonts, used on apidog.com directly. |
| UI / body | **Inter** (`400 / 500 / 600`) | Product chrome, labels, body copy — a neutral workhorse under the rounded display. |
| Code / response / meta | **JetBrains Mono** (`400 / 500`) | URLs, JSON request/response bodies, schema types, timings. |

Scale: hero 54px (Poppins 700), section heading 30px, endpoint/label 14px (Inter), code 12.5px (JetBrains Mono). Set marketing display in **Poppins**; keep dense product UI in Inter so it stays legible.

---

## Shape, spacing & motion

- **Radius:** cards & panels `12px`, buttons & inputs `9px`, method chips & pills `7px`, avatars/marks `9999px`. Rounded, matching Poppins' softness.
- **Spacing:** 8px grid; the client is a classic three-pane API tool — endpoint **sidebar** · **request builder** · **response + schema validation**.
- **Elevation:** panels sit on a soft blue-tinted shadow (`0 16px 44px rgba(20,40,90,.10)`); the primary Send button carries the blue→cyan gradient with a subtle glow on hover.
- **Motion:** pressing **Send** shows a brief in-flight state, then the response and its **schema-validation** checks stream in row by row. Smooth and sequential, **deterministic** — every endpoint has a fixed response and validation result.

---

## Components

- **Logo mark** — a light-blue **X** of four rounded blades crossed by a bold royal-blue horizontal "bone", in the blue→cyan gradient; pairs with the `Apidog` wordmark in Poppins.
- **API client** — the core surface: endpoint **sidebar** (method-colored tree) → **request bar** (method chip + URL + Send) with Params/Headers/Body tabs → **response panel** (status · time · size + pretty JSON).
- **Schema-validation strip** — Apidog's signature: each response field checked ✓ against the endpoint's designed schema; a mismatch (wrong type, missing field) shows ✗ with the expected type. This is "debug on specs / keep docs in sync" made visible.
- **Method chip** — a small rounded pill colored by HTTP method (GET green, POST amber, PUT blue, DELETE red, PATCH purple).
- **Buttons** — gradient/solid blue primary (Send, Download), white bordered secondary (Launch Web App).

---

## Guardrails

**Do**
- Keep a **bright white / pale-blue canvas** with deep **navy ink** — Apidog is a light, friendly product (dark mode secondary).
- Use one **blue→cyan gradient** (`#1A66FF → #00AAFF`) for the mark, hero, Send button and active states.
- Set marketing **display in Poppins**; keep dense product UI in Inter, code in JetBrains Mono.
- Lead with the **all-in-one** story — design, debug, test, docs, mock — and make **schema validation** visible (the design-first differentiator).
- Color HTTP methods and statuses as **functional signals only** (GET green, POST amber, DELETE red…).

**Don't**
- Present Apidog as just a request-runner — the point is **design + test in one**, with responses checked against the spec.
- Introduce a competing brand hue; blue→cyan is the only brand family (navy is the ink).
- Set body or dense tables in Poppins — the rounded display is for headings/wordmark.
- Make the gradient neon or muddy — it's a clean royal-blue warming to cyan.
- Drop the X-and-bone mark for a generic API/globe icon.
