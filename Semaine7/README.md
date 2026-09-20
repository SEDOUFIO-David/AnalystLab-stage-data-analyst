# Projet HealthConnect — Track Data Analytics — Semaine 7

**Programme :** AnalystLab Africa — Experience Lab Internship Programme
**Semaine 7 :** HealthConnect Testing, Refinement & End-to-End Validation
**Track :** Data Analytics
**Auteur :** SEDOUFIO Kossi David

---

## Où j'en étais après la Semaine 6

La Semaine 6 avait produit un rapport d'analyse avancée avec un résultat central : un segment de patients combinant un délai de réservation supérieur à 30 jours et au moins 2 antécédents de no-show affichait un taux de 72,96 % (n ≈ 233). La limite identifiée à l'époque concernait la fiabilité de certaines combinaisons reposant sur très peu de cas.

Cette semaine n'ajoute pas de nouvelle analyse depuis zéro. Elle vérifie que ce qui a été produit tient la route.

---

## Ce que j'ai testé

Quatre choses : l'exactitude du calcul du KPI principal, le bon fonctionnement des filtres du dashboard, la stabilité du segment à haut risque sous d'autres angles (âge, genre, canal de rappel), et la fiabilité des effectifs derrière chaque résultat.

---

## Ce que ça a donné

Le KPI de 72,96 % a été confirmé par une mesure de vérification indépendante et un calcul manuel — les trois méthodes donnent exactement le même résultat. Les filtres et le croisé-filtrage du dashboard fonctionnent correctement.

Le segment reste stable sur toutes les tranches d'âge (66,67 % à 76,27 %) et entre les genres (71,88 % à 74,81 %).

Un graphique s'est révélé défectueux : il croisait le KPI avec la variable de délai déjà utilisée pour le calculer, ce qui donnait la même valeur sur toutes les tranches. Une fois identifié, le problème venait d'un filtre interne de la mesure DAX qui écrasait celui du graphique. Le visuel a été retiré.

Le test le plus intéressant porte sur le canal de rappel, au sein du segment à risque uniquement :

| Canal | Taux de no-show | Effectif |
|---|---|---|
| WhatsApp | 68,85 % | 61 |
| Aucun rappel | 72,31 % | 65 |
| SMS | 74,70 % | 83 |
| Email | 79,17 % | 24 (à confirmer) |

WhatsApp ressort comme le canal le plus efficace pour cette population précise — un résultat qui n'était pas visible dans l'analyse générale de la Semaine 5, où l'effet des rappels semblait faible dans l'ensemble.

---

## Recommandations mises à jour

- Cibler le suivi personnalisé sur tout le segment à risque, sans distinction d'âge ou de genre
- Privilégier WhatsApp comme canal de rappel pour ce segment plutôt que le SMS actuellement dominant
- Rester prudent sur le résultat Email, basé sur un échantillon plus restreint

*(Détail complet dans `/reports/Test_Affinement_Semaine7_HealthConnect.docx`)*

---

## Collaboration inter-tracks

Le point d'intégration établi la semaine dernière avec une perspective Data Science a été revérifié. La variable d'interaction délai × historique reste justifiée. Une nouvelle piste s'ajoute : le canal de rappel, dont l'effet n'apparaît qu'une fois restreint au segment à risque, pourrait valoir la peine d'être testé comme variable candidate secondaire pour un futur modèle.

---

## Ce que ça m'a fait travailler

- Vérifier un résultat par plusieurs méthodes indépendantes plutôt que de lui faire confiance d'emblée
- Repérer une anomalie qui n'était pas visible au premier regard
- Distinguer un vrai effet d'un artefact de petit échantillon
- Affiner une recommandation générale en action précise et chiffrée

---

## Structure du dossier Semaine 7

```
Semaine7/
├── README.md
└── reports/
    ├── Test_Affinement_Semaine7_HealthConnect.docx
    └── Resume_Projet_Semaine7_HealthConnect.docx
```

---

## Liens

- Dossier Google Drive : *https://drive.google.com/drive/folders/1FbvcJUbiaTfHNpePHJ91y-cgUUGHDasJ?usp=sharing*
- Publication LinkedIn : *https://lnkd.in/p/d9dw_ppf*
- Publication X : *https://x.com/Davidsedoufio/status/2101731054759317601?s=20*
- Semaines précédentes : dossiers `/Semaine2`, `/Semaine3`, `/Semaine4`, `/Semaine5`, `/Semaine6` de ce dépôt

---

## Pour la Semaine 8

Confirmer si possible le résultat sur le canal Email avec un échantillon plus large, et préparer une synthèse regroupant l'ensemble des résultats validés depuis la Semaine 5 en vue de la présentation finale.

---

*Projet réalisé dans le cadre du Programme AnalystLab Africa Experience Lab #AnalystLabAfrica*
