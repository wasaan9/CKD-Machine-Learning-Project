# CKD-Machine-Learning-Project
# Machine Learning-Based Prediction and Classification of Chronic Kidney Disease

## Project Overview

This graduation project applies statistical and machine learning methods to predict and classify **Chronic Kidney Disease (CKD)** using clinical patient data.

The study uses a dataset of **400 patients and 25 clinical variables**. The data were cleaned and preprocessed before applying supervised and unsupervised learning techniques.

The main objective is to compare different classification algorithms, identify important clinical predictors of CKD, and explore hidden patient subgroups using clustering and dimensionality reduction techniques.

---

## 🎯 Research Objectives

The project aims to:

1. Classify patients as **CKD or Non-CKD** using:

   * Logistic Regression
   * Random Forest
   * XGBoost

2. Compare the performance of the three classification models using evaluation metrics.

3. Identify the clinical variables that are most strongly associated with CKD using Random Forest variable importance.

4. Explore hidden patient subgroups using:

   * K-Means Clustering
   * Principal Component Analysis (PCA)

---

## 📊 Dataset

The dataset contains **400 patient records** and **25 variables**, including 24 predictor variables and one target variable.

The variables include clinical measurements such as:

* Age
* Blood Pressure
* Specific Gravity
* Albumin
* Blood Glucose
* Blood Urea
* Serum Creatinine
* Sodium
* Potassium
* Hemoglobin
* Packed Cell Volume
* White Blood Cell Count
* Red Blood Cell Count
* Hypertension
* Diabetes Mellitus
* Appetite
* Anemia
* CKD Classification

The dataset was obtained from Kaggle and was originally collected from a hospital in Tamil Nadu, India.

---

##  Data Preprocessing

Several preprocessing steps were performed before model development:

* Removal of the ID column
* Cleaning categorical values
* Correction of incorrect target labels
* Conversion of variables stored as text into numeric format
* Median imputation for missing numeric values
* Mode imputation for missing categorical values
* Encoding categorical variables
* Stratified 70:30 train-test split
* Application of SMOTE to the training set to address class imbalance

SMOTE was applied only to the training data to prevent data leakage and ensure that the test set consisted of real, unseen patient records.

---

##  Machine Learning Models

### 1. Logistic Regression

Logistic Regression was used as a statistical classification method for predicting whether a patient belongs to the CKD or Non-CKD class.

### 2. Random Forest

Random Forest is an ensemble learning method based on multiple decision trees.

In addition to classification, Random Forest was used to identify the most important clinical variables through:

* Mean Decrease Gini
* Mean Decrease Accuracy

### 3. XGBoost

XGBoost is a boosting-based machine learning algorithm in which decision trees are built sequentially to improve previous predictions.

## The model was configured for binary classification using the `binary:logistic` objective.

##  Model Evaluation

The classification models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC Curve
* Area Under the Curve (AUC)
* Confusion Matrix

These metrics were used to compare the predictive performance of Logistic Regression, Random Forest, and XGBoost.

---

##  Clustering Analysis

K-Means clustering was used as an unsupervised learning technique to explore whether natural patient subgroups existed beyond the binary CKD/Non-CKD classification.

The optimal number of clusters was investigated using:

* Within-Cluster Sum of Squares (WCSS)
* Elbow Method
* Silhouette Score

The analysis identified a **three-cluster solution**, representing different patient patterns related to CKD status.

---

##  Principal Component Analysis (PCA)

Principal Component Analysis was applied to reduce the dimensionality of the continuous variables while preserving as much of the original variance as possible.

The resulting principal components were then used as inputs for K-Means clustering to investigate the underlying structure of the patient data.

---

##  Key Results

The three classification models achieved comparable performance on the test set, with each model reaching approximately **99.17% accuracy** and an **AUC above 0.99**.

The strongest predictors identified in the study included:

* Hemoglobin
* Packed Cell Volume
* Specific Gravity
* Serum Creatinine
* Albumin

The clustering analysis identified three patient groups corresponding broadly to:

1. CKD – Advanced Stage
2. CKD – Near-Normal Stage
3. Non-CKD – Healthy

The project also found that PCA supported the stability of the identified cluster structure.

---

##  Methods and Techniques

**Supervised Learning**

* Logistic Regression
* Random Forest
* XGBoost

**Unsupervised Learning**

* K-Means Clustering
* PCA

**Data Preprocessing**

* Missing Value Imputation
* Categorical Encoding
* Standardization
* SMOTE
* Train-Test Split

**Evaluation**

* Confusion Matrix
* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* WCSS
* Silhouette Score

---

##  Project Team

**Department of Statistics – Faculty of Sciences**
**King Abdulaziz University**

* Esraa Badweel — 2307126
* Balqess Alelg — 2311812
* Nourah Alnefaie — 2113389
* Wasan Alsamiri — 2209404

**Supervisor:**
Dr. Tahany Basir

**Summer Semester 1448 – 2026**

---

## Project Report

The complete graduation project report is available in this repository:

**[View the Full Project Report (PDF)](./FRM_Machine_Learning_Based_Prediction_and_Classification_of_chronic.pdf)**

---

## 📚 Topics Covered

`Machine Learning` · `Statistics` · `Data Analysis` · `Chronic Kidney Disease` · `Classification` · `Logistic Regression` · `Random Forest` · `XGBoost` · `K-Means` · `PCA` · `Data Preprocessing`

---

## ⚠️ Disclaimer

This project is an academic graduation project developed for statistical and machine learning analysis. The models presented in this study are not intended to replace professional medical diagnosis or clinical decision-making.
