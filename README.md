# Machine Learning Course: Patient Risk Stratification

## 🎯 **Project Goal**

**Implement a machine learning model to stratify breast cancer patients into high and low risk groups using RNA expression data and clinical features.**

## What You'll Learn

1. Explore and preprocess high-dimensional genomics data
2. Select informative features from gene expression profiles
3. Train classification and survival models for risk prediction
4. Evaluate models using clinical metrics (C-index, precision in low-risk)
5. Stratify patients into validated risk groups
6. Deploy production-ready risk prediction models

## Dataset

**Metabric Dataset** (~2,000 breast cancer patients):
- **Gene expression data**: RNA expression profiles for thousands of genes
- **Clinical data**: Patient demographics, tumor characteristics, treatment information
- **Survival data**: Recurrence-free survival (RFS_MONTHS, RFS_STATUS)

*Source: Curtis, C. et al. Nature 486, 346–352 (2012)*

## Project Structure

```
machine_learning_course/
├── data/                           # Download data files here
│   ├── clinical_patient_data.csv
│   ├── clinical_sample_data.csv
│   └── expression_data.csv
├── notebooks/                      # 4 sequential notebooks
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_preprocessing.ipynb
│   ├── 03_feature_selection.ipynb
│   └── 04_model_development.ipynb
└── results/                        # Generated outputs
```

## Setup

### Prerequisites
- Python 3.8+
- Jupyter Notebook
- Basic Python, pandas, and statistics knowledge

### Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd machine_learning_course
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the Metabric dataset**:
   
   Download these files from Google Drive and save them in the `data/` directory:
   
   - **Clinical Patient Data**: [Download Link](https://drive.google.com/file/d/15AXx2ZKiQ8MhK8EgK6xnE0XbW_PAxY0j/view?usp=sharing)
     - Save as: `data/clinical_patient_data.csv`
   
   - **Clinical Sample Data**: [Download Link](https://drive.google.com/file/d/1q4I2v-12jUrwJ3Jf8CICi235ZvsODDW7/view?usp=sharing)
     - Save as: `data/clinical_sample_data.csv`
   
   - **Expression Data**: [Download Link](https://drive.google.com/file/d/1qi6Nevc7ypmZO9AzCINssQqSFOMnL0sZ/view?usp=sharing)
     - Save as: `data/expression_data.csv`

5. **Launch Jupyter**:
   ```bash
   jupyter notebook
   ```

## Workflow

Complete the 4 notebooks in order:

### **1. Data Exploration** (`01_data_exploration.ipynb`)
- Load RNA expression and clinical data
- Visualize data distributions and quality
- Explore survival outcomes (RFS_MONTHS, RFS_STATUS)

### **2. Data Preprocessing** (`02_data_preprocessing.ipynb`)
- Handle missing values and normalize expression data
- Filter low-variance genes
- Prepare RFS target variables
- Create train/validation/test splits

### **3. Feature Selection** (`03_feature_selection.ipynb`)
Apply 7 feature selection methods:
- Advanced variance filtering
- De-correlation analysis
- Differential expression between risk groups
- Random Forest importance with KneeLocator
- LASSO and SVM-based selection
- Boruta all-relevant feature detection
- Cox regression survival association
- **Output**: Optimized feature sets for modeling

### **4. Model Development** (`04_model_development.ipynb`)
- Train classification models (Logistic, SVM, Random Forest, GBM, Neural Networks)
- Train survival models (Cox regression)
- Evaluate using C-index and precision in low-risk
- **Stratify patients into low/medium/high risk groups**
- Validate with Kaplan-Meier survival curves
- Select and deploy final production model

## Key Concepts

### Methods
- **Classification**: Logistic Regression, SVM, Random Forest, Gradient Boosting, Neural Networks
- **Survival Analysis**: Cox Proportional Hazards regression
- **Feature Selection**: Variance filtering, differential expression, Random Forest importance, LASSO, Boruta, Cox association

### Evaluation Metrics
- **C-index**: Concordance index for ranking predictions
- **Precision in Low-Risk**: Identifying patients who truly don't need aggressive treatment
- **Risk Stratification**: Statistical validation of patient groups (Kaplan-Meier curves, log-rank tests)
- **Calibration**: Agreement between predicted and observed event rates

## Expected Outcome

By completing this course, you will:
- Build a production-ready risk stratification model
- Generate **low, medium, and high risk patient groups** with statistical validation
- Create Kaplan-Meier survival curves showing clear risk separation
- Deploy a model with C-index > 0.7 and validated precision metrics
- Produce complete documentation for clinical implementation

---

**Good luck with your risk stratification project!** 🎯📊
