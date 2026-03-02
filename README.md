# 💰 Cost-Optimized Customer Churn Decision System

## 📌 Business Goal
Telecom companies lose revenue when customers churn.
Retention campaigns cost money, so contacting every customer is inefficient.

This project builds a churn decision system that minimizes total business loss by optimizing prediction thresholds using financial cost.

---

## 📊 Dataset
Telco Customer Churn (Kaggle)

After cleaning:
- 7032 customers
- 20 features
- Target: Churn (~27% positive rate)

---

## 🤖 Models Evaluated
- Logistic Regression (class_weight balanced)
- Random Forest (class_weight balanced)
- SMOTE-based models
- XGBoost (scale_pos_weight)

Evaluation Metrics:
- ROC-AUC
- PR-AUC (important for imbalance)
- Recall & Precision

---

## 💸 Cost Function

False Negative (missed churn): ₹5000  
False Positive (unnecessary retention offer): ₹500  

Total Business Loss:
Total Cost = (FP × 500) + (FN × 5000)

---

## 🏆 Business Impact

Cost-optimized threshold tuning reduced simulated loss:

- Baseline Cost: ₹357,500
- Optimized Cost: ₹263,000
- Total Savings: ₹94,500
- ≈ 26% reduction in business loss

This demonstrates how machine learning should align with financial objectives rather than accuracy alone.

---

## 🛠 How to Run

Install dependencies:

pip install -r requirements.txt

Open notebook:

notebook/churn project.ipynb