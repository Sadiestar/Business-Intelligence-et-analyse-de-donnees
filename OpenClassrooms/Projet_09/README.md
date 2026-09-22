# Projet 9 — Analyser la performance commerciale avec Power BI

> Relier ventes, rentabilité et stocks pour soutenir le pilotage de Bottleneck.

## Contexte

Bottleneck souhaite suivre quotidiennement sa performance commerciale, sa rentabilité, l’évolution des prix d’achat, les stocks, les promotions et le lancement de la gamme sans alcool. Le dispositif s’adresse au PDG, au responsable des ventes et aux chefs de produits. Le livrable opérationnel est un tableau de bord , accompagné d'un rapport d’analyse.

## Besoin métier

- Détecter un écart de performance.
- Identifier le segment ou le produit concerné.
- Expliquer la cause de l’écart.
- Définir une action mesurable.
- Suivre quotidiennement l’activité, la marge, les coûts, les stocks et les promotions.

## Démarche

1. État des lieux
Base SQLite composée de 4 tables sur 13 mois (oct. 2022 – oct. 2023) :

2. Problèmes identifiés
- Décimaux à convertir en culture fr-FR (Price, Purchase_Price, Price_Offer).
- Commandes vides à distinguer de zéro pour les moyennes et taux.
- 110 SKU Finance absents de Web sans vente (hors catalogue actif).

3. Outils retenus
- Extraction : connexion directe SQLite via ODBC.
- Traitement : Power Query (typage, normalisation, contrôles qualité, tables intermédiaires).
- Analyse : Power BI Desktop (modèle en étoile, mesures DAX, mode Import).
- Diffusion : Power BI Service pour actualisation planifiée.

4. Architecture cible
Chaîne SQLite → Power Query → modèle en étoile Power BI (Dim_Date, Dim_Produit, faits d’activité et de promotions).

## Résultats

- Données suffisantes pour analyser l’activité, la marge, les coûts, les stocks et les promotions.
- Modèle en étoile : relations filtrées à sens unique, mesures centralisées.
- Tableau de bord organisé en parcours décisionnel : synthèse exécutive, performance produits, rentabilité, stocks, promotions, sans alcool, historique produit.
- Alertes actionnables : chaque alerte conduit aux produits concernés et aux indicateurs de contrôle.

## Impact / recommandations

Impact :

- Pilotage quotidien fluide grâce au mode Import.
- Analyse par thème avec un chemin de navigation cohérent.
- Décisions actionnables basées sur des données fiables.

Recommandations :

- Maintenir les règles de transformation et la documentation dans Power Query.
- Relier chaque alerte à une action métier mesurable.
- Conserver SQLite + Power Query comme solution principale ; les exports CSV en secours ; envisager le cloud pour une montée en charge future.
- Surveiller les 110 SKU Finance hors catalogue actif.
  
## Livrables

- [Tableau de bord Power BI](./TDB.pbix)
- [Rapport d’analyse](./Rapport_analyse.pdf)
- [Présentation du projet](./Presentation_projet.pdf)
- [Dictionnaire des données](./Dictionnaire%20des%20données%20-%20Bottleneck.pdf)
- [Schéma de la base](./Schéma%20de%20la%20base%20de%20données.pdf)
