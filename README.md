# Brand System (Shared)

Shared “brand system” specs for the Ball Lightning AB ecosystem:

- Ball Lightning
- The Builder Coil
- Chronomation

This repo is intentionally framework-agnostic. It documents design foundations, token contracts, UI conventions, and cross-brand policies so the structure/patterns can be reused across codebases.

## What lives here
- Shared design foundation (neutrals, typography contracts, layout conventions)
- Per-brand palettes + semantic token mapping (accent1, accent2, gradients, tag styles)
- Component conventions (card/button/nav behaviors, accessibility baseline)
- Cross-brand policies (newsletter ownership, content syndication rules)

## What does NOT live here
- Site routing/IA, page copy, product requirements
- Secrets, credentials, or operational values

## Files
- `pdd-brands-shared.yaml` — baseline rules + clearly marked optional overlays
- `optional-visual-refresh.yaml` — optional visual overlay proposal (opt-in)

## How to consume from another repo
Pin to a commit SHA for deterministic builds:

- `https://github.com/BallLightningAB/brand-system/blob/<SHA>/pdd-brands-shared.yaml`

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
