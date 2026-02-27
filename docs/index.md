# 🌌 InterIA Suite

<style>
input.tog[type="radio"]{display:none}
label.tog{font-size:1.1rem;float:right;position:sticky;top:0;cursor:pointer;padding:.45rem .9rem;background:rgba(126,126,126,.25);border-radius:.25rem;margin-right:.2rem}
input.tog[type="radio"]:checked+label.tog{background:rgba(216,162,126,.52)}
.toggle-fr,input.tog[type="radio"]:checked+label.tog+.toggle>.toggle-en{display:block}
input.tog[type="radio"]:checked+label.tog+.toggle>.toggle-fr,.toggle-en{display:none}
</style>

<form>
<input class="tog" type="radio" id="toggle-fr" name="toggle">
<label class="tog" for="toggle-fr">🇫🇷</label>
<input class="tog" type="radio" id="toggle-en" name="toggle" checked>
<label class="tog" for="toggle-en">🇬🇧</label>
<div class="toggle">

<div class="toggle-fr">

> **Suite InterIA** — port d’entrée unifié pour le style, la qualité, le cosmos documentaire et le multivers de vos dépôts scientifiques.

---

## 🧭 Vue d’ensemble

La Suite InterIA rassemble plusieurs briques coordonnées :

- 🎨 **InterIA Style**
  Templates, branding, guides de style et conventions rédactionnelles.
- 🧪 **InterIA Quality Pack v4** (`interia-quality`)
  Moteur qualité modulaire, aide à la refonte, pont IA, cartes de structure (Cosmos, Galaxies, Multivers).
- 🌐 **InterIA Cosmos**
  Cartes de structure d’un dépôt (Python / Markdown / LaTeX / BibTeX) + timeline documentaire.
- 🌠 **InterIA Multiverse**
  Analyses multi‑dépôts, distances structurelles, gravité documentaire, visualisation 3D.
- 👥 **InterIA Community**
  Discussions, gouvernance, templates corporate, code de conduite.

Ce dépôt **`interia-suite`** sert de :

- point d’entrée documentaire,
- vue d’ensemble cohérente,
- index des dépôts et paquets associés.

---

## 🧩 Composants principaux

### 🎨 Style InterIA

- Référentiel des :
  - templates de README & “hero pages”,
  - guides de style (Markdown / LaTeX / code),
  - snippets pour GitHub (issues, PR, CI).
- Dépôt cible :
  `https://github.com/couret-interia/interia-style`

### 🧪 Pack InterIA Quality v4

- Paquet Python **`interia-quality`** :
  - plugins qualité (Python, Markdown, LaTeX, BibTeX),
  - refactor plan (`refactor_plan.json` / `.md`),
  - pont IA (`ai_request.json`, `ai_response.json`, `ai_prompt.txt`),
  - cartes Cosmos & Galaxies,
  - portail HTML local (board InterIA).
- Dépôt :
  `https://github.com/couret-interia/interia-quality`
- Paquet PyPI :
  `https://pypi.org/project/interia-quality/`

### 🌐 Cosmos & Chronologie

- Niveau dépôt unique :
  - `cosmos_map.json`, `cosmos_map_summary.json`,
  - `cosmos_timeline.json`, `cosmos_history/…`.
- Visualisation :
  - `interia_quality/board/cosmos_explorer.html`,
  - `interia_quality/board/cosmos_timeline.html`.

### 🌠 Multi unvers

- Niveau multi‑dépôts :
  - `interia_multiverse_map.json`,
  - `interia_multiverse_matrix.json`,
  - `interia_multiverse_gravity.json`,
  - `interia_multiverse_3d.json`.
- Visualisation :
  - `interia_quality/board/multiverse_3d.html`.

### 👥 Communauté

- Discussions, RFC, coordination :
  - `https://github.com/couret-interia/community`
- Code de conduite & politiques communes.

---

## 🚀 Où commencer ?

Pour **un dépôt scientifique existant** :

1. Installer le moteur qualité :

    ```bash
    pip install interia-quality
    ```

2. À la racine du dépôt :

    ```bash
    interia-quality           # checks de base
    interia-quality cosmos-map
    interia-quality latex-galaxy
    interia-quality bib-galaxy
    ```

3. Pour le board HTML :

    ```bash
    interia-quality init-board
    interia-quality portal
    ```

