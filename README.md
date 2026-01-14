# concert-enjoyment-classification
End-to-end deep learning project for ordinal classification of concert enjoyment ratings, including EDA, feature analysis, and model evaluation.

## Overview
This project focuses on predicting concert enjoyment levels based on audience, environmental, and contextual features.  
The task is formulated as an **ordinal classification problem**, where enjoyment ratings have a natural order.

## Problem Statement
Given features describing a concert experience, predict the level of enjoyment on an ordered scale (e.g., 1–4).

## Dataset
- Source: [link](https://www.kaggle.com/competitions/inf8245e-fall-2022/data)
- Target variable: Enjoyment rating (ordinal)
- Key challenges:
  - Class imbalance
  - Feature collinearity
  - Ordinal nature of the target

## Methodology
- Data preprocessing and exploratory analysis
- Feature scaling and selection
- Models evaluated:
  - Ordinal Ridge Regression (Mord)
  - SVM Ordinal classifiers for comparison
  - **Deep learning ordinal classifier using `OrdinalLogisticModel` from `spacecutter.models`**
- Hyperparameter tuning using cross-validation

## Evaluation Metrics
- Mean Absolute Error (MAE) — linear ordinal models
- Mean Squared Error (MSE) — linear ordinal models
- Quadratic Weighted Kappa (QWK) — linear ordinal models
- Classification report — deep learning model
- Confusion matrix with ordinal interpretation — deep learning model

## Results
- Ordinal models outperformed standard classification baselines
- Hyperparameter tuning did not significantly improve performance
- Feature collinearity impacted regression-based approaches

## Key Learnings
- Importance of choosing models aligned with the target structure
- Limitations of regression under high multicollinearity
- Proper evaluation of ordinal predictions

## Project structure
```text
notebooks/
├── 01_eda.ipynb
└── 03_test_evaluation.ipynb
src/
data/
