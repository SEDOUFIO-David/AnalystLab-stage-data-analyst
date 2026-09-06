#  HealthConnect Clinic — Data Analytics | Week 5

> Analyse des rendez-vous médicaux et identification des facteurs associés aux No-Shows

---

##  Présentation du projet

**HealthConnect Clinic** est un projet d'analyse de données visant à mieux comprendre les comportements liés aux rendez-vous médicaux non honorés (*No-Shows*).

L'objectif de cette analyse est de transformer les données de rendez-vous en **insights exploitables** afin d'aider la clinique à :

- réduire le taux de No-Show ;
- identifier les profils de rendez-vous nécessitant une attention particulière ;
- améliorer la stratégie de rappel des patients ;
- optimiser l'utilisation des créneaux de consultation ;
- soutenir la prise de décision à partir des données.

Ce projet correspond aux travaux réalisés durant la **Semaine 5 du HealthConnect Experience Lab — Data Analytics Track**.

---

##  Objectifs de la Semaine 5

Les principaux objectifs de cette phase étaient de :

1. Préparer et contrôler la qualité des données ;
2. Réaliser une analyse exploratoire des rendez-vous ;
3. Identifier les principaux facteurs associés aux No-Shows ;
4. Développer des KPI pertinents ;
5. Construire un dashboard interactif avec Power BI ;
6. Formuler des insights orientés métier ;
7. Proposer des recommandations opérationnelles ;
8. Préparer les prochaines étapes du projet.

---

##  Dataset

Le dataset contient **5 000 rendez-vous** et **18 variables**.

Chaque ligne représente un rendez-vous médical.

### Principales variables

| Variable | Description |
|---|---|
| `appointment_id` | Identifiant unique du rendez-vous |
| `patient_id` | Identifiant du patient |
| `gender` | Genre du patient |
| `age` | Âge du patient |
| `age_group` | Groupe d'âge |
| `appointment_type` | Type de rendez-vous |
| `booking_date` | Date de réservation |
| `appointment_date` | Date du rendez-vous |
| `appointment_day` | Jour du rendez-vous |
| `appointment_time` | Période de la journée |
| `booking_lead_days` | Nombre de jours entre réservation et rendez-vous |
| `previous_appointments` | Nombre de rendez-vous précédents |
| `previous_no_shows` | Nombre de No-Shows précédents |
| `reminder_sent` | Indique si un rappel a été envoyé |
| `reminder_channel` | Canal utilisé pour le rappel |
| `distance_to_clinic_km` | Distance entre le patient et la clinique |
| `waiting_time_minutes` | Temps d'attente |
| `appointment_outcome` | Résultat du rendez-vous |

---

##  Préparation et qualité des données

Un audit initial des données a été réalisé avant l'analyse.

Les contrôles effectués comprennent notamment :

- vérification des types de données ;
- recherche des doublons ;
- contrôle de l'unicité des identifiants ;
- vérification de la cohérence des dates ;
- contrôle de la cohérence du délai de réservation ;
- analyse des valeurs manquantes ;
- vérification de la cohérence entre les variables comportementales.

### Résultats principaux

- **5 000 lignes analysées**
- **18 variables**
- Aucun doublon complet identifié
- Aucun doublon sur `appointment_id`
- Les dates de réservation et de rendez-vous sont cohérentes
- `booking_lead_days` est cohérent avec la différence entre les deux dates

### Valeurs manquantes

| Variable | Valeurs manquantes |
|---|---:|
| `reminder_channel` | 1 366 |
| `distance_to_clinic_km` | 90 |
| `waiting_time_minutes` | 60 |

Les valeurs manquantes ont été traitées séparément lors de la préparation des données.

Pour `reminder_channel`, l'absence de valeur correspond aux rendez-vous pour lesquels aucun rappel n'a été envoyé et a donc été représentée par **« Aucun »**.

Pour la distance et le temps d'attente, une imputation par la médiane a été utilisée.

> Le mécanisme statistique des valeurs manquantes n'a pas été formellement établi ; aucune hypothèse de type MCAR/MAR/MNAR n'est donc retenue sans test complémentaire.

---

##  Analyse exploratoire

L'analyse exploratoire a porté principalement sur les facteurs susceptibles d'être associés au comportement de présence.

Les variables étudiées comprennent notamment :

- le délai de réservation ;
- l'historique des No-Shows ;
- la distance par rapport à la clinique ;
- les rappels ;
- le canal de rappel ;
- le type de rendez-vous ;
- l'âge ;
- le jour et la période du rendez-vous.

---

##  KPI principaux

### Taux global de No-Show

Sur les **5 000 rendez-vous**, **2 423** sont des No-Shows.

**Taux global de No-Show : 48,46 %**

