Projet HealthConnect — Track Data Analytics — Semaine 6

Programme : AnalystLab Africa — Experience Lab Internship Programme Semaine 6 : HealthConnect Integration, Advanced Development & Validation Track : Data Analytics Auteur : SEDOUFIO Kossi David

Où j'en étais après la Semaine 5

La Semaine 5 avait produit un premier rapport complet : nettoyage des données, exploration, cinq KPI calculés, et un dashboard Power BI avec un taux global de no-show de 48,46 %. Le résultat le plus marquant restait la combinaison entre délai de réservation et historique de no-show — sans que leur effet cumulé ait été précisément mesuré.

Cette semaine n'est pas une répétition de la précédente. L'objectif était d'approfondir ce qui méritait de l'être, de vérifier la fiabilité des chiffres, et de faire enfin une vraie collaboration inter-tracks plutôt que de simplement l'annoncer.

Ce que j'ai approfondi

J'ai croisé le délai de réservation, l'historique de no-show et la distance à la clinique deux par deux, avec un contrôle systématique des effectifs derrière chaque taux — pour ne pas se fier à des chiffres reposant sur seulement 1 ou 2 cas.

Résultat central : un rendez-vous pris à plus de 30 jours affiche 55,18 % de no-show même sans aucun antécédent (n ≈ 1 410). Le délai de réservation n'est donc pas juste un marqueur de patients déjà à risque, c'est un facteur indépendant.

Quand délai long et historique de récidive se combinent, l'effet grimpe à 72,96 % (n ≈ 233) — le segment le plus à risque identifié jusqu'ici. Certaines combinaisons affichent 100 % de no-show, mais reposent sur 1 à 4 cas seulement : pas assez pour être généralisées.

KPI validés et affinés
KPI	Résultat	Statut
Taux global de no-show	48,46 %	Confirmé stable
Taux par délai de réservation	55,18 % (+30j) même sans antécédent	Confirmé comme facteur indépendant
Taux de récidive	43,5 % à 68,8 % selon l'historique	Confirmé, s'accentue avec le délai
Taux par distance	46,5 % à 57,8 %	Effet réel mais secondaire
Segment à haut risque (nouveau)	72,96 % (délai +30j et 2+ antécédents)	Résultat le plus actionnable

(Détail complet dans /reports/Analyse_Avancee_Semaine6_HealthConnect.docx)

Dashboard mis à jour

Le dashboard de la Semaine 5 a été enrichi, pas reconstruit : une matrice croisée délai × historique, une carte KPI dédiée au segment à haut risque, et une note de prudence sur les combinaisons à faible effectif.

Intégration inter-tracks

Je n'ai pas encore de partenaire sur un autre track à ce stade du programme, alors j'ai simulé la perspective Data Science pour répondre à l'exigence d'intégration de cette semaine. J'ai transmis mes résultats validés (variables déterminantes, segment à haut risque, effectifs), puis, sous cette autre casquette, j'ai traduit ces résultats en recommandations concrètes de modélisation : quelles variables tester en priorité, comment traiter la variable cible, et un point d'attention repéré — la variable temps d'attente ne devrait pas servir dans un modèle prédictif, puisqu'elle n'est connue que le jour même du rendez-vous.

(Documentation complète des 7 points d'intégration dans le rapport principal)

Recommandations métier
Renforcer les rappels pour les rendez-vous réservés plus de 30 jours à l'avance
Mettre en place un suivi personnalisé pour le segment à haut risque
Ne pas fonder de décision sur les combinaisons à trop faible effectif
Ce que ça m'a fait travailler
Distinguer un vrai signal statistique d'un artefact de petit échantillon
Croiser plusieurs variables pour repérer un effet cumulatif
Traduire une analyse descriptive en recommandations de modélisation
Documenter une collaboration inter-tracks de façon rigoureuse et transparente
Structure du dossier Semaine 6
Semaine6/
├── README.md
└── reports/
    ├── Analyse_Avancee_Semaine6_HealthConnect.docx
    └── Resume_Projet_Semaine6_HealthConnect.doc
Pour la Semaine 7

Retester l'effet des rappels spécifiquement sur le segment à haut risque plutôt que sur l'ensemble des patients, et revalider ce segment si un volume de données plus large devient disponible.

Projet réalisé dans le cadre du Programme AnalystLab Africa Experience Lab #AnalystLabAfric
