# Séance 1 — Introduction à Python pour les SHS

Premier module du cycle *Python pour les SHS* : une prise en main complète du
langage Python et de l'écosystème pandas, sans prérequis de programmation.

## Objectifs

- Comprendre les bases du langage Python (variables, listes, tuples,
  dictionnaires, conditions, boucles, fonctions).
- Manipuler un jeu de données tabulaire avec **pandas** : charger, inspecter,
  sélectionner, renommer, nettoyer, filtrer.
- Explorer statistiquement des données quantitatives et qualitatives
  (comptages, `groupby`, agrégations).
- Visualiser des données avec **matplotlib**, **seaborn** et **plotly**.

## Contenu du dossier

| Fichier | Description |
|---|---|
| `Seance1_Python_SHS.ipynb` | Notebook de cours (1 journée / 7h), avec exercices intégrés et solutions repliables. |
| `QCM_Seance1_Python_SHS.html` | Quiz interactif d'auto-évaluation en fin de formation (25 questions, correction immédiate, diagnostic par section). À ouvrir directement dans un navigateur. |
| `Exercice1_Python_youmei.ipynb` | Exercice à faire à la maison, sur un jeu de données différent (`youmei.csv`), pour vérifier l'acquisition des compétences. |
| `data/` | Jeux de données utilisés par les notebooks ci-dessus. |

## Données

- `data/youmei.csv` — annuaire d'étudiants chinois aux États-Unis (1917),
  utilisé par l'exercice à la maison.
- `data/auc.csv` — **non inclus** (voir `data/AUC_MANQUANT.md`) : requis par
  le notebook de cours, à fournir séparément.

## Pour commencer

1. Installez Python (via [Anaconda](https://www.anaconda.com/download)) ou
   utilisez [Google Colab](https://colab.research.google.com) sans rien
   installer localement.
2. Placez `auc.csv` dans `data/` (voir ci-dessus).
3. Ouvrez `Seance1_Python_SHS.ipynb` et suivez le déroulé indiqué en tête de
   notebook.
4. À la fin de la séance, testez-vous avec `QCM_Seance1_Python_SHS.html`.
5. Avant la séance suivante, faites `Exercice1_Python_youmei.ipynb` en
   autonomie.
