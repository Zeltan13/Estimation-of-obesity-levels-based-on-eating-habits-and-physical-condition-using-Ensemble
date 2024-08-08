# Obesity Level Prediction using Ensemble Methods

## Project Overview

This project involves predicting the level of obesity of an individual based on their eating habits and physical conditions using ensemble methods in Python. We utilized Random Forest with Bagging, Gradient Boosting, and Stacking classifiers to achieve high accuracy. The Random Forest model with Bagging was selected as the baseline due to its superior performance.

## Dataset

The dataset used is "Estimation of Obesity Levels Based On Eating Habits and Physical Condition." It contains synthetic data generated using Weka and SMOTE, with 23% of the data collected directly from users. The data includes information from Mexico, Peru, and Colombia.

## Requirements

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- Google Colab (for data handling)

## Installation

Install the required libraries using pip:

  ```bash
  pip install pandas numpy matplotlib seaborn scikit-learn

Data Preprocessing
Load the Data:
Load the dataset from Google Drive and perform initial data exploration.

Data Cleaning:

Convert categorical features to numeric.
Handle missing values.
Scale numerical features using StandardScaler.
Feature Selection:

Calculate correlations with the target variable.
Select the top features for the model.
Feature Engineering:

Create a new feature BMI (Body Mass Index) for better analysis.
Model Implementation
1. Baseline Model: Random Forest with Bagging
Description: Utilized Random Forest with Bagging for baseline comparison.
Accuracy: 98.58%
Validation Accuracy: 98.57%
Training Time: 0.41 seconds
Cross-Validation Scores: [0.9852, 0.9822, 0.9852, 0.9822, 0.9941]
2. Boosting: Gradient Boosting
Description: Implemented Gradient Boosting for comparison.
Accuracy: 97.87%
Training Time: 0.39 seconds
Cross-Validation Scores: [0.9734, 0.9556, 0.9615, 0.9703, 0.9763]
3. Stacking
Description: Applied Stacking with multiple base models.
Accuracy: 97.40%
Training Time: 1.15 seconds
Cross-Validation Scores: [0.9645, 0.9704, 0.9763, 0.9763, 0.9852]
Model Exploration
Additional Random Forest models with varying parameters were explored:

Model 1: 200 Trees, Max Depth 15

Accuracy: 98.82%
Training Time: 0.58 seconds
Cross-Validation Scores: [0.9852, 0.9822, 0.9852, 0.9822, 0.9911]
Model 2: 5 Trees, Max Depth 15

Accuracy: 97.87%
Training Time: 0.02 seconds
Cross-Validation Scores: [0.9734, 0.9556, 0.9615, 0.9703, 0.9763]
Model 3: 100 Trees, Max Depth 5

Accuracy: 97.40%
Training Time: 0.25 seconds
Cross-Validation Scores: [0.9645, 0.9704, 0.9763, 0.9763, 0.9852]
Results
The Random Forest model with Bagging (Baseline) showed the best performance in terms of accuracy and cross-validation scores.
All models achieved accuracy above 97%, with minimal differences in training and validation times.
Conclusion
The Random Forest with Bagging was selected as the baseline model due to its highest accuracy and validation performance. Other models, including Gradient Boosting and Stacking, also performed well but were either slower or less accurate.
