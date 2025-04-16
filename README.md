# 🏥 Hospital Readmission Risk Prediction

This project uses machine learning to predict whether a patient will be readmitted to the hospital within 30 days of discharge. It leverages the UCI Diabetes Readmission Dataset and focuses on building interpretable models to support better clinical decisions.

## 🔍 Objective
To build a classification model that can predict high-risk patients and help hospitals reduce avoidable readmissions, lower costs, and improve care quality.

---

## 📦 Dataset

- **Source:** [UCI ML Repository – Diabetes 130-US hospitals](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008)
- **Records:** ~100,000 hospital encounters
- **Target Variable:** `readmitted` (within 30 days or not)

---

## 🧰 Tools & Libraries

- Python  
- Scikit-learn  
- XGBoost  
- SHAP (Explainability)  
- Matplotlib / Seaborn  
- Google Colab

---

## 🔄 Workflow

1. **Data Cleaning**
   - Handled missing values
   - Dropped high-null or irrelevant columns
   - Balanced dataset via upsampling

2. **Feature Engineering**
   - One-hot encoded categorical variables
   - Removed identifiers and low-variance features

3. **Modeling**
   - Trained Logistic Regression, Random Forest, and XGBoost
   - Evaluated using Accuracy, F1-score, ROC AUC

4. **Explainability**
   - Used SHAP for global and local interpretability
   - Visualized top features influencing predictions

---

## 🧠 Results

| Model               | Accuracy | F1-Score | ROC AUC |
|---------------------|----------|----------|---------|
| Logistic Regression | 62%      | 0.62     | 0.676   |
| Random Forest       | 100%     | 1.00     | 0.999   |
| XGBoost             | **69%**  | **0.69** | **0.755** |

✅ **XGBoost performed best** with balanced generalization and interpretability.

---

## 📊 SHAP Summary Plot

The model revealed that `number_inpatient`, `discharge_disposition_id`, and `number_diagnoses` were the most impactful features.

---

## 🚀 Run This Notebook

Open the notebook in Google Colab:

https://colab.research.google.com/drive/1HyrJkC5lum3XkyEgwUtaoxMrK2BQafDX

1. Upload the dataset (`diabetic_data.csv`)
2. Run all cells
3. View metrics, SHAP plots, and predictions

---

## 🏁 Future Improvements

- Deploy via Streamlit or FastAPI
- Add patient follow-up recommendation engine
- Extend to other chronic disease datasets

---

## 📬 Contact

**Author:** Alen George 
**Email:** alengeorge654@gmail.com  
**LinkedIn:** https://www.linkedin.com/in/alengeorge9307/
