# Analyse et visualisation de données médicales avec Power BI et RAG

## Présentation du projet

Ce projet porte sur l’analyse, la visualisation et l’interprétation intelligente de données médicales en combinant la **Business Intelligence (BI)** et l’**intelligence artificielle (IA)**.

La solution repose sur deux composantes complémentaires : des tableaux de bord interactifs développés avec **Microsoft Power BI** et un système de génération augmentée par récupération, appelé **Retrieval-Augmented Generation (RAG)**, implémenté en Python.

L’objectif est de faciliter l’exploration des données médicales, d’identifier des tendances, d’analyser les niveaux de risque des patients et de répondre à des questions en langage naturel à partir des informations disponibles dans le jeu de données.

Ce projet a été réalisé dans le cadre d’un projet de fin d’année en ingénierie informatique et réseaux, option MIAGE, à l’École Marocaine des Sciences de l’Ingénieur (EMSI), à Casablanca.

## Objectifs du projet

Les principaux objectifs de ce projet sont les suivants :

- Analyser et structurer les données médicales afin de faciliter leur exploitation.
- Concevoir des tableaux de bord interactifs pour visualiser les indicateurs cliniques.
- Étudier la répartition des patients selon l’âge, le genre, les symptômes et les diagnostics.
- Visualiser les niveaux de risque et de sévérité des patients.
- Analyser les paramètres vitaux et les catégories de pression artérielle.
- Étudier les plans de traitement en fonction des diagnostics et des symptômes.
- Développer un système RAG permettant d’interroger le jeu de données en langage naturel.
- Générer des réponses contextualisées à partir des informations récupérées.
- Combiner la visualisation décisionnelle et l’intelligence artificielle pour faciliter l’analyse des données.

## Architecture générale

L’architecture du projet repose sur trois composantes principales.

### 1. Couche données

Le projet utilise un jeu de données médicales comprenant plus de 2 000 dossiers de patients. Les principales informations exploitées sont :

- **Données démographiques :** âge et genre.
- **Paramètres vitaux :** température corporelle, fréquence cardiaque et saturation en oxygène.
- **Informations cliniques :** symptômes et diagnostics médicaux.
- **Évaluation clinique :** niveaux de risque et de sévérité.
- **Prise en charge :** catégories de pression artérielle et plans de traitement.

Ce jeu de données constitue la source principale des analyses réalisées dans Power BI et du système RAG développé en Python.

### 2. Analyse et visualisation avec Power BI

Microsoft Power BI est utilisé pour transformer les données médicales en indicateurs et en visualisations interactives.

Les tableaux de bord permettent notamment :

- L’analyse démographique des patients par âge et par genre.
- Le suivi des indicateurs moyens des paramètres vitaux.
- La visualisation de la répartition des symptômes et des diagnostics.
- L’analyse des niveaux de risque et de sévérité.
- L’étude des catégories de pression artérielle.
- L’exploration des plans de traitement selon les diagnostics et les symptômes.

Les visualisations facilitent l’exploration des données et permettent d’obtenir une vue synthétique des principales caractéristiques de la population étudiée.

Le rapport Power BI est fourni au format `.pbix`.

### 3. Intelligence artificielle : système RAG médical

Le deuxième volet du projet repose sur un système de génération augmentée par récupération (RAG), développé en Python et expérimenté dans Google Colab.

Le système vise à permettre à l’utilisateur de poser des questions en langage naturel et d’obtenir des réponses contextualisées à partir des informations présentes dans le jeu de données médicales.

Le processus repose sur les étapes suivantes :

1. **Prétraitement des données :** chargement, nettoyage et transformation des informations.
2. **Préparation des contenus :** structuration des informations médicales sous une forme exploitable.
3. **Vectorisation sémantique :** représentation des contenus sous forme de vecteurs numériques appelés *embeddings*.
4. **Indexation vectorielle :** stockage des représentations dans ChromaDB.
5. **Recherche sémantique :** récupération des informations les plus pertinentes par rapport à la question posée.
6. **Génération de réponses :** utilisation d’un modèle de langage pour produire une réponse contextualisée à partir des informations récupérées.

LangChain assure l’orchestration des différentes étapes du système RAG, tandis que ChromaDB est utilisé pour le stockage vectoriel et la recherche par similarité.

