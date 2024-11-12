# Breast Cancer Wisconsin Dataset Analysis

This repository provides an analysis of the Breast Cancer Wisconsin dataset from the UCI Machine Learning Repository. Multiple machine learning models were implemented to predict the target variable (benign/malignant) based on the dataset features. The models were evaluated using k-fold cross-validation with an 80-20 train-test split.

## Dataset

- **Source**: [UCI Machine Learning Repository - Breast Cancer Wisconsin Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)
- **Description**: This dataset contains 699 instances of breast cancer data with 30 numeric features describing characteristics of cell nuclei in images obtained through fine needle aspirate of breast mass.
- **Features**: The dataset contains 9 features: Clump thickness, Uniformity of cell size, Uniformity of cell shape, Marginal adhesion, Single epithelial cell size, Bare nuclei, Bland chromatin, Normal nucleoli, Mitoses.
- **Target Variable**: Binary classification (0 = benign, 1 = malignant)

## Models Used

The following models were evaluated using 10-fold cross-validation, providing a comprehensive performance metric:

2. **Logistic Regression**
3. **Kernel SVM**
4. **K-Nearest Neighbors (KNN)**
5. **Naive Bayes**
6. **Random Forest**

## Results

Each model's performance is reported below, with **accuracy**, and **standard deviation**.

| Model               | Accuracy  | Std. Dev |
| ------------------- | --------- | -------- |
| Logistic Regression | `96.24 %` | 1.26 %   |
| Kernel SVM          | `96.95 %` | 1.41 %   |
| K-Nearest Neighbors | `96.78 %` | 1.35 %   |
| Naive Bayes         | `96.24 %` | 1.48 %   |
| Random Forest       | `96.06 %` | 2.24 %   |

**Note**: The highest accuracy was achieved by the Kernel SVM model (96.95%).

## Installation

To run the code, clone the repository and install the dependencies:

```bash
git clone https://github.com/rioZga/BreastCancerML.git
cd BreastCancerML
pip install -r requirements.txt
```

## Usage

1. **Data Loading**: The dataset is fetched using the `ucimlrepo` library.
2. **Preprocessing**: Missing values are filled with the column mean.
3. **Model Training and Evaluation**: Each model is evaluated using 10-fold cross-validation.

## Dependencies

- `pandas`
- `numpy`
- `scikit-learn`
- `ucimlrepo`
