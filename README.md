# Exploration du discours écologique dans les sites de festivals (Sujet 9)

Ce dépôt contient le code source et les données structurées pour l'analyse du Web Mining des engagements environnementaux des festivals de musique. Ce projet a été réalisé dans le cadre du cours **MLSMM2153 : Web Lens** (2025-2026).

## Présentation du projet
L'objectif est d'analyser comment les organisateurs de festivals intègrent la durabilité dans leur communication. Nous identifions spécifiquement les **actions concrètes** par rapport aux **promesses vagues** via des techniques de Text Mining et de Link Analysis.

## Installation et Utilisation
Ce projet a été développé sur **Google Colab**. 

### Pourquoi Google Colab ?
Le choix de cet environnement a été dicté par plusieurs impératifs méthodologiques :
* **Réplicabilité immédiate** : L'environnement est pré-configuré, permettant aux professeurs de reproduire l'analyse sans installation locale complexe.
* **Puissance de calcul** : L'utilisation de modèles de langage lourds (spaCy pour la lemmatisation multilingue) bénéficie des ressources RAM/CPU de Colab.
* **Collaboration** : Facilitation du travail de groupe asynchrone pour la rédaction et le débogage du pipeline.

1. **Lancer le code** : Ouvrez le fichier `.ipynb` présent dans ce dépôt via Google Colab.
2. **Bibliothèques requises** :
   - `pandas`, `matplotlib`, `numpy` (Analyse de données)
   - `spacy`, `nltk`, `langdetect` (Traitement du langage naturel)
   - `scikit-learn` (Clustering K-Means et TF-IDF)
3. **Modèles spaCy** : Exécutez `!python -m spacy download fr_core_news_sm` et `en_core_web_sm` dans le notebook.

## Méthodologie (Répicabilité)
Conformément aux consignes de réplicabilité:
* **Collecte (Scraping)** : Navigation automatisée avec filtres sur les mots-clés "éco", "durabilité", etc..
* **Prétraitement** : Nettoyage multilingue (FR, EN, NL), tokenisation et lemmatisation via spaCy.
* **Analyse Sémantique** : Création d'un ratio basé sur des lexiques personnalisés (Concret vs Vague).
* **Clustering** : Segmentation en 5 groupes thématiques validée par la méthode du coude.
* **Link Analysis** : Exportation vers Gephi pour l'analyse des centralités (PageRank, Betweenness).

## Contenu du dépôt
* `Projet_Web_Mining_GroupeX.ipynb` : Notebook principal contenant tout le pipeline.
* `gephi_nodes.csv` & `gephi_edges.csv` : Données pour l'importation directe dans Gephi.
* `festival_pages_dataset.csv` : Corpus structuré après nettoyage.

## Auteurs (Groupe X)
* Charles-Pirlot Diégo 08112000
* Valère Scheuren
