# Stytch Design System

## Brand Overview
Stytch is the developer-first authentication platform — passwordless login, session management, and B2B auth. The visual identity is clean and modern — very dark backgrounds, vivid violet-purple accents, and security-forward UI patterns. UI communicates trust through clarity and precision.

## Color Palette

### Primary
- Brand Violet: `#9747FF`
- Violet Light: `#B97AFF`
- Violet Dark: `#7020DD`

### Backgrounds
- Base: `#080812`
- Surface: `#10101E`
- Elevated: `#18182A`
- Border: `#28283C`

### Semantic
- Active: `#22C55E`
- Inactive: `#94A3B8`
- Error: `#EF4444`
- Warning: `#F59E0B`

### Text
- Primary: `#F0F0FF`
- Secondary: `#8B8BAA`
- Muted: `#5A5A70`
- On-violet: `#FFFFFF`

### Auth Method Colors
- Magic Link: `#9747FF`
- OTP: `#3B82F6`
- OAuth: `#FB923C`
- Passkey: `#22C55E`
- Password: `#94A3B8`

## Typography

### Font Stack
- UI: `Inter, system-ui, sans-serif`
- Code/Tokens: `JetBrains Mono, monospace`

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

### User Row
- Avatar (initials on violet bg)
- Email + user ID in mono below
- Auth methods used as icon row
- Status badge: Active / Locked / Pending
- Last login in muted text

### Session Card
- Session token (masked, first+last 4 in mono)
- Created + last active timestamps
- IP address + location in secondary text
- Device/browser string in muted text
- Revoke button: red outline, right-aligned

### Magic Link Preview
- Email preview card: from, subject
- Big violet button mockup in preview
- Token TTL shown as countdown badge
- Sent/opened/clicked tracking chips

### OTP Input
- 6 segmented input boxes
- Active box: violet border 2px
- Filled: solid bg, white digit
- Error: red border with shake animation
- Success: green border fade

### Auth Method Badges
- Small icon + method name pill
- Magic Link: violet
- OTP SMS/Email: blue
- OAuth (Google/GitHub): orange
- Passkey: green
- Password: grey

### Project Environment Toggle
- Live vs Test pill in header
- Live: violet filled
- Test: grey outline
- All keys/tokens change per environment

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

- Border radius: 4px (badges, pills), 6px (inputs, cards), 8px (modals)
- Border: `1px solid #28283C`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.5)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.6)`

## Iconography
- Line icons, 16px and 20px
- Lock, key, shield, fingerprint, mail for auth concepts
- Provider logos for OAuth methods

## Motion
- OTP digit entry: 80ms scale bounce per digit
- Error shake: 300ms horizontal oscillation
- Session revoke: fade out 200ms
- Magic link sent: checkmark reveal 200ms

## Guardrails

### DO
- Always mask session tokens — show only 4+4 chars
- Use violet exclusively for primary actions
- Show auth method icons on every user row
- Separate Live/Test environments visually and persistently
- Show session timestamps in both relative and absolute format

### DON'T
- Don't show full session tokens — ever
- Don't use green for anything except Active/success states
- Don't omit last-login from user rows — it's key audit context
- Don't allow revoke without confirmation dialog
- Don't mix auth method colors across different contexts