Pour **une intégration plus profonde** (mode “vendored” avec Makefile, cibles multivers, etc.), voir :

- `interia-quality/INTERIA_SUITE.md` (vue Quality Pack)
- `docs/getting_started.md` (ce dépôt).

---

## 🔗 Liens utiles

- 🧪 InterIA Quality Pack v4
  `https://github.com/couret-interia/interia-quality`
- 🎨 InterIA Style
  `https://github.com/couret-interia/interia-style`
- 👥 InterIA Community
  `https://github.com/couret-interia/community`
- 📦 PyPI `interia-quality`
  `https://pypi.org/project/interia-quality/`

---

</div>

<div class="toggle-en">

> **InterIA Suite** — unified entry point for style, quality, documentary cosmos and multiverse of your scientific repositories.

---

## 🧭 Overview

The InterIA Suite brings together several coordinated components:

- 🎨 **InterIA Style**
  Templates, branding, style guides and writing conventions.
- 🧪 **InterIA Quality Pack v4** (`interia-quality`)
  Modular quality engine, refactor assist, AI Bridge, structure maps (Cosmos, Galaxies, Multiverse).
- 🌐 **InterIA Cosmos**
  Single‑repo structure maps (Python / Markdown / LaTeX / BibTeX) + documentary timeline.
- 🌠 **InterIA Multiverse**
  Cross‑repo analysis, structural distances, documentary gravity, 3D visualisation.
- 👥 **InterIA Community**
  Discussions, governance, corporate templates, code of conduct.

This **`interia-suite`** repository acts as:

- the main documentation entry point,
- a coherent high‑level overview,
- an index of related repos and packages.

---

## 🧩 Core components

### 🎨 InterIA Style

- Reference for:

  - README & hero templates,
  - style guides (Markdown / LaTeX / code),
  - GitHub snippets (issues, PRs, CI).
- Repo:
  `https://github.com/couret-interia/interia-style`

### 🧪 InterIA Quality Pack v4

- Python package **`interia-quality`**:

  - quality plugins (Python, Markdown, LaTeX, BibTeX),
  - refactor plan (`refactor_plan.json` / `.md`),
  - AI Bridge (`ai_request.json`, `ai_response.json`, `ai_prompt.txt`),
  - Cosmos & Galaxy maps,
  - local HTML board / portal.
- Repo:
  `https://github.com/couret-interia/interia-quality`
- PyPI:
  `https://pypi.org/project/interia-quality/`

### 🌐 Cosmos & Timeline

- Per‑repo structures:

  - `cosmos_map.json`, `cosmos_map_summary.json`,
  - `cosmos_timeline.json`, `cosmos_history/…`.
- Views:

  - `interia_quality/board/cosmos_explorer.html`,
  - `interia_quality/board/cosmos_timeline.html`.

### 🌠 Multiverse

- Cross‑repo structures:

  - `interia_multiverse_map.json`,
  - `interia_multiverse_matrix.json`,
  - `interia_multiverse_gravity.json`,
  - `interia_multiverse_3d.json`.
- View:

  - `interia_quality/board/multiverse_3d.html`.

### 👥 Community

- Discussions, RFCs, coordination:

  - `https://github.com/couret-interia/community`
- Code of conduct & shared policies.

---

## 🚀 Where to start?

For an **existing scientific repo**:

1. Install the quality engine:

    ```bash
    pip install interia-quality
    ```

2. At the repo root:

    ```bash
    interia-quality           # basic checks
    interia-quality cosmos-map
    interia-quality latex-galaxy
    interia-quality bib-galaxy
    ```

3. For the HTML board:

    ```bash
    interia-quality init-board
    interia-quality portal
    ```

For a **deeper integration** (vendored mode with Makefile, multiverse targets, etc.), see:

- `interia-quality/INTERIA_SUITE.md` (Quality Pack view)
- `docs/getting_started.md` (this repo).

---

## 🔗 Useful links

- 🧪 InterIA Quality Pack v4
  `https://github.com/couret-interia/interia-quality`
- 🎨 InterIA Style
  `https://github.com/couret-interia/interia-style`
- 👥 InterIA Community
  `https://github.com/couret-interia/community`
- 📦 PyPI `interia-quality`
  `https://pypi.org/project/interia-quality/`

---

</div>
</div>
</form>
