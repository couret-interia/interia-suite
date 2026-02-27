<details><summary><b>🇫🇷 Français</b> — cliquer pour déployer</summary>

# 🚀 Bien démarrer avec InterIA Suite

`interia-suite` est le **portail de coordination** de la Suite InterIA :

- **InterIA Quality Pack v4** – moteur qualité, refactor plan, AI Bridge, Cosmos, galaxies, Multiverse
- **InterIA Style** – guides de style, templates, structure de dépôt
- **InterIA Community** – discussions, code de conduite, gouvernance

Cette page te prend par la main pour passer de **zéro** à :

- un dépôt qui passe les checks qualité,
- un **board InterIA** qui s’ouvre dans le navigateur,
- une première **Cosmos Map**,
- et éventuellement un **Multivers** si tu as plusieurs dépôts.

> Pour la vision “conceptuelle” d’ensemble, voir aussi
> [`INTERIA_SUITE.md`](../INTERIA_SUITE.md).

---

## 1. Installer le moteur qualité

Dans ton virtualenv (recommandé) :

```bash
pip install interia-quality
````

Vérification rapide :

```bash
python -c "import interia_quality; print(interia_quality.__name__)"
# doit afficher: interia_quality
```

---

## 2. Brancher InterIA sur un dépôt existant

Depuis la racine de ton dépôt :

```bash
cd /chemin/vers/mon/depot

# 1. Checks qualité de base
interia-quality          # ou: interia-quality check

# 2. (Optionnel) Installer les assets HTML/CSS/JS
interia-quality init-board

# 3. Ouvrir le portail InterIA
interia-quality portal
```

Nous obtenons :

- un **board** sous `./interia_quality/board/…`,
- une page `interia_portal.html` qui centralise :

  - le rapport qualité (`quality_report.html`),
  - la prévisualisation IA (`ai_preview.html`),
  - la carte Cosmos,
  - les galaxies LaTeX / BibTeX,
  - le Multivers 3D.

Pour en savoir plus sur les tableaux et le board : voir `docs/quality.md`.

---

## 3. Construire un plan de refactorisation

Dans le même dépôt :

```bash
interia-quality refactor-plan
interia-quality refactor-apply
```

Cela génère :

- `refactor_plan.json` – version machine,
- `refactor_plan.md` – version humaine,
- et applique quelques **refactors sûrs** (docstrings, petites hygiènes).

> Détails dans `docs/quality.md` (section “Refactor plan”).

---

## 4. Activer le Pont IA (AI Bridge)

Workflow typique :

```bash
# 1. Plan de refactor
interia-quality refactor-plan

# 2. Construire la requête IA
interia-quality ai-request      # produit ai_request.json
# ou
interia-quality ai-prompt       # produit aussi ai_prompt.txt à copier/coller dans un LLM

# 3. Envoyer ai_request.json (ou ai_prompt.txt) à ton LLM
#    et sauvegarder la réponse dans ai_response.json

# 4. Résumé et application
interia-quality ai-summary
interia-quality ai-apply
```

Le tout est **JSON-first** et **IA-agnostique** : aucune dépendance à un fournisseur.

> Détails complets : `docs/ai_bridge.md`.

---

## 5. Générer Cosmos & Galaxies

Toujours depuis la racine du dépôt :

```bash
# Carte Cosmos
interia-quality cosmos-map      # cosmos_map.json + cosmos_map_summary.json

# Galaxies LaTeX / BibTeX
interia-quality latex-galaxy    # latex_galaxy.json
interia-quality latex-explorer  # latex_explorer.json
interia-quality bib-galaxy      # bib_galaxy.json
```

Ensuite, via le board (ou un simple `python -m http.server 8000`) tu peux ouvrir :

- `interia_quality/board/cosmos_explorer.html`
- `interia_quality/board/doctor_latex_galaxy.html`
- `interia_quality/board/galaxy_latex_explorer.html`
- `interia_quality/board/bib_galaxy.html`

> Détails sur les métriques et interprétation : `docs/quality.md`.

---

## 6. Passer au Multivers (plusieurs dépôts)

### 6.1. Préparer chaque dépôt

Sur **chaque** dépôt :

```bash
cd /chemin/vers/repoX
interia-quality
interia-quality cosmos-map
```

Nous obtienons au minimum :

- `quality_report.json`
- `cosmos_map.json`*
- `cosmos_map_summary.json`

### 6.2. Lancer les outils Multiverse

Depuis un dépôt qui contient le Quality Pack (ou un dépôt “hub”) :

```bash
make multiverse-map repos="../repoA ../repoB ../repoC"
make multiverse-gravity
make multiverse-3d[-html] repos="../repoA ../repoB ../repoC"
```

Résultats :

- `interia_multiverse_map.json`
- `interia_multiverse_matrix.json`
- `interia_multiverse_gravity.json`
- `interia_multiverse_3d.json`
  - `multiverse_3d.html` dans le board

> Détails et interprétation : `docs/multiverse.md`.

---

## 7. Où aller ensuite ?

- **Vue conceptuelle globale** : `INTERIA_SUITE.md`
- **Mécanique qualité / refactor / Cosmos / galaxies** : `docs/quality.md`
- **Pont IA (AI Bridge)** : `docs/ai_bridge.md`
- **Multivers et analyses multi‑dépôts** : `docs/multiverse.md`

InterIA Suite te fournit le **langage commun** pour voir, mesurer et documenter tes dépôts scientifiques – le reste, c’est ton univers ✨

</details>

<details open><summary><b>🇬🇧 English</b> — click to collapse</summary>

# 🚀 Getting started with InterIA Suite

`interia-suite` is the **coordination portal** for the InterIA ecosystem:

- **InterIA Quality Pack v4** – quality engine, refactor plan, AI Bridge, Cosmos, galaxies, Multiverse
- **InterIA Style** – style guides, templates, repository conventions
- **InterIA Community** – discussions, code of conduct, governance

This page walks you from **zero** to:

- a repo that passes basic quality checks,
- a running **InterIA board** in your browser,
- a first **Cosmos Map**,
- and optionally a **Multiverse** if you have several repos.

> For a more conceptual overview, see
> [`INTERIA_SUITE.md`](../INTERIA_SUITE.md).

---

## 1. Install the quality engine

In your virtualenv (recommended):

```bash
pip install interia-quality
```

Quick sanity check:

```bash
python -c "import interia_quality; print(interia_quality.__name__)"
# should print: interia_quality
```

---

## 2. Plug InterIA into an existing repo

From the root of your project:

```bash
cd /path/to/my/repo

