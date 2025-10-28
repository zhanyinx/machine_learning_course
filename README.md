# Machine Learning Course: Risk Classification from Transcriptomics Data

## Course Overview

This repository contains materials for an introduction to machine learning course focused on developing a **risk classification model from transcriptomics data** using the **Metabric dataset**. Students will learn to apply machine learning techniques to real-world genomics data for predicting breast cancer patient outcomes.

## Learning Objectives

By the end of this course, students will be able to:

1. **Understand transcriptomics data** and its application in precision medicine
2. **Explore and visualize** high-dimensional genomics datasets
3. **Preprocess genomics data** including normalization and quality control
4. **Apply feature selection** techniques for high-dimensional data
5. **Train and evaluate** various machine learning models for classification
6. **Interpret model results** in a clinical context
7. **Validate models** using appropriate cross-validation strategies
8. **Communicate findings** through visualizations and reports

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
│   ├── 04_model_training.ipynb
│   ├── 05_model_evaluation.ipynb
│   ├── 06_risk_stratification.ipynb
│   └── 07_final_model.ipynb
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

4. **Model Training** (`04_model_training.ipynb`)
   - Train baseline logistic regression
   - Implement random forest classifier
   - Apply support vector machines
   - Train gradient boosting models

5. **Model Evaluation** (`05_model_evaluation.ipynb`)
   - Calculate performance metrics (AUC, accuracy, F1-score)
   - Create ROC curves and confusion matrices
   - Perform cross-validation
   - Compare model performance

6. **Risk Stratification** (`06_risk_stratification.ipynb`)
   - Generate risk scores for patients
   - Create risk groups (low, intermediate, high)
   - Perform survival analysis
   - Validate clinical utility

7. **Final Model** (`07_final_model.ipynb`)
   - Select best performing model
   - Retrain on full training set
   - Final validation on test set
   - Create deployment-ready model

## Key Machine Learning Concepts Covered

### Supervised Learning
- Classification vs. regression
- Binary and multi-class classification
- Model selection and hyperparameter tuning

### Model Types
- **Linear Models**: Logistic regression, LASSO
- **Tree-Based**: Random Forest, Gradient Boosting
- **Instance-Based**: k-NN
- **Kernel Methods**: Support Vector Machines
- **Neural Networks**: Multi-layer perceptrons

### Model Evaluation
- Cross-validation strategies
- Performance metrics for imbalanced data
- ROC curves and AUC
- Precision-recall curves
- Statistical significance testing

### Feature Engineering
- Handling high-dimensional data
- Feature selection techniques
- Dimensionality reduction (PCA, t-SNE)
- Feature importance interpretation

### Genomics-Specific Concepts
- Gene expression normalization
- Batch effect correction
- Pathway analysis
- Survival analysis and Cox regression

## Assessment and Exercises

Each notebook contains:
- **Guided exercises** with step-by-step instructions
- **Practice problems** for hands-on experience
- **Discussion questions** for deeper understanding
- **Extension challenges** for advanced students

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
