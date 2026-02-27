# Changelog

All notable changes to this project will be documented in this file.

## [0.1.0] - 2026-02-27

### Added

- Canonical **INTERIA_SUITE.md** describing the global InterIA Suite:
  - InterIA Style
  - InterIA Quality Pack v4 (quality engine, refactor, AI Bridge, Cosmos & Multiverse)
  - Cosmos Map & Timeline
  - Multiverse (multi-repo analysis)
  - Community & governance links.
- New **README.md** for `interia-suite` with FR/EN toggle and direct links to:
  - `interia-style`
  - `interia-quality`
  - `community`
  - PyPI package `interia-quality`.
- Initial **docs/** structure:
  - `docs/index.md` — high-level landing page for the Suite.
  - `docs/getting_started.md` — how to plug InterIA Quality into an existing repo.
  - `docs/quality.md` — pointer to `interia-quality` documentation & board.
  - `docs/style.md` — pointer to `interia-style` & style guides.
  - `docs/community.md` — pointer to community repo, discussions & code of conduct.
- Initial **skeletons/**:
  - `skeletons/minimal-repo/` with:
    - minimal `README.md` template for scientific repos,
    - example `Makefile` delegating to `interia-quality` (CLI / pip mode),
    - optional `pyproject.toml` scaffold.
- Initial **tools/**:
  - `tools/interia_init.py` — helper script to copy the minimal skeleton into a new repo.
- Cross-repo links and references so that:
  - `interia-quality` can point to this repo as the canonical “Suite overview”,
  - future `INTERIA_SUITE.md` files in other repos can reference this one.

### Notes

- This release focuses on **documentation, structure and onboarding**, not on adding new code.
- All implementation details for the quality engine, AI Bridge, Cosmos & Multiverse live in the `interia-quality` repository.
