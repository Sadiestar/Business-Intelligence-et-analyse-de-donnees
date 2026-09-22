# Projet 10 — Étudier le marché du jeu vidéo

> Croiser données de marché et signaux d’engagement pour orienter un positionnement stratégique.

## Contexte

UOI Games prépare son premier développement AAA et doit choisir un segment suffisamment attractif pour limiter les risques d'une première production. L'étude porte sur le marché français du jeu vidéo, avec pour objectif d'analyser, positionner et valider un concept avant engagement des coûts de production à grande échelle.

## Besoin métier

- Genre : quel genre offre un bassin de demande suffisant sans concurrence insoutenable ?
- Écosystème : quelle plateforme bénéficie de la dynamique la plus favorable pour un premier lancement ?
- Risque : quelles validations réduisent le risque avant d'engager une production AAA ?
- Décision attendue : sélectionner un positionnement, puis le tester avant la production à grande échelle.

## Démarche

1. Analyse SWOT et PESTEL d'UOI Games : forces (liberté de positionnement, PI originale), faiblesses (première production AAA, notoriété limitée), opportunités (segments variés, testabilité) et menaces (concurrence, coûts, attentes fortes).
2. Consolidation de quatre sources dans Power Query et modélisation dans Power BI :
   - Ventes historiques (Ventes_jeux_1980_2016.csv)
   - Ventes de consoles (Vente de console 2022.csv)
   - Visibilité et appréciation (RAWG et All_publish_VideoGame_2022.csv)
   - Marché français récent (SELL, bilan 2025)

3. Analyses : évolution du marché, répartition par support, part du dématérialisé, poids des genres, classifications PEGI, positionnement genre × plateforme (visibilité vs note médiane).
4. Validation : questionnaire (Google Forms) et prototype jouable avant investissement AAA.

## Résultats

- Marché français : 5,9 Md€ en 2025, +31 % depuis 2017.
- Mobile : part passée de 17 % (2017) à 31 % (2025), contribue à +175 M€ de croissance 2024-2025.
- Console : premier écosystème mais en recul (-95 M€) ; part passée de 54 % à 44 %.
- PC : relativement stable (+4 M€), part passée de 29 % à 26 %.
- Dématérialisation : 89 % des ventes en 2025 (vs 69 % en 2017).
- Genres : Action 27,3 %, Sport 18,3 %, Tir/FPS 15,6 %, RPG 11,7 %, Aventure 10,7 %.
- PEGI : PEGI 3 (29 %) et PEGI 18 (30 %) dominent ; PEGI 16 (18 %) est un compromis à tester.
- Positionnement : segments Action sur PlayStation 2/3, Aventure sur PlayStation 3 et Action sur Xbox 360 combinent notoriété et appréciation.
- Simulation : 48,3 % préfèrent mobile, 80 % le numérique, orientation action-aventure mobile.

## Impact / recommandations

Recommandation principale : Action-Aventure Mobile
- Cible : joueurs réguliers adolescents et adultes.
- Distribution : numérique, modèle free-to-play.
- Classification : PEGI 16 à tester (hypothèse, pas conclusion définitive).
- Objectif : ~4 400 téléchargements la première année (scénario central).

Trois validations avant l'investissement AAA :
1.Enquête terrain (≥ 300 joueurs ciblés) — GO si intérêt ≥ 60 %.
2.Prototype jouable — GO si rétention ≥ 35 %.
3.Test économique — GO si modèle rentable (premium vs free-to-play).

Points de vigilance :
- Les données mobiles ne permettent pas d'estimer précisément le chiffre d'affaires.
- Les 300 réponses du questionnaire sont simulées et doivent être remplacées par une enquête réelle.
- Le taux de joueurs payants et le revenu moyen par joueur restent à mesurer.
- Le niveau d'ambition, le budget et le périmètre AAA doivent être définis avant association définitive au label.

## Livrables

- [Analyse Power BI](./Analyses.pbix)
- [Présentation du projet](./Prez_projet_10.pdf)
