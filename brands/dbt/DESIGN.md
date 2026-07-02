# dbt Design System

## Brand Overview

dbt (by dbt Labs) is "the open standard for modern, AI-ready data transformation." The identity is bright and engineering-native: the signature **dbt orange `#FE6703`** and its rounded-arrow mark, a vivid **purple `#632FF5`**, a punchy **lime `#D8FF33`** accent, and a deep navy `#101828`. Headings run in **Polymath** (dbt's display face), body in **polymath-text**, and code in **IBM Plex Mono** — dbt is a code-first tool, so mono is everywhere.

The defining visual is the **DAG** — the lineage graph of models flowing sources → staging → marts.

> Verified live from getdbt.com (2026). Orange `#FE6703` confirmed 25× in the production CSS; fonts are served via Adobe Typekit (polymath / polymath-text / ibm-plex-mono), which is domain-locked — so this reference uses close Google Fonts equivalents (**Space Grotesk** ≈ Polymath, **Inter** ≈ polymath-text) and the real **IBM Plex Mono**.

## Color Palette

### Primary — dbt orange
- **Orange**: `#FE6703` — brand, primary CTAs, the mark, selected lineage
- **Orange Hover**: `#E85D00` (light) / `#FF7E28` (dark)
- **Button text**: `#101828` — dark navy text on orange (orange is too bright for white)

### Accent
- **Purple**: `#632FF5` — links, secondary; light `#9C79FF`, deep `#6A00FF`
- **Lime**: `#D8FF33` — highlight, "fresh" data accent
- **Yellow**: `#FFCC25` — warnings, callouts

### Node types (DAG / lineage)
- **Source**: `#23C05C` green · **Staging**: `#6B9AFF` blue · **Intermediate**: `#9C79FF` purple · **Mart**: `#FE6703` orange

### Neutrals
- **Ink / navy**: `#101828` — headings, body, dark page
- **Grey**: `#4A5060` · **Muted**: `#8F8F9C` · **Border**: `#E5E7EB`
- **Pale purple**: `#F6F5FF` (page) · **White**: `#FFFFFF`

### Semantic
- **Success (pass)**: `#23C05C` · **Warning**: `#FFCC25` · **Error (fail)**: `#E5484D`

## Typography

Three fonts, one role each. Polymath is Typekit-locked, so this reference approximates it; IBM Plex Mono is the real, Google-Fonts-hosted face.

- **Display — Space Grotesk** (≈ Polymath) (400–700): hero, page + section headings
- **UI / Body — Inter** (≈ polymath-text) (400/500/600): all body, labels, nav, buttons, UI
- **Mono — IBM Plex Mono** (400/500): model names, SQL, CLI, node labels

### Scale
| Token | Size | Weight | Font | Use |
|-------|------|--------|------|-----|
| display | 54px | 700 | Space Grotesk | Hero |
| h1 | 32px | 700 | Space Grotesk | Page title |
| h2 | 22px | 600 | Space Grotesk | Section heading |
| body-lg | 17px | 400 | Inter | Lead paragraph |
| body | 14px | 400 | Inter | Default UI |
| small | 12px | 400 | Inter | Metadata |
| mono | 12px | 400 | IBM Plex Mono | Model names, SQL |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons / inputs: 8px
- Cards / panels: 12px
- DAG nodes: 8px
- Pills / badges: 9999px
- Base: 6px

## Components

### Button
- **Primary**: orange `#FE6703`, **navy `#101828`** text. Labels: `Get started`, `Run models`, `Book a demo`
- **Secondary**: transparent, `--border-strong` outline. Labels: `Read the docs`, `View lineage`
- Orange is theme-invariant; only the hover shifts by theme

### DAG node
Rounded rect with a type dot (source-green / staging-blue / intermediate-purple / mart-orange), model name in mono, and materialization label (`view` / `table` / `incremental`). Click to focus its lineage.

### Lineage edge
Bezier connectors between nodes. On focus, the selected node plus all upstream + downstream nodes and edges light up in orange; everything else dims.

## Signature — Model Lineage (DAG)

dbt's defining view: the model dependency graph. Nodes flow **sources → staging → intermediate → marts**; clicking any model focuses it and highlights its full upstream + downstream lineage in orange while dimming the rest — exactly how you trace a column through a dbt project. Real model names (`stg_orders`, `fct_orders`, `dim_customers`).

## Guardrails

**DO**
- Use dbt orange `#FE6703` for primary actions, the mark, and focused lineage
- Put **navy text on orange** buttons — orange is too bright for white
- Color DAG nodes by type: source-green, staging-blue, intermediate-purple, mart-orange
- Set headings in Polymath (≈ Space Grotesk), code/model names in IBM Plex Mono
- Use purple and lime as accents — they add the dbt energy without competing with orange

**DON'T**
- Don't put white text on the orange button — contrast fails; use navy
- Don't use purple or lime as the primary action — orange owns "go"
- Don't set model names or SQL in a sans — dbt is code-first; mono everywhere
- Don't tint dark surfaces neutral-grey — dbt's dark is navy `#101828`
- Don't fabricate a DAG — use real dbt model naming (`stg_`, `int_`, `fct_`, `dim_`)
</content>
