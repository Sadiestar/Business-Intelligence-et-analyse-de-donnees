# Projet 4 — Préparer des données dans le respect du RGPD

> Concilier qualité des données, conformité et besoins d’analyse.

## Contexte

À la suite d’une plainte client et d’une limitation temporaire des traitements prononcée par la CNIL, l’entreprise Dev’Immédiat doit démontrer sa conformité au RGPD et encadrer strictement les traitements de données personnelles issues de son CRM. Ce projet vise à produire une extraction anonymisée exploitable et à documenter les mesures correctives.

## Besoin métier

- Sécuriser immédiatement la conformité RGPD et limiter les traitements au strict nécessaire.
- Préparer les éléments justificatifs attendus par la CNIL en vue de la levée de la limitation.
- Fournir une extraction CRM anonymisée à l’équipe Performance Commerciale, sans exposer de données identifiantes ni de tarifs détaillés.

## Démarche

1. Extraction SQL ciblée : sélection des seules variables utiles au pilotage 2022 (dossiers complets).
2. Exclusion des données sensibles ou identifiantes : nom, email, adresse, numéro de sécurité sociale, groupe sanguin, localisation précise, identifiants techniques, etc.
3. Anonymisation via Power Query :
   - Généralisation (binning) : revenus, valeur de résidence, points perdus, âge du véhicule, tarif.
   - Agrégation temporelle : date de demande ramenée au mois.
   - Binarisation : présence d’enfants, conduite accompagnée.
   - Suppression de tous les identifiants directs.

4. Documentation des traitements : dictionnaire des variables, règles de transformation et justification RGPD.
5. Formulation de recommandations organisationnelles : minimisation, habilitations, traçabilité, transparence, conservation.

## Résultats

- Extraction CRM anonymisée conforme aux exigences RGPD, sans identifiants directs ni données sensibles.
- Confidentialité tarifaire préservée : les tarifs sont livrés uniquement par tranches.
- Valeur analytique maintenue : analyses possibles sur les volumes mensuels, les formules et les tranches tarifaires.
- Documentation complète des traitements SQL et Power Query, garantissant transparence et reproductibilité.
- Recommandations opérationnelles prêtes à être intégrées dans les processus internes.

## Impact / recommandations

Impact :

- Réduction forte du risque de ré-identification et sécurisation des traitements de données personnelles.
- Base saine pour la levée de la limitation CNIL et la reprise des analyses commerciales.

Recommandations :

- Minimisation : mettre en place une whitelist des variables par usage, interdire les exports complets et imposer des requêtes validées.
- Habilitations & traçabilité : appliquer le moindre privilège, journaliser les accès/exports et alerter sur toute extraction anormale.
- Transparence & droits : actualiser les notices d’information et structurer un circuit de traitement des demandes (SLA, preuve de réponse).
- Conservation & purge : définir des durées par finalité, automatiser la purge/anonymisation et bloquer les champs libres sans durée de rétention.
- Adhésion des équipes : pédagogie sur les risques, co-construction avec le métier, règles simples et visibles, formations courtes et suivi d’indicateurs.

## Livrables

- [Rapport d’analyse](./Rapport.pdf)
- [Recommandations RGPD](./Recommandations_RGPD.pdf)
