# ⚽ Football Match Result Prediction using MLflow Champion–Challenger Workflow

![Python](https://img.shields.io/badge/Python-3.x-blue)
![MLflow](https://img.shields.io/badge/MLflow-Experiment%20Tracking-orange)
![Databricks](https://img.shields.io/badge/Databricks-ML-red)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-green)

## 📌 Project Overview

This project demonstrates an end-to-end Machine Learning lifecycle using **Databricks**, **MLflow**, and **Unity Catalog**.

The objective is to predict the outcome of a football match:

- 🏠 Home Win
- 🤝 Draw
- 🚗 Away Win

Instead of focusing only on model accuracy, this project implements a **Champion–Challenger architecture**, where a better-performing model is automatically promoted to become the new production Champion.

---

# 🏗️ Project Architecture

```
Football Match Dataset
            │
            ▼
Data Understanding
            │
            ▼
Data Preparation
            │
            ▼
Train Champion (Decision Tree)
            │
            ▼
MLflow Experiment Tracking
            │
            ▼
Register Champion Model
            │
            ▼
Champion Inference
            │
            ▼
Train Challenger (Logistic Regression)
            │
            ▼
Compare Macro F1 Score
            │
            ▼
Automatic Promotion
            │
            ▼
Champion Alias Updated
            │
            ▼
Inference using Stable Alias
```

---

# 📂 Repository Structure

```
football-mlflow-champion-challenger/

│
├── notebooks/
│   ├── 01_Data_Understanding.ipynb
│   ├── 02_Data_Preparation.ipynb
│   ├── 03_Champion_Model.ipynb
│   ├── 04_Champion_Registry.ipynb
│   ├── 05_Champion_Inference.ipynb
│   ├── 06_Challenger_Model.ipynb
│   ├── 07_Automatic_Promotion.ipynb
│   └── 08_Final_Inference.ipynb
│
├── screenshots/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# 📊 Dataset

Football Match Statistics Dataset

Target Variable

- match_result

Possible Classes

- Home Win
- Draw
- Away Win

Dataset Split

| Dataset | Rows |
|----------|------|
| Training | 15,999 |
| Testing | 4,000 |

Features

- Numerical Features: 51
- Categorical Features: 6

To prevent target leakage, the following columns were removed:

- home_score
- away_score

---

# ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Databricks
- MLflow
- Unity Catalog
- Matplotlib
- Git
- GitHub

---

# 🤖 Models

## Champion Model

Algorithm

DecisionTreeClassifier

Performance

- Accuracy: **0.3558**
- Macro F1: **0.3407**

---

## Challenger Model

Algorithm

LogisticRegression

Performance

- Accuracy: **0.6515**
- Macro F1: **0.6222**

---

# 📈 Model Comparison

| Model | Accuracy | Macro F1 |
|---------|----------|----------|
| Decision Tree | 0.3558 | 0.3407 |
| Logistic Regression | 0.6515 | 0.6222 |

## Improvement

Absolute Macro F1 Improvement

```
0.6222 - 0.3407 = 0.2815
```

Relative Improvement

```
82.62%
```

---

# 🚀 Champion–Challenger Workflow

1. Train Champion Model
2. Log Experiment to MLflow
3. Register Champion
4. Run Champion Inference
5. Train Challenger
6. Compare Evaluation Metrics
7. Register Better Model
8. Promote Challenger
9. Update Champion Alias
10. Perform Inference using Stable Alias

---

# 🏷️ Model Registry

Registered Model

```
workspace.default.football_match_result_model
```

Champion Alias

```
champion
```

Before Promotion

```
Version 2
Decision Tree
```

After Promotion

```
Version 3
Logistic Regression
```

The previous Champion remains available for rollback.

---

# 📷 Project Screenshots

The `screenshots` folder contains:

- MLflow Experiment
- Champion Results
- Challenger Results
- Automatic Promotion
- Model Registry
- Final Inference

---

# 📌 Key Learning Outcomes

✔ MLflow Experiment Tracking

✔ Databricks Model Registry

✔ Unity Catalog

✔ Champion–Challenger Architecture

✔ Automatic Model Promotion

✔ Stable Alias-Based Inference

✔ Model Versioning

✔ GitHub Version Control

---

# 👨‍💻 Author

**Pranav Sujit Nair**

M.Sc. Applied Data Science and Artificial Intelligence

SRH University Hamburg

---

# ⭐ Acknowledgements

This project was developed as part of the Machine Learning coursework using Databricks and MLflow.
