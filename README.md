# ❤️ Heart Disease Prediction Modeling

This project aims to predict the presence of heart disease in patients using machine learning algorithms. By leveraging medical and demographic data, the model identifies high-risk individuals for early diagnosis and better healthcare outcomes.

## 📊 Objective

- **Identify Key Factors** influencing heart disease (e.g., age, cholesterol, chest pain type).
- **Build predictive models** (Logistic Regression, Decision Tree, Random Forest, LDA, QDA) to classify patients.
- **Optimize model performance** with a focus on minimizing false negatives, which are critical in medical diagnosis.

## 🗃️ Dataset

- **Source:** [Kaggle - Heart Disease Dataset](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset)
- **Size:** 1,025 patient records
- **Features:**
  - Categorical: `sex`, `cp`, `fbs`, `restecg`, `exang`, `slope`, `ca`, `thal`, `target`
  - Numerical: `age`, `trestbps`, `chol`, `thalach`, `oldpeak`
- **Target Variable:** `target` (1 = Heart Disease, 0 = No Heart Disease)

## 🔍 Exploratory Data Analysis (EDA)

- Summary statistics and distributions
- Heatmaps and correlation analysis
- Outlier detection and removal (IQR method)
- Feature encoding (binary & one-hot encoding)

## ⚙️ Data Preprocessing

- Handling categorical variables via dummy encoding
- Normalization using `StandardScaler`
- Splitting data into 70% training and 30% testing sets
- Removing outliers from numerical features

## 🧠 Machine Learning Models

### 1. **Logistic Regression**
- Accuracy: 85%
- AUC: 0.93
- Balanced performance, good generalization
- Strong recall on the positive class (Heart Disease)

### 2. **Decision Tree**
- Accuracy: 95%
- AUC: 0.98
- High precision and recall
- Depth limited to 6 to prevent overfitting

### 3. **Random Forest**
- Accuracy: 96%
- AUC: ~1.00
- Best performance across all metrics
- Robust to noise and handles both linear/non-linear patterns

### 4. **Linear Discriminant Analysis (LDA)**
- Accuracy: 84%
- AUC: 0.93
- Good generalization and class separation

### 5. **Quadratic Discriminant Analysis (QDA)**
- Accuracy: 84%
- AUC: 0.92
- Handles non-linearity well, but slightly less performant

## 📈 Model Evaluation Metrics

- **Precision, Recall, F1-Score**
- **Confusion Matrix**
- **ROC-AUC Curve**
- **25-Fold Cross Validation**

## 🔬 Feature Importance (Top Features)

- Chest Pain Type (`cp`)
- Number of Major Vessels Colored (`ca`)
- Age
- Thalassemia (`thal`)
- Cholesterol Level (`chol`)

## 💼 Business Impact

- Enables early detection and intervention
- Supports risk-based patient prioritization
- Reduces unnecessary procedures
- Assists insurance and preventive healthcare strategies

## 📦 Dependencies

```bash
pandas
numpy
matplotlib
seaborn
scikit-learn
```

## ▶️ How to Run

1. Clone this repository
2. Install dependencies (`pip install -r requirements.txt`)
3. Run the notebook `Heart Disease Prediction Modeling.ipynb`
4. Evaluate and visualize the model results

---

Let me know if you'd like this saved as a `README.md` file or if you want to include visual plots from the notebook.
