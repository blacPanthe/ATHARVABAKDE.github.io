# Heart Disease Prediction Modeling

**Author:** Atharva Bakde &nbsp;|&nbsp; **Date:** April 2025

Early detection of cardiovascular disease can significantly improve patient outcomes. This project builds and compares five classification models on 1,025 patient records, with a focus on **minimizing false negatives** — missed diagnoses that can have fatal consequences.

---

## Dataset

| Property | Detail |
|---|---|
| Source | [Kaggle — Heart Disease Dataset](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset) |
| Records | 1,025 patients |
| Features | 13 medical attributes |
| Target | `1` = Heart Disease, `0` = No Heart Disease |
| Class balance | ~50 / 50 |

**Numerical features:** `age`, `trestbps`, `chol`, `thalach`, `oldpeak`  
**Categorical features:** `sex`, `cp`, `fbs`, `restecg`, `exang`, `slope`, `ca`, `thal`

---

## Workflow

1. **Exploratory Data Analysis** — distributions, correlations, outlier detection
2. **Preprocessing** — IQR outlier removal → one-hot encoding → StandardScaler → 70/30 stratified split
3. **Modeling** — five classifiers trained and tuned
4. **Evaluation** — Accuracy, Precision, Recall, F1-Score, AUC-ROC, 25-fold cross-validation

---

## Results

| Model | Accuracy | Recall | Precision | F1-Score | AUC |
|---|---|---|---|---|---|
| Logistic Regression | 86.0% | 91.8% | 82.9% | 87.1% | 0.926 |
| Decision Tree | 90.9% | 93.0% | 89.6% | 91.3% | 0.957 |
| **Random Forest** | **96.1%** | **98.7%** | **93.9%** | **96.3%** | **0.996** |
| LDA | 83.8% | 91.8% | 79.7% | 85.3% | 0.926 |
| QDA | 84.4% | 86.7% | 83.5% | 85.1% | 0.922 |

**Random Forest is the recommended model.** It missed only **2 out of 158** disease cases on the test set — a recall of 98.7% — making it well-suited for medical screening.

---

## Key Findings

- **Chest pain type (`cp`)** is the dominant predictor (28.9% feature importance)
- **Number of major vessels (`ca`)** and **age** are the next most important features
- **Fasting blood sugar (`fbs`)** showed zero predictive value in this dataset
- No strong multicollinearity detected — all features contribute independently

---

## Setup

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn requests
```

### Run
1. Clone the repository
   ```bash
   git clone https://github.com/blacPanthe/ATHARVABAKDE.github.io.git
   ```
2. Open `Heart_Disease_Prediction_Modeling.ipynb` in Jupyter or Google Colab
3. Run all cells — the dataset loads automatically from Google Drive
