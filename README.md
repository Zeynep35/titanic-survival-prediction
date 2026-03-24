# Titanic Survival Prediction

This project is an ongoing end-to-end data science study based on the Titanic dataset. 
The objective is to analyze passenger data, apply preprocessing and feature engineering techniques, and build classification models to predict survival.

Currently, the project focuses on exploratory data analysis (EDA) and understanding the dataset. 
Further steps such as feature engineering, model building, and evaluation will be implemented progressively.

This project is part of a learning process aimed at building a strong foundation in data science and machine learning.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn








# 🚢 Titanic Survival Prediction (Machine Learning Project)

## 📌 Project Overview

This project aims to predict whether a passenger survived the Titanic disaster using machine learning techniques. The goal is not only to build a predictive model, but also to understand model behavior and improve performance through feature engineering and threshold optimization.

---

## 🧠 Problem Type

* Binary Classification
* Target Variable: `Survived` (0 = No, 1 = Yes)

---

## ⚙️ Workflow

### 1. Data Preprocessing

* Handled missing values
* Encoded categorical variables:

  * `Sex` → Binary Encoding
  * `Embarked` → One-Hot Encoding
* Cleaned and prepared dataset for modeling

---

### 2. Feature Engineering

Created new features to improve model performance:

* `FamilySize` = SibSp + Parch + 1
* `IsAlone` = Whether the passenger is alone
* `FarePerPerson` = Fare / FamilySize
* `Sex_Pclass` = Interaction between gender and class

---

### 3. Model Selection

Tested multiple models:

* Logistic Regression
* Decision Tree
* Random Forest

📌 **Random Forest** was selected due to better overall performance and stability.

---

### 4. Model Evaluation

Used multiple evaluation metrics:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

---

### 5. Error Analysis (Key Step)

Analyzed misclassified samples to understand:

* Where the model struggles
* Which passenger groups are harder to predict

---

### 6. Model Optimization

#### 🔧 Hyperparameter Tuning

Optimized Random Forest parameters:

* `max_depth = 5`
* `n_estimators = 100`

#### 🎯 Threshold Tuning (Important)

Instead of using the default threshold (0.5), adjusted to:

```
threshold = 0.35
```

✔ This improved **recall**
✔ Reduced **false negatives** (missed survivors)

---

### 7. Feature Importance Analysis

Examined which features influenced the model most:

* `Title`, `Sex`, `Pclass`, `Fare` were most important

---

## 📊 Final Results

* Accuracy: ~0.82
* Recall (Survived): ~0.80
* Balanced performance between precision and recall

📌 Focus was on reducing **false negatives** (i.e., predicting survivors correctly)

---

## 🔥 Key Insights

* Feature engineering had a strong impact on performance
* Title (social status) is a highly informative feature
* Adjusting the classification threshold significantly improved recall
* Model performance depends not only on algorithms, but also on data representation

---

## 🚀 What I Learned

* Importance of feature engineering in ML pipelines
* Difference between model performance and model behavior
* How to interpret confusion matrix and classification metrics
* How to tune threshold based on business objective
* Why evaluation strategy matters more than model choice

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

---

## 📌 Conclusion

This project demonstrates a complete machine learning workflow, from data preprocessing to model optimization and interpretation. Instead of relying on default settings, the model was improved through careful analysis and decision-making.

---

## 📎 Future Improvements

* Try Gradient Boosting / XGBoost
* Perform cross-validation
* More advanced feature engineering
* Hyperparameter tuning with larger search space

---
