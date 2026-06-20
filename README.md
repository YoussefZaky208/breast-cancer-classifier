# Breast Cancer Diagnostic Classifier

ML classification of breast tumors (malignant vs. benign) using SVM and K-NN with PCA.

## Overview
Built on the Wisconsin Diagnostic Breast Cancer dataset (569 samples, 30 features extracted 
from FNA cell images). Goal: accurately classify tumors to support clinical decision-making.

## Approach
- **Preprocessing:** StandardScaler normalization across all 30 features
- **Dimensionality reduction:** PCA — 10 components retaining 95.21% of variance (66.7% feature reduction)
- **Models:** SVM (Linear & RBF kernels), K-Nearest Neighbors (k=3,5,7)
- **Hyperparameter tuning:** Systematic C and gamma testing across multiple configurations

## Results

| Model | Accuracy | Precision | Recall |
|-------|----------|-----------|--------|
| SVM RBF (C=26, γ=0.01) | **97.37%** | **100%** | 92.86% |
| SVM Linear (C=2) + PCA | 97.37% | 100% | 92.86% |
| K-NN (k=5) | 95.61% | 97.44% | 90.48% |

Best model: **RBF SVM (C=26, γ=0.01)** — 97.37% accuracy, zero false positives.  
PCA reduced features by 66.7% while maintaining top accuracy and achieving ~3x training speed improvement.

## Files
- `Diagnostic_Breast_Cancer_Machine_Learning_Project.ipynb` — full implementation
- `Breast_Cancer_ML_Final_Report.pdf` — project report

## Dataset
[Diagnostic Breast Cancer Dataset — Kaggle](https://www.kaggle.com/datasets/ahmeduzaki/diagnostic-breast-cancer-dataset)
