# 🏠 House Prices Prediction (Ames, Iowa)

Ce projet vise à prédire le prix de vente de maisons à Ames (Iowa) à partir de caractéristiques disponibles dans un jeu de données fourni par Kaggle.

> 🎯 Objectif : construire un modèle de machine learning performant pour estimer les `SalePrice` à partir des variables d’entrée (`train.csv`) et soumettre les prédictions sur `test.csv`.

---

## 📁 Structure du projet

```
house-prices-prediction/
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── data_description.txt
├── 01_exploration.ipynb
├── 02_preprocessing.ipynb
├── 03_modelisation.ipynb
├── 03_modelisation_avancee.ipynb
├── 04_prediction.ipynb
├── 05_optimisation.ipynb
├── 06_prediction_optimisee.ipynb
├── submission_optimisee.csv
└── README.md
```

---

## 🔍 Jeu de données

- Données disponibles sur Kaggle :  
  👉 [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

- 79 variables d’entrée : surface, qualité des matériaux, année de construction, nombre de pièces, etc.

---

## 🧪 Méthodologie

1. **Exploration des données** : détection des valeurs manquantes, distributions, corrélations.
2. **Prétraitement** :
   - Imputation des valeurs manquantes
   - Encodage One-Hot des variables catégorielles
3. **Modélisation** :
   - Régression Linéaire
   - Random Forest
   - Gradient Boosting
   - XGBoost
4. **Optimisation** :
   - `GridSearchCV` sur Gradient Boosting et XGBoost
   - Validation croisée (5-fold) avec RMSE
5. **Prédiction finale** :
   - Modèle final entraîné sur 100 % des données avec les meilleurs hyperparamètres
   - Prédictions enregistrées dans `submission_optimisee.csv`

---

## 📈 Résultats

| Modèle                 | RMSE (validation croisée) |
|------------------------|----------------------------|
| Régression Linéaire    | 31 001                     |
| Random Forest          | 29 050                     |
| Gradient Boosting      | **25 685** ✅               |
| XGBoost                | 25 767                     |

---

## 📤 Fichier de soumission

Le fichier final `submission_optimisee.csv` respecte le format demandé par Kaggle :

```csv
Id,SalePrice
1461,169277.6
1462,187000.0
...
```

---

## 🛠️ Stack technique

- Python, Pandas, Numpy
- Scikit-learn, XGBoost, LightGBM
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 💡 À venir (améliorations possibles)

- Transformation `log(SalePrice)` pour optimiser le score Kaggle
- Feature Engineering avancé
- Stacking ou blending de modèles

---

## ✍️ Autrice

👤 **Florence Josse**  
📎 [Profil LinkedIn](https://www.linkedin.com/in/florence-josse-94875ab3/)

---

## 📌 Remerciements

Merci à la communauté Kaggle pour la mise à disposition du dataset et des notebooks inspirants.


