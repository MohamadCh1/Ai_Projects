# Scikit-Learn Heart Disease Classification 🫀

This project walks through a complete supervised machine learning workflow using Scikit-Learn to predict heart disease from patient data.

## 🔍 Project Overview

We use the [heart-disease.csv](https://raw.githubusercontent.com/mrdbourke/zero-to-mastery-ml/master/data/heart-disease.csv) dataset to:

- Load and explore data using Pandas
- Train and compare multiple classifiers
- Tune hyperparameters with `RandomizedSearchCV`
- Evaluate model performance using accuracy, precision, recall, F1-score, and confusion matrix
- Save and reload trained models using `joblib`

## 📊 Models Compared

- Logistic Regression
- Random Forest
- Support Vector Classifier (SVC)
- K-Nearest Neighbors (KNN)
- Decision Tree
- LinearSVC

## 🧪 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix (Seaborn heatmap)

## 📁 Outputs

- `model_accuracy_comparison.png` — Bar plot comparing model scores
- `confusion_matrix.png` — Visual confusion matrix for best-performing model
- `heart-disease-model.joblib` — Saved trained model

## 🛠️ Tools Used

- Python
- Scikit-Learn
- Pandas
- NumPy
- Matplotlib
- Seaborn
- joblib

## 📎 Credits

Inspired by [Daniel Bourke's Zero to Mastery ML series](https://github.com/mrdbourke/zero-to-mastery-ml)

## 🚀 How to Run

1. Clone the repo  
   ```bash
   git clone https://github.com/MohamadCh1/Ai_Projects.git
   cd Ai_Projects/scikit-learn-heart-disease-classification

