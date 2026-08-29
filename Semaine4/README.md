# Projet HealthConnect — Track Data Analytics — Semaine 4

**Programme :** AnalystLab Africa — Experience Lab Internship Programme
**Semaine 4 :** HealthConnect Project Kickoff & Problem Understanding
**Track :** Data Analytics
**Auteur :** [SEDOUFIO Kossi David]

---

## Le contexte

À partir de la Semaine 4, tous les stagiaires du programme, quel que soit leur track, rejoignent un même projet : HealthConnect Clinic, une clinique fictive qui perd près d'un rendez-vous sur deux à cause d'absences non annoncées. Chaque track y contribue à sa façon. Le mien, c'est Data Analytics.



Question de départ : comment HealthConnect peut-elle utiliser les données et l'IA pour réduire les rendez-vous manqués et mieux accompagner ses patients ?

---

## Ce que j'avais à faire cette semaine

Comprendre les données de rendez-vous disponibles et repérer ce qui pourrait expliquer les no-shows, sans encore rien calculer ni visualiser. Une semaine de cadrage, pas d'exécution.

---

## Le jeu de données

**HealthConnect_Appointment_Data.csv** — 5000 rendez-vous fictifs et anonymisés, avec des infos sur les patients, les rendez-vous, l'historique de fréquentation, les rappels envoyés, la distance à la clinique, et le résultat final de chaque rendez-vous.

Documentation associée : **HealthConnect_Data_Dictionary** (explication de chaque variable).

---

## Ce qui ressort

Le taux global de no-show tourne autour de **48,5%**. Presque un rendez-vous sur deux.

Deux variables se détachent nettement des autres :

| Variable | Écart de taux de no-show observé |
|---|---|
| Délai de réservation (booking_lead_days) | 24,8% en dessous de 3 jours, jusqu'à 60,5 % au-delà de 30 jours |
| Historique de no-show (previous_no_shows) | 43,5% sans antécédent, jusqu'à 68,8% avec 3 no-shows ou plus |

La distance à la clinique joue aussi, mais de façon plus modérée. Et surprise : l'envoi d'un rappel ne change presque rien au taux d'absence dans ces données — contrairement à ce qu'on aurait pu croire.

---

## Les questions que je veux creuser

1. Quel est le taux global de rendez-vous manqués à la clinique ?
2. Le délai entre la prise de rendez-vous et le jour J joue-t-il sur le risque de no-show ?
3. Les patients ayant déjà manqué des rendez-vous sont-ils plus susceptibles de recommencer ?
4. La distance au domicile influence-t-elle l'assiduité ?
5. Un rappel fait-il vraiment baisser le taux de no-show, et un canal marche-t-il mieux qu'un autre ?

---

## KPI potentiels

- Taux global de no-show
- Taux de no-show par tranche de délai de réservation
- Taux de récidive de no-show
- Taux de no-show par tranche de distance
- Efficacité du rappel selon le canal utilisé

*(Détail complet dans `/reports/Document_Analyse_Initiale_Semaine4_HealthConnect.docx`)*

---

## Comment je compte m'y prendre

Power BI en outil principal, dans la continuité des semaines précédentes, avec Python en soutien pour des vérifications rapides. Je vais commencer par le délai de réservation et l'historique de no-show, puisque ce sont les deux facteurs qui pèsent le plus à ce stade.

---

## Ce que ça m'a fait travailler

- Lire et s'appuyer sur un dictionnaire de données
- Évaluer la qualité d'un jeu de données (valeurs manquantes, doublons, cohérence)
- Croiser des variables pour repérer des tendances
- Formuler des questions métier et des KPI justifiés, sans se précipiter sur les calculs

---

---

## Liens

- Dossier Google Drive : *[https://drive.google.com/drive/folders/10WjNvnApgpipBvjrFBIxy0idn0ebS4y7?usp=sharing]*
- Publication LinkedIn : *[https://lnkd.in/p/dETiU2JR]*
- Publication X : *[https://x.com/Davidsedoufio/status/2093651819528421788?s=20]*


---

## Pour la Semaine 5

Nettoyer les dernières valeurs manquantes, construire les KPI identifiés cette semaine, et commencer à visualiser ce qui relie délai de réservation, historique de no-show et taux d'absence.

---

*Projet réalisé dans le cadre du Programme AnalystLab Africa Experience Lab #AnalystLabAfrica*
