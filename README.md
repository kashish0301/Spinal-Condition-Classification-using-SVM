# Spinal-Condition-Classification-using-SVM-and-Kmeans

This repository contains the code, data, and report for analyzing vertebral column data using supervised and unsupervised machine learning methods, specifically K-Means Clustering and Support Vector Machines (SVM).

## Table of Contents
- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Data](#data)
- [Methods](#methods)
  - [Unsupervised Classification](#unsupervised-classification)
  - [Supervised Classification](#supervised-classification)
- [Results](#results)
- [How to Run](#how-to-run)
- [References](#references)

## Project Overview
This project aims to analyze spinal conditions using vertebral column data. Both unsupervised and supervised classification techniques are applied, leveraging the strengths of K-Means Clustering and Support Vector Machines (SVM) to diagnose spinal conditions.

The project consists of:
- Exploratory Data Analysis (EDA)
- Unsupervised Learning (K-Means)
- Supervised Learning (SVM)
- Dimensionality reduction using Principal Component Analysis (PCA)

## Repository Structure

```
.
├── Project Report.pdf                       # Full project report detailing methodology, results, and discussion
├── Supervised&Unsupervised_code.ipynb       # Jupyter notebook with all the code for the analysis
├── vertebral_column_data.txt                # Dataset used in the project
├── vertebral_column_metadata.txt            # Metadata describing the dataset
└── README.md                                # Documentation of the project
```

## Data
The data used for this project is stored in the `vertebral_column_data.txt` file. This dataset contains medical attributes of patients related to their vertebral columns. The data is labeled to indicate if a patient suffers from any condition related to their vertebral health.

### Key Features:
- `pelvic_incidence`
- `pelvic_tilt`
- `lumbar_lordosis_angle`
- `sacral_slope`
- `pelvic_radius`
- `grade_of_spondylolisthesis`

The metadata for this dataset is available in `vertebral_column_metadata.txt`.

## Methods

### Unsupervised Classification: K-Means Clustering
K-Means clustering was used to group the data into distinct clusters based on the medical features provided. The elbow method was applied to determine the optimal number of clusters.

### Supervised Classification: Support Vector Machines (SVM)
Support Vector Machines (SVM) with the Radial Basis Function (RBF) kernel was used for classifying the data into spinal condition categories. The model was tuned using GridSearchCV to find the optimal hyperparameters.

#### Hyperparameters:
- `C`: Regularization parameter
- `gamma`: Kernel coefficient
- `kernel`: RBF

### Dimensionality Reduction: PCA
Principal Component Analysis (PCA) was used to reduce the dimensionality of the data while retaining 90% of the original variance, improving the performance of the K-Means and SVM models.

## Results
- **K-Means Clustering**: Achieved a classification accuracy of 66%.
- **SVM with RBF Kernel**: Achieved an accuracy of 90% on the test data.

A detailed comparative analysis of these models can be found in the `Project Report.pdf`.

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/kashish0301/Spinal-Condition-Classification-using-SVM.git
   ```
2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the Jupyter notebook:
   ```bash
   jupyter notebook Supervised&Unsupervised_code.ipynb
   ```
4. Run all cells to replicate the analysis and results.
