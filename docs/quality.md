# 🚀 Getting started with InterIA Suite

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

> Deux façons d’adopter la Suite InterIA :
> **(1)** via le paquet PyPI `interia-quality` (mode CLI),
> **(2)** en embarquant le pack complet dans un dépôt (mode “vendored”).

---

## 1. Pré‑requis

- Python ≥ 3.9
- `pip` / `venv` recommandés
- (Optionnel) `make` pour profiter des cibles `Makefile` InterIA

---

## 2. Mode 1 — via `pip` (CLI uniquement)

Ce mode est idéal pour tester InterIA sur un dépôt existant **sans** modifier sa structure.

### 2.1. Installer le moteur qualité

Dans votre environnement virtuel :

```bash
pip install interia-quality
````

Vérifier l’installation :

```bash
python -c "import interia_quality; print(interia_quality.__version__)"
interia-quality --help
```

### 2.2. Lancer les premiers checks

Depuis la racine de votre dépôt :

```bash
cd /chemin/vers/mon-repo

# Quality checks (plugins Python / Markdown / LaTeX / BibTeX)
interia-quality           # alias: interia-quality check

# Plan de refactor
interia-quality refactor-plan

# Application des refactors sûrs (docstrings, petites améliorations)
interia-quality refactor-apply
```

Vous obtenez notamment :

- `quality_report.json`
- `refactor_plan.json`
- `refactor_plan.md`

### 2.3. Cartes de structure (Cosmos & Galaxies)

Toujours dans le même dépôt :

```bash
# Carte Cosmos (structure globale du dépôt)
interia-quality cosmos-map
# => cosmos_map.json, cosmos_map_summary.json

# Timeline documentaire
interia-quality cosmos-timelapse
# => cosmos_history/…, cosmos_timeline.json

# Galaxie LaTeX
interia-quality latex-galaxy
interia-quality latex-explorer

# Galaxie BibTeX (citations, manquants, inutilisés)
interia-quality bib-galaxy
```

---

## 3. Mode 2 — “vendored” (pack complet dans un dépôt)

Ce mode est recommandé pour les dépôts **officiels InterIA** ou les projets
où l’on veut embarquer :

- le paquet `interia_quality/`
- le board HTML
- le `Makefile` avec toutes les cibles InterIA (cosmos, galaxies, multivers, AI, portail…)

### 3.1. Utiliser `interia_install.py`

Depuis le dépôt `interia-quality` (ou l’archive du Quality Pack) :

```bash
cd interia-quality-pack-v4/

# Installer dans un autre dépôt
python interia_install.py /chemin/vers/mon-repo

# Forcer si un interia_quality/ existe déjà
python interia_install.py /chemin/vers/mon-repo --force
```

L’installateur va :

- copier `interia_quality/` dans le dépôt cible,
- copier `interia_quality/board/…`,
- créer un `Makefile` si nécessaire,
- insérer un bloc de cibles InterIA (quality-all, cosmos, galaxies, multiverse, portail…).

### 3.2. Utiliser le Makefile

Une fois installé, depuis votre dépôt :

```bash
cd /chemin/vers/mon-repo

# Qualité + plan de refactor
make quality-all

# Portail InterIA (analyse minimale + ouverture du portail)
make portal-all

# Galaxies
make latex-galaxy-html
make bib-galaxy-html

# Cosmos
make cosmos-map-html
make cosmos-timeline-html

# Multivers (multi-dépôts)
make multiverse-map repos="../repoA ../repoB ../repoC"
make multiverse-3d[-html] repos="../repoA ../repoB ../repoC"
```

---

## 4. Board & Portail InterIA

Le board est fourni dans `interia_quality/board/…`.

### 4.1. Copier le board (mode CLI)

Si vous utilisez seulement le paquet PyPI (`pip`), vous pouvez copier le board
dans un dépôt sans l’installer en vendored :

```bash
cd /chemin/vers/mon-repo
interia-quality init-board
# ou pour écraser le dossier existant
interia-quality init-board --force
```

Vous obtenez :

```text
./interia_quality/board/…
```

### 4.2. Ouvrir le portail

Ensuite :

```bash
interia-quality portal
```

Cela :

- lance un petit serveur HTTP local (port `8000`),
- ouvre `interia_quality/board/interia_portal.html` dans votre navigateur.

Depuis ce portail, la barre du haut vous donne accès à :

- 🧪 Quality Report
- 🤖 AI Bridge / Refactor Assist
- 🔭 LaTeX Galaxy Explorer
- 🌌 LaTeX Galaxy
- 💫 BibTeX Galaxy
- 🌐 Cosmos Map
- ⏳ Cosmos Timeline
- 🌠 Multiverse 3D
- ❓ Quality Docs

---

## 5. Et ensuite ?

- Pour la vision globale de la Suite : `INTERIA_SUITE.md`
- Pour le détail du moteur qualité : README du dépôt `interia-quality`
- Pour les templates & guides : `interia-style`
- Pour la gouvernance & les discussions : `community`

</div>

<div class="toggle-en">

> Two main ways to adopt InterIA Suite:
> **(1)** via the PyPI package `interia-quality` (CLI mode),
> **(2)** by vendoring the full pack into your repo.

---

## 1. Prerequisites

- Python ≥ 3.9
- `pip` / `venv` recommended
- (Optional) `make` to benefit from InterIA Makefile targets

---

## 2. Mode 1 — via `pip` (CLI only)

This is ideal to try InterIA on an existing repo **without** changing its layout.

### 2.1. Install the quality engine

Inside your virtualenv:

```bash
pip install interia-quality
```

Check it works:

```bash
python -c "import interia_quality; print(interia_quality.__version__)"
interia-quality --help
```

### 2.2. Run first checks

At the root of your project:

```bash
cd /path/to/my-repo

