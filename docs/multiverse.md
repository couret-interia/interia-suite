# 🌌 InterIA Multiverse

The InterIA Multiverse analyses several repositories together:

- structural distance,
- documentary gravity (citations + macros),
- thematic bridges (BibTeX keywords, citation keys),
- code bridges (Python imports),
- 3D multiverse visualisation.

## Usage

From a repository equipped with InterIA:

```bash
make multiverse-map repos="../repoA ../repoB ../repoC"
make multiverse-gravity
make multiverse-bridges
make multiverse-3d-html
```

Outputs include:

- `interia_multiverse_map.json`
- `interia_multiverse_matrix.json`
- `interia_multiverse_gravity.json`
- `interia_multiverse_3d.json`
