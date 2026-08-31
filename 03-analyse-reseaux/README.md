# Séance 3 — Analyse de réseaux et analyse spatiale avec Python

Troisième module du cycle : passer d'un tableau de données à sa **structure
relationnelle** (réseaux, avec **NetworkX**) et à sa **structure spatiale**
(cartographie, avec **geopandas**, **folium** et **geopy**) — deux approches
complémentaires, réunies dans une même séance à la demande d'un groupe
comptant plusieurs géographes.

**Prérequis :** Séances 1 (pandas) et 2 (fouille de texte, pour l'annexe sur
les réseaux de co-occurrence textuelle).

## Objectifs

**Réseaux**
- Comprendre le vocabulaire de base de l'analyse de réseau (nœuds, liens,
  réseaux bipartis, projections).
- Construire un réseau d'affiliation biparti université ↔ employeur à partir
  d'un tableau de données (`auc.csv`).
- Calculer des mesures de réseau : densité, composantes connexes,
  centralités (degré, intermédiarité, proximité, vecteur propre).
- Détecter des communautés (algorithme de Louvain).

**Analyse spatiale**
- Manipuler des données spatiales avec un `GeoDataFrame` (geopandas) :
  géométries, systèmes de coordonnées (CRS), reprojection.
- Construire une carte choroplèthe (nombre d'étudiants par État américain de
  formation) et une carte de points (villes d'installation en 1936), en
  version statique et interactive (folium).
- Calculer des distances réelles (géodésiques) entre deux lieux avec `geopy`.

**La synthèse des deux approches**
- Cartographier un réseau en plaçant ses nœuds à leurs coordonnées réelles
  plutôt que sur une disposition abstraite — une véritable carte de flux
  migratoires entre universités américaines et villes chinoises.

## Contenu du dossier

| Fichier | Description |
|---|---|
| `Seance3_Reseaux_Cartes.ipynb` | Notebook de cours (1 journée / 7h) : réseaux (sections 1-3), cartographie (sections 4-6), synthèse réseaux + cartes (section 7), mini-projet (section 8). Une annexe optionnelle (hors format 7h) reprend un réseau de co-occurrence textuelle à partir du corpus de la Séance 2. |
| `Exercice3_Python_reseaux.ipynb` | Exercice à faire à la maison, **centré sur les réseaux uniquement**, sur un jeu de données d'affiliations associatives (`association.csv`) — un terrain différent de celui du cours pour consolider les mêmes compétences réseau. |
| `data/` | Jeux de données utilisés par les notebooks ci-dessus. |

## Données

- `data/auc.csv` — utilisé de bout en bout dans le notebook de cours, pour
  les réseaux **et** pour la cartographie (colonnes `University`/`Employer`
  pour les réseaux ; `State`/`City` pour les cartes).
- `data/youmei.csv`, `data/association.csv`, `data/affiliation.csv` —
  utilisés par l'exercice à la maison (mêmes individus que la Séance 1,
  avec leurs appartenances associatives et institutionnelles).
- Le fond de carte des États-Unis (GeoJSON) est téléchargé directement
  depuis GitHub au moment de l'exécution du notebook de cours (section 4) —
  **gardez une connexion internet active** à ce moment de la séance.
- L'annexe du notebook de cours utilise également `olympic_corpus.csv`
  (voir `../02-fouille-de-texte/data/`) — copiez-le dans `data/` si vous
  souhaitez l'explorer.

## Pour commencer

```bash
pip install pandas numpy matplotlib seaborn networkx pyvis geopandas folium geopy mapclassify
```

Ouvrez `Seance3_Reseaux_Cartes.ipynb` : `auc.csv` est déjà présent dans
`data/`, aucune préparation supplémentaire n'est nécessaire pour suivre le
notebook de cours de bout en bout.
