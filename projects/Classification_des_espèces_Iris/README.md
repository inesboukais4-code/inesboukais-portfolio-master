# Système Intelligent de Classification Botanique

## Analyse prédictive du dataset Iris de Fisher

Ce projet consiste à développer un système de classification automatique des espèces de fleurs d’Iris en utilisant des techniques d’apprentissage automatique supervisé.

L’objectif est de prédire l’espèce d’une fleur à partir de mesures morphologiques telles que la longueur et la largeur des sépales et des pétales.

Le modèle est entraîné à partir du célèbre dataset Iris de Fisher, un jeu de données de référence en machine learning. :contentReference[oaicite:1]{index=1}

---

# Objectifs du projet

Les principaux objectifs sont :

- automatiser l’identification des espèces de fleurs
- explorer et analyser un dataset réel
- appliquer plusieurs algorithmes de machine learning
- comparer les performances des modèles
- réaliser une phase de prédiction sur de nouvelles données

Ce projet illustre les bases du Machine Learning supervisé.

---

# Dataset utilisé

Le dataset **Iris** contient :

- 150 observations
- 4 caractéristiques (features) :
  - longueur du sépale
  - largeur du sépale
  - longueur du pétale
  - largeur du pétale
- 3 classes d’espèces :
  - Iris Setosa
  - Iris Versicolor
  - Iris Virginica

Ces caractéristiques permettent de distinguer les différentes espèces grâce à leurs propriétés morphologiques. :contentReference[oaicite:2]{index=2}

---

# Exploration et analyse des données

Les données ont été analysées et structurées avec Pandas afin de créer un DataFrame.

Les étapes principales :

- chargement du dataset
- analyse descriptive
- sélection des variables explicatives
- séparation entre variables d’entrée (X) et variable cible (Y)

---

# Visualisation des données

Une visualisation des données a été réalisée avec Matplotlib afin d’observer la séparation entre les différentes classes.

L’analyse visuelle montre que :

- l’espèce Setosa est clairement séparée des autres
- Versicolor et Virginica sont plus proches et nécessitent un modèle plus précis pour être distinguées. :contentReference[oaicite:3]{index=3}

---

# Stratégie d’apprentissage

Pour entraîner et évaluer les modèles, les données ont été divisées en :

- 70 % données d’entraînement
- 30 % données de test

Cette méthode permet de vérifier que le modèle fonctionne correctement sur des données inconnues. :contentReference[oaicite:4]{index=4}

---

# Algorithmes utilisés

Plusieurs modèles de machine learning ont été implémentés et comparés.

## K-Nearest Neighbors (KNN)

Principe :

Le modèle classe une observation selon la classe majoritaire de ses k voisins les plus proches.

Configuration :

- k = 7 voisins

Performance :

- précision : 97.7 %

Ce modèle s’est révélé être le plus performant pour ce dataset. :contentReference[oaicite:5]{index=5}

---

## Réseau de Neurones (MLP)

Le modèle MLP (Multi-Layer Perceptron) simule un réseau de neurones artificiels.

Architecture :

- deux couches cachées
- 5 neurones par couche

Optimisation :

- algorithme Adam
- régularisation pour limiter le surapprentissage.

---

## Random Forest

La Forêt Aléatoire est un modèle d’ensemble basé sur plusieurs arbres de décision.

Configuration :

- profondeur maximale de l’arbre limitée à 2.

---

# Phase de prédiction

Une fois le modèle entraîné, il peut être utilisé pour prédire l’espèce de nouvelles fleurs.

Exemple :

```
nouveau_jeu = [[5.1, 3.5, 1.4, 0.2],
               [6.2, 3.4, 5.4, 2.3]]

prediction = modele.predict(nouveau_jeu)
```

Résultat :

```
['Iris-setosa', 'Iris-virginica']
```

---

# Technologies utilisées

- Python
- Scikit-learn
- Pandas
- Matplotlib

---

# Résultats

Après comparaison des différents modèles :

- le KNN a obtenu la meilleure performance
- précision obtenue : 97.7 %

Les visualisations confirment que les caractéristiques morphologiques sont de bons indicateurs pour distinguer les espèces d’Iris. :contentReference[oaicite:6]{index=6}

---

# Ce que ce projet m’a apporté

Ce projet m’a permis de :

- comprendre les bases du machine learning supervisé
- manipuler des datasets scientifiques
- implémenter plusieurs modèles d’apprentissage
- analyser et comparer leurs performances
- réaliser des visualisations de données

---

# Auteur

**Ines Boukais**

Projet réalisé dans le cadre d’un cours d’**Intelligence Artificielle**  
Année universitaire **2023 / 2024**


## Rapport
[📄 Voir le rapport](rapport_.pdf)
