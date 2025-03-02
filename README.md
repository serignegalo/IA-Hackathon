# Prédiction des Prix des Maisons - Kaggle Competition

## Description du Projet

Ce projet vise à prédire les prix de vente de maisons en utilisant l'ensemble de données fourni par la compétition Kaggle "House Prices - Advanced Regression Techniques". L'objectif est d'appliquer des techniques de machine learning pour modéliser la relation entre les caractéristiques des maisons et leur prix de vente.

## Données Utilisées

Les données proviennent du dataset de l'Hackathon organise par la Zone01 et comprennent plusieurs caractéristiques des maisons, telles que :

* Alley : Type d'accès à l'allée

* MasVnrType : Type de parement en maçonnerie

* MasVnrArea : Surface du parement en maçonnerie (en pieds carrés)

* Et de nombreuses autres variables influençant le prix final.

## Prétraitement des Données

1. Gestion des valeurs manquantes : Suppression des colonnes avec trop de valeurs manquantes ou imputation par la mediane.

2. Encodage des variables catégorielles : Transformation en variables dummies.

3. Standardisation des données : Application de StandardScaler pour normaliser les features.

4. Transformation logarithmique : Application de log1p sur SalePrice pour stabiliser la distribution des prix.

## Modélisation

* Modèle Utilisé : Extreme Gradient Boosting Regressor(XGBRegressor)

* Feature Selection : Utilisation de l'importance des variables pour réduire le nombre de features.

* Entraînement & Prédiction :

    * Entraînement du modèle sur les données d'entraînement.

    * Prédiction des prix sur l'ensemble de test.

    * Transformation inverse avec expm1 pour retrouver les prix d'origine.

## Génération du Fichier de Soumission

Le fichier de soumission est généré sous le format suivant :

```Id,SalePrice
1461,169000.1
1462,187724.1233
1463,175221
...
```

Ce fichier est ensuite soumis sur la plateforme Kaggle pour l'évaluation.

## Exécution du Projet

* Prérequis

    * Python 3

    * Bibliothèques : pandas, numpy, scikit-learn, matplotlib, seaborn

* Instructions

*  Installation des dépendances

```pip install pandas numpy scikit-learn matplotlib seaborn```

*  Exécution du script principal

```python main.py```

*  Génération du fichier de soumission Le fichier sample_submission.csv est créé automatiquement après l'exécution du script.

Améliorations Possibles

Creation de nouvelles colonnes pour ameliorer la data

Optimisation des hyperparamètres du Random Forest.

Feature engineering avancé pour améliorer la précision du modèle.

****


Auteurs : [abdbalde, bakseck, gdiokhan]


