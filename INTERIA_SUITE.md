# 🌌 InterIA Suite – Canonical Overview

<details><summary><b>🇫🇷 Français</b> — cliquer pour déployer</summary>

> **Suite InterIA** — point d’entrée unifié pour le style, la qualité, le cosmos documentaire et\
le multivers de vos dépôts scientifiques.

Ce document est la **vue canonique** de la Suite InterIA :

- les pages docs (`docs/index.md`, `docs/getting_started.md`),
- le portail board (`interia_portal.html`),
- et les “Quality Docs” (`docs/quality/index.html`)

doivent *raconter la même histoire que lui*.

---

## 1. 🎯 Rôle de ce document

`INTERIA_SUITE.md` sert de :

- **carte maîtresse** de la Suite (vision, composants, liens),
- **référence commune** pour tous les dépôts InterIA,
- **pont** entre :
  - la documentation GitHub (`docs/…`),
  - le board HTML (`interia_quality/board/…`),
  - et les README locaux (`interia-quality`, `interia-style`, `community`, etc.).

Dans les autres dépôts (par ex. `interia-quality`, `interia-style`), on peut :

- soit **copier** ce fichier tel quel,
- soit **symlinker**/importer la version canonique de `interia-suite`.

---

## 2. 🧭 Vue d’ensemble de la Suite InterIA

La Suite InterIA assemble plusieurs briques coordonnées :

- 🎨 **InterIA Style**
  Templates, branding, guides de style et conventions rédactionnelles.
- 🧪 **InterIA Quality Pack v4** (`interia-quality`)
  Moteur qualité modulaire, aide au maintien, pont IA, cartes de structure (Cosmos, Galaxies, Multivers).
- 🌐 **InterIA Cosmos**
  Cartes de structure d’un dépôt (Python / Markdown / LaTeX / BibTeX) + timeline documentaire.
- 🌠 **InterIA Multiverse**
  Analyses multi‑dépôts, distances structurelles, gravité documentaire, visualisation 3D.
- 👥 **InterIA Community**
  Discussions, gouvernance, templates corporate, code de conduite.

Le dépôt **`interia-suite`** fournit :

- la **vision globale**,
- l’**index** des composants,
- les **documents de démarrage**
  - `docs/index.md` (Accueil),
  - `docs/getting_started.md` (Comment démarrer).

---

## 3. 🧩 Composants principaux

### 3.1 🎨 Style InterIA

- Rôle :
  - unifier le **branding**,
  - proposer des **templates de README** (standard + hero),
  - fournir des **STYLE_GUIDE** (Markdown, LaTeX, code),
  - livrer des snippets GitHub (issues, PR, CI).
- Dépôt cible :
  `https://github.com/couret-interia/interia-style`

On y trouve notamment les gabarits de `README.md`, `README_FR.md`, `README_hero*.md` cités dans certains projets.

---

### 3.2 🧪 Pack InterIA Quality v4 (`interia-quality`)

- Paquet Python autonome, publié sur PyPI sous le nom **`interia-quality`**.
- Fournit :
  - Plugins qualité (Python / Markdown / LaTeX / BibTeX),
  - `quality_report.json` et `refactor_plan.{json,md}`,
  - Pont IA (AI Bridge) : `ai_request.json`, `ai_response.json`, `ai_prompt.txt`,
  - Cartes Cosmos & Galaxies (LaTeX, BibTeX),
  - Un **board HTML** avec portail, rapports et explorateurs (LaTeX, Cosmos, Multivers).

Points d’entrée principaux :

- **CLI** : `interia-quality`
  (voir `README` du dépôt `interia-quality`)
- **Board** : `interia_quality/board/interia_portal.html`
  (ou `interia-quality portal` / `make portal-all`)

---

### 3.3 🌐 Cosmos & Chronologie

Niveau **dépôt unique** :

- **Fichiers produits** :
  - `cosmos_map.json`, `cosmos_map_summary.json`
  - `cosmos_timeline.json`, `cosmos_history/…`
- **Usage typique** (via CLI ou Makefile) :
  - `interia-quality cosmos-map`
  - `interia-quality cosmos-timelapse`

Visualisation via board :

- `cosmos_explorer.html`
- `cosmos_timeline.html`

---

### 3.4 🌠 Multi univers

Niveau **multi‑dépôts** :

- **Fichiers** :
  - `interia_multiverse_map.json`
  - `interia_multiverse_matrix.json`
  - `interia_multiverse_gravity.json`
  - `interia_multiverse_3d.json`
- **Usage typique** (Makefile) :

```bash
make multiverse-map repos="../repoA ../repoB ../repoC"
make multiverse-gravity
make multiverse-3d[-html] repos="../repoA ../repoB ../repoC"
```

Visualisation via board :

- `multiverse_3d.html`

---

### 3.5 👥 Communauté InterIA

- Centralise :
  - discussions publiques (GitHub Discussions),
  - code de conduite et politiques communes,
  - RFC et décisions d’architecture.
- Dépôt :
  `https://github.com/couret-interia/community`

---

## 4. 🚀 Comment adopter la Suite InterIA ?

