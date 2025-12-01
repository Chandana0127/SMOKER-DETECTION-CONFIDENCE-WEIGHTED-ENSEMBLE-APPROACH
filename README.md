# Smoker Detection from Bio-Signals Using Confidence-Weighted Ensemble Learning

A novel machine learning approach for predicting smoking status from health biomarkers using calibration-based ensemble weighting.

## Overview

This project addresses the binary classification problem of detecting smokers vs. non-smokers using routine health examination data. Our key innovation is weighting ensemble components by their **calibration quality** (ECE and Brier Score) rather than accuracy, ensuring models with more reliable probability estimates contribute proportionally more to predictions.

## Key Results

| Metric | Score |
|--------|-------|
| ROC-AUC | 0.8630 |
| Accuracy | 77.9% |
| ECE | 0.0114 |
| Brier Score | 0.1483 |

## Approach

- **Feature Engineering**: Expanded 22 original biomarkers to 73 features (body composition, lipid ratios, liver function indicators, cardiovascular markers)
- **Base Models**: XGBoost, LightGBM, CatBoost, TabNet, NODE
- **Ensemble Strategy**: Confidence-weighted aggregation based on calibration metrics
- **Class Balancing**: SMOTE for handling imbalanced data

## Dataset

Kaggle Playground Series S3E24 - 159,256 health records with 22 biomarker features including blood chemistry, body measurements, and vital signs.

## Repository Structure

```
├── SMOKER_DETECTION_CONFIDENCE_WEIGHTED_ENSEMBLE_APPROACH.ipynb
├── SMOKER_DETECTION_CONFIDENCE-WEIGHTED_ENSEMBLE_APPROACH.pdf
├── ConfusionMatrix.png
├── Roc.png
├── heatmap.png
├── Pipeline.png
└── README.md
```

## Usage

1. Open the notebook in Google Colab
2. Upload the dataset (Kaggle Playground Series S3E24)
3. Run all cells sequentially

## Requirements

```
pandas, numpy, scikit-learn, xgboost, lightgbm, catboost
pytorch-tabnet, torch, shap, imbalanced-learn, matplotlib, seaborn
```

## Team

| Member | Responsibilities |
|--------|-----------------|
| Chandana Vinay Kumar | Feature engineering, TabNet/NODE, SHAP analysis |
| Dileep Pabbathi | XGBoost/LightGBM, ensemble implementation |
| Ajay Bingi | CatBoost, calibration analysis, visualizations |
| Aarya Pendharkar | Data exploration and analysis |

**Arizona State University** - CSE 572 Data Mining

## License

MIT License
