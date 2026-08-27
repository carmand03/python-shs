# Séance 4 — Introduction aux LLMs avec Ollama : construire un mini RAG

Quatrième et dernier module du cycle : utiliser un grand modèle de langage
(LLM) en local avec **Ollama**, et construire un système de génération
augmentée par récupération (**RAG**) sur le corpus de presse olympique.

**Prérequis :** Séances 1 à 3 (pandas, fouille de texte, réseaux).

## Objectifs

- Comprendre ce qu'est un LLM, ses usages et ses limites (hallucinations) —
  et pourquoi des modèles **locaux** présentent un intérêt particulier pour
  la recherche (confidentialité, reproductibilité, coût, fonctionnement hors
  ligne).
- Installer et utiliser Ollama pour dialoguer avec un LLM local en Python.
- Comprendre les *embeddings* et la similarité sémantique.
- Construire un système RAG complet : découpage de documents (*chunking*),
  indexation, recherche, génération de réponses ancrées dans les sources.
- Évaluer et fiabiliser les réponses produites (vérification des citations,
  *prompt engineering*).

## Contenu du dossier

| Fichier | Description |
|---|---|
| `Seance4_LLM_Ollama_RAG.ipynb` | Notebook de cours (1 journée / 7h), avec exercices intégrés et solutions repliables. |
| `data/olympic_corpus.csv` | Corpus de presse utilisé pour construire le mini RAG (même corpus que la Séance 2). |

## ⚠️ Droits de réutilisation des données

Voir la remarque dans `../02-fouille-de-texte/README.md` : `olympic_corpus.csv`
est dérivé d'une base commerciale (ProQuest) — vérifiez les conditions de
redistribution avant de rendre ce dépôt public.

## Pour commencer

Ollama est une application, pas un paquet Python : elle s'installe
séparément.

```bash
# 1. Installer Ollama (macOS/Windows : télécharger sur ollama.com/download)
curl -fsSL https://ollama.com/install.sh | sh   # Linux

# 2. Télécharger les modèles utilisés dans ce notebook
ollama pull llama3.2
ollama pull nomic-embed-text

# 3. Installer le client Python
pip install ollama pandas numpy scikit-learn matplotlib seaborn
```

Ouvrez ensuite `Seance4_LLM_Ollama_RAG.ipynb`. Un ordinateur sans carte
graphique dédiée convient (le modèle `llama3.2` tourne correctement sur
CPU), au prix d'un temps de réponse un peu plus long.
