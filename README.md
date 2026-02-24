# 💳 Credit Card Default Prediction using Support Vector Machine (SVM)

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?style=flat&logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)
![Algorithm](https://img.shields.io/badge/Algorithm-SVM-purple?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

A machine learning project that predicts whether a credit card holder in Taiwan will **default on their next payment** using a **Support Vector Classifier (SVC)**. This project demonstrates a complete ML pipeline from data preprocessing to model evaluation.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Technologies Used](#-technologies-used)
- [Results](#-results)
- [How to Run](#-how-to-run)
- [Project Structure](#-project-structure)

---

## 🔍 Overview

Credit card default prediction is a critical problem in the banking and financial industry. Being able to identify customers who are likely to default allows financial institutions to take preventive action and manage risk effectively.

This project applies a **Support Vector Machine (SVM)** — a powerful classification algorithm that finds the optimal hyperplane to separate classes — to predict payment default based on customer financial data.

**Target Variable:** `default.payment.next.month` — whether the customer will default (1 = Yes, 0 = No)

---

## 📂 Dataset

**File:** `credit card taiwan svm algorithm.csv`

The dataset contains credit card client information from Taiwan, including:

- **Demographics** — Age, Gender, Education, Marital Status
- **Credit information** — Credit limit (`LIMIT_BAL`)
- **Payment history** — Past monthly payment status (PAY_0 to PAY_6)
- **Bill amounts** — Monthly bill statements (BILL_AMT1 to BILL_AMT6)
- **Payment amounts** — Monthly payment amounts (PAY_AMT1 to PAY_AMT6)
- **Target** — `default.payment.next.month` (binary)

> Missing values in the `AGE` column were handled by filling with the **column mean**.

---

## 🔄 Project Workflow

```
1. Data Loading & Exploration
       ↓
2. Data Preprocessing
   - Handled missing values in AGE (mean imputation)
   - Dropped irrelevant column (ID)
   - Defined features (X) and target (y)
       ↓
3. Train-Test Split (75% Train / 25% Test)
       ↓
4. Model Training — Support Vector Classifier (SVC)
   - kernel: RBF (default)
   - gamma: auto
       ↓
5. Model Evaluation
   - Predictions on test set
   - Model accuracy score
```

---

## 🛠 Technologies Used

| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Pandas | Data loading and manipulation |
| NumPy | Numerical operations |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | Model training & evaluation |
| Jupyter Notebook | Development environment |

---

## 📊 Results

The Support Vector Classifier (SVC) was trained with `gamma='auto'` and evaluated on 25% held-out test data using `model.score()` which returns the **accuracy** of the model.

> SVM is particularly effective for high-dimensional datasets and performs well even when the number of features exceeds the number of samples.

---

## ▶️ How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/sanzidd/Support-Vector-Machine-ML-.git
   cd Support-Vector-Machine-ML-
   ```

2. **Install required libraries**
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   ```

3. **Open the notebook**
   ```bash
   jupyter notebook "Support Vector Machine ML.ipynb"
   ```

4. **Run all cells** from top to bottom.

---

## 📁 Project Structure

```
Support-Vector-Machine-ML-/
│
├── Support Vector Machine ML.ipynb      # Main notebook with full ML pipeline
├── credit card taiwan svm algorithm.csv # Dataset
└── README.md                            # Project documentation
```

---

## 💡 Key Concepts Used

- **Support Vector Machine (SVM)** — finds the optimal decision boundary (hyperplane) that maximizes the margin between classes
- **RBF Kernel** — maps data into higher dimensions to handle non-linearly separable data
- **Mean Imputation** — fills missing values with the column average to preserve data integrity
- **Train-Test Split** — evaluates model performance on unseen data

---

## 🙋‍♂️ Author

**Sanzid**  
[![GitHub](https://img.shields.io/badge/GitHub-sanzidd-black?style=flat&logo=github)](https://github.com/sanzidd)

---

> ⭐ If you found this project helpful, feel free to give it a star!
