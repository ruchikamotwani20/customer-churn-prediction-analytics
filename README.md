# Predictive Analytics: Building a Customer Churn Prediction Model
<div align="justify">
An end to end machine learning project to proactively identify customers at risk of churning, using Python, Pandas, and a recall optimized Random Forest model.

## 📊 Interactive Dashboard Preview

![Churn Risk Dashboard Preview](results/visualizations/screnshot_dashboard.png)

🔗 [View the full interactive dashboard on Tableau Public](https://public.tableau.com/views/CustomerChurnPredictionRiskAnalyticsDashboard/CustomerChurnRiskIntelligenceDashboard?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## 🚨 1. The Business Challenge

A telecommunications company faces a critical problem: customer retention. Acquiring a new customer costs significantly more than retaining an existing one. The key business goal is to minimize missed at risk customers, enabling proactive intervention.

🎯 **Key Business Question**

> _Can we build a model that reliably identifies the majority of customers who are likely to churn?_

---

## ✅ 2. The Solution & Key Results

A complete machine learning pipeline was developed, from data cleaning and EDA to automated model tuning with `GridSearchCV`. The final result is a Random Forest Classifier optimized for recall, designed to maximize the detection of at risk customers.

**📈 Model Performance (on Unseen Test Data):**
| Metric           | Score  | Business Impact                                     |
|------------------|--------|-----------------------------------------------------|
| Recall Churn)    | 72%    |Identifies the majority of customers truly at risk   |
| Overall Accuracy | 79%    |Correctly predicts ~8 out of 10 outcomes             |
| Precision (Churn)| 55%    |Acceptable trade off to maximize the detection rate  |

---

## 💡 3. Actionable Business Recommendations

This model enables a shift from reactive to proactive retention. The predictions can be transformed into a concrete business strategy:

### 🎯 Tiered Risk Segmentation
Instead of treating all at risk customers equally, segment them by churn probability to manage retention efforts effectively.
- **Critical Risk (≥ 80%)** → Target with immediate, high value interventions (e.g., personal calls).
- **High Risk (65–80%)** → Target with automated, personalized offers (e.g., email campaigns).
- **Moderate Risk (50–65%)** → Include in broad loyalty programs and monitor.

### 📋 Proactive Retention Watchlist Dashboard
- A Tableau dashboard (from exported CSV) serves as a **daily watchlist**.
- Helps the retention team prioritize outreach by risk level.

### 🔍 Root Cause Analysis
- Analyze churn prone profiles (e.g., contract types, services).
- Feed insights into pricing/product strategies to reduce churn long term.

---

## 🔄 4. Workflow & Methodology

1. **EDA & Cleaning**  
   Discovered strong churn patterns (e.g., Month to Month contracts).

2. **Preprocessing**  
   Used `ColumnTransformer` pipeline:
   - `StandardScaler` → numerical  
   - `OneHotEncoder` → categorical  
   - No leakage, fully reusable

3. **Model Training & Tuning**  
   - `RandomForestClassifier`  
   - `GridSearchCV` for hyperparameter optimization (recall focused)

4. **Model Evaluation**  
   - Tested on unseen data  
   - Exported results to CSV for business use

5. **Deployment Output**  
   - Used for dashboard creation in Tableau

---

## 🛠️ 5. Technical Stack

| Category         | Tools/Libraries                          |
|------------------|------------------------------------------|
| Language         | Python                                   |
| Libraries        | Pandas, Scikit-learn, Matplotlib, Seaborn|
| Environment      | Jupyter Notebook / Google Colab          |
| Visualization    | Tableau Public                           |

---

## 📊 Interactive Dashboard

Explore the full dashboard, segment risk levels, and customer insights:

🔗 [**Customer Churn Intelligence Dashboard** on Tableau Public](https://public.tableau.com/views/CustomerChurnPredictionRiskAnalyticsDashboard/CustomerChurnRiskIntelligenceDashboard?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

</div>

## 📁 Repository Contents

| Path | Description |
|------|-------------|
| [`data/WA_Fn-UseC_-Telco-Customer-Churn.csv`](data/WA_Fn-UseC_-Telco-Customer-Churn.csv) | Main dataset of telco customer profiles and churn labels. |
| [`notebooks/churn_analysis_and_modeling.ipynb`](notebooks/churn_analysis_and_modeling.ipynb) | Main Jupyter Notebook containing full workflow: EDA, preprocessing, modeling, and evaluation. |
| [`notebooks/churn_analysis_and_modeling.py`](notebooks/churn_analysis_and_modeling.py) | Python script version of the notebook for automation or reuse. |
| [`results/churn_risk_analysis_recall_optimized.csv`](results/churn_risk_analysis_recall_optimized.csv) | Final churn predictions with probabilities and labels for the full customer base. |



