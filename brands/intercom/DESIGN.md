# Intercom Design System

## Brand Overview
Intercom is a customer messaging platform — live chat, support, and product tours. The brand is approachable and human, built on a signature blue with conversational UI patterns.

## Color Palette

### Primary
- **Blue**: `#1F8EFA` — primary brand, CTAs, user bubbles
- **Blue Dark**: `#0F7AE5` — hover, pressed
- **Blue Light**: `#5AACFF` — highlights

### Semantic
- **Success**: `#00C896`
- **Warning**: `#F5A623`
- **Error**: `#FC4747`
- **Online**: `#00C896` — green dot

### Surfaces (Dark Mode)
- **Background**: `#0C1219`
- **Surface**: `#14202E`
- **Elevated**: `#1D2F42`
- **Border**: `#283E55`

### Text
- **Primary**: `#EDF2F7`
- **Secondary**: `#7FA8C4`
- **Muted**: `#3D6080`

## Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Mono Font**: JetBrains Mono (for user IDs, conversation IDs)

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Chat bubbles: 18px (rounded), flat on sender side bottom
- Buttons: 8px
- Cards: 12px
- Inputs: 8px

## Components

### Chat Bubble
- User message: blue bg, right-aligned
- Agent message: surface bg, left-aligned, avatar left
- Timestamp below bubble, muted

### Conversation List Row
- Avatar + name + preview text truncated
- Unread count badge blue, right
- Last message time right-aligned

### Presence Dot
- 10px circle, green = online, grey = offline
- Positioned bottom-right of avatar

### Team Badge
- Team name with member count, surface bg

## Guardrails
- Chat bubbles must have generous padding — conversations need breathing room
- User vs agent messages must be clearly distinct at a glance
- Online status dot must always be visible on avatars
- Never truncate a message preview below 2 lines
- Conversation IDs in monospace
