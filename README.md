# Machine Learning Course: Clinical Risk Classification from Transcriptomics Data

## Course Overview

This repository contains materials for a comprehensive machine learning course focused on developing **clinical risk classification models from transcriptomics data** using the **Metabric dataset**. Students will learn to apply both time-independent and time-dependent machine learning techniques to real-world genomics data for predicting breast cancer patient outcomes and stratifying patients into meaningful risk groups.

## Learning Objectives

By the end of this course, students will be able to:

1. **Understand transcriptomics data** and its application in precision medicine
2. **Explore and visualize** high-dimensional genomics datasets
3. **Preprocess genomics data** including normalization and quality control
4. **Apply feature selection** techniques for high-dimensional data
5. **Develop time-independent classification models** for patient risk assessment
6. **Implement time-dependent survival analysis models** including Cox regression
7. **Evaluate models using clinical metrics** including C-index and precision in low-risk groups
8. **Perform risk stratification analysis** to create meaningful patient groups
9. **Compare and select optimal models** using comprehensive evaluation frameworks
10. **Validate models** using appropriate statistical methods and clinical utility assessment
11. **Interpret model results** in a clinical context with explainability tools
12. **Deploy production-ready models** with clinical implementation materials

## Dataset: Metabric

The **Molecular Taxonomy of Breast Cancer International Consortium (Metabric)** dataset contains:
- Gene expression profiles for ~2,000 breast cancer samples
- Clinical and pathological annotations
- Long-term survival follow-up data
- Multiple molecular subtypes and risk classifications

**Citation**: Curtis, C. et al. The genomic and transcriptomic architecture of 2,000 breast tumours reveals novel subgroups. *Nature* 486, 346–352 (2012).

## Project Structure

```
machine_learning_course/
├── README.md                 # This file
├── requirements.txt          # Python dependencies
├── .gitignore               # Git ignore file
├── data/                    # Data directory (download files here)
│   ├── clinical_patient_data.csv    # Patient demographics and outcomes
│   ├── clinical_sample_data.csv     # Sample-level clinical data
│   └── expression_data.csv          # Gene expression data
├── notebooks/              # Jupyter notebooks (main learning materials)
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_preprocessing.ipynb
│   ├── 03_feature_selection.ipynb
│   └── 04_model_development.ipynb    # Comprehensive modeling pipeline
├── models/                 # Trained model artifacts
└── results/               # Analysis outputs
    ├── figures/           # Plots and visualizations
    └── reports/           # Analysis reports
```

## Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook or JupyterLab
- Basic knowledge of Python and pandas
- Understanding of basic statistics and linear algebra

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
   
   - **Expression Data**: [Download Link](https://drive.google.com/file/d/1q4I2v-12jUrwJ3Jf8CICi235ZvsODDW7/view?usp=sharing)
     - Save as: `data/expression_data.csv`

5. **Launch Jupyter**:
   ```bash
   jupyter notebook
   ```

### Course Progression

Follow the notebooks in order:

1. **Data Exploration** (`01_data_exploration.ipynb`)
   - Load and examine the Metabric dataset
   - Understand data structure and quality
   - Visualize gene expression distributions
   - Explore clinical variables and outcomes

2. **Data Preprocessing** (`02_data_preprocessing.ipynb`)
   - Handle missing values
   - Normalize gene expression data
   - Filter low-variance genes
   - Create train/validation/test splits

3. **Feature Selection** (`03_feature_selection.ipynb`)
   - Apply univariate feature selection
   - Use recursive feature elimination
   - Implement LASSO regularization
   - Compare feature selection methods

4. **Comprehensive Model Development** (`04_model_development.ipynb`)
   - **Activity 1**: Library setup and environment configuration
   - **Activity 2**: Data loading and feature set preparation
   - **Activity 3**: Time-independent classification models (Logistic, SVM, RF, GB, Neural Networks)
   - **Activity 4**: Time-dependent survival analysis models (Cox regression, Random Survival Forest)
   - **Activity 5**: Comprehensive evaluation with clinical metrics (C-index, precision in low-risk)
   - **Activity 6**: Risk stratification analysis and patient group validation
   - **Activity 7**: Model comparison and selection using multi-criteria evaluation
   - **Activity 8**: Final model validation, interpretation, and clinical deployment

## Key Machine Learning Concepts Covered

### Time-Independent Classification
- **Linear Models**: Logistic regression with L1/L2 regularization
- **Tree-Based**: Random Forest, Gradient Boosting, XGBoost
- **Kernel Methods**: Support Vector Machines (RBF, Linear kernels)
- **Neural Networks**: Multi-layer perceptrons with regularization
- **Ensemble Methods**: Voting classifiers and model stacking

### Time-Dependent Survival Analysis
- **Cox Proportional Hazards**: Time-to-event modeling with covariates
- **Random Survival Forest**: Non-parametric ensemble survival models
- **Time-Varying Coefficients**: Models with temporal dependencies
- **Kaplan-Meier Estimation**: Non-parametric survival curve estimation
- **Log-Rank Tests**: Statistical comparison of survival curves

### Clinical Evaluation Metrics
- **C-index (Concordance Index)**: Primary ranking metric for risk models
- **Precision in Low-Risk Groups**: Clinical utility for identifying low-risk patients
- **Calibration Analysis**: Model reliability assessment with calibration curves
- **Risk Stratification**: Statistical validation of patient group separation
- **Decision Curve Analysis**: Clinical utility and net benefit evaluation

### Advanced Model Evaluation
- **Cross-validation strategies** for time-dependent data
- **Bootstrap confidence intervals** for robust performance estimates
- **Subgroup analysis** and model generalization assessment
- **Missing data sensitivity** analysis and handling strategies
- **Model interpretability** with SHAP values and feature importance

### Feature Engineering for Genomics
- **High-dimensional data handling** and curse of dimensionality
- **Gene expression normalization** and batch effect correction
- **Feature selection techniques** (univariate, recursive, LASSO)
- **Dimensionality reduction** (PCA, t-SNE) for visualization
- **Pathway analysis** and biological interpretation

### Clinical Implementation
- **Risk calculator development** for clinical decision support
- **Model deployment** and production-ready implementation
- **Clinical validation frameworks** and regulatory considerations
- **Continuous learning** and model updating strategies
- **Electronic health record integration** considerations

## Assessment and Exercises

The comprehensive model development notebook contains:
- **8 Guided Activities** with step-by-step instructions covering the complete ML pipeline
- **Hands-on Implementation** of both time-independent and time-dependent models
- **Clinical Evaluation Framework** with real-world metrics (C-index, precision in low-risk)
- **Risk Stratification Analysis** for meaningful patient group classification
- **Model Comparison** using multi-criteria evaluation and statistical validation
- **Production Deployment** with clinical implementation materials and documentation
- **Extension Challenges** for advanced students including external validation and regulatory preparation

## Resources and References

### Essential Papers
1. Curtis, C. et al. (2012). The genomic and transcriptomic architecture of 2,000 breast tumours reveals novel subgroups. *Nature*, 486(7403), 346-352.
2. Pereira, B. et al. (2016). The somatic mutation profiles of 2,433 breast cancers refines their genomic and transcriptomic landscapes. *Nature Communications*, 7, 11479.

### Textbooks
- Hastie, T., Tibshirani, R., & Friedman, J. (2009). *The Elements of Statistical Learning*
- James, G., Witten, D., Hastie, T., & Tibshirani, R. (2013). *An Introduction to Statistical Learning*
- Gentleman, R. et al. (2005). *Bioinformatics and Computational Biology Solutions Using R and Bioconductor*

### Online Resources
- [scikit-learn documentation](https://scikit-learn.org/)
- [pandas documentation](https://pandas.pydata.org/)
- [matplotlib/seaborn tutorials](https://matplotlib.org/stable/tutorials/index.html)

## Contributing

This is an educational repository. Students are encouraged to:
- Submit issues for bugs or unclear instructions
- Propose improvements to notebooks
- Share interesting findings or extensions
- Contribute additional exercises or examples

## License

This course material is provided for educational purposes. Please cite appropriately if using in academic work.

## Contact

For questions about the course materials, please open an issue in this repository or contact the course instructor.

---

**Happy Learning!** 🧬📊🤖
