# Credit Card Fraud Detection

[![Made with Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)]()
[![Jupyter Notebook](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)]()
[![Kaggle](https://img.shields.io/badge/Kaggle-Projects-20beff?logo=kaggle)]()

This project focuses on detecting fraudulent credit card transactions using machine learning techniques on a highly imbalanced dataset. The aim is to maximize detection (recall) of fraudulent transactions while minimizing false alarms.

---

## 📌 Problem Statement

Credit card fraud is rare (<0.2% of transactions), making standard accuracy metrics misleading. The challenge is to correctly detect fraudulent transactions while avoiding unnecessary false positives.

---

## 📊 Dataset

- **Source:** [Kaggle – Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- **Rows:** 284,807 transactions  
- **Fraudulent cases:** 492 (~0.17%)  
- **Features:** PCA-transformed (V1–V28), plus `Time` and `Amount`  
- **Target:** `Class` (0 = legitimate, 1 = fraud)  

> ⚠️ Dataset is not included due to size constraints (>150MB). See **Data** section below.

---

## 📂 Project Structure

```
credit-card-fraud-detection/
├── notebook.ipynb
├── requirements.txt
└── data/
├── .gitignore
└── README.md
```


- `notebook.ipynb` – Full workflow: EDA, preprocessing, modeling, evaluation  
- `requirements.txt` – Dependencies  
- `data/` – Instructions for downloading the dataset  

---

## 🔍 EDA & Preprocessing

- Confirmed **extreme class imbalance**  
- Checked for missing values → none  
- Scaled `Amount` feature  
- Stratified K-Fold used for train-test splitting  
- Applied **SMOTE** on training folds only  
- Threshold tuning applied to improve recall

---

## 🤖 Model

- **Algorithm:** RandomForestClassifier  
- **Training Strategy:** Stratified 5-Fold Cross-Validation  
- **Class Imbalance Handling:** SMOTE oversampling  
- **Threshold Tuning:** Adjusted probability threshold to improve recall

---

## ✅ Results

| Metric                 | Before Threshold Tuning | After Threshold Tuning |
| ---------------------- | ----------------------- | ---------------------- |
| Mean Recall            | 0.83                    | 0.87                   |
| Mean Average Precision | 0.85                    | 0.85                   |
| Accuracy               | 99.8%                   | 99.8%                  |

> Custom threshold significantly reduced false negatives while keeping false positives manageable.

---

## 🚀 How to Run

1. **Clone the repo:**
```bash
git clone https://github.com/<your-username>/kaggle-work.git
cd kaggle-work/credit-card-fraud-detection
```

2. **Install dependencies:**

```bash
pip install -r requirements.txt
```

3. **Download dataset from Kaggle:**

```bash
https://www.kaggle.com/mlg-ulb/creditcardfraud
```

4. **Place the CSV in:**

```bash
data/raw/creditcard.csv
```

5. **Open the notebook:**

```
jupyter notebook notebook.ipynb
```

---


## 🔜 Future Improvements

 - Try boosting algorithms (XGBoost, LightGBM, CatBoost)

 - Add SHAP / LIME explainability

 - Deploy as an interactive Streamlit dashboard

 - Cost-sensitive learning for additional fraud penalty
  
 ---

 

### Author: `Sukrat Singh`
⭐ Star this repo if you find it helpful!