# 1. Basic quality checks
interia-quality          # or: interia-quality check

# 2. (Optional) Install board assets
interia-quality init-board

# 3. Open the InterIA portal
interia-quality portal
```

You get:

- a **board** under `./interia_quality/board/…`,
- a `interia_portal.html` page that centralises:

  - the quality report (`quality_report.html`),
  - AI preview (`ai_preview.html`),
  - the Cosmos map,
  - LaTeX / BibTeX galaxies,
  - the 3D Multiverse.

For more about the board and dashboards: see `docs/quality.md`.

---

## 3. Build a refactor plan

Still in the same repo:

```bash
interia-quality refactor-plan
interia-quality refactor-apply
```

This generates:

- `refactor_plan.json` – machine‑readable,
- `refactor_plan.md` – human‑friendly mirror,
- and applies a few **safe refactors** (docstring stubs, small cleanups).

> Details in `docs/quality.md` (Refactor plan section).

---

## 4. Use the AI Bridge

Typical workflow:

```bash
# 1. Refactor plan
interia-quality refactor-plan

# 2. Build the AI request
interia-quality ai-request      # produces ai_request.json
# or
interia-quality ai-prompt       # also produces ai_prompt.txt ready to paste into an LLM

# 3. Send ai_request.json (or ai_prompt.txt) to your LLM
#    and save the answer as ai_response.json

# 4. Summarise & apply
interia-quality ai-summary
interia-quality ai-apply
```

Everything is **JSON‑first** and **AI‑agnostic**: no vendor lock‑in.

> Full details in `docs/ai_bridge.md`.

---

## 5. Generate Cosmos & galaxies

From the repo root:

```bash
# Cosmos map
interia-quality cosmos-map      # cosmos_map.json + cosmos_map_summary.json

# LaTeX / BibTeX galaxies
interia-quality latex-galaxy    # latex_galaxy.json
interia-quality latex-explorer  # latex_explorer.json
interia-quality bib-galaxy      # bib_galaxy.json
```

Then, via the board (or a simple `python -m http.server 8000`) you can open:

- `interia_quality/board/cosmos_explorer.html`
- `interia_quality/board/doctor_latex_galaxy.html`
- `interia_quality/board/galaxy_latex_explorer.html`
- `interia_quality/board/bib_galaxy.html`

> Metrics and interpretation: see `docs/quality.md`.

---

## 6. Move to the Multiverse (multiple repos)

### 6.1. Prepare each repo

On **each** repository:

```bash
cd /path/to/repoX
interia-quality
interia-quality cosmos-map
```

You get at least:

- `quality_report.json`
- `cosmos_map.json`
- `cosmos_map_summary.json`

### 6.2. Run Multiverse tools

From a repo that hosts the Quality Pack (or a “hub” repo):

```bash
make multiverse-map repos="../repoA ../repoB ../repoC"
make multiverse-gravity
make multiverse-3d[-html] repos="../repoA ../repoB ../repoC"
```

Outputs:

- `interia_multiverse_map.json`
- `interia_multiverse_matrix.json`
- `interia_multiverse_gravity.json`
- `interia_multiverse_3d.json`
  - `multiverse_3d.html` in the board

> Details and interpretation: `docs/multiverse.md`.

---

## 7. Where to go next?

- **Global conceptual view**: `INTERIA_SUITE.md`
- **Quality / refactor / Cosmos / galaxies mechanics**: `docs/quality.md`
- **AI Bridge**: `docs/ai_bridge.md`
- **Multiverse & cross‑repo analysis**: `docs/multiverse.md`

InterIA Suite gives you the **shared language** to see, measure and document your scientific repos – the rest is your universe ✨

</details>
