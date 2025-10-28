# Data Directory

This directory contains the complete Metabric dataset files for the machine learning course.

## Available Files ✓

All required data files are now present:

### 1. Clinical Patient Data
- **File**: `data_clinical_patient.txt`
- **Format**: Tab-separated with comment headers (lines starting with #)
- **Contains**: Patient demographics, tumor characteristics, survival outcomes
- **Dimensions**: ~1,904 patients × multiple clinical variables

### 2. Clinical Sample Data  
- **File**: `data_clinical_sample.txt`
- **Format**: Tab-separated with comment headers (lines starting with #)
- **Contains**: Sample-level clinical annotations and metadata
- **Dimensions**: Sample-level information linked to patients

### 3. Expression Data
- **File**: `data_mrna_illumina_microarray.txt`
- **Format**: Tab-separated, direct data format (no comment lines)
- **Contains**: Illumina microarray gene expression profiles
- **Dimensions**: ~20,603 genes × ~1,904 samples
- **Structure**: Hugo_Symbol (index) | Entrez_Gene_Id | Sample columns (MB-XXXX format)

## Dataset Information

The Metabric (Molecular Taxonomy of Breast Cancer International Consortium) dataset contains:
- Gene expression profiles for ~2000 breast cancer samples
- Clinical and pathological annotations  
- Long-term survival follow-up data
- Molecular subtype classifications

## Download Instructions

1. Click each Google Drive link above
2. Click the "Download" button in Google Drive
3. Save files with the exact names shown above in this directory
4. The notebooks will automatically detect and load the data