# Detecting-Parkinsons-using-Vocal-Features
## 🩺 Overview

Parkinson’s Disease (PD) is a progressive neurological disorder that affects movement and speech. Subtle vocal changes often appear in the early stages of PD, which can be detected using machine learning. This project focuses on building a reliable diagnostic system that identifies PD from vocal biomarkers.

---

## 🔍 Problem Statement

**Can we build an accurate machine learning model that detects Parkinson’s Disease from voice samples?**

---

## 📂 Dataset

- **Source:** [Kaggle - Parkinson’s Disease Dataset](https://www.kaggle.com/)
- **Rows:** 195 samples
- **Features:** 23 vocal measurements + 1 target (`status`: `0 = healthy`, `1 = Parkinson’s`)
- **Key Features:** Jitter, Shimmer, MDVP frequency measures, HNR, NHR, PPE, D2, DFA

---

## 🧹 Data Preprocessing

- Dropped irrelevant columns (`name`)
- Converted `status` to binary `uint8`
- Checked for and handled missing values
- Applied **StandardScaler** to normalize all features
- Balanced dataset to avoid bias in classification

---

## 📊 Exploratory Data Analysis

- 🔸 **Boxplots** to visualize feature distributions
- 🔸 **Pairplots** to analyze feature relationships
- 🔸 **Heatmap** to identify highly correlated features
- 🔸 **Pie charts** to show data balance (healthy vs. Parkinson’s)

---

## ⚙️ Model Development

Trained and evaluated 3 classification models:

### ✅ Random Forest Classifier
- Ensemble of decision trees
- Handles non-linear relationships well
- High interpretability

### 🚀 Gradient Boosting Classifier
- Sequential ensemble of weak learners
- Robust to overfitting with hyperparameter tuning

### 🔎 Support Vector Classifier (SVC)
- Performs well on high-dimensional data
- Kernel trick used for non-linear classification

---

## 📈 Evaluation Metrics

- **Accuracy** – % of correct predictions  
- **F1 Score** – Balance between precision and recall  
- **Precision** – True positives out of predicted positives  
- **Recall** – True positives out of actual positives  
- **ROC AUC** – Area under the ROC curve  

---

## 🧪 Results

| Model             | Accuracy | F1 Score | Precision | Recall | ROC AUC |
|------------------|----------|----------|-----------|--------|---------|
| Random Forest     | ✅ High  | ✅ High  | ✅ High    | ✅ High| ✅ High |
| Gradient Boosting | ✅ High  | ✅ High  | ✅ High    | ✅ High| ✅ High |
| SVC               | Moderate| Moderate | Moderate  | Moderate| Moderate|

---

## 🔧 Model Deployment

- All models were saved using `joblib`
- Deployment-ready prediction functions are defined to use trained models on new input data
