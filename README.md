# A Comprehensive Analysis of Payment System Security

This project investigates threats and safeguards associated with credit card transactions using real-world data and machine learning techniques. It was developed as part of the CS559: Quantitative Security course at Colorado State University under the guidance of Prof. Yashwant K. Malaiya.

## 📌 Project Overview

As digital payments continue to grow, so do the risks of fraud and cyberattacks. This project presents a **data-driven framework for detecting credit card fraud** by combining:

- Risk-based authentication
- Adaptive security layers
- Machine learning classifiers
- Data balancing (SMOTE)

It also includes case study analyses of real-world payment breaches and proposes a layered detection framework inspired by the **NIST Cybersecurity Framework**.

## 🧪 Dataset

- Source: [Kaggle Credit Card Fraud Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- 285,000+ transactions
- PCA-transformed features (V1–V28)
- Highly imbalanced (fraud = 0.17%)

## 🧠 Machine Learning Models Used

| Algorithm              | Notebook |
|------------------------|----------|
| Logistic Regression    | `CCD-LogisticRegression.ipynb` |
| K-Nearest Neighbors    | `CCD-KNN.ipynb` |
| Random Forest (Over/Under) | `CCD-RandomForest-Oversampled.ipynb`, `CCD-RandomForest_UnderSampled.ipynb` |
| Decision Tree (Over/Under) | `CCD-DecisionTree-OverSampledData.ipynb`, `CCD-DecisionTree_UnderSampledData.ipynb` |
| Stochastic Gradient Descent (SGD) | `CCD-SGD.ipynb` |

### ✅ Oversampling Strategy:
- **SMOTE** (Synthetic Minority Oversampling Technique) used for balancing the minority class (fraud)

## 📊 Evaluation Metrics

The project prioritizes evaluation based on:
- **F1 Score**
- **AUC-ROC**
- Accuracy (for reference only, due to class imbalance)

### 📈 Results Summary (from `Results_Report.ipynb`)

| Model               | F1-Score | AUC-ROC | Accuracy |
|--------------------|----------|---------|----------|
| Logistic Regression| 0.843    | 0.947   | 0.998    |
| Random Forest       | 0.914    | 0.919   | 0.920    |
| KNN                 | 0.031    | 0.728   | 0.945    |
| SGD                 | 0.080    | 0.935   | 0.964    |

## 📄 Report

- `Analysis_of_payment_systems_credit_card_security_Final.pdf`: Full research report including introduction, literature review, case studies, framework, and results.
- Case studies included: **Capital One**, **British Airways**, **Target**, **Neiman Marcus**, **Interbank (Peru)**

## 🧩 Framework

Proposed a **layered ML fraud detection architecture** with:
- **Fraud Prevention Layer**
- **Fraud Detection Layer**
- **Policy Review Layer**
