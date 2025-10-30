# Notebooks: Patient Risk Stratification Pipeline

This directory contains 4 sequential Jupyter notebooks for building a machine learning model to **stratify breast cancer patients into high and low risk groups** using RNA expression and clinical data.

## 🎯 Goal

**Minimize errors in the low-risk group** — patients predicted as low-risk should truly have no recurrence events. High precision in low-risk identification is critical for treatment de-escalation decisions.

## Workflow (Complete in Order)

### **1. Data Exploration** (`01_data_exploration.ipynb`)
- Load RNA expression and clinical data (Metabric dataset)
- Visualize gene expression distributions and data quality
- Explore survival outcomes: RFS_MONTHS (time to recurrence) and RFS_STATUS (event indicator)
- Understand baseline event rates and patient characteristics

### **2. Data Preprocessing** (`02_data_preprocessing.ipynb`)
- Handle missing values in expression and clinical data
- Normalize gene expression data (StandardScaler)
- Filter low-variance genes (initial quality filtering)
- Prepare RFS target variables for modeling
- Create stratified train/validation/test splits

### **3. Feature Selection** (`03_feature_selection.ipynb`)
Apply 7 advanced feature selection methods:
- **Variance filtering**: Select highly variable genes (stricter than preprocessing)
- **De-correlation**: Remove redundant correlated features
- **Differential expression**: Statistical tests between risk groups
- **Random Forest importance**: With KneeLocator for optimal cutoff
- **LASSO/SVM selection**: L1-regularized embedded methods
- **Boruta**: All-relevant feature detection with shadow features
- **Cox regression**: Survival-based feature association

**Output**: Optimized ensemble feature sets for modeling

### **4. Model Development** (`04_model_development.ipynb`)
- Train classification models: Logistic Regression, SVM, Random Forest, Gradient Boosting, Neural Networks
- Train survival models: Cox Proportional Hazards regression
- **Evaluate using clinical metrics**:
  - C-index (concordance index)
  - **Precision in Low-Risk** (primary metric) — minimize false low-risk predictions
  - Calibration quality
- **Stratify patients into low/medium/high risk groups**
- Validate with Kaplan-Meier survival curves and log-rank tests
- Optimize hyperparameters for best model
- Final test set validation and deployment preparation

**Output**: Production-ready risk stratification model with maximized precision in low-risk group

---

## Success Criteria

By completing all 4 notebooks, you will have:
- ✅ A validated risk prediction model (C-index > 0.7)
- ✅ **High precision in low-risk group** (minimal events in low-risk patients)
- ✅ Statistically validated patient risk groups (low/medium/high)
- ✅ Kaplan-Meier curves showing clear survival separation
- ✅ Complete model documentation for clinical deployment