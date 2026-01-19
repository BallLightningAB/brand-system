# Brand System (Shared)

This repo contains the shared “brand system” for the Ball Lightning AB ecosystem:
- Ball Lightning (balllightning.cloud)
- The Builder Coil (thebuildercoil.com)
- Chronomation (chronomation.com)

It is intentionally framework-agnostic and written as specs (YAML) so each site/app can implement it in its own codebase.

## What lives here
- Shared design foundation (backgrounds, neutrals, typography contracts)
- Per-brand palettes + semantic tokens (accent1, accent2, gradient, tag styles)
- Shared component conventions (ShadCN theme expectations, button/card/nav behaviors)
- Cross-brand policies (newsletter canonical ownership, syndication rules)

## What does NOT live here
- Site information architecture, page copy, routing
- Product-specific requirements for Chronomation, TBC, or Ball Lightning
- Secrets or operational credentials

## Files
- `pdd-brands-shared.yaml` — source of truth for shared rules (active baseline + optional overlays)
- `optional-visual-refresh.yaml` — optional overlay proposal (may contradict baseline; opt-in only)

## How to consume from another repo
Pin to a commit SHA for deterministic builds.

Example reference format:
- `https://github.com/<org>/<repo>/blob/<SHA>/pdd-brands-shared.yaml`

Recommended workflow:
1. Propose changes here via PR (even if self-merged).
2. Merge → new SHA.
3. Update downstream repos to pin the new SHA.

## Newsletter policy (important)
The newsletter (“The Upkeep”) is canonical on **The Builder Coil** only.
Other brand sites (e.g. Ball Lightning) must not store subscriber PII or run their own list.
They may only link/CTA to thebuildercoil.com for signup.

## License
MIT — see `LICENSE`.