Le code Python correspondant est disponible dans le dépôt GitHub.

## Technologies et outils utilisés

| Technologie | Rôle dans le projet |
|---|---|
| Python | Traitement des données et développement du système RAG |
| Microsoft Power BI | Analyse décisionnelle et visualisation interactive |
| DAX | Calcul des mesures et des indicateurs dans Power BI |
| Pandas | Chargement, nettoyage et transformation des données |
| LangChain | Orchestration du processus RAG |
| ChromaDB | Stockage des vecteurs et recherche sémantique |
| Google Colab | Environnement de développement et d’exécution Python |
| Excel / CSV | Stockage et exploitation des données médicales |
| GitHub | Hébergement du code et des livrables du projet |




### Prérequis

Pour exploiter les différents éléments du projet, les outils suivants peuvent être nécessaires :

- Microsoft Power BI Desktop pour ouvrir le rapport `.pbix`.
- Python 3 pour exécuter le script du système RAG.
- Les bibliothèques Python utilisées dans l’implémentation.
- Le fichier de données médicales utilisé comme source.
- Les accès et paramètres de configuration du modèle de langage, si celui-ci nécessite des identifiants ou une clé API.

### Utilisation du rapport Power BI

1. Cloner ou télécharger le dépôt GitHub.
2. Ouvrir le fichier `.pbix` avec Microsoft Power BI Desktop.
3. Vérifier le chemin d’accès au fichier Excel si Power BI demande de localiser la source de données.
4. Actualiser les données si nécessaire.
5. Explorer les tableaux de bord, les indicateurs et les filtres interactifs.

### Exécution du système RAG

1. Cloner ou télécharger le dépôt GitHub.
2. Ouvrir le script Python ou l’importer dans Google Colab.
3. Installer les dépendances nécessaires à l’exécution du code.
4. Configurer le chemin d’accès au jeu de données et les paramètres du modèle de langage.
5. Exécuter les étapes de prétraitement, de vectorisation et d’indexation prévues dans le script.
6. Interroger le système en langage naturel afin d’obtenir des réponses fondées sur les informations récupérées.

Les commandes d’installation exactes dépendent des bibliothèques et du modèle de langage effectivement utilisés dans le script.

## Exemples de questions exploitables

Le système RAG est conçu pour faciliter l’exploration des données médicales à travers des questions telles que :

- Quels sont les symptômes les plus fréquents chez les patients présentant un niveau de risque élevé ?
- Comment les patients se répartissent-ils selon les différents diagnostics ?
- Quelles tendances peut-on observer entre les paramètres vitaux et les niveaux de risque clinique ?
- Quels plans de traitement sont associés aux différents diagnostics ?
- Quelles sont les principales caractéristiques démographiques des patients étudiés ?

La pertinence des réponses dépend de la qualité des données disponibles, du mécanisme de récupération et du modèle de langage utilisé.

## Limites et utilisation responsable

Ce projet constitue un prototype académique destiné à l’analyse exploratoire des données médicales.

- La fiabilité des résultats dépend de la qualité et de l’exhaustivité du jeu de données.
- Les réponses générées par le système RAG doivent être vérifiées à partir des données sources.
- Les associations observées entre variables ne permettent pas, à elles seules, d’établir des relations de causalité.
- Le système ne constitue pas un outil de diagnostic médical et ne remplace pas l’expertise des professionnels de santé.
- Les données médicales sensibles ou permettant d’identifier des personnes ne doivent pas être publiées dans un dépôt public.

## Perspectives d’amélioration

Plusieurs évolutions peuvent être envisagées :

- Automatiser davantage le prétraitement et l’actualisation des données.
- Améliorer la pertinence de la recherche sémantique.
- Ajouter des références aux sources utilisées pour générer les réponses.
- Développer une interface utilisateur dédiée à l’interrogation du jeu de données.
- Renforcer la complémentarité entre les tableaux de bord Power BI et le système RAG.
- Mettre en place des tests systématiques pour évaluer la qualité des réponses générées.

## Avertissement

Ce projet illustre l’intégration de la Business Intelligence et de l’intelligence artificielle pour l’exploration des données médicales. Il s’agit d’un prototype à vocation académique et analytique, qui n’a pas été présenté comme un système médical validé pour un usage clinique.
