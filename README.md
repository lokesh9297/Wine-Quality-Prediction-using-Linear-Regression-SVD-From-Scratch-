# Wine Quality Prediction using Linear Regression & SVD (From Scratch)

## Overview
This project implements **Linear Regression from scratch** using both **Gradient Descent** and **Singular Value Decomposition (SVD)** without relying on machine learning libraries like `scikit-learn`. The goal is to predict wine quality based on multiple chemical properties from the **Wine Quality Dataset**.

## Dataset
The dataset used is the [Wine Quality Dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/) from UCI Machine Learning Repository. It contains **1599 samples** of red wine with **11 input features** and a **target variable (quality)**.

### Features:
- Fixed acidity
- Volatile acidity
- Citric acid
- Residual sugar
- Chlorides
- Free sulfur dioxide
- Total sulfur dioxide
- Density
- pH
- Sulphates
- Alcohol

### Target:
- Quality (score between 3-8)

## Implementation Details
### 1. **Simple Linear Regression (From Scratch Using Gradient Descent)**
We implement multiple linear regression using **gradient descent** with:
- **Mean Squared Error (MSE) loss function**
- **Feature scaling (Standardization)**
- **Train-Test Split (80% train, 20% test)**

#### **Steps:**
1. Load the dataset from CSV
2. Standardize the features manually using mean and standard deviation
3. Initialize weights and bias manually
4. Implement gradient descent algorithm:
   - Compute gradients for weights and bias
   - Update parameters iteratively
5. Train on the training set
6. Evaluate on the test set (MSE and R² score computed manually)

### 2. **SVD-Based Regression (From Scratch Without Libraries)**
Instead of gradient descent, we solve for weights using **Singular Value Decomposition (SVD)**.

#### **Steps:**
1. Compute the **SVD decomposition manually**: \( A = U S V^T \)
2. Compute the **Moore-Penrose pseudo-inverse** manually: \( A^+ = V S^+ U^T \)
3. Compute the optimal weights using the computed inverse: \( X = A^+ B \)
4. Predict and evaluate on test data (MSE and R² score computed manually)

- **Bias term added explicitly in the feature matrix**

## Results
- **Gradient Descent Regression:**
  - Training MSE: *~0.42*
  - Test MSE: *~0.39*
  - R² Score: *~0.34*
- **SVD-Based Regression:**
  - Training MSE: *~0.42*
  - Test MSE: *~0.39*
  - R² Score: *~0.34*
