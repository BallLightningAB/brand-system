# Brand System (Shared)

Shared “brand system” specs for the Ball Lightning AB ecosystem:

- Ball Lightning
- The Builder Coil
- Chronomation

This repo is intentionally framework-agnostic. It documents design foundations, token contracts, UI conventions, and cross-brand policies so the structure/patterns can be reused across codebases.

## System overview
Shared documents live in this repo. Project-specific PDDs live in their own product repos and **reference** the shared docs.

## What lives here
- Shared design foundation (neutrals, typography contracts, layout conventions)
- Per-brand palettes + semantic token mapping (accent1, accent2, gradients, tag styles)
- Component conventions (card/button/nav behaviors, accessibility baseline)
- Cross-brand policies (newsletter ownership, content syndication rules)

## What does NOT live here
- Site routing/IA, page copy, project-specific requirements
- Secrets, credentials, or operational values

## Files
- `shared-design-system.yaml` — shared design + cross-brand policies
- `shared-architecture.yaml` — shared architecture + policy references (email, hosting, integrations)
- `shared-ecosystem-pdd.yaml` — shared PDD across brands
- `optional-visual-refresh.yaml` — optional visual overlay proposal (opt-in)

## Project-specific PDDs (live in product repos)
- The Builder Coil: `https://github.com/BallLightningAB/thebuildercoil/blob/main/specs/memory-bank/thebuildercoil-pdd.yaml`
- Chronomation: (to be added)
- Ball Lightning: (to be added)

## Reference format (cross-file anchors)
Use dot-delimited paths after a `#` to point at a YAML section.

Example:
- `shared-architecture.yaml#architecture.techstack.thebuildercoil`
- `shared-ecosystem-pdd.yaml#meta.ecosystem`

## PDD vs Architecture decision guide
- **PDD (shared-ecosystem-pdd.yaml)**: Why, who, what.
  - Vision, objectives, personas, scope.
  - Product/brand definitions.
  - References to architecture/design.
- **Architecture (shared-architecture.yaml)**: How, where, deployment.
  - Tech stack, tenancy model, data model, routes.
  - Media/video strategy, email architecture.
  - Non-functional, env vars, implementation plan.
- **Design System (shared-design-system.yaml)**: Visual and interaction standards.
  - Tokens, typography, palettes, component guidance.
  - Cross-brand policies and precedence.

## How to consume from another repo
Pin to a commit SHA for deterministic builds:

- `https://github.com/BallLightningAB/brand-system/blob/<SHA>/shared-design-system.yaml`
- `https://github.com/BallLightningAB/brand-system/blob/<SHA>/shared-architecture.yaml`
- `https://github.com/BallLightningAB/brand-system/blob/<SHA>/shared-ecosystem-pdd.yaml`

Recommended workflow:
1. Change this repo via PR (even if self-merged).
2. Merge → new SHA.
3. Update downstream repos to the new pinned SHA.

## Newsletter policy (important)
“The Upkeep” is canonical on **The Builder Coil** only.

Other brand sites (e.g. Ball Lightning) must not store subscriber PII or maintain a separate list.
They may only link/CTA to The Builder Coil for signup.

## License
- Code/specs: Apache-2.0 — see `LICENSE`
- Brand identifiers and brand assets: restricted — see `TRADEMARKS.md` and `brand-assets/README.md`
