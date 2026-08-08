# Analyse du désabonnement client (Customer Churn) — Telco

Projet réalisé dans le cadre du programme d'internat en Data Analytics d'**AnalystLab Africa** (Semaine 1 — Business Analytics Case Study).

## Contexte

ABC Communications Ltd, opérateur télécom fictif, cherche à comprendre pourquoi une partie de ses clients résilient leur abonnement (churn) afin de mettre en place des stratégies de rétention ciblées. Ce projet analyse le comportement de 7 043 clients pour identifier les facteurs de résiliation et formuler des recommandations business.

## Dataset

- **Source** : [Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Volume** : 7 043 clients, 21 variables
- **Variable cible** : `Churn` (Yes/No) — 26,5 % de résiliation

## Méthodologie

1. Chargement et inspection des données (dimensions, types, valeurs manquantes, doublons)
2. Nettoyage : conversion de `TotalCharges` en numérique, imputation de 11 valeurs manquantes (clients à ancienneté nulle)
3. Analyse exploratoire par question business, avec visualisations (barres, histogrammes, boxplots, heatmap de corrélation)
4. Synthèse des facteurs de risque et recommandations

## Principaux résultats

| Facteur | Observation | Corrélation avec le churn |
|---|---|---|
| Type de contrat | 42,7 % (mensuel) vs 2,8 % (2 ans) | -0,40 |
| Ancienneté | Médiane 10 mois (résiliés) vs 38 mois (fidèles) | -0,35 |
| Service Internet | Fibre optique : 41,9 % vs DSL : 19 % | +0,31 |
| Services complémentaires | Sans sécurité en ligne : 41,8 % vs avec : 14,6 % | -0,17 |
| Mode de paiement | Chèque électronique : 45,3 % vs prélèvement auto : 15,2 % | — |

**Constat clé** : aucune variable seule n'explique le churn. C'est la combinaison de plusieurs signaux (contrat court, faible ancienneté, fibre optique, peu de services complémentaires, paiement manuel) qui permet d'identifier un client à risque.

## Recommandations

1. Encourager la migration vers des contrats engageants (remises, mois offerts)
2. Renforcer l'onboarding des nouveaux clients (0–12 mois)
3. Auditer l'expérience fibre optique (qualité, prix, satisfaction)
4. Packager les services de rétention (sécurité, support technique) dans les offres d'entrée
5. Simplifier les paiements en incitant au prélèvement automatique
6. Construire un scoring de risque de désabonnement combinant les facteurs identifiés
7. Suivre un tableau de bord mensuel du churn par segment

## Contenu du dépôt

- `Analyse_churn_Week1.ipynb` — Notebook complet (inspection, nettoyage, analyse, visualisations, recommandations)
- `README.md` — Ce fichier

## Outils utilisés

Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## Auteur

Projet réalisé par SEDOUFIO Kossi Davi dans le cadre du programme AnalystLab Africa — Data Analytics Internship.

`#AnalystLabAfrica`
