# Temporal Design System

## Brand Overview

Temporal is the durable-execution platform — code that survives crashes, retries, and time,
modeled as long-running Workflows and Activities. The identity is confident and near-black,
lit by a vivid spectrum: **purple `#B664FF`**, **mint `#1FF1A5`**, indigo, pink, and lime.
The product's signature is the **event history** — the durable, replayable timeline of a
Workflow execution. Dark-first.

> "The world's best AI runs on Temporal."

## Typography

- **Aeonik** — Temporal's real brand typeface (Air → Black + italics), self-hosted, CORS ✅ —
  **used directly** for display, headings, and UI.
- **Mono** — Workflow IDs, event names, run IDs (here: **JetBrains Mono**).

## Color Palette

### Primary
- Purple: `#B664FF` — brand accent, timers, highlights
- Mint: `#1FF1A5` — completed / success (deep `#59FDA0`)
- Indigo: `#444CE7` — running / started
- Ink: `#141414` — page, surfaces

### Accent (spectrum)
- Pink: `#FF6BFF` · Lime: `#C3FF62` · Red: `#FF5555`

### Surfaces — Dark (real near-black)
- Page: `#141414`
- Surface: `#1C1C1E`
- Elevated: `#26262A`
- Border: `#33333A`

### Surfaces — Light
- Page: `#F8FAFC`
- Card: `#FFFFFF`
- Border: `#E5E7EB`

### Text
- Primary (dark `#F8FAFC` / light `#141414`)
- Secondary: `#9CA3AF`
- Muted: `#6B7280`

### Event / Status
- Scheduled: `#9CA3AF` · Running: `#444CE7` · Completed: `#1FF1A5`
- Failed / Retry: `#FF5555` · Timer: `#B664FF`

## Logo

The **Temporal mark** — the four-lobed atom/starburst (viewBox `0 0 24 24`, single path),
rendered in brand purple `#B664FF` on dark, or `currentColor` in monochrome contexts. Pairs
with the "Temporal" wordmark set in Aeonik.

## Signature Component — Workflow Event History

The Temporal execution view: a Workflow header (Workflow ID, type, status) over the **event
history** — the durable, ordered timeline of events (WorkflowExecutionStarted →
ActivityTaskScheduled/Started/Completed → Timer → Completed). Starting the workflow streams
events in, including an Activity that **fails and retries** before succeeding — the visible
proof of durable execution. Status advances Running → Completed.

## Guardrails

**DO**
- Render the Temporal mark in brand purple `#B664FF` (or a single flat color).
- Use Aeonik for display and UI; the vivid spectrum as accents on near-black.
- Color events by status — running indigo, completed mint, retry red.
- Set Workflow IDs, event names, and run IDs in the mono stack.
- Make durability visible — show retries and attempts in the history.

**DON'T**
- Don't reduce the brand to a single blue — Temporal leads with purple + mint.
- Don't invent dark surfaces; anchor on the real near-black `#141414`.
- Don't reuse a status color for an unrelated event type.
- Don't set IDs or event names in a proportional font.
- Don't hide failed attempts — the retry story is the product.
