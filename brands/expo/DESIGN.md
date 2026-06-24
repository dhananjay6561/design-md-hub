# Expo — Design System

Everything you need to build apps. Expo is a full-stack React Native framework with powerful cloud services — EAS Build, EAS Submit, EAS Update — helping teams move faster from code to production on iOS and Android.

---

## Colors

### App Icon Palette

Expo's product uses a rainbow gradient of platform category colors. All confirmed from `--expo-color-app-*` CSS custom properties in production.

| Token | Hex | Role |
|---|---|---|
| app-cyan | `#07C0CB` | App icon teal |
| app-light-blue | `#1E92C4` | SDK / APIs |
| app-dark-blue | `#0B67AF` | Navigation |
| app-indigo | `#4B50B2` | Build / EAS |
| app-purple | `#8945A3` | Auth |
| app-pink | `#C04891` | Notifications |
| app-orange | `#E96D3C` | Camera / Media |
| app-gold | `#F38F2F` | Payments |
| app-yellow | `#EEBC01` | Maps |
| app-lime | `#AABD04` | Analytics |
| app-light-green | `#6AA72A` | Storage |
| app-dark-green | `#3A8E39` | CLI / Dev tools |

### Surfaces — Light Mode (Radix Slate, confirmed)

| Slate step | Hex | Token |
|---|---|---|
| slate-1 | `#FCFCFD` | bg / screen |
| slate-2 | `#F9F9FB` | subtle bg |
| slate-3 | `#F0F0F3` | element bg |
| slate-4 | `#E8E8EC` | hover bg |
| slate-5 | `#E0E1E6` | selected |
| slate-6 | `#D9D9E0` | border-2 |
| slate-7 | `#CDCED6` | border |
| slate-8 | `#B9BBC6` | text muted |
| slate-9 | `#8B8D98` | placeholder |
| slate-10 | `#80838D` | text-3 |
| slate-11 | `#60646C` | text-2 |
| slate-12 | `#1C2024` | text |

### Surfaces — Dark Mode (Radix Slate dark + Expo override, confirmed)

| Slate step | Hex | Token |
|---|---|---|
| screen | `#0C0D0E` | bg / screen (Expo override of slate-1) |
| slate-2 | `#18191B` | subtle bg / surface |
| slate-3 | `#212225` | element bg / cards |
| slate-4 | `#272A2D` | hover bg |
| slate-5 | `#2E3135` | selected |
| slate-6 | `#363A3F` | border-2 |
| slate-7 | `#43484E` | border |
| slate-8 | `#5A6169` | text muted |
| slate-9 | `#696E77` | placeholder |
| slate-10 | `#777B84` | text-3 |
| slate-11 | `#B0B4BA` | text-2 |
| slate-12 | `#EDEEF0` | text |

### Semantic Colors (Radix scales, confirmed)

| Role | Light step-9 | Light text (step-11) | Dark step-9 | Dark text (step-11) |
|---|---|---|---|---|
| Success | `#30A46C` | `#218358` | `#30A46C` | `#3DD68C` |
| Warning | `#FFC53D` | `#AB6400` | `#FFC53D` | `#FFCA16` |
| Error | `#E5484D` | `#CE2C31` | `#E5484D` | `#FF9592` |
| Info | `#0090FF` | `#0D74CE` | `#0090FF` | `#70B8FF` |

---

## Typography

### Font Families

| Role | Family | Weights | Source |
|---|---|---|---|
| UI / Body / Display | Inter | 100–900 (variable) | `static.expo.dev/static/fonts/inter-latin.woff2` |
| Code / Terminal | JetBrains Mono | 100–800 (variable) | `static.expo.dev/static/fonts/jetbrains-mono-latin.woff2` |

### Type Scale

| Level | Size | Weight | Line Height | Font |
|---|---|---|---|---|
| h1 | 48px | 700 | 1.1 | Inter |
| h2 | 32px | 700 | 1.2 | Inter |
| h3 | 20px | 600 | 1.3 | Inter |
| body-lg | 16px | 400 | 1.6 | Inter |
| body | 14px | 400 | 1.5 | Inter |
| label | 11px | 600 | 1 | Inter |
| code | 13px | 400 | 1.6 | JetBrains Mono |

---

## Spacing & Radius

Base unit: 4px

| Token | Value |
|---|---|
| radius-sm | 4px |
| radius-md | 6px |
| radius-lg | 8px |
| radius-xl | 12px |
| radius-2xl | 16px |
| radius-full | 9999px |

---

## Components

### Buttons (confirmed from `--expo-theme-button-*` tokens)

| Variant | Background | Text | Border |
|---|---|---|---|
| Primary | `#000` | `#FFF` | — |
| Secondary | `var(--slate-3)` | `var(--slate-12)` | — |
| Tertiary | transparent | `var(--slate-12)` | `1px var(--slate-7)` |

### Build Status Badges

| Status | Background | Text |
|---|---|---|
| Finished | `var(--green-3)` | `var(--green-11)` |
| Failed | `var(--red-3)` | `var(--red-11)` |
| In Queue | `var(--amber-3)` | `var(--amber-11)` |
| Cancelled | `var(--slate-3)` | `var(--slate-11)` |

---

## Guardrails

**DO**
- Use Radix Slate tokens for all surface colors — never hardcode surface hex values directly
- Use Inter for all UI text; JetBrains Mono for terminal output, logs, and build IDs
- Keep primary buttons black — Expo's brand is intentionally B&W for primary actions
- Use the app icon palette as decorative category indicators only, never as status or interactive colors
- Dark screen bg is `#0C0D0E`, not slate-1 `#111113` — Expo explicitly overrides it

**DON'T**
- Don't use the rainbow app colors for buttons, alerts, or status — they're platform/category identifiers
- Don't use Inter below 11px or JetBrains Mono below 12px
- Don't deviate from Radix semantic color steps — green-9 for filled badges, green-11 for text
- Don't add border-radius beyond 16px in product UI — keep it clean and tight
- Don't use `#000` as a surface color — only as a button background