Deux modes, reflétés dans `docs/getting_started.md` :

### 4.1 1er Mode — via PyPI (`interia-quality`)

Idéal pour tester InterIA **sans modifier la structure** d’un dépôt.

1. Installer le moteur qualité :

    ```bash
    pip install interia-quality
    ```

2. À la racine du dépôt :

    ```bash
    interia-quality
    interia-quality refactor-plan
    interia-quality cosmos-map
    interia-quality latex-galaxy
    interia-quality bib-galaxy
    ```

3. Pour le board :

    ```bash
    interia-quality init-board
    interia-quality portal
    ```

---

### 4.2 2eme Mode — “vendored” (pack complet dans un dépôt)

Recommandé pour les dépôts **officiels InterIA** ou les projets longs.

- Utiliser `interia_install.py` (dans le Quality Pack) pour :
  - copier `interia_quality/`,
  - copier `interia_quality/board/…`,
  - injecter ou créer un `Makefile` avec les cibles InterIA.

Référence détaillée : `docs/getting_started.md`.

---

## 5. 🛰️ Board & Portail InterIA

Le **board** est la face HTML de la Suite :

- Portail : `interia_portal.html`
- Qualité : `quality_report.html`
- AI Bridge : `ai_preview.html`
- Galaxies : `galaxy_latex_explorer.html`, `doctor_latex_galaxy.html`, `bib_galaxy.html`
- Cosmos & Timeline : `cosmos_explorer.html`, `cosmos_timeline.html`
- Multivers : `multiverse_3d.html`
- Docs qualité : `docs/quality/index.html`

Le portail résume exactement ce document :

- même liste de briques,
- mêmes liens conceptuels (quality → cosmos → multiverse → AI).

---

## 6. 🗺️ Topologie des dépôts InterIA

- **`interia-suite`**
  Vue d’ensemble, docs d’entrée, `INTERIA_SUITE.md` canonique.
- **`interia-quality`**
  Moteur qualité, CLI, board, AI Bridge, Cosmos & Multiverse.
- **`interia-style`**
  Templates, guides de style, gabarits corporate.
- **`community`**
  Discussions, code de conduite, RFC, policies.

> Si un dépôt a besoin d’expliquer “où il se situe dans la Suite”, il peut :
>
> - pointer vers `interia-suite` dans son README,
> - et copier une version condensée de ce document.

---

## 7. 🔗 Synchronisation docs / board

Cette version de `INTERIA_SUITE.md` est pensée pour être :

- **alignée** avec :
  - `docs/index.md`
  - `docs/getting_started.md`
- **miroir textuel** du portail :
  - `interia_quality/board/interia_portal.html`
  - `interia_quality/board/docs/quality/index.html`

Si tu modifies la vision InterIA (composants, workflows), il suffit de :

1. Mettre à jour **CE fichier en premier**.
2. Repercuter les mêmes sections (souvent par copier‑coller léger) dans :

   - les docs (`docs/…`),
     - `docs/index.md`
     - `docs/getting_started.md`
   - le portail board + “Quality Docs”.

De cette façon, GitHub et le portail qualité InterIA **racontent toujours la même histoire**.

---

</details>

<details open><summary><b>🇬🇧 English</b> — click to collapse</summary>

> **InterIA Suite** — unified entry point for style, quality, documentary cosmos and\
multiverse of your scientific repositories.

This document is the **canonical view** of the InterIA Suite:

- the docs pages (`docs/index.md`, `docs/getting_started.md`),
- the board portal (`interia_portal.html`),
- and the “Quality Docs” page (`docs/quality/index.html`)

should *tell the same story* as this file.

---

## 1. 🎯 Purpose of this document

`INTERIA_SUITE.md` acts as:

- the **master map** of the Suite (vision, components, links),
- the **shared reference** for all InterIA repos,
- a **bridge** between:
  - GitHub docs (`docs/…`),
  - the HTML board (`interia_quality/board/…`),
  - local READMEs (`interia-quality`, `interia-style`, `community`, etc.).

Other repos (e.g. `interia-quality`, `interia-style`) can:

- either **copy** this file as‑is,
- or **symlink**/import the canonical version from `interia-suite`.

---

## 2. 🧭 InterIA Suite overview

The Suite combines several coordinated bricks:

- 🎨 **InterIA Style**
  Templates, branding, style guides and writing conventions.
- 🧪 **InterIA Quality Pack v4** (`interia-quality`)
  Modular quality engine, refactor assist, AI Bridge, structure maps (Cosmos, Galaxies, Multiverse).
- 🌐 **InterIA Cosmos**
  Single‑repo maps (Python / Markdown / LaTeX / BibTeX) + documentary timeline.
- 🌠 **InterIA Multiverse**
  Cross‑repo analysis, structural distances, documentary gravity, 3D visualisation.
- 👥 **InterIA Community**
  Discussions, governance, corporate templates, code of conduct.

The **`interia-suite`** repo provides:

- the **global vision**,
- an **index** of components,
- **onboarding docs**:
  - `docs/index.md` (landing),
  - `docs/getting_started.md` (how‑to).

---

## 3. 🧩 Main components

