# Projet 11 — Augmenter un projet data avec l’IA

> Utiliser l’intelligence artificielle de manière critique, documentée et contrôlée.

## Contexte

Bottleneck dispose de trois exports (ERP, WordPress, table de liaison) et d’un notebook historique produisant des KPI. Le responsable des ventes et le CODIR souhaitent consolider ces sources, comprendre au moins huit familles d’erreurs et obtenir des indicateurs fiables pour les décisions commerciales et le futur tableau de bord.

## Besoin métier

Produire, à partir des extractions au 31 octobre et des ventes d’octobre, une vue produit fiable du chiffre d’affaires, des marges et des stocks, tout en rendant visibles les limites de qualité et les décisions de traitement. Le projet doit auditer le notebook historique, le comparer à des versions améliorées par assistants IA, puis recalculer les KPI avec la version retenue.

## Démarche

1. Cadrer : audit du notebook historique (111 cellules) et des trois sources ; identification des faiblesses (prix négatifs, stocks négatifs, alias de DataFrames, export erroné, Pareto excluant la frontière, interprétation causale).
2. Comparer : veille sur Copilot, DeepSeek et ChatGPT. 12 essais, dont 3 contrôlés (série 4) avec même prompt et même export. Notation : exactitude, couverture, priorisation, clarté, respect des consignes.
3. Améliorer : chaque proposition IA est validée ou rejetée par un humain, intégrée au notebook, exécutée sur noyau neuf, puis contrôlée par exports.
4. Valider : notebook final 13 cellules, 3 graphiques, 5 fichiers de preuve ; validation métier TVA/statuts/prix à faire.

## Résultats

- Produits appariés : 713 / 716 ERP en ligne (99,58 %).
- CA TTC : 143 598,90 € pour 5 737 unités vendues.
- Valeur du stock : 277 225,11 € ; marge brute : 44 636,66 € (TVA 20 % supposée).
- Pareto : 434 produits nécessaires pour 80 % du CA (60,9 % du catalogue).
- Prix atypiques : 31 alertes IQR, 13 Z-score (IQR retenu comme principal).
- Comparaison IA (série 4) : ChatGPT 4,00/4 ; Copilot 3,60/4 ; DeepSeek 3,42/4. ChatGPT retenu pour revue approfondie, Copilot pour contrôle rapide, DeepSeek en seconde lecture.
- Améliorations clés : jointures contrôlées, prix négatifs conservés + drapeau, vocabulaire « association » au lieu de causalité, traçabilité (5 exports + journal).

## Impact / recommandations

Impact : KPI recalculés et fiabilisés, reproductibilité et traçabilité renforcées, notebook pédagogique exploitable.

Recommandations :

- Compléter les 3 clés manquantes et viser 100 % de couverture.
- Faire valider la TVA, les règles de statut et le traitement des prix incohérents par les responsables métier.
- Exécuter les contrôles qualité à chaque extraction et collecter plusieurs mois de ventes avant d’interpréter la couverture de stock.
- Pour l’IA : prompt commun, limiter les appels, archiver les réponses, validation humaine obligatoire ; conserver ChatGPT pour la revue approfondie, Copilot pour le contrôle rapide, DeepSeek pour une seconde lecture filtrée.
- Documenter chaque décision et conserver les preuves (rapport_qualite.csv, rapport_jointures.csv, kpi_bottleneck.csv, resultats_cles.json, journal_ia.md).

## Livrables

- [Dossier du projet](./Documentation_Data_IA_augmenté.pdf)
- [Support de soutenance](./Présentation_Data_IA_augmenté.pdf)
- [Notebook Python_original_Projet_06](../Projet_06/notebook_bottleneck.ipynb)
- [Notebook amélioré](Notebook_042026_ameliore_IA_pedagogique.ipynb)
  
