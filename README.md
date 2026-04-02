# Customer Churn Prediction

![Status](https://img.shields.io/badge/status-in%20progress-yellow)
 
A machine learning project exploring customer churn on the [IBM Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn). The goal is to identify customers likely to cancel their service, enabling businesses to intervene with targeted retention strategies.
 
---
 
## Project Structure
 
```
├── notebook.ipynb          # Main analysis notebook
├── data/
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv   # Raw dataset (not tracked by git)
├── requirements.txt        # Python dependencies
└── README.md
```
 
---
 
## Approach
 
| Step | Description |
|------|-------------|
| Data Overview | Shape, dtypes, and summary statistics |
| Missing Values | Identify and handle nulls or inconsistencies |
| EDA | Visualise churn distribution and key feature relationships |
| Feature Analysis | Contract type, tenure, charges vs. churn |
 
---
 
## Key Findings
 
- The dataset is moderately imbalanced, with churn accounting for roughly 26% of customers.
- Customers on **month-to-month contracts** churn at significantly higher rates than those on annual or two-year contracts.
 
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
 
Download the Telco Customer Churn dataset from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) and place it in a `data/` directory:
 
```
data/WA_Fn-UseC_-Telco-Customer-Churn.csv
```
 
> You'll need a Kaggle account. You can also use the Kaggle CLI:
> ```bash
> kaggle datasets download -d blastchar/telco-customer-churn -p data/ --unzip
> ```
 
### 4. Run the notebook
 
```bash
jupyter notebook notebook.ipynb
```
 
---
 
## Requirements
 
- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- jupyter
 
See `requirements.txt` for pinned versions.
 
---
 
## Dataset
 
**IBM Telco Customer Churn** — [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
 
Each row represents a customer. Features include demographics (gender, age, dependents), account details (contract type, tenure, billing), and service usage (phone, internet, streaming). The target variable is `Churn` (Yes/No).
 
---
 
## Author
 
Lucas Baildon — [GitHub](https://github.com/LucasBaildon) · [LinkedIn](https://linkedin.com/in/lucas-baildon)