### Délai de réservation

| Délai de réservation | Taux de No-Show |
|---|---:|
| 0–7 jours | 27,81 % |
| 8–14 jours | 33,55 % |
| 15–30 jours | 43,21 % |
| >30 jours | 60,49 % |

### Historique de No-Show

| No-Shows précédents | Taux de No-Show |
|---|---:|
| 0 | 43,51 % |
| 1 | 53,49 % |
| 2 | 59,36 % |
| 3+ | 68,82 % |

### Distance

| Distance | Taux de No-Show |
|---|---:|
| ≤5 km | 46,45 % |
| 5–10 km | 46,51 % |
| 10–20 km | 49,43 % |
| >20 km | 57,76 % |

### Rappels

| Statut / canal | Taux de No-Show |
|---|---:|
| Aucun rappel | 51,39 % |
| Rappel envoyé | 47,36 % |
| Email | 48,41 % |
| SMS | 45,75 % |
| WhatsApp | 49,77 % |

---

##  Principaux insights

L'analyse met principalement en évidence les tendances suivantes :

### 1. Le délai de réservation est fortement associé au No-Show

Les rendez-vous réservés plus de 30 jours à l'avance présentent un taux de No-Show de **60,49 %**, contre **27,81 %** pour ceux réservés dans les 7 jours.

### 2. Les No-Shows précédents constituent un signal important

Le taux de No-Show augmente avec le nombre de No-Shows précédents, passant de **43,51 %** pour les patients sans No-Show antérieur à **68,82 %** pour ceux ayant au moins 3 No-Shows précédents.

### 3. La distance présente une association modérée

Les patients vivant à plus de 20 km de la clinique présentent un taux observé de No-Show de **57,76 %**.

### 4. Les résultats diffèrent selon le canal de rappel

Le SMS présente le taux de No-Show observé le plus faible parmi les canaux analysés, avec **45,75 %**.

Cette observation doit toutefois être interprétée avec prudence : elle ne permet pas d'affirmer que le SMS cause une meilleure présence.

### 5. Les facteurs peuvent se combiner

Le croisement de plusieurs variables, notamment le délai de réservation et l'historique de No-Show, permet d'identifier des segments présentant des taux de No-Show particulièrement élevés.

Cette approche suggère l'intérêt d'une **segmentation des rendez-vous selon plusieurs facteurs de risque**.

---

##  Recommandations métier

À partir des résultats obtenus, cinq axes d'action ont été proposés :

### 1. Renforcer les rappels pour les rendez-vous >30 jours

Mettre en place un parcours de rappel spécifique pour les rendez-vous réservés longtemps à l'avance.

### 2. Mettre en place un suivi personnalisé des patients avec des No-Shows répétés

Identifier les patients ayant plusieurs No-Shows antérieurs et renforcer la confirmation de leurs prochains rendez-vous.

### 3. Porter une attention particulière aux patients vivant à plus de 20 km

Étudier les éventuelles barrières liées à la distance et proposer, lorsque cela est possible, des solutions adaptées.

### 4. Tester et optimiser les canaux de rappel

Comparer les performances des différents canaux dans des conditions comparables afin d'identifier la stratégie de communication la plus efficace.

### 5. Développer une segmentation des rendez-vous à risque

Combiner plusieurs facteurs tels que le délai de réservation, l'historique de No-Show et la distance afin de mieux prioriser les interventions.

---

##  Dashboard

Le dashboard a été développé avec **Microsoft Power BI** afin de permettre une lecture synthétique des principaux indicateurs et tendances.

Il permet notamment d'explorer :

- le taux global de No-Show ;
- la distribution des résultats des rendez-vous ;
- le comportement selon le délai de réservation ;
- l'historique des No-Shows ;
- la distance par rapport à la clinique ;
- les performances observées des rappels ;
- différents segments démographiques et opérationnels.

---

##  Outils utilisés

### Data Preparation
- Microsoft Power Query
- Excel / CSV

### Data Analysis
- Analyse exploratoire
- Agrégations et segmentation
- Analyse comparative

### Data Visualization
- Microsoft Power BI

### Calcul des KPI
- DAX

### Documentation
- Markdown
- Git / GitHub

---

##  Structure du projet

```text
HealthConnect-Clinic/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── HealthConnect_Appointment_Data.csv
│   │
│   └── processed/
│       └── HealthConnect_Appointment_Data_Cleaned.csv
│
├── documentation/
│   ├── Week_5_Analytical_Technical_Documentation.pdf
│   └── Week_5_Recommendations.pdf
│
├── powerbi/
│   └── HealthConnect_Clinic_Dashboard.pbix
│
├── analysis/
│   └── EDA/
│
└── screenshots/
    └── dashboard.png
