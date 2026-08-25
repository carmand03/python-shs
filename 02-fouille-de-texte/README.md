# Séance 2 — Fouille de texte avec Python

Deuxième module du cycle : de l'analyse de tableaux à l'analyse de corpus
textuels, sur un corpus de presse historique chinoise centré sur les Jeux
Olympiques.

**Prérequis :** Séance 1 (bases de Python et de pandas).

## Objectifs

- Explorer un corpus de texte et ses métadonnées.
- Construire des concordances / KWIC (*Keyword In Context*).
- Analyser les n-grammes et collocations les plus caractéristiques.
- Détecter les grands thèmes d'un corpus avec **BERTopic** (topic modeling).
- Extraire des entités nommées (personnes, lieux, organisations) avec
  **spaCy**.
- Mesurer la tonalité des textes avec une analyse de sentiment (bonus).

## Contenu du dossier

| Fichier | Description |
|---|---|
| `Seance2_TextMining_Python.ipynb` | Notebook de cours (1 journée / 7h), avec exercices intégrés et solutions repliables. |
| `data/olympic_corpus.csv` | Corpus de presse (~17 000 articles, 1833–1953) extrait de la collection ProQuest Chinese Newspapers via la plateforme HistText. |

## ⚠️ Droits de réutilisation des données

`olympic_corpus.csv` est dérivé de la collection **ProQuest Chinese
Newspapers**, une base commerciale sous licence. **Vérifiez les conditions
de réutilisation et de redistribution avant de rendre ce dépôt public** —
il est possible que ce fichier doive être retiré du dépôt (ou hébergé
séparément, en accès restreint) selon les termes de la licence ProQuest de
votre institution.

## Pour commencer

```bash
pip install pandas numpy matplotlib seaborn plotly nltk scikit-learn spacy bertopic sentence-transformers
python -m spacy download en_core_web_sm
```

Ouvrez ensuite `Seance2_TextMining_Python.ipynb` et suivez le déroulé
indiqué en tête de notebook. Les cellules BERTopic/spaCy nécessitent une
connexion internet lors du premier téléchargement des modèles.
