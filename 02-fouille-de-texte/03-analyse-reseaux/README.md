# Séance 3 — Analyse et visualisation de réseaux avec Python

Troisième module du cycle : passer d'un tableau de données ou d'un corpus de
texte à un réseau relationnel, avec **NetworkX** et **pyvis**.

**Prérequis :** Séances 1 (pandas) et 2 (fouille de texte, pour la
construction du réseau de co-occurrence).

## Objectifs

- Comprendre le vocabulaire de base de l'analyse de réseau (nœuds, liens,
  réseaux bipartis, projections).
- Construire un réseau d'affiliation biparti à partir d'un tableau de
  données (`auc.csv`).
- Calculer des mesures de réseau : densité, composantes connexes,
  centralités (degré, intermédiarité, proximité, vecteur propre).
- Construire un réseau de co-occurrence à partir d'entités nommées extraites
  d'un corpus de texte (`olympic_corpus.csv`, Séance 2).
- Détecter des communautés (algorithme de Louvain) et produire des
  visualisations interactives.

## Contenu du dossier

| Fichier | Description |
|---|---|
| `Seance3_ReseauxPython.ipynb` | Notebook de cours (1 journée / 7h), avec exercices intégrés et solutions repliables. |
| `Exercice3_Python_reseaux.ipynb` | Exercice à faire à la maison, sur un jeu de données d'affiliations associatives (`association.csv`), pour vérifier l'acquisition des compétences. |
| `data/` | Jeux de données utilisés par les notebooks ci-dessus. |

## Données

- `data/youmei.csv`, `data/association.csv`, `data/affiliation.csv` —
  utilisés par l'exercice à la maison (mêmes individus que la Séance 1,
  avec leurs appartenances associatives et institutionnelles).
- `data/auc.csv` — **non inclus** (voir `data/AUC_MANQUANT.md`) : requis par
  le notebook de cours (section 2, réseau université–employeur).
- Le notebook de cours utilise également `olympic_corpus.csv` (voir
  `../02-fouille-de-texte/data/`) pour la section 4 (réseau de
  co-occurrence d'entités) — copiez-le dans `data/` si besoin.

## Pour commencer

```bash
pip install pandas numpy matplotlib seaborn networkx pyvis spacy
python -m spacy download en_core_web_sm
```

Placez `auc.csv` (voir ci-dessus) et une copie de `olympic_corpus.csv` dans
`data/`, puis ouvrez `Seance3_ReseauxPython.ipynb`.
