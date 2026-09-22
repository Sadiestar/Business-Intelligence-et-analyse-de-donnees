# Projet 3 — Requêter une base de données avec SQL

> Produire des résultats fiables à partir d’une base de données relationnelle.

## Contexte

Dans le cadre de l'exploitation de données issues de fichiers CSV, ce projet vise à structurer et interroger une base de données relationnelle à l'aide du langage SQL et du SGBDR SQLite. L'enjeu est de garantir la qualité et la cohérence des données pour permettre des analyses fiables.

## Besoin métier

- Garantir la qualité et la cohérence des données brutes.
- Structurer et exploiter des données issues de fichiers CSV.
- Interroger les données à l'aide du langage SQL pour répondre à des besoins d'analyse.

## Démarche

1. Analyse des fichiers sources (CSV) et réalisation du dictionnaire des données : Identification des clés (primaires/étrangères), description fonctionnelle de chaque champ et correspondance CSV ↔ dictionnaire.
2. Conception du schéma relationnel : Modélisation des tables Region et Contrat et de leurs relations (1,N).
3. Chargement des données dans SQLite : Création des tables, mise en place des contraintes d'intégrité référentielle et import des fichiers CSV.
4. Exploration et interrogation avec SQL : Requêtes d'analyse et de vérification des données.

## Résultats

- Dictionnaire des données : Référence commune, claire et partagée pour la modélisation.
- Schéma relationnel : Modèle cohérent et normalisé. Une région peut être associée à plusieurs contrats (relation 1,N via la clé étrangère Code_dep_code_commune).
- Base de données opérationnelle : Chargement réussi de region.csv (38 916 lignes) et contrat.csv (30 335 lignes).
- Résolution d'une anomalie d'intégrité référentielle : Le SGBDR a bloqué l'import initial avec l'erreur « FOREIGN KEY constraint failed ». L'analyse a révélé 3 valeurs présentes dans la table Contrat mais absentes de la table Region ('97460', '97437', '97470'), représentant 9 lignes impactées. Ces valeurs ont été intégrées dans la clé primaire de la table Region pour assurer l'intégrité référentielle.

## Impact / recommandations

Impact :

- La base de données est désormais normalisée, cohérente et fiable, permettant des analyses SQL robustes et une exploitation optimale des données.

Recommandations :

- Automatiser les contrôles d'intégrité référentielle en amont de l'import pour détecter les valeurs orphelines.
- Documenter les corrections apportées aux données sources afin de garantir la traçabilité.
- Optimiser l'indexation des clés primaires et étrangères pour améliorer les performances des requêtes SQL lors de l'exploration.

## Livrable

- [Méthodologie et documentation](./Méthodologie_%26_documentation_022026.pdf)
