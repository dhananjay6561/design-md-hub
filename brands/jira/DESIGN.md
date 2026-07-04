# Jira Design System

## Brand Overview

Jira is Atlassian's project-management tool for the AI era — used by millions of agile teams to
plan, track, and release work. The design language is the **Atlassian Design System (ADS)**:
professional, information-dense, systematic. A confident blue anchors a neutral canvas, and a
precise set of status, priority, and issue-type semantics does the heavy lifting. Light-first —
the board is a bright workspace.

> "Plan, track, and release great software — the #1 project-management tool for agile teams."

## Typography

- **Charlie Display** / **Charlie Text** — Atlassian's proprietary brand typefaces (headings /
  body). Proprietary; not distributable.
- **Fallback used here:** **Inter** for both display and text (≈ Charlie — humanist grotesque).
- Code / issue keys / metadata → the ADS code stack (here: **JetBrains Mono**).

## Color Palette

### Primary — Atlassian Blue
- Blue (brand / links): `#0C66E4`
- Blue Bold (hover): `#1558BC`
- Blue Classic: `#0052CC`
- Blue Subtle (tint): `#E9F2FF`

### Issue Priority
- Highest: `#C9372C` (red, ↑↑)
- High: `#E56910` (orange, ↑)
- Medium: `#E2B203` (amber, =)
- Low: `#4688EC` (blue, ↓)

### Status
- To Do: `#626F86` (neutral)
- In Progress: `#0C66E4` (blue)
- In Review: `#5E4DB2` (purple)
- Done: `#22A06B` (green)

### Issue Types
- Story: `#63BA3C` · Task: `#4BADE8` · Bug: `#E5493A` · Epic: `#904EE2`

### Surfaces — Light
- Page: `#FFFFFF`
- Sunken (board): `#F7F8F9`
- Card: `#FFFFFF`
- Border: `#DFE1E6`

### Surfaces — Dark (real ADS neutrals)
- Page: `#1D2125`
- Surface: `#22272B`
- Raised (card): `#282E33`
- Border: `#38414A`

### Text
- Primary (light `#172B4D` / dark `#C7D1DB`)
- Subtle: `#44546F` (dark `#9FADBC`)
- Muted: `#626F86`

## Logo

The **Jira mark** — three ascending chevrons forming an upward arrow (viewBox `0 0 24 24`,
single path), filled with the Jira blue gradient `#2684FF → #0C66E4`. The gradient direction is
fixed; the mark is never flattened to a flat blue in brand contexts.

## Signature Component — Board

An agile board mirroring Jira: four columns (**To Do / In Progress / In Review / Done**) with
issue cards. Each card carries an issue-type icon, summary, key (`KAN-##`), priority icon, and
an assignee avatar. Click a card to **advance it to the next column** — column counts update
live, and a card in Done stays put. This is the core Jira work moment.

## Guardrails

**DO**
- Keep the Jira mark's blue gradient intact and upward-facing.
- Use ADS status colors consistently — To Do neutral, In Progress blue, Done green.
- Pair issue-type and priority with an icon, never color alone (accessibility).
- Set issue keys and metadata in the mono stack.
- Keep the board neutral (`#F7F8F9`) so colored cards and lozenges lead.

**DON'T**
- Don't flatten or recolor the Jira gradient mark.
- Don't invent dark surfaces; anchor on the real ADS neutral scale (`#1D2125`…).
- Don't reuse a status color for an unrelated meaning.
- Don't set issue keys in a proportional font.
- Don't put more than one bold/primary button in a single action group.
