# Projet HealthConnect — Track Data Analytics — Semaine 8 (Livraison finale)

**Programme :** AnalystLab Africa — Experience Lab Internship Programme
**Semaine 8 :** HealthConnect Final Integration & Presentation
**Track :** Data Analytics
**Auteur :** SEDOUFIO Kossi David 

---

## Où j'en étais après la Semaine 7

La Semaine 7 avait validé le résultat central du projet : un segment de patients combinant un délai de réservation supérieur à 30 jours et au moins 2 antécédents de no-show affiche un taux de 72,96 %, contre 48,46 % en moyenne. Ce chiffre avait été confirmé par triple vérification, testé sur l'âge et le genre, et affiné avec une découverte sur le canal de rappel : WhatsApp réduit le risque plus efficacement que le SMS au sein de ce segment précis.

Cette dernière semaine consolide tout ce travail en un livrable final, sans reprendre l'analyse à zéro.

---

## Le résultat en une phrase

HealthConnect Clinic perd près d'un rendez-vous sur deux à cause d'absences non annoncées. Un sous-groupe précis, représentant environ 5 % des rendez-vous, concentre un risque d'absence une fois et demie supérieur à la moyenne — et ce sous-groupe est identifiable dès la prise de rendez-vous, avant même que le rendez-vous n'ait lieu.

---

## KPI finaux

| KPI | Valeur |
|---|---|
| Taux global de no-show | 48,46 % |
| Taux du segment à haut risque | 72,96 % (n ≈ 233) |
| Taux par délai de réservation | 24,8 % à 60,5 % |
| Taux de récidive par historique | 43,5 % à 68,8 % |
| Taux par distance à la clinique | 46,5 % à 57,8 % |
| Taux du segment à risque par canal de rappel | 68,85 % (WhatsApp) à 79,17 % (Email) |

---

## Recommandations finales

- Signaler automatiquement les rendez-vous à haut risque dès leur réservation (délai + historique)
- Privilégier WhatsApp comme canal de rappel pour ce segment précis, plutôt que le SMS actuellement utilisé par défaut
- Proposer des créneaux plus rapprochés en priorité pour les patients à historique de récidive connu, quand la disponibilité le permet
- Confirmer le résultat sur le canal Email avant généralisation, son échantillon restant limité (24 cas)
- Garder un ciblage simple : le segment reste stable sur tous les âges et les deux genres, pas besoin de complexifier par sous-groupe démographique

---

## Limites

- Le résultat sur le canal Email repose sur un échantillon restreint (24 cas)
- Les résultats mesurent des associations, pas des relations de cause à effet
- Le dataset est fictif et anonymisé ; une validation sur des données réelles serait nécessaire avant tout déploiement
- Aucun partenaire n'était assigné au track Data Science à ce stade du programme, ce qui n'a pas permis de réaliser la collaboration inter-tracks prévue par le devoir
- D'autres seuils de délai que 30 jours (par exemple 15 ou 20 jours) n'ont pas été testés

*(Détail complet dans `/reports/`)*

---

## Le dashboard

Le dashboard Power BI final comprend une page de garde avec les chiffres clés, une vue d'ensemble, une page dédiée au segment à haut risque, et les visualisations validées lors des tests de la Semaine 7. Le graphique défectueux identifié cette semaine-là (croisement erroné avec la variable de délai) a été retiré.

---

## Vidéo de présentation

Une vidéo individuelle de 5 à 10 minutes couvre : la contribution du track Data Analytics, l'absence de collaboration inter-tracks à ce stade, les tests et affinements réalisés, et la façon dont ces résultats soutiennent les décisions de HealthConnect.

---

## Ce que ce projet m'a fait travailler, semaine après semaine

- Identifier des variables pertinentes à partir d'un dictionnaire de données
- Construire et croiser des KPI dans Power BI et DAX
- Valider un résultat par plusieurs méthodes indépendantes avant de lui faire confiance
- Distinguer un vrai effet d'un artefact de petit échantillon
- Transformer une observation générale en recommandation précise et actionnable
- Documenter un travail de façon honnête, limites comprises

---

## Structure du dossier Semaine 8

```
Semaine8/
├── README.md
├── dashboard/
│   └── healthconnect_final.pbix
├── video/
│   └── presentation_semaine8.mp4
└── reports/
    ├── Package_Final_Semaine8_HealthConnect.docx
    └── Resume_Executif_HealthConnect.docx
```

---

## Liens

- Dossier Google Drive : https://drive.google.com/drive/folders/1YRSTY1iROykudm0JY3m55D2jETFuSyqv?usp=sharing
- Publication LinkedIn : https://lnkd.in/p/dJQ3gMmQ
- Publication X : https://x.com/Davidsedoufio/status/2104337082843898305?s=20
- Semaines précédentes : dossiers `/Semaine2` à `/Semaine7` de ce dépôt

---

*Projet réalisé dans le cadre du Programme AnalystLab Africa Experience Lab #AnalystLabAfrica*
