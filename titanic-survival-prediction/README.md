# 🚢 Titanic Survival Prediction

This project builds a complete machine learning pipeline to predict passenger survival on the Titanic. It includes data preprocessing, model training, evaluation, visualization, and hyperparameter tuning using scikit-learn and XGBoost.

---

## 📊 Dataset

- **Source**: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- **Target**: `Survived` (0 = No, 1 = Yes)
- **Features Used**:
  - Categorical: `Cabin`, `Embarked`, `Sex`, `Ticket`
  - Numerical: `Age`, `Parch`, `Pclass`, `SibSp`, `Fare`

---

## 🧪 Workflow Overview

### 1. Exploratory Data Analysis (EDA)
- Visualizations:
  - Survival by Sex, Age, Parch, and Pclass
- Output saved as `titanic_visuals.png`

### 2. Preprocessing
- **Numerical**: Median imputation
- **Categorical**: Most frequent imputation + One-Hot Encoding
- Combined using `ColumnTransformer` and `Pipeline`

### 3. Model Training
- Models compared:
  - Logistic Regression
  - Random Forest Classifier
  - XGBoost Classifier
- Evaluation metric: Accuracy on test set

### 4. Model Evaluation
- Metrics:
  - Accuracy, Precision, Recall, F1 Score
  - Confusion Matrix (Seaborn heatmap)
- Cross-validation (5-fold)

### 5. Hyperparameter Tuning
- Performed on Logistic Regression using `GridSearchCV`
- Tuned:
  - `C`: [0.01, 0.1, 1, 10, 100]
  - `penalty`: ['l1', 'l2']
  - `solver`: ['liblinear', 'saga']

---

## 📈 Results

| Model                  | Accuracy |
|------------------------|----------|
| Logistic Regression    | ~0.78    |
| Random Forest Classifier | ~0.81 |
| XGBoost Classifier     | ~0.82    |

> Final tuned Logistic Regression achieved improved accuracy with optimized hyperparameters.

---

## 📌 How to Run

```bash
# 1. Create virtual environment
python -m venv venv-titanic
source venv-titanic/bin/activate  # or venv-titanic\Scripts\activate on Windows

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the script
python titanic_model.py



🧠 Credits
Special thanks to:
- Daniel Bourke — for ML inspiration and tutorials
- Lara Wehbe — for guidance and support

🚀 Future Improvements
- Feature engineering for Cabin and Ticket
- Ensemble voting or stacking
- Deployment via Flask or Streamlit
- Model interpretability with SHAP or LIME
