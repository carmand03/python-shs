# Python pour les SHS

Un cycle de quatre journées de formation à Python, conçu pour des
chercheurs et chercheuses en sciences humaines et sociales sans expérience
préalable de programmation. Chaque séance est une journée complète (7h),
autonome, et construite autour de jeux de données réels issus de l'histoire
sociale de la Chine républicaine.

Les quatre séances forment une **progression cohérente** : on part de la
manipulation de tableaux de données (Séance 1), on l'étend au texte brut
(Séance 2), puis à la structure relationnelle des données (Séance 3), et
enfin à l'interaction avec des modèles de langage ancrés dans un corpus
(Séance 4). Chaque séance réutilise, autant que possible, les jeux de
données et les acquis des séances précédentes.

## Objectifs pédagogiques du cycle

- Donner à des chercheur·ses sans formation en programmation une autonomie
  réelle en Python pour leurs propres corpus (tableaux, texte, réseaux).
- Privilégier la pratique : chaque notebook alterne explications, démonstrations
  et exercices, avec des solutions repliables pour l'auto-évaluation.
- Ancrer chaque méthode dans un cas d'usage historique concret, plutôt que
  dans des exemples abstraits.
- Donner les moyens de continuer à apprendre en autonomie après la
  formation (aide-mémoire, index des fonctions, ressources) plutôt que de
  seulement transmettre des recettes.

## Structure du dépôt

```
python-pour-les-shs/
├── 01-introduction-python/     Séance 1 — Bases de Python, pandas, visualisation
├── 02-fouille-de-texte/        Séance 2 — Fouille de texte (KWIC, n-grammes, BERTopic, NER)
├── 03-analyse-reseaux/         Séance 3 — Analyse et visualisation de réseaux (NetworkX)
├── 04-llm-rag/                 Séance 4 — LLM locaux avec Ollama, mini RAG
├── requirements.txt            Dépendances Python agrégées des 4 séances
└── README.md                   Ce fichier
```

Chaque dossier `0X-.../` est **autonome** et contient :

- un notebook de cours (`Seance*.ipynb`), avec son propre déroulé horaire ;
- le cas échéant, un exercice à faire à la maison et/ou un quiz
  d'auto-évaluation ;
- un sous-dossier `data/` avec les jeux de données nécessaires ;
- un `README.md` local détaillant les objectifs, le contenu et la marche à
  suivre pour cette séance précise.

## Vue d'ensemble des quatre séances

| # | Séance | Compétences principales | Jeux de données |
|---|---|---|---|
| 1 | [Introduction à Python](01-introduction-python/) | Bases du langage, pandas, matplotlib/seaborn/plotly | `auc.csv`*, `youmei.csv` |
| 2 | [Fouille de texte](02-fouille-de-texte/) | KWIC, n-grammes, BERTopic, spaCy (NER), sentiment | `olympic_corpus.csv` |
| 3 | [Analyse de réseaux](03-analyse-reseaux/) | NetworkX, réseaux bipartis, centralités, communautés | `auc.csv`*, `olympic_corpus.csv`, `youmei.csv`, `association.csv`, `affiliation.csv` |
| 4 | [LLM & RAG](04-llm-rag/) | Ollama, embeddings, retrieval-augmented generation | `olympic_corpus.csv` |

## Prérequis techniques

- **Python** via [Anaconda](https://www.anaconda.com/download) (installation
  locale) ou [Google Colab](https://colab.research.google.com) (aucune
  installation requise).
- **Jupyter Notebook**, inclus avec Anaconda ou disponible nativement sur
  Colab.
- Pour la Séance 4 uniquement : [Ollama](https://ollama.com/download), une
  application à installer séparément (voir le README de ce dossier).

Un fichier [`requirements.txt`](requirements.txt) agrège l'ensemble des
dépendances Python des quatre séances ; chaque dossier de séance précise
également, dans son propre README, les seules dépendances qui le concernent.
