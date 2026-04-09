# Customer Churn Prediction

![Status](https://img.shields.io/badge/status-complete-brightgreen)

An end-to-end machine learning project analysing customer churn using the IBM Telco Customer Churn dataset. The objective is to predict customer churn and derive **model-backed business insights** to improve retention strategies.

---

## Project Structure

```
├── notebook.ipynb          # Main analysis and modelling notebook
├── data/
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv   # Raw dataset (not tracked by git)
├── requirements.txt        # Python dependencies
└── README.md
```

---

## Approach

| Step                      | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| Data Exploration          | Examined dataset structure, distributions, and missing values               |
| Data Cleaning             | Converted data types, handled missing values, encoded target variable       |
| Feature Engineering       | Removed identifiers, one-hot encoded categorical variables, scaled features |
| Train/Test Split          | Stratified split to preserve churn distribution                             |
| Modelling                 | Logistic Regression (baseline) and Random Forest (comparison model)         |
| Evaluation                | Precision, Recall, F1-score, ROC-AUC, confusion matrix                      |
| Cross-Validation          | 5-fold stratified validation for robust performance estimates               |
| Feature Importance        | Interpreted drivers using coefficients and tree-based importance            |

---

## Models Used

### Logistic Regression
- `class_weight="balanced"` to address class imbalance (~26% churn)
- Feature scaling applied
- Interpretable coefficients for business insights

### Random Forest
- Captures non-linear relationships
- No scaling required
- Used for performance comparison and feature importance

---

## Key Findings

### Data Insights
- Churn rate is ~26%, indicating moderate class imbalance
- Customers on **month-to-month contracts** churn significantly more
- **Short tenure** strongly correlates with higher churn

### Model-Driven Insights

- **Contract Type**
  - Month-to-month → strong churn driver  
  - Two-year contracts → strong retention factor  
  → Incentivise long-term contracts

- **Tenure**
  - Longer tenure reduces churn risk significantly  
  → Focus on early customer lifecycle (first 6 months)

- **Payment Method**
  - Electronic check → higher churn  
  - Auto-pay methods → lower churn  
  → Encourage automatic payments

- **Fiber Optic Internet**
  - Associated with higher churn  
  → Investigate pricing, service quality, or expectations

---

## Model Evaluation

Models were evaluated using:

- Classification Report (Precision, Recall, F1-score)
- Confusion Matrix
- ROC Curve and ROC-AUC score

> Accuracy was not prioritised due to class imbalance.

### Additional Validation

- 5-fold **Stratified Cross-Validation** used for more reliable performance estimates

---

## Feature Importance

- **Logistic Regression**
  - Coefficients used to identify positive/negative churn drivers

- **Random Forest**
  - Feature importance scores used to rank influential variables

These insights directly support business recommendations.

---

## Business Impact

This project moves beyond prediction into **actionable insights**:

- Identify high-risk customers early
- Improve onboarding and early retention strategies
- Encourage long-term contracts and auto-pay adoption
- Investigate churn drivers in specific services (e.g. fiber)

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/LucasBaildon/customer-churn-prediction.git
cd customer-churn-prediction
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the dataset

Download from Kaggle and place in:

```
data/WA_Fn-UseC_-Telco-Customer-Churn.csv
```

Or via CLI:

```bash
kaggle datasets download -d blastchar/telco-customer-churn -p data/ --unzip
```

### 4. Run the notebook

```bash
jupyter notebook notebook.ipynb
```

---

## Requirements

See `requirements.txt` for full dependencies.

Key libraries include:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

---

## Dataset

IBM Telco Customer Churn dataset (Kaggle)

Each row represents a customer, including:

- Demographics (gender, dependents)
- Account information (contract type, tenure, billing)
- Services used (internet, streaming, phone)

**Target variable:** `Churn` (binary: 0 = No, 1 = Yes)

---

## Author

Lucas Baildon  
https://github.com/LucasBaildon  
https://linkedin.com/in/lucas-baildon
