# Terraform Design System

## Brand Overview

Terraform (by HashiCorp) is the standard for infrastructure as code — "Automate Infrastructure on Any Cloud." The identity is calm and technical: the unmistakable **Terraform purple `#7B42BC`** and its stacked-parallelogram mark, neutral surfaces, and a monospace CLI whose `plan`/`apply` diff — green to add, yellow to change, red to destroy — is one of the most recognizable outputs in all of software.

Dark-first: infra work lives in the terminal. Purple drives every action; the plan diff colors carry the semantics.

> Verified live from developer.hashicorp.com/terraform (2026). Terraform purple `#7B42BC` confirmed as the button token (hover `#713DAD`, active `#65369A`); fonts Gilmer + Metro + DejaVu Sans Mono confirmed CORS-clean from HashiCorp's CDN.

## Color Palette

### Primary — Terraform purple
- **Purple**: `#7B42BC` — brand, primary CTAs, the mark
- **Purple Hover**: `#713DAD` — hover
- **Purple Active**: `#65369A` — pressed/active
- **Purple Light**: `#A067DA` — accents, dark-mode brand lift

### Plan diff (semantic — the signature)
- **Create (+)**: `#23C05C` green — resources to add
- **Update (~)**: `#E5A000` amber — resources to change in-place
- **Destroy (-)**: `#E5484D` red — resources to destroy

### Neutrals
- **Ink**: `#1B1D22` — headings, body (light) / dark page
- **Grey**: `#656A76` — secondary text
- **Border**: `#DADADD` · **Fill**: `#F2F2F3` · **Off-white**: `#F9F9FB` · **White**: `#FFFFFF`
- **HashiCorp blue**: `#2E71E5` — corporate link accent (use sparingly)

## Typography

Three fonts, one role each — HashiCorp's real brand fonts, all CORS-clean from their CDN.

- **Display — Gilmer** (300–700): hero, page + section headings
- **UI / Body — Metro** (300/400/600/700): all body, labels, nav, buttons, UI
- **Mono — DejaVu Sans Mono** (400): CLI, plan/apply output, code, resource addresses

### Scale
| Token | Size | Weight | Font | Use |
|-------|------|--------|------|-----|
| display | 54px | 700 | Gilmer | Hero |
| h1 | 32px | 700 | Gilmer | Page title |
| h2 | 22px | 600 | Gilmer | Section heading |
| body-lg | 17px | 400 | Metro | Lead paragraph |
| body | 14px | 400 | Metro | Default UI |
| small | 12px | 400 | Metro | Metadata |
| mono | 12.5px | 400 | DejaVu Sans Mono | CLI, plan output |

## Spacing
4px base — 4, 8, 12, 16, 24, 32, 48, 64.

## Border Radius
- Buttons / inputs: 6px
- Cards / panels: 8px
- Terminal: 10px
- Pills / badges: 9999px
- Base: 5px

## Components

### Button
- **Primary**: purple `#7B42BC`, white text (hover `#713DAD`, active `#65369A`). Labels: `Get Started`, `terraform apply`, `Install`
- **Secondary**: transparent, `--border-strong` outline. Labels: `Documentation`, `Cancel`
- On dark, purple lifts to `#8B52CC` for contrast — white text in both

### Plan diff line
Monospace row prefixed with `+` / `~` / `-` in create-green / update-amber / destroy-red. Resource comments (`# aws_instance.web will be created`) sit in grey above each block.

### Terminal
Always dark (`#0A0A0C`), DejaVu Sans Mono, prompt in purple, streamed output lines fading in — the home of Terraform.

## Signature — Plan & Apply

Terraform's defining moment: `terraform plan` renders a colored resource diff (add/change/destroy) with the `Plan: 2 to add, 1 to change, 1 to destroy` summary; hitting **terraform apply** streams each resource `Creating… / Modifying… / Destroying…` line by line, ending in a green `Apply complete! Resources: 2 added, 1 changed, 1 destroyed.` Deterministic, real HCL resource names.

## Guardrails

**DO**
- Use Terraform purple `#7B42BC` for primary actions and the mark — it is the brand
- Color the plan diff semantically: green `+` add, amber `~` change, red `-` destroy — never swap
- Keep the CLI in DejaVu Sans Mono on a near-black terminal in both themes
- Set headings in Gilmer, body/UI in Metro — one role each
- Lift purple to `#8B52CC` on dark so it stays legible

**DON'T**
- Don't recolor the stacked-parallelogram mark — it is fixed Terraform purple
- Don't use HashiCorp corporate blue `#2E71E5` as the Terraform primary — purple owns Terraform
- Don't set body or UI in Gilmer — it's display only; Metro owns the UI
- Don't render a light terminal — the CLI is always dark
- Don't fabricate plan output — use real resource types and a deterministic apply
</content>