# Quality checks (Python / Markdown / LaTeX / BibTeX plugins)
interia-quality           # alias: interia-quality check

# Refactor plan
interia-quality refactor-plan

# Apply safe refactors (docstring templates, small cleanups)
interia-quality refactor-apply
```

You will get, among others:

- `quality_report.json`
- `refactor_plan.json`
- `refactor_plan.md`

### 2.3. Structure maps (Cosmos & Galaxies)

In the same repo:

```bash
# Global structure map
interia-quality cosmos-map
# => cosmos_map.json, cosmos_map_summary.json

# Documentary timeline
interia-quality cosmos-timelapse
# => cosmos_history/…, cosmos_timeline.json

# LaTeX galaxy
interia-quality latex-galaxy
interia-quality latex-explorer

# BibTeX galaxy (citations, missing & unused)
interia-quality bib-galaxy
```

---

## 3. Mode 2 — “vendored” (embed the full pack)

This mode is recommended for **official InterIA** repos or projects
where you want to ship:

- the `interia_quality/` package,
- the HTML board,
- the `Makefile` with all InterIA targets (cosmos, galaxies, multiverse, AI, portal…).

### 3.1. Using `interia_install.py`

From the `interia-quality` repo (or the Quality Pack archive):

```bash
cd interia-quality-pack-v4/

# Install into another repo
python interia_install.py /path/to/my-repo

# Force if an interia_quality/ tree already exists
python interia_install.py /path/to/my-repo --force
```

The installer will:

- copy `interia_quality/` into the target repo,
- copy `interia_quality/board/…`,
- create a `Makefile` if needed,
- append a commented block with InterIA targets
  (quality-all, cosmos, galaxies, multiverse, portal…).

### 3.2. Using the Makefile

Once installed, from your repo:

```bash
cd /path/to/my-repo

# Quality checks + refactor plan
make quality-all

# InterIA portal (minimal analysis + open portal)
make portal-all

# Galaxies
make latex-galaxy-html
make bib-galaxy-html

# Cosmos
make cosmos-map-html
make cosmos-timeline-html

# Multiverse (multiple repos)
make multiverse-map repos="../repoA ../repoB ../repoC"
make multiverse-3d[-html] repos="../repoA ../repoB ../repoC"
```

---

## 4. Board & InterIA Portal

The board is shipped under `interia_quality/board/…`.

### 4.1. Copy the board (CLI mode)

If you only use the PyPI package (`pip`), you can copy the board
into any repo without vendoring the whole pack:

```bash
cd /path/to/my-repo
interia-quality init-board
# or to overwrite existing content
interia-quality init-board --force
```

You will get:

```text
./interia_quality/board/…
```

### 4.2. Open the portal

Then:

```bash
interia-quality portal
```

This will:

- start a small local HTTP server (port `8000`),
- open `interia_quality/board/interia_portal.html` in your browser.

From the portal, the top bar gives direct access to:

- 🧪 Quality Report
- 🤖 AI Bridge / Refactor Assist
- 🔭 LaTeX Galaxy Explorer
- 🌌 LaTeX Galaxy
- 💫 BibTeX Galaxy
- 🌐 Cosmos Map
- ⏳ Cosmos Timeline
- 🌠 Multiverse 3D
- ❓ Quality Docs

---

## 5. What next?

- For the global Suite vision: `INTERIA_SUITE.md`
- For the quality engine details: `interia-quality` README
- For templates & style guides: `interia-style`
- For governance & discussions: `community` repo

</div>
</div>
</form>
