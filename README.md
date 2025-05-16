# Forecasting-Municipal-Debt-with-Machine-Learning

<img width="656" alt="Image" src="https://github.com/user-attachments/assets/65f26cf7-82a6-4301-b40e-549250289f3e" />

-----------------------------------------------
## 📌 Description   
This project applies machine learning to assess and predict the likelihood of bad debt in municipal financial systems. Using real-world billing and payment data from South African municipalities, the goal is to assist in proactive financial planning and risk mitigation.

## 🎯 Objective  
To build a predictive model that can identify high-risk municipal accounts likely to become bad debts. This tool will help municipalities improve financial stability by enabling early intervention and smarter resource allocation.

## 📂 Dataset Source  
- The dataset is publicly available on Kaggle:  
  [Municipal Debt Dataset – Kaggle](https://www.kaggle.com/datasets/paresh2047/municipal-debt-data)

It includes 2 years of billing, payment, property, and consumer identity data from 8 municipalities.

## 🧠 Machine Learning Models Used  
Three supervised learning models were implemented and compared:

- **CatBoost**: Gradient boosting optimized for categorical data  
- **MLP Classifier**: Deep learning-based Multilayer Perceptron  
- **Random Forest**: Ensemble-based decision tree classifier

## 🚀 How to Run the Code

### Option 1: Run via Notebook
1. Open Jupyter Notebook:
   ```bash
   jupyter notebook notebooks/Municipal_debt_risk_ML.ipynb
   ```

2. Run all cells step by step (from data preprocessing to model evaluation).

### Option 2: Run via Python Scripts (if split into modules)
```bash
python src/preprocessing.py
python src/model_training.py
python src/evaluation.py
```

Make sure the dataset is placed in the `data/` folder.

## 📈 Key Results and Evaluation

| Model          | AUC Score | False Negatives | False Positives |
|----------------|-----------|------------------|------------------|
| **CatBoost**       | **1.00**      | 56               | 0                |
| MLP Classifier | 0.99      | 847              | 2                |
| Random Forest  | 0.99      | Similar to CatBoost | Higher than CatBoost |

- **CatBoost** performed best with perfect AUC and no false positives.
- Property value, property size, and collection ratio were important predictors.
- The models showed promise but highlight issues like data imbalance and quality, which should be improved in future work.
