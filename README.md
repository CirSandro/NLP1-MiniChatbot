# Mini-Chatbot NLP Assistant

Ce projet est une évaluation réalisée dans le cadre d'un cours de NLP (Natural Language Processing). L'objectif est de construire un assistant virtuel capable de détecter les intentions de l'utilisateur et d'extraire les entités nommées pour générer des réponses adaptées.

## Contexte

**Sujet d'évaluation de 2h :** Construire un mini-chatbot capable d'extraire les entités nommées d'une phrase, d'identifier les sujets principaux et de générer une réponse. Le projet utilise un dataset comprenant 100 exemples pour divers types d'intentions (`translate`, `transfer`, `timer`, `definition`, `meaning_of_life`, etc.).

L'objectif ultime est de créer un assistant généraliste qui détecte l'intention de l'utilisateur, les entités pertinentes, et identifie les intentions hors sujet si elles sont présentes.

## Objectifs

1. **Exploration de données (EDA)**
   - Compter les classes et les exemples.
   - Visualiser les 20 mots les plus fréquents (hors mots vides) pour les classes `transfer`, `timer` et `meaning_of_life`.
   - Calculer le nombre moyen de mots dans les phrases.

2. **Préparation des données**
   - Nettoyer les phrases (suppression des stop words, ponctuation, lemmatisation) et ajouter une colonne `processed_sentence`.
   - Séparer les données `oos` (out of scope) dans de nouveaux dataframes.

3. **Modélisation des sujets**
   - Construire une matrice TF-IDF et appliquer LSA pour identifier des topics parmi les intentions existantes et les données hors-sujet.

4. **Classification**
   - Construire des matrices Bag of Words (BoW) et TF-IDF, et entraîner des classifieurs de Régression Logistique pour chaque approche.
   - Évaluer les classifieurs et sélectionner la meilleure méthode.
   - Analyse de la confusion entre les intentions spécifiques.

5. **Reconnaissance d'entités nommées (NER)**
   - Identifier les types d'entités à reconnaître pour les intentions sélectionnées.
   - Utiliser des règles personnalisées avec spaCy pour reconnaître les langues, dates et pays dans les phrases.

6. **Développement du chatbot**
   - Construire une boucle interactive pour détecter l’intention et les entités dans les phrases de l’utilisateur, et générer des réponses.

## Structure du Projet

```plaintext
.
├── README.md
└── src
    └── TP_final_NLP1_2024.ipynb
