# Projet 8 — Réaliser une analyse de données avec Python

> Faire émerger des enseignements utiles à partir d’une démarche analytique reproductible.

## Contexte

Dans le cadre de l’analyse des transactions immobilières parisiennes (2017-2021), l’entreprise « Les Plus Beaux Logis de Paris » souhaite exploiter ses données historiques pour mieux comprendre la structure de son portefeuille d’actifs et estimer la valeur de ses biens. L’analyse est réalisée en Python, en mobilisant des techniques de machine learning.

## Besoin métier

- Estimer la valeur foncière d’un bien immobilier à partir de ses caractéristiques (surface, localisation, type, etc.).
- Mieux comprendre la composition du portefeuille d’actifs immobiliers.
- Segmenter les biens pour distinguer les appartements des locaux commerciaux et identifier des profils d’investissement.

## Démarche

1. Préparation des données :

- Nettoyage et préparation des données de transactions (2017-2021).
- Encodage des variables catégorielles (One-Hot Encoding).
- Séparation des données : 70 % pour l’entraînement, 30 % pour le test.

2. Modélisation :

- Partie 1 – Modèle prédictif (Régression linéaire) : Prédiction de la valeur foncière à partir de la surface réelle, de l’arrondissement, du type de bien et de la date de transaction.
- Partie 2 – Modèle de classification (K-Means) : Regroupement des biens en 2 clusters pour distinguer les appartements des locaux commerciaux, avec standardisation des variables (StandardScaler).

## Résultats

Le notebook conserve l’ensemble du raisonnement analytique, tandis que la présentation synthétise les constats pour un public métier.

## Impact / recommandations

La démarche rend l’analyse vérifiable et réutilisable. Il est recommandé de conserver les hypothèses, les limites et les contrôles dans toute future actualisation.

## Livrables

- [Notebook Python](./Notebook.ipynb)
- [Présentation PDF](./Presentation.pdf)
