# 🌿 ML-Powered Stress Recognition and Wellness Recommendation System  

This project uses **machine learning** to detect stress levels and provide personalized wellness recommendations.  
By combining demographic, behavioral, and health-related data, the system improves accuracy compared to traditional self-reports.  

---

## 📊 Dataset  
We used the [Sleep Health and Lifestyle Dataset](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset?resource=download) (374 participants).  

**Features included:**  
- Demographics: Age, Gender  
- Sleep: Duration, Quality  
- Activity: Daily steps, Activity level  
- Health: Blood pressure, Heart rate, BMI  
- Target: Stress level (1–10 scale, later binarized)  

---

## ⚙️ Methodology  
1. **Preprocessing**  
   - Mean imputation for missing data  
   - Normalization of features  
   - Feature engineering (average sleep quality, aggregated activity)  

2. **Models Used**  
   - Logistic Regression (baseline, interpretable)  
   - Support Vector Machine (robust in high-dimensional space)  
   - XGBoost (captures complex non-linear relationships)  

3. **Ensemble Meta-Model**  
   - Stacking approach with Logistic Regression as the meta-classifier  
   - Combines outputs of base models into a final prediction  

---

## 📈 Results  
| Model               | Accuracy | Precision | Recall | F1-Score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression  | 0.81     | 0.82      | 0.81   | 1.00     |
| SVM                  | 0.41     | 0.08      | 0.17   | 0.80     |
| XGBoost              | 1.00     | 1.00      | 1.00   | 0.11     |
| **Meta-Model**
