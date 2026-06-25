# 📊 Analyse Économique et Statistique des Ventes — Librairie Lapage

## 📝 Présentation du Projet
Ce projet d'analyse de données est une mission complète d'**audit de performance commerciale** pour une librairie en ligne (Lapage), couvrant une période d'activité de 24 mois (de mars 2021 à février 2023). 

L'objectif principal a été de nettoyer les données de transactions, d'analyser les indicateurs clés (KPI) de l'entreprise, et de mener une analyse statistique inferentielle approfondie pour modéliser le comportement de la clientèle selon des critères démographiques (âge, genre).

**Statut du projet :** 🏁 Terminé et soutenu avec succès.

## 🎯 Principaux Résultats & Insights Métiers
* **Volume d'activité :** Un Chiffre d'Affaires total de **12,03 M€** analysé sur deux ans, marqué par une forte saisonnalité en fin d'année (octobre à décembre).
* **Concentration du CA (Analyse de Lorenz) :** La construction de la courbe de Lorenz et le calcul de l'indice de Gini ont révélé une forte concentration de la richesse induite par un profil de clientèle **B2B** (4 clients "outliers" majeurs : `c_1609`, `c_4958`, `c_6714` et `c_3454` représentant une part stratégique du CA).
* **Segmentation Produits :** Identification claire de 3 structures de prix distinctes via un test de Kruskal-Wallis (p-value < 2.2e-16), confirmant les catégories 0 (Entrée de gamme), 1 (Milieu de gamme) et 2 (Premium).
* **Corrélations Démographiques validées :**
  * **Genre vs Catégorie :** Rejet de l'hypothèse d'indépendance par un **test du Chi-deux** ($\chi^2 = 22.669$, p-value = 0.00001196). Il existe un lien statistiquement hautement significatif entre le genre du client et ses préférences de lecture.
  * **Âge vs Habitudes d'achat :** Les tests de corrélation de Spearman ont démontré que si l'âge n'influe pas sur le montant total dépensé, il est corrélé positivement avec la *fréquence d'achat* ($rho = 0.19$) et négativement avec la *taille du panier moyen* ($rho = -0.18$). Les clients plus âgés achètent plus souvent, mais par plus petits volumes unitaires.

## 🛠️ Stack Technique & Outils
L'intégralité du projet a été développée en **Langage R** pour garantir la reproductibilité de la démarche scientifique :
* **Data Manipulation :** `tidyverse` (`dplyr`, `tidyr`, `stringr`)
* **Data Visualization :** `ggplot2` (graphes de tendances, boîtes à moustaches, courbe de Lorenz)
* **Analyses Statistiques :** Packages natifs de R pour les tests d'hypothèses (`vcd` pour les analyses de contingence, tests de corrélation, Kruskal-Wallis).

## Données
Pour les fichiers trop lourds (transactions.csv, ventes.csv), j'ai utilisé des échantillons de 1000 lignes.

## 🚀 Méthodologie de Reproductibilité

1. **Cloner le projet :**
   ```bash
   git clone [https://github.com/ton-nom-utilisateur/analyse-ventes-lapage.git](https://github.com/ton-nom-utilisateur/analyse-ventes-lapage.git)
   cd analyse-ventes-lapage
