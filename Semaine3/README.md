Tableau de Bord Exécutif — Analyse Avancée & Business Intelligence — Global Superstore

Programme : AnalystLab Africa — Stage en Analyse de Données Semaine 3 : Analyse Avancée des Données, Développement de KPI et Tableau de Bord de Business Intelligence Auteur : SEDOUFIO Kossi David Outils utilisés : Microsoft Power BI, Power Query, DAX

  Contexte du projet

Ce projet prolonge le travail réalisé en Semaine 2 sur le jeu de données Global Superstore. L'objectif de la Semaine 3 est d'approfondir l'analyse de la performance commerciale de l'entreprise et de transformer ces résultats en un tableau de bord de Business Intelligence interactif et actionnable pour la direction.

Le projet s'appuie directement sur le fichier Power BI de la Semaine 2, enrichi de nouvelles pages, mesures DAX et analyses.

 Jeu de données

Global Superstore Dataset — environ 51 000 commandes réparties sur 4 ans (2011-2014), couvrant 147 pays, 7 marchés et 3 segments de clientèle (Consumer, Corporate, Home Office).

Source : Kaggle — Global Superstore Dataset


  Indicateurs clés (KPI)
Indicateur	Valeur
Ventes Totales	12,64M
Profit Total	1,47M
Marge Bénéficiaire	11,61%
Nombre de Commandes	25,04K
Vente Moyenne/Commande	505
Remise Moyenne	14,29%
Sous-Catégories à Perte	1
  Mesures DAX principales

Le modèle inclut 10 mesures DAX, parmi lesquelles :

Marge Bénéficiaire — DIVIDE([Profit Total],[Ventes Totales])
Croissance Ventes YoY — basée sur SAMEPERIODLASTYEAR, via une table de calendrier dédiée
Sous-Categories a Perte — identifie les sous-catégories dont le profit cumulé est négatif
Remise Moyenne — AVERAGE([Discount])

(Documentation complète dans /reports/Documentation_Mesures_DAX_Semaine3.docx)

   Analyse avancée — 6 axes couverts
Performance des ventes — tendances mensuelles et trimestrielles (Trimestre 2 en tête, Trimestre 1 en retrait)
Rentabilité — marge par catégorie, sous-catégorie et marché (Technology la plus rentable, Tables la seule en perte)
Performance des produits — produits les plus/moins rentables, ratio ventes/profit
Performance régionale — Central domine largement en profit, forte disparité entre régions
Clients et segments — Consumer génère 51,4% du chiffre d'affaires ; certains clients à profit négatif identifiés
Remises — la rentabilité devient négative au-delà de 30% de remise

(Détail complet dans /reports/Document_Analyse_Avancee_Semaine3.docx)

  Problèmes métier identifiés
Impact critique des remises élevées sur la rentabilité (seuil de 30%)
La sous-catégorie Tables génère des pertes nettes
Sous-performance systématique du Trimestre 1
Forte concentration géographique de la performance (région Central)
Certains clients génèrent un profit négatif
  Recommandations clés
Plafonner les remises commerciales à 20% maximum
Auditer la structure de coût/prix de la sous-catégorie Tables
Répliquer le modèle de succès de la région Central dans les régions faibles
Lancer des actions commerciales ciblées en début d'année (Trimestre 1)
Mettre en place un suivi de rentabilité par client

(Détail complet dans /reports/Rapport_Analyses_Recommandations_Semaine3.docx)

  Compétences développées
Modélisation de données avec table de calendrier et relations
Création de mesures DAX avancées (intelligence temporelle, filtres contextuels)
Analyse multi-dimensionnelle (temporelle, produit, région, client, remise)
Conception de tableaux de bord interactifs multi-pages avec slicers
Rédaction de rapports d'analyse et de recommandations pour la direction


Projet réalisé dans le cadre du Programme de Stage en Analyse de Données #AnalystLabAfrica
