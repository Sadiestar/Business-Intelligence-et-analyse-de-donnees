# Projet 7 — Piloter des projets avec Power BI

> Centraliser les indicateurs pour faciliter le suivi et la prise de décision.

## Contexte

À partir des données extraites d’un logiciel de gestion de projets entre 2018 et début 2022, SANITORIAL souhaite mettre en place un tableau de bord Power BI pour suivre l’avancement des projets, identifier les retards, contrôler les performances et arbitrer les décisions.

## Besoin métier

- Direction générale : vue globale, alerte sur écarts > 15 %, réduction des risques stratégiques.
- Direction régionale : suivi des projets régionaux, actions correctives, escalade des projets à risque.
- Direction pays : vision coûts, délais, livrables, compréhension des écarts, plan correctif local.
- Objectif : un seul tableau de bord pour différentes attentes et niveaux de décision.
  
## Démarche

1. Construction du modèle en étoile :
   - Dim_Project : enrichie avec type de projet, pays, région.
   - Dim_Phase : code et libellé de phase.
   - Fact_Project : consolidation des données prévues et réelles (dates, durées, coûts, livrables).

2. Transformations :
   - Fusion des sources (Projections, Project Type, Country_Profiles, projects_plans, Fact_Planned, Fact_Actual).
   - Correction des noms de pays, gestion des régions manquantes, typage des colonnes.
   - Calcul de la date de fin prévue : End Date Planned = Start Date + Planned_Duration.

3. Rapport Power BI : visualisations par pays, statut portefeuille, top risques, évolution annuelle, réel vs prévisionnel.

## Résultats

- Budget consommé : 60,20 M€.
- Projets en alerte : 41 (39 % du portefeuille).
- Nombre de projets : 104.
- Score Performance : 90 % (proche de la cible mais fragile).
- Réel vs prévisionnel : coûts 107 %, livrables 90 %, durée 87 %.
- Performance par année : 88 % (2018), 92 % (2019), 84 % (2020), 89 % (2021), 79 % (2022).
- Top risques : projets à 42 %, 32 %, 31 %, 30 %, 29 % de risque.

## Impact / recommandations

Impact :

- Vision adaptée aux niveaux stratégique, analytique et opérationnel.
- Identification des pays et projets en difficulté.
- Meilleure maîtrise du portefeuille et des engagements.

Recommandations :

- Prioriser les actions correctives sur les pays et projets les plus en difficulté.
- Renforcer le suivi des projets « À surveiller ».
- Mettre en place un pilotage rigoureux des coûts, délais et livrables.
- Réduire les projets en alerte, sécuriser les délais, améliorer la maîtrise budgétaire.
- Homogénéiser les pratiques de pilotage projet à l’échelle internationale pour stabiliser durablement la performance.

## Livrables

- [Tableau de bord Power BI](./Tableau-de-bord.pbix)
- [Présentation PDF](./Presentation_PowerBI.pdf)
