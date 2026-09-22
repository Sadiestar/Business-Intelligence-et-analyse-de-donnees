# Projet 6 — Analyser la qualité des stocks avec Python

> Rapprocher plusieurs sources pour fiabiliser l’analyse des produits et des stocks.

## Contexte

Bottleneck, boutique de vins et spiritueux, dispose de données extraites au 31 octobre 2024 issues de trois sources : ERP (825 produits), site Web (1513 lignes) et table de liaison. L’objectif est de fiabiliser et rapprocher ces données, d’analyser les performances commerciales (CA, marge, stock) et de proposer des axes d’amélioration pour optimiser la gestion des stocks.

## Besoin métier

- Nettoyer et consolider les données multi-sources.
- Analyser les performances : chiffre d’affaires, marges, rotation des stocks.
- Identifier les produits performants et les surstocks.
- Proposer des recommandations actionnables pour améliorer la rentabilité et réduire le cash immobilisé.

## Démarche

1. Nettoyage et consolidation :
   - ERP : correction des incohérences (statut stock, prix négatifs, stocks négatifs, marge négative) → 716 produits retenus.
   - Web : suppression des colonnes techniques, des SKU manquants/doublons et des ventes négatives → 712 lignes.
   - Liaison : suppression des identifiants non numériques et des product_id sans id_web → 731 lignes.
   - Fusion finale → 711 observations fiables.

2. Feature engineering : création de z_score, ca_par_article, rotation_stock, stock_value, taux_marge.
3. Analyses : univariée (prix), bivariée (CA vs volume), Pareto, analyse des stocks, taux de marge, corrélations, segmentation produits.
   
## Résultats

- CA total : 143 204,70 €.
- Pareto : 60 % des produits génèrent 80 % du CA et des volumes.
- Segmentation : 207 stars, 149 premium, 180 volumes, 174 faibles.
- Surstock : flop 20 avec 14 à 31 mois de stock ; valeur totale du stock = 269 241 € (> CA).
- Marges moyennes : Cognac 82,3 %, Whisky 81,7 %, Gin 74,8 %, Vin 61,5 %, Champagne 40 %, Huile d’olive 33,4 %.
- Corrélations : prix élevé → ventes faibles ; stock élevé → immobilisation ; marge non corrélée aux ventes/CA.

## Impact / recommandations

Axe 1 – Recentrer le catalogue : déréférencer les produits à faible CA, volume et marge ; concentrer les efforts sur les produits performants.
Axe 2 – Piloter la rentabilité : définir un seuil minimum de marge, revoir le pricing (notamment Champagne) et segmenter l’offre.
Axe 3 – Optimiser les stocks : fixer des seuils de 2 à 4 mois max, réduire les surstocks, prioriser les produits à forte rotation, mettre en place des alertes surstock/rupture.

Actions opérationnelles :

- Court terme : corriger les prix sous coût, publier/désactiver les 91 produits ERP sans équivalent web, mettre à jour la table de liaison.
- Moyen terme : ajouter des contraintes de validation dans l’ERP, automatiser la synchronisation stock, réconciliation mensuelle Web/ERP.
- Long terme : outil de dataviz en temps réel, alertes automatiques, unification des référentiels produits.

## Livrable

- [Notebook Python](./notebook_bottleneck.ipynb)
- [Présentation](./Presentation_Bottleneck.pdf)
