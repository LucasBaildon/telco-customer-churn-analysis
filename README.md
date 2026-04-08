# Customer Churn Prediction

![Status](https://img.shields.io/badge/status-in%20progress-yellow)

An end-to-end machine learning project analysing customer churn using the IBM Telco Customer Churn dataset. The objective is to identify customers likely to cancel their service and provide actionable insights to improve retention strategies.

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

| Step                      | Description                                                            |
| ------------------------- | ---------------------------------------------------------------------- |
| Data Cleaning             | Handled missing values and corrected data types                        |
| Exploratory Data Analysis | Analysed churn distribution and feature relationships                  |
| Feature Engineering       | Encoded categorical variables for modelling                            |
| Modelling                 | Trained a Logistic Regression model as a baseline                      |
| Evaluation                | Assessed performance using confusion matrix and classification metrics |

---

## Key Findings

* Churn accounts for ~26% of customers, indicating moderate class imbalance
* Customers on **month-to-month contracts** have significantly higher churn rates
* Customers with **short tenure** are more likely to churn

---

## Model Performance (WIP)

Initial baseline model:

* Logistic Regression classifier
* Evaluation using precision, recall, and F1-score

> Further improvements (feature importance, model comparison, and tuning) are in progress.

---

## Business Impact

The analysis highlights key drivers of customer churn, enabling businesses to:

* Target high-risk customers early in their lifecycle
* Incentivise long-term contracts to improve retention
* Optimise billing strategies to reduce churn risk

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

Download the dataset from Kaggle and place it in:

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

---

## Dataset

IBM Telco Customer Churn dataset (Kaggle)

Each row represents a customer, including:

* Demographics (gender, dependents)
* Account information (contract type, tenure, billing)
* Services used (internet, streaming, phone)

Target variable: `Churn` (Yes/No)

---

## Author

Lucas Baildon
https://github.com/LucasBaildon
https://linkedin.com/in/lucas-baildon
