# 📊 Customer Churn Analysis

This project predicts whether a telecom customer is likely to churn using various machine learning classifiers. The dataset used is provided by IBM and includes customer demographic, account, and usage information.

---

## 📁 Dataset

- **Source**: [IBM Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Rows**: ~7043
- **Target Variable**: `Churn` (Yes / No)
- **Class Imbalance**: 73% No Churn, 27% Churn

---

## 🔍 Exploratory Data Analysis (EDA)

- Checked for nulls and datatype issues
- Converted `TotalCharges` to numeric
- Encoded categorical variables using one-hot encoding
- Performed correlation analysis

---

## ⚙️ Preprocessing

- Balanced the dataset using **SMOTEENN** (SMOTE + Edited Nearest Neighbors)
- Applied **StandardScaler** where necessary (for models like Logistic Regression, KNN, SVM)

---

## 🤖 Models Used

| Model                   | Notes                                          |
|------------------------|------------------------------------------------|
| Decision Tree          | Basic tree model for baseline performance      |
| Random Forest          | Ensemble model for better generalization       |
| XGBoost                | Boosted tree classifier with high accuracy     |
| Gradient Boosting      | Compared alongside XGBoost                     |
| Logistic Regression    | Linear model, required scaling                 |
| K-Nearest Neighbors    | Distance-based model, required scaling         |
| SVM (RBF Kernel)       | Non-linear model, tuned with `C` and `gamma`  |

---

## 📈 Performance Metrics


Evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

⚠️ Due to class imbalance, **recall** and **F1-score** were prioritized over accuracy.

### 🔄 After Resampling (SMOTEENN)

| Model                | Accuracy | Precision | Recall | F1 Score |
|----------------------|----------|-----------|--------|----------|
| Decision Tree        | 0.94     | 0.95      | 0.94   | 0.94     |
| Random Forest        | 0.92     | 0.93      | 0.93   | 0.93     |
| XGBoost              | 0.96     | 0.96      | 0.97   | 0.97     |
| Gradient Boosting    | 0.96     | 0.97      | 0.96   | 0.97     |
| Logistic Regression  | 0.94     | 0.96      | 0.93   | 0.94     |
| K-Nearest Neighbors  | 0.93     | 0.92      | 0.96   | 0.94     |
| SVM (RBF Kernel)     | 0.93     | 0.92      | 0.96   | 0.94     |

📝 *Values are approximated from confusion matrix and metrics in notebook*
---

## ✅ Best Performing Model

**XGBoost** emerged as the best model after resampling, balancing **accuracy**, **recall**, and **F1-score**.

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- imbalanced-learn
- Matplotlib
- Jupyter Notebook

---

##  Author
**Siddharth Jain**  
Aspiring Data Analyst | Passionate about Business + Data  
[LinkedIn](https://www.linkedin.com/in/siddharth-jain-979a35253/)

