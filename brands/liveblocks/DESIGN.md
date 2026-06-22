# Liveblocks Design System

## Brand Overview
Liveblocks is the realtime collaboration infrastructure platform. The visual identity is modern and kinetic — near-black backgrounds, vibrant orange-red accents, and presence/cursor-centric UI metaphors. UI communicates live multiplayer state: who's here, what they're doing, and what changed.

## Color Palette

### Primary
- Brand Orange: `#FF5C00`
- Orange Light: `#FF8040`
- Orange Dark: `#CC4A00`

### Backgrounds
- Base: `#0C0C0C`
- Surface: `#141414`
- Elevated: `#1C1C1C`
- Border: `#2C2C2C`

### Semantic
- Online: `#22C55E`
- Away: `#F59E0B`
- Offline: `#525252`
- Error: `#EF4444`

### Presence Colors (User Cursors)
- User 1: `#FF5C00`
- User 2: `#3B82F6`
- User 3: `#8B5CF6`
- User 4: `#EC4899`
- User 5: `#22C55E`
- User 6: `#F59E0B`

### Text
- Primary: `#F5F5F5`
- Secondary: `#A0A0A0`
- Muted: `#666666`
- On-orange: `#FFFFFF`

## Typography

### Font Stack
- UI: `Plus Jakarta Sans, system-ui, sans-serif`
- Code: `JetBrains Mono, monospace`

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

### Presence Avatars
- Circular crop, 28px default
- Stack with -8px overlap, max 5 visible + "+N" overflow
- Online: green ring border
- Away: yellow ring border
- Offline: no ring, desaturated
- Hover: name tooltip

### Cursor Overlay
- SVG cursor icon in user's presence color
- Name tag below cursor in same color
- Smooth interpolated movement (60fps)
- Fade out after 3s inactivity

### Room Event Feed
- Event rows: actor avatar + action + target + timestamp
- Event types: joined, left, commented, changed, reacted
- Timestamp in muted relative text
- New events slide in from top

### Comment Thread
- Avatar + name + timestamp header
- Body text with @mention highlights in orange
- Reaction row: emoji + count
- Reply count badge
- Resolved: dimmed with strikethrough thread line

### Notification Badge
- Position: top-right of trigger element
- Red filled circle with white count
- Max display: "9+" for counts ≥ 10
- Animate in: scale 0.5→1 with bounce

### Connection Status Bar
- Thin bar at top of collaborative area
- Connected: hidden (no bar)
- Connecting: orange animated bar
- Disconnected: red solid bar + message
- Reconnecting: orange pulsing bar

## Spacing

```
4px   — cursor/avatar gap
8px   — component padding xs
12px  — component padding sm
16px  — base padding
20px  — card padding
24px  — section gap
32px  — major section gap
48px  — page section spacing
```

## Elevation & Borders

- Border radius: 50% (avatars), 6px (comment bubbles), 8px (panels)
- Border: `1px solid #2C2C2C`
- Shadow sm: `0 1px 4px rgba(0,0,0,0.4)`
- Shadow md: `0 4px 16px rgba(0,0,0,0.5)`

## Motion
- Cursor movement: 60fps lerp interpolation
- Avatar stack reorder: 250ms ease
- Comment appear: 200ms slide + fade
- Notification badge: 150ms scale bounce
- Connection bar: 300ms fade in/out

## Guardrails

### DO
- Assign each user a unique presence color and use it consistently
- Show presence avatars whenever collaborative context is active
- Animate cursor positions smoothly — choppy cursors break immersion
- Use orange only for the brand's primary actions
- Show connection status non-intrusively (bar only when degraded)

### DON'T
- Don't show offline users in presence avatars — hide or dim them
- Don't reuse presence colors within the same session
- Don't show raw user IDs — always resolve to display names
- Don't stack more than 5 visible avatars without overflow count
- Don't animate every realtime event — only meaningful state changes
