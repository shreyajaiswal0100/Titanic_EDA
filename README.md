# 🚢 Titanic Dataset — Exploratory Data Analysis (EDA)

> *"Survival on the Titanic was not random — it was systematically structured by gender, wealth, age, and social position."*

---

## 📌 Project Overview

This notebook performs a comprehensive, end-to-end **Exploratory Data Analysis** on the Titanic dataset to uncover the key factors that influenced passenger survival. It covers feature engineering, univariate, bivariate, and multivariate analysis, missing value treatment, and outlier handling — with a written conclusion after every chart and every section.

---

## 📂 Notebook Structure

| Section | Description |
|---------|-------------|
| 📋 **EDA Report** | Shape, dtypes, missing values, duplicates, statistical summary |
| ⚙️ **Feature Engineering** | 8 new features: FamilySize, FamilyType, AgeGroup, FarePerPerson, NameTitle, Surname, FamilyGroup, TicketGroupSize |
| 📊 **Univariate Analysis** | Distribution of Family Type, Family Size, Age Group, Ticket Group Size |
| 🔗 **Bivariate Analysis** | Survival vs Family Size/Type, Age Group, Ticket Group, Top Surnames |
| 🌐 **Multivariate Analysis** | Sex + Class + Embarked interactions, Pairplot, Survival Heatmap |
| 🧹 **Data Cleaning** | Mean vs Median vs Random Fill comparison for Age imputation |
| 📦 **Outlier Treatment** | Custom IQR-based clipping for Fare column |

---

## 🔑 Key Findings

| Factor | Insight |
|--------|---------|
| **Gender** | Strongest predictor — females survived at ~74% vs ~19% for males |
| **Passenger Class** | 1st class: ~63% survival → 3rd class: ~24% — wealth = lifeboat access |
| **Age** | Infants & children were prioritized; seniors had the lowest survival odds |
| **Family Size** | Size 2–4 = best survival ("sweet spot"); solo travelers & large families fared worst |
| **Fare** | Higher fare = higher class = better ship placement & lifeboat access |
| **Embarkation** | Cherbourg (C) passengers survived best — proxy for 1st class composition |

---

## 👤 Survival Profiles

| Profile | Survival Odds |
|---------|--------------|
| 1st-class female, small family, Cherbourg | 🟢 ~95% |
| 2nd-class female | 🟢 ~75% |
| 1st-class male | 🟡 ~37% |
| 3rd-class female, solo | 🟡 ~40% |
| 2nd-class male | 🔴 ~17% |
| 3rd-class male, solo traveler | 🔴 ~10% |

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-EDA-green?logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plots-red)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-yellow?logo=jupyter)
![NumPy](https://img.shields.io/badge/NumPy-Arrays-lightblue?logo=numpy)

---

## 📁 Dataset

- **Source:** [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic)
- **Files used:** `train.csv`, `test.csv`
- **Train shape:** 891 rows × 12 columns
- **Survival rate:** ~38.4% survived

---
```

> **Note:** Download `train.csv` and `test.csv` from [Kaggle](https://www.kaggle.com/c/titanic/data) and place them in the same folder.

---

## 📌 Features Used for Modeling (Recommended)

Based on this EDA, the best features for a survival prediction model:

```
Sex, Pclass, Age, FamilySize, FamilyType,
FarePerPerson, Embarked, NameTitle, TicketGroupSize
```
