# 🤖 Machine Learning Project — Classification Pipeline

This project demonstrates a **full machine learning workflow**: from data cleaning and exploratory analysis to model training, hyperparameter tuning, and model interpretation.  
The goal was to compare multiple algorithms and extract **business insights** using feature importance and SHAP values.  

---

## 📂 Workflow

1. **Data Preprocessing**
   - Outlier removal (IQR)
   - Missing value imputation
   - Feature scaling (StandardScaler) and encoding (OneHotEncoder)
   - PCA for correlated variables

2. **Exploratory Data Analysis**
   - Distribution plots (histograms, boxplots)
   - Correlation heatmaps
   - Target balance check

3. **Modeling**
   - Logistic Regression
   - Random Forest
   - Gradient Boosting
   - XGBoost
   - Voting Ensemble (soft voting)

4. **Hyperparameter Tuning**
   - Performed with `GridSearchCV` (5-fold Stratified CV)
   - Selected best models based on **ROC AUC**

5. **Evaluation**
   - Metrics: Accuracy, F1 Score, ROC AUC
   - ROC & Precision-Recall curves
   - Confusion matrix
   - Calibration plots
   - Probability histograms

6. **Interpretability**
   - Feature importance (RF, GB, LR coefficients)
   - SHAP values (Logistic Regression & Gradient Boosting)

---

## 📊 Results

- **Gradient Boosting** and **Random Forest** achieved the best ROC AUC (~0.97–0.98).  
- **Logistic Regression** underperformed but provided interpretability.  
- **Voting Ensemble** improved robustness but not significantly beyond best single models.  
- SHAP analysis confirmed the most impactful features aligned with domain intuition.  

---

## 🔑 Insights
- Some engineered features (e.g., PCA component) carried significant predictive power.  
- Ensemble methods provided stability across folds.  
- SHAP values allowed mapping feature importance to **business-level recommendations**.  

---

## 🚀 Future Work
- Test advanced ensemble methods (Stacking, LightGBM, CatBoost)  
- Experiment with deep learning models for comparison  
- Deploy best model as an API (Flask/FastAPI)  

---

## 📌 Repository
👉 [GitHub: Zhalgas03/Machine-Learning](https://github.com/Zhalgas03/Machine-Learning)
