# Projet 5 — Suivre la satisfaction client avec SQL

> Traduire un besoin métier en indicateurs de suivi fiables.

## Contexte

BestMarket souhaite améliorer la qualité de son service en analysant les retours clients issus de plusieurs canaux (réseaux sociaux, application mobile, téléphone, email). Une base dédiée centralise 3 000 retours client afin d’évaluer la satisfaction, identifier les axes d’amélioration et mesurer la performance via des indicateurs clés.

## Besoin métier

- Mesurer le nombre de retours, les notes moyennes, le taux de recommandation et le Net Promoter Score (NPS).
- Analyser les données par typologie / catégorie produit, département, source de retour, jour et mois.
- Répondre à 17 questions métier (livraison, SAV, drive, réseaux sociaux, boissons, etc.).
- Identifier les magasins et produits sous-performants et les leviers d’amélioration.

## Démarche

1. Analyse du besoin et définition des indicateurs attendus.
2. Complétude de la base : création d’une base SQLite, exécution du script SQL, import des fichiers CSV (ref_magasin.csv, etc.).
3. Mise à jour du schéma relationnel et du dictionnaire de données : tables retour_client, produit, magasin.
4. Contrôle qualité et cohérence : vérification des jointures, absence de doublons, notes non nulles, associations produit/magasin.
5. Rédaction des requêtes SQL répondant aux questions métier et aux axes complémentaires (NPS par produit, magasin, service, canal).
   
## Résultats

- Base opérationnelle : 3 000 retours clients, 4 catégories de produits, 84 magasins.
- Indicateurs globaux :
  - Taux de recommandation : 70,5 %
  - NPS global : 30,97
  - Promoteurs : 1 200 / Passifs : 1 529 / Détracteurs : 271

- NPS par source : téléphone (33,81) > email (29,65) > réseaux sociaux (29,56).
- NPS par service : qualité produit (35,03) > SAV (31,51) > livraison (31,14) > drive (29,62) > expérience en magasin (27,34).
- Classements : top 5 magasins par note, départements les mieux notés, typologies produits avec le meilleur SAV (Loisirs, High-Tech).
- Analyses complémentaires :
  - Le volume de retours n’influence pas significativement la satisfaction.
  - Le canal d’expression a un impact modéré.
  - La satisfaction dépend davantage de l’expérience (magasin, SAV, livraison, drive) que du produit lui-même.

## Impact / recommandations

Impact :

- Les analyses fournissent une vision claire de la satisfaction client et des disparités entre magasins, produits et canaux.
- Elles permettent de prioriser les actions correctives et d’objectiver les décisions.

Recommandations :

- Produits : capitaliser sur les produits leaders (mise en avant, extension de gamme), améliorer le cœur de gamme et sécuriser les produits faibles.
- Magasins : identifier et diffuser les bonnes pratiques des magasins performants, accompagner les magasins en difficulté (formation, pilotage local), mettre en place un suivi NPS par magasin.
- Expérience client : homogénéiser les performances magasins, renforcer les équipes SAV sur les périodes de forte activité, améliorer l’expérience en magasin (principal point faible).
- Données : enrichir la base avec la dimension magasin (nom, localisation) et les retours via application mobile pour affiner les analyses.

## Livrable

- [Expression du besoin](./Expression_besoin.pdf)
- [Expression du besoin](./Expression_besoin.pdf)
