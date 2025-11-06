# Phishing URL Detection

This project focuses on detecting phishing websites using machine learning by analyzing URLs. The model learns patterns and features commonly found in phishing URLs and predicts whether a given URL is **Legitimate (1)** or **Phishing (0)**.

---

## 🔍 Project Overview

Phishing websites are malicious sites that attempt to steal sensitive user information. This project uses:

* URL-based feature extraction
* Preprocessing and encoding
* XGBoost classification model

The trained model is saved as **`xgboost_phishing_model.pkl`** so it can be reused for prediction.

---

## 📁 Repository Structure

```
phishing-url-detection/
│
├── PhiUSIIL_Phishing_URL_Dataset.csv    # Dataset used for training (uploaded as .zip)
├── Phishing_url.ipynb                   # Notebook containing model training & preprocessing
├── xgboost_phishing_model.pkl           # Saved trained model
└── README.md                            # Project documentation
```


```

---

## 🧠 Model
Multiple **Ensemble Machine Learning Models** were trained and evaluated for phishing URL classification:
| Model | Accuracy | Precision | Recall | F1 Score |
|-------|----------|-----------|--------|----------|
| Random Forest | 0.998346 | 0.997889 | 0.999221 | 0.998555 |
| AdaBoost | 0.994805 | 0.992845 | 0.998109 | 0.995470 |
| Gradient Boosting | 0.997455 | 0.996193 | 0.999370 | 0.997779 |
| **XGBoost (Chosen Model)** | **0.998791** | **0.998223** | **0.999666** | **0.998944** (Chosen Model)** | **Highest Accuracy** | Fast, robust, handles imbalance well |


After comparing all models, **XGBoost** was selected as the final model due to its superior performance and ability to generalize well.


The final trained model is saved as **`xgboost_phishing_model.pkl`** for deployment and predictions.


------|---------|
------|---------|
| 0 | Phishing URL |
| 1 | Legitimate URL |
---

