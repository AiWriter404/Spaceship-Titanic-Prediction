# 🚀 Spaceship Titanic - Prediction

Predicting which passengers were transported to an alternate dimension during the Spaceship Titanic's collision with a spacetime anomaly — a binary classification problem based on Kaggle's [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic) competition.

## 🏆 Result

**Public Leaderboard Score: 0.80360**

## 📊 Project Overview

This project implements a complete, end-to-end machine learning pipeline — from raw data exploration to a tuned, cross-validated model — following clean data science practices (no data leakage, train/test consistency, and reproducible results).

### Pipeline Summary

1. **Exploratory Data Analysis (EDA)**
   - Dataset structure, statistical summary, target distribution, data types, unique value counts

2. **Data Cleaning**
   - Missing value imputation (median for numerical, mode for categorical)
   - Consistent train → test imputation (using train statistics only, avoiding data leakage)

3. **Feature Engineering**
   - Split `Cabin` into `Deck`, `CabinNum`, and `Side`
   - Extracted `GroupSize` from `PassengerId` (passengers traveling together)
   - Created `TotalSpend` (sum of all amenity spending columns)
   - Dropped low-value columns (`Name`, original `Cabin`)

4. **Encoding**
   - Boolean columns (`CryoSleep`, `VIP`) converted to 0/1
   - One-hot encoding for categorical features (`HomePlanet`, `Destination`, `Deck`, `Side`)

5. **Modeling**
   - Baseline: Random Forest Classifier
   - Final Model: **Tuned XGBoost Classifier**
   - Validated using **5-fold Cross-Validation** for reliable performance estimation
   - Feature importance analysis to guide feature selection

6. **Submission**
   - Verified prediction format and class balance before submission

## 🛠️ Tech Stack

- **Python**
- **Pandas / NumPy** — data manipulation
- **Scikit-learn** — preprocessing, Random Forest, cross-validation
- **XGBoost** — final gradient boosting model

## 📁 Repository Structure

```
├── spaceship-titanic-prediction.ipynb   # Full notebook (EDA → Model → Submission)
├── submission.csv                        # Final Kaggle submission file
└── README.md
```

## 🔗 Links

- **Kaggle Notebook:** [Spaceship Titanic Prediction](https://www.kaggle.com/code/muhammadumer7804/spaceship-titanic-prediction?scriptVersionId=336629306)
- **Competition:** [Spaceship Titanic - Kaggle](https://www.kaggle.com/competitions/spaceship-titanic)

## 👤 Author

**Muhammad Umer**

---

*This project was built as a hands-on learning exercise in the end-to-end machine learning workflow: data cleaning, feature engineering, model comparison, and validation.*
