# WorkOS Design System

## Brand Overview
WorkOS provides enterprise authentication infrastructure — SSO, SCIM, and audit logs for B2B SaaS. The visual identity is clean and trustworthy — near-black backgrounds, indigo accents, and a structured, compliance-forward aesthetic. UI feels polished and enterprise-grade without sacrificing developer ergonomics.

## Color Palette

### Primary
- Brand Indigo: `#6366F1`
- Indigo Light: `#818CF8`
- Indigo Dark: `#4338CA`

### Backgrounds
- Base: `#09090B`
- Surface: `#111113`
- Elevated: `#18181C`
- Border: `#27272A`

### Semantic
- Active: `#22C55E`
- Inactive: `#94A3B8`
- Error: `#EF4444`
- Warning: `#F59E0B`
- Info: `#6366F1`

### Text
- Primary: `#FAFAFA`
- Secondary: `#A1A1AA`
- Muted: `#71717A`
- On-indigo: `#FFFFFF`

### Provider Colors
- Google: `#4285F4`
- Microsoft: `#00A4EF`
- Okta: `#007DC1`
- GitHub: `#E8E8E8`
- SAML: `#6366F1`
- OIDC: `#818CF8`

## Typography

### Font Stack
- UI: `Plus Jakarta Sans, system-ui, sans-serif`
- Code/Keys: `JetBrains Mono, monospace`

### Scale
- xs: 11px / 1.5
- sm: 13px / 1.5
- base: 14px / 1.6
- md: 16px / 1.5
- lg: 18px / 1.4
- xl: 22px / 1.3
- 2xl: 28px / 1.2

### Weights
- Regular: 400
- Medium: 500
- Semibold: 600
- Bold: 700

## Components

### SSO Connection Card
- Provider logo (Google, Okta, Microsoft, etc.) + name
- Status badge: Active (green) / Inactive (grey) / Error (red)
- Domain(s) shown in mono below provider name
- Protocol badge: SAML / OIDC pill
- Edit / Test / Delete actions in overflow menu

### Directory Sync Row
- Provider icon + directory name
- Sync status: synced (green checkmark), syncing (spinner), error (red)
- Last synced time in muted text
- User/group count badges

### Organization Card
- Org name + logo/avatar
- Domain list below name
- SSO enabled badge if configured
- Member count
- Created date in muted text

### Audit Log Entry
- Event type in semibold (e.g. `user.created`, `sso.login`)
- Actor email/ID in mono
- Target resource in secondary text
- Timestamp right-aligned
- IP address in muted mono

### API Key Row
- Key name, truncated key in mono (`sk_live_••••••1234`)
- Created date
- Last used date (or "Never")
- Copy button, revoke button
- Environment badge: Live / Sandbox

### Environment Toggle
- Live vs Sandbox pill selector in header
- Live: indigo filled, Sandbox: grey outline
- Key values change per environment

## Spacing

```
4px   — icon gap
8px   — tight padding
12px  — component padding sm
16px  — base padding
20px  — card padding
24px  — section gap
32px  — major section gap
48px  — page section spacing
```

## Elevation & Borders

- Border radius: 4px (badges, pills), 6px (cards, inputs), 8px (modals)
- Border: `1px solid #27272A`
- Shadow sm: `0 1px 3px rgba(0,0,0,0.4)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.5)`

## Iconography
- Line icons, 16px and 20px
- Provider logos: official SVG marks where available
- Lock, key, user, building, shield for auth concepts
- Checkmark, x, spinner for status

## Motion
- Transitions: 150ms ease
- Card hover: subtle border brightening
- Status badge change: 200ms color transition
- Modal: fade + slide-up 200ms

## Guardrails

### DO
- Always mask API keys — show only last 4 chars
- Use provider logos/colors for SSO connection identity
- Show environment (Live/Sandbox) persistently in the header
- Display audit logs in reverse chronological order
- Use indigo exclusively for primary CTA buttons

### DON'T
- Don't show full API secrets after creation
- Don't use green for anything other than Active/success states
- Don't omit timestamps from audit log entries — compliance requires them
- Don't collapse provider type (SAML/OIDC) — it's critical context
- Don't skip confirmation dialogs for destructive actions (revoke, delete)
