# Auth0 Design System

## Overview

Auth0 (by Okta) is the identity platform for developers — "secure AI agents, humans, and whatever comes next." The current brand is built on a confident **indigo** (not the legacy orange), a warm off-white paper surface, geometric grotesque display type, and the four-shape shield mark. It reads as secure and modern, but developer-first and approachable rather than sterile enterprise.

**Brand personality:** Secure, modern, developer-first, identity for humans and AI.

**Positioning (live copy):** "Secure users, AI agents, and more with an easy-to-implement, scalable, and adaptable authentication and authorization platform."

---

## Colors

Auth0 is **light-first** on a warm `#FFFEFA` paper background with white cards; dark mode is a neutral near-black (`#111111`). Indigo is the identity.

### Primary — indigo
| Token | Hex | Usage |
|-------|-----|-------|
| `--indigo` | `#635DFF` | Primary brand, CTAs, the "Continue" button |
| `--blue` | `#3F59E4` | Links, secondary actions, focus |
| `--purple-deep` | `#4016A0` | Deep accent, emphasis, gradients |

### Accents — lavender
| Token | Hex | Usage |
|-------|-----|-------|
| `--lavender` | `#BCBAFF` | Soft accent, illustration |
| `--periwinkle` | `#99A7F1` | Highlight tint |
| `--sky` | `#B6CAFF` | Light-blue accent |
| `--violet` | `#C698FF` | Purple accent |

### Surfaces — Light
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#FFFFFF` | Cards, the login widget |
| `--bg2` | `#FFFEFA` | Page background (warm paper) |
| `--bg3` | `#F4F4F4` | Fills, hover |
| `--border` | `#E5E5E5` | Borders, dividers |

### Surfaces — Dark (neutral near-black)
| Token | Hex | Usage |
|-------|-----|-------|
| `--bg` | `#191919` | Cards, panels |
| `--bg2` | `#111111` | Page background |
| `--bg3` | `#2A2A2A` | Elevated, hover |
| `--border` | `rgba(255,255,255,.10)` | Borders, dividers |

### Text & semantic
| Token | Hex (light) | Hex (dark) | Usage |
|-------|-------------|------------|-------|
| `--text` | `#191919` | `#FFFEFA` | Headings, body |
| `--text2` | `#555555` | `#ABABAB` | Labels, secondary |
| `--text3` | `#8C929C` | `#8C929C` | Muted, placeholder |
| `--success` | `#4CB7A3` | `#4CB7A3` | Authenticated, healthy |

---

## Typography

| Role | Font | Notes |
|------|------|-------|
| Display / headings | **Aeonik** (≈ Space Grotesk) | Aeonik is commercial; Auth0 also ships Space Grotesk — the CORS-safe substitute, on Google Fonts |
| UI / body | **Inter** | Auth0's actual body font — Google Fonts |
| Mono / code | **Roboto Mono** | Auth0's actual mono (also Aeonik Mono) — Google Fonts |

### Scale
| Token | Size | Weight | Sample |
|-------|------|--------|--------|
| `display-2xl` | 52px | 600 | Auth0 |
| `display-xl` | 32px | 600 | Built for what you're building |
| `display-md` | 22px | 500 | More signups. Less friction. |
| `text-lg` | 16px | 400 | Body / lead copy |
| `text-sm` | 14px | 400 | UI copy, form labels |
| `ui-mono` | 12px | 400 | `auth0 login --domain your-tenant` |

---

## Components

- **Buttons:** indigo `#635DFF` primary (white text, safe in both themes), outline secondary, text link. Radius `8px`.
- **Universal Login:** the Lock widget — logo, email/password, Continue, social providers, tab toggle.
- **Social buttons:** outlined, provider icon + label (Google, GitHub, Microsoft).
- **Inputs:** 1px border, `#635DFF` focus ring at 3px / ~25% alpha.
- **Badges:** `Verified`, `MFA`, `Passkey` — indigo/teal semantic fills.

### Radius & elevation
| Token | Value |
|-------|-------|
| `radius-sm` | 6px |
| `radius-md` | 8px |
| `radius-lg` | 14px |
| `shadow-card` | `0 2px 4px rgba(25,25,25,.06), 0 12px 32px rgba(25,25,25,.10)` |

---

## Signature component

**Universal Login.** Auth0's defining artifact: the drop-in login box. The widget shows the Auth0 logo, email + password fields, an indigo **Continue** button, an "or continue with" divider, and social providers. Tabs toggle between **Log in** and **Sign up** (changing the button and footer copy); pressing Continue animates through "Authenticating…" to an authenticated state.

Seen with no branding, the centered login card with social buttons and the indigo Continue button is unmistakably Auth0 Universal Login.

---

## Guardrails

**DO**
- Use indigo `#635DFF` as the one primary — it's the current Auth0 brand color.
- Keep page backgrounds warm paper `#FFFEFA`; let indigo carry emphasis.
- Keep the shield mark monochrome; render it on paper, white, or dark.
- Use neutral near-black (`#111111`) for dark surfaces — not navy.
- Use teal `#4CB7A3` only for genuine success / authenticated states.

**DON'T**
- Don't use the legacy orange `#EB5424` — Auth0 rebranded to indigo `#635DFF`.
- Don't tint dark surfaces blue/navy — Auth0's dark is neutral gray-black.
- Don't set display headings in Roboto Mono or the body font — Aeonik / Space Grotesk owns headings.
- Don't overload the login widget — one primary action (Continue), providers secondary.
- Don't fake provider names — use real IdPs (Google, GitHub, Microsoft).
