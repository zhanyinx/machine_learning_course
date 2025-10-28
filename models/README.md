# Models Directory

This directory stores trained machine learning models and model artifacts.

## Contents

- Serialized model files (.pkl, .joblib, .h5)
- Model configurations and hyperparameters
- Feature importance rankings
- Model performance metrics

## File Naming Convention

- `{algorithm}_{date}_{version}.pkl` (e.g., `random_forest_20251027_v1.pkl`)
- `{algorithm}_config_{date}.json` for hyperparameters
- `{algorithm}_features_{date}.csv` for feature importance

## Models to Implement

1. **Logistic Regression** - Baseline linear model
2. **Random Forest** - Ensemble method with feature importance
3. **Support Vector Machine** - For non-linear classification
4. **Gradient Boosting** - Advanced ensemble method
5. **Neural Network** - Deep learning approach
6. **Cox Proportional Hazards** - For survival analysis