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

Partie 1 – Prédiction de la valeur foncière :

- Excellente performance : Coefficient de détermination R² = 0,986
- Erreur moyenne relative inférieure à 10 %, rendant les prédictions fiables et robustes.
- Valorisation du portefeuille : Au 31 décembre 2022, la valeur totale estimée s’élève à environ 169 M€ (56 % de biens particuliers, 44 % de biens professionnels).

Partie 2 – Classification des biens :

- Les variables « nombre de pièces principales » et « prix au m² » sont les plus discriminantes.
- Taux de correspondance élevé : 91,27 % pour la distinction appartements / locaux commerciaux.
- K-Means est un bon outil d’exploration et de segmentation, mais ne remplace pas l’expertise métier.

## Impact / recommandations

Impact :

- Ces modèles constituent des outils d’aide à la décision pour l’estimation et la segmentation du portefeuille immobilier.

Limites identifiées :

- La régression linéaire suppose une relation linéaire (simplificatrice dans l’immobilier) et est sensible aux valeurs aberrantes.
- Certaines variables importantes ne sont pas prises en compte (état du bien, étage, travaux, environnement, etc.).
- Le modèle est entraîné sur des données passées (2017-2021) et peut perdre en fiabilité si le marché évolue.

Recommandations :

- Interpréter les résultats avec prudence et les confronter systématiquement à l’expertise métier.
- Enrichir le modèle avec des variables explicatives supplémentaires (état du bien, performance énergétique, etc.).
- Intégrer des données plus récentes pour maintenir la fiabilité des analyses et des prédictions.

## Livrables

- [Notebook Python](./NotebookP8.ipynb)
- [Présentation PDF](./Presentation.pdf)
