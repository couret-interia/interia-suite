# InterIA Suite – Roadmap

This roadmap focuses on the *meta* layer of the Suite (docs, onboarding, skeletons).
Implementation details of the quality engine live in `interia-quality`.

## 0.2.0 – Examples & guided paths

- Add **concrete examples** under `docs/`:
  - “From zero to InterIA‑ready repo” walkthrough.
  - Example of using the InterIA board (portal, quality report, cosmos map).
- Provide an **opinionated skeleton** for:
  - LaTeX‑centric scientific repo (paper only).
  - Mixed code + paper repo (src/ + tex/ + notebooks/).
- Add **links back** from:
  - `interia-quality`’s README to `interia-suite/INTERIA_SUITE.md`,
  - `interia-style`’s README to `interia-suite/INTERIA_SUITE.md`.

## 0.3.0 – Automation & coherence checks

- Add a small **validation script** to check:
  - that README, docs, and portal pages tell a consistent “InterIA Suite” story,
  - that cross‑repo links (URLs) are still valid.
- Optional: provide a tiny **CLI helper** in `tools/` to:
  - create skeleton repos,
  - apply Suite updates (README templates, links) across multiple repos.

## 0.4.0+ – Ecosystem integration

- Document patterns for:
  - CI integration (quality checks, board artifacts),
  - publishing “Proof Gallery” (GitHub Pages) for scientific repos.
- Add **case studies** of real‑world InterIA repos (anonymised or public).
