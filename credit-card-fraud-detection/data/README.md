# Data Folder

This folder contains information about the dataset used in this project.  

> ⚠️ The dataset is **not included** due to size constraints (>150MB) and GitHub file limits.

---

## 📥 Dataset Source

You can download the Credit Card Fraud Detection dataset from Kaggle:

**Kaggle link:** [Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)

---

## 📂 Folder Structure
```
data/
├── raw/ # Place the downloaded CSV file here
└── processed/ # Optional: store cleaned or scaled dataset
```

After downloading, place the file as:



`data/raw/creditcard.csv`


The notebook (`notebook.ipynb`) will automatically load the dataset from this location.

---

## Notes:-

- The dataset is highly imbalanced (~0.17% fraud).  
- Preprocessing (scaling, SMOTE) is applied in the notebook.  
- Keeping raw data separate allows reproducibility and avoids committing large files to GitHub.