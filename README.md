# Toxicity Prediction Using Chemical Descriptors

![Python](https://img.shields.io/badge/Python-3.14-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.6-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📋 Project Overview

This project builds a machine learning model to predict whether a chemical compound is **Toxic** or **NonToxic** based on 1,203 molecular descriptors. The analysis includes comprehensive Exploratory Data Analysis (EDA), feature selection, cross-validation, and model comparison.

## 📊 Dataset

- **Source**: Chemical descriptors dataset
- **Samples**: 171 chemical compounds
- **Features**: 1,203 molecular descriptors
- **Target**: `Class` (Toxic/NonToxic)
- **Class Distribution**:
  - NonToxic: 115 samples (67.3%)
  - Toxic: 56 samples (32.7%)

![Class Distribution](outputs/class_distribution.png)

## 🔬 Methodology

### 1. Exploratory Data Analysis (EDA)
- Class distribution analysis
- Feature distributions visualization
- Correlation analysis of top features
- Data quality checks (missing values, constant features)

### 2. Preprocessing
- Removal of constant features
- Feature scaling using StandardScaler
- Train-test split (80-20 with stratification)

### 3. Feature Selection
- **ANOVA F-test** to select top 100 most significant features
- Feature importance ranking using Random Forest

### 4. Model Training
- **Algorithm**: Random Forest Classifier
- **Hyperparameters**:
  - n_estimators: 200
  - max_depth: 15
  - class_weight: 'balanced' (handles class imbalance)
  - random_state: 42

### 5. Validation
- **Cross-validation**: 5-fold stratified cross-validation
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, ROC-AUC

## 📈 Results

### Model Performance
| Metric | Score |
|--------|-------|
| Cross-validation ROC-AUC | 0.5544 (±0.1390) |
| Test Accuracy | 65.71% |
| Test ROC-AUC | 0.5795 |

### Classification Report
