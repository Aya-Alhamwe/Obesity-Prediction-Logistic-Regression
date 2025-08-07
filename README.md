# 📊 Obesity Level Prediction with Logistic Regression

## 🧠 Project Overview
This project aims to predict obesity levels using the **Obesity Level Prediction Dataset** through **Logistic Regression**.

Although Logistic Regression is usually used for binary classification, this project demonstrates how to adapt it to handle **multi-class classification** by implementing:

- ✅ One-vs-All (OvA)  
- ✅ One-vs-One (OvO)  
- ✅ Multinomial Logistic Regression (Softmax)

---

## 📁 Files

- `obesity_classification.ipynb`: Main notebook containing all code, visualizations, preprocessing, and model training.  
- `README.md`: Project overview, structure, and results.

---

## 📌 Problem Statement
The task is to classify individuals into **7 different obesity levels**, such as:

- Obesity Type I  
- Obesity Type II / III  
- Normal Weight, etc.

This makes it a **multi-class classification** problem.

---

## 🛠️ Technologies Used

- Python  
- Pandas, NumPy  
- Seaborn, Matplotlib (for visualizations)  
- Scikit-learn (for preprocessing, modeling, and evaluation)

---

## ⚙️ Pipeline Overview

The full machine learning pipeline includes:

1. **Loading the data**
2. **Exploratory Data Analysis (EDA)** with visualizations
3. **Data Preprocessing**
   - Checking for missing values
   - Standardizing numerical features
   - One-Hot Encoding for categorical features
   - Label encoding the target (`NObeyesdad`)
4. **Train-Test Split** (80/20 with stratification)
5. **Model Training** using three Logistic Regression strategies:
   - OvA (`multi_class='ovr'`)
   - OvO via `OneVsOneClassifier`
   - Softmax (`multi_class='multinomial'`)
6. **Evaluation** using accuracy score

---

## 📈 Results

| Strategy               | Accuracy   |
|------------------------|------------|
| One-vs-All (OvA)       | ~76.12%    |
| One-vs-One (OvO)       | ~92.2%     |
| Softmax (Multinomial)  | ~87.9%     |

✅ **One-vs-One gave the best performance** in this case.

---

## 🔄 Reusable Pipeline

The notebook includes a function:

```python
def obesity_risk_pipeline(data_path, test_size=0.2)
```
Which automates:

Data loading

Preprocessing

Training a Softmax-based Logistic Regression model

Printing accuracy

## 📌 Conclusion
This project shows how Logistic Regression can be effectively applied to multi-class problems, especially with the right strategy and preprocessing techniques.

## 📬 Contact
If you have any questions, ideas, or suggestions — feel free to reach out or open an issue!


