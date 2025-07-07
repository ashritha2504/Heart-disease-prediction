# 🫀 Heart Disease Risk Prediction Using K-Nearest Neighbors (KNN)

This project aims to predict the 10-year risk of heart disease using the **Framingham Heart Study dataset** and the **K-Nearest Neighbors (K-NN)** algorithm. The model was developed and evaluated using different K values (3, 5, and 7), with a focus on model performance, recall, and accuracy.

## 📊 Dataset
The dataset used is `framingham.csv`, which includes features such as:
- Age
- Gender
- Smoking behavior
- Blood pressure
- Cholesterol levels
- BMI
- Diabetes
- Heart rate
- Glucose levels
- Target variable: `TenYearCHD` (1 = risk of heart disease, 0 = no risk)

## ⚙️ Methodology

### 🔍 Preprocessing
- Missing values were imputed:
  - Categorical: Mode imputation
  - Numerical: Median imputation
- Features were normalized using `StandardScaler` to account for distance-based learning.
- Train/test split: 80/20 ratio

### 🧠 Modeling
- Used **KNN Classifier** from `scikit-learn`
- Trained models with **K = 3, 5, 7**
- Evaluated using:
  - Accuracy
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-score)

### 📈 Results Summary

| K Value | Accuracy | Recall (Class 1) | Precision (Class 1) |
|---------|----------|------------------|----------------------|
| 3       | 81.37%   | 0.11             | 0.22                 |
| 5       | 83.02%   | 0.05             | 0.18                 |
| 7       | 83.25%   | 0.03             | 0.15                 |

Despite high overall accuracy, all models struggled with identifying patients at actual risk (Class 1), suggesting a **class imbalance issue**.

## 🧪 Evaluation
- Model with **K=7** performed best in terms of accuracy
- Model with **K=3** had better recall for heart disease cases
- Visual tools like **correlation heatmaps** were used to explore feature relationships

## 🚀 Future Improvements
- Apply techniques like **SMOTE** or **class weighting** to address class imbalance
- Experiment with other algorithms: Random Forest, SVM, Logistic Regression, Ensemble methods
- Perform hyperparameter tuning and cross-validation
- Engineer new features to improve predictive power


