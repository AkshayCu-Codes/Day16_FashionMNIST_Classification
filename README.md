# Fashion MNIST Classification using Random Forest

## Overview
This project implements a machine learning pipeline on the Fashion MNIST dataset to classify images into 10 clothing categories using a Random Forest classifier with hyperparameter tuning.

## Dataset
- Input: 784 pixel values (28x28 grayscale images)
- Target: label (0–9)

## Workflow
1. Data Loading and Sampling (10% of dataset)
2. Data Exploration (distribution, statistics, missing values)
3. Train/Validation/Test Split (60/20/20)
4. Normalization: scale pixel values to [-1, 1]
5. Model Training (Random Forest)
6. Hyperparameter Tuning (GridSearchCV)
7. Evaluation (accuracy, classification report, confusion matrix)

## Model
Baseline:
- n_estimators = 300
- max_features = 3
- min_samples_split = 200

Tuned Parameters:
- n_estimators = 200
- max_features = 6
- min_samples_split = 200

## Results
- Baseline Accuracy: 0.77
- Tuned Accuracy: 0.79

## Observations
- Strong performance on most classes
- Misclassifications between visually similar categories
- Lower recall for class 'Shirt'

## How to Run
1. Install dependencies:
   pip install pandas numpy matplotlib scikit-learn

2. Update dataset path in code:
   file_name = "path/to/fashion-mnist_train.csv"

3. Run the notebook or script

## Conclusion
Random Forest provides a solid baseline for image classification. Hyperparameter tuning improves performance, though challenges remain in distinguishing similar classes.