### 3.1 🎨 InterIA Style

- Role:
  - unify **branding**,
  - provide **README / hero** templates,
  - ship **STYLE_GUIDE** (Markdown, LaTeX, code),
  - include GitHub snippets (issues, PRs, CI).
- Repo:
  `https://github.com/couret-interia/interia-style`

This is where the generic corporate templates live.

---

### 3.2 🧪 InterIA Quality Pack v4 (`interia-quality`)

- Standalone Python package, published on PyPI as **`interia-quality`**.
- Provides:
  - quality plugins (Python / Markdown / LaTeX / BibTeX),
  - `quality_report.json` and `refactor_plan.{json,md}`,
  - AI Bridge: `ai_request.json`, `ai_response.json`, `ai_prompt.txt`,
  - Cosmos & Galaxy maps,
  - a **local HTML board** with portal, reports and explorers.

Main entry points:

- **CLI**: `interia-quality`
  (see `interia-quality` repo README)
- **Board**: `interia_quality/board/interia_portal.html`
  (or `interia-quality portal` / `make portal-all`)

---

### 3.3 🌐 Cosmos & Timeline

Single‑repo view:

- **Files**:
  - `cosmos_map.json`, `cosmos_map_summary.json`
  - `cosmos_timeline.json`, `cosmos_history/…`
- **Typical CLI usage**:
  - `interia-quality cosmos-map`
  - `interia-quality cosmos-timelapse`

Board views:

- `cosmos_explorer.html`
- `cosmos_timeline.html`

---

### 3.4 🌠 Multiverse

Multi‑repo view:

- **Files**:
  - `interia_multiverse_map.json`
  - `interia_multiverse_matrix.json`
  - `interia_multiverse_gravity.json`
  - `interia_multiverse_3d.json`
- **Typical Make targets**:

```bash
make multiverse-map repos="../repoA ../repoB ../repoC"
make multiverse-gravity
make multiverse-3d[-html] repos="../repoA ../repoB ../repoC"
```

Board view:

- `multiverse_3d.html`

---

### 3.5 👥 InterIA Community

- Hosts:
  - public discussions (GitHub Discussions),
  - code of conduct & shared policies,
  - RFCs and architecture decisions.
- Repo:
  `https://github.com/couret-interia/community`

---

## 4. 🚀 How to adopt InterIA Suite

This mirrors `docs/getting_started.md`.

### 4.1 Mode 1 — via PyPI (`interia-quality`)

Ideal when you want to try InterIA **without changing** the repo layout.

1. Install the quality engine:

    ```bash
    pip install interia-quality
    ```

2. At the repo root:

    ```bash
    interia-quality
    interia-quality refactor-plan
    interia-quality cosmos-map
    interia-quality latex-galaxy
    interia-quality bib-galaxy
    ```

3. For the board:

    ```bash
    interia-quality init-board
    interia-quality portal
    ```

---

### 4.2 Mode 2 — “vendored” (embed the full pack)

Recommended for **official InterIA** repos and long‑lived projects.

- Use `interia_install.py` (from the Quality Pack) to:
  - copy `interia_quality/`,
  - copy `interia_quality/board/…`,
  - inject/create a `Makefile` with InterIA targets.

Detailed flow: see `docs/getting_started.md`.

---

## 5. 🛰️ Board & InterIA Portal

The **board** is the HTML face of the Suite:

- Portal: `interia_portal.html`
- Quality: `quality_report.html`
- AI Bridge: `ai_preview.html`
- Galaxies: `galaxy_latex_explorer.html`, `doctor_latex_galaxy.html`, `bib_galaxy.html`
- Cosmos & Timeline: `cosmos_explorer.html`, `cosmos_timeline.html`
- Multiverse: `multiverse_3d.html`
- Quality Docs: `docs/quality/index.html`

The portal is meant to **mirror this document**:

- same list of bricks,
- same conceptual pipeline (quality → cosmos → multiverse → AI).

---

## 6. 🗺️ InterIA repos topology

- **`interia-suite`**
  Global view, entry docs, canonical `INTERIA_SUITE.md`.
- **`interia-quality`**
  Quality engine, CLI, board, AI Bridge, Cosmos & Multiverse tools.
- **`interia-style`**
  Corporate templates, style guides, shared assets.
- **`community`**
  Discussions, code of conduct, RFCs, governance.

> If a repo needs to explain “where it sits in the Suite”, it can:
>
> - link to `interia-suite` in its README,
> - and embed a condensed version of this document.

---

## 7. 🔗 Sync between docs and board

This `INTERIA_SUITE.md` is designed to be:

- **aligned** with:
  - `docs/index.md`
  - `docs/getting_started.md`
- **textual mirror** of the portal:
  - `interia_quality/board/interia_portal.html`
  - `interia_quality/board/docs/quality/index.html`

When you update the Suite vision (components, workflows):

1. Update **this file first**.
2. Reflect the changes (usually via light copy/paste) in:

   - the docs (`docs/…`),
     - `docs/index.md`
     - `docs/getting_started.md`
   - the board portal and quality docs.

That way, GitHub and the InterIA board always **tell the same story**.

---

</details>
