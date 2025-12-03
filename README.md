# Healthcare Provider Fraud Detection  
Machine Learning Project – GIU Berlin (Winter 2025)

This project builds a machine learning system to identify potentially fraudulent healthcare providers using Medicare claim data. It includes data preprocessing, feature engineering, model training, model evaluation, and a complete fraud-analysis pipeline.

---

## 📁 Project Structure

- **notebooks/**
  - `01_data_exploration_and_feature_engineering.ipynb`
  - `02_modeling.ipynb`
  - `03_evaluation.ipynb`
- **data/**
  - Raw and processed datasets  
- **models/**
  - Tuned Logistic Regression, Random Forest, and XGBoost models  
- **reports/**
  - Final technical report and presentation slides  

---

## 🧬 Data Used
The project uses 4 Medicare claim datasets:
- Beneficiary data  
- Inpatient claims  
- Outpatient claims  
- Provider fraud labels  

The data is merged and aggregated **per Provider**, which is the unit of prediction.

---

## 🔧 Pipeline Summary

### 1. **Data Preparation**
- Merge inpatient, outpatient, beneficiary, and labels datasets  
- Clean missing values  
- Aggregate all information to provider level  

### 2. **EDA & Feature Engineering**
- Explore fraud vs non-fraud patterns  
- Create financial, count, and ratio features  
- Handle skew and outliers  

### 3. **Modeling**
Models trained:
- Logistic Regression  
- Random Forest  
- XGBoost  

Class imbalance handled using:
- Stratified split  
- Class weights  
- Scale_pos_weight (XGBoost)

Hyperparameter tuning performed for all models.

### 4. **Evaluation**
Metrics:
- Precision  
- Recall  
- F1-score  
- ROC-AUC  
- PR-AUC (main metric)

Visualizations:
- Confusion matrices  
- ROC curves  
- Precision–Recall curves  

**Best model: XGBoost** (highest PR-AUC).

### 5. **Error Analysis**
- False Positives: providers that look suspicious but are legitimate  
- False Negatives: subtle fraud patterns not captured by current features  

---

## 🚀 Key Findings
- XGBoost is the most effective model for fraud detection  
- Fraudulent providers often show unusually high reimbursement and claim patterns  
- Subtle fraud requires richer features (temporal or diagnosis-based)

---

## 📦 Deliverables
- Cleaned datasets  
- Tuned models  
- Full notebook pipeline  
- Technical report (PDF)  
- Presentation slides  

