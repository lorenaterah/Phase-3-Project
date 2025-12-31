# Telecom Customer Churn Prediction

## Project Overview
This project aims to **predict customer churn** for a telecom company using demographic, account, and usage data. The goal is to identify customers likely to leave so that proactive retention strategies can be applied, reducing revenue loss and improving customer satisfaction.

The project involves **data preprocessing, exploratory data analysis (EDA), feature selection, model training, and evaluation** of multiple classification models.

---

## Dataset
- **Number of records:** 3,333 customers  
- **Number of features:** 21  
- **Target variable:** `churn` (1 = churned, 0 = stayed)  
- **Feature types:**  
  - **Numerical:** account length, total day/eve/night/intl minutes & charges, number of voicemail messages, customer service calls  
  - **Categorical:** state, area code, international plan, voice mail plan  

**Note:** The target is imbalanced, with fewer churners than non-churners.

---

## Project Steps

1. **Data Understanding & EDA**  
   - Analyze distributions, correlations, and relationships between features and churn.  
   - Identify outliers and anomalies.  

2. **Data Preprocessing**  
   - Handle missing values and inconsistencies.  
   - Encode categorical features.  
   - Scale numerical features.  
   - Select top predictive features.  

3. **Model Training**  
   - Models trained: Logistic Regression, Decision Tree, Random Forest, Random Forest with threshold adjustment.  
   - Iterative approach: preprocessing → feature selection → training → evaluation → tuning.  

4. **Model Evaluation**  
   - Metrics: Accuracy, Precision, Recall, F1-score (focus on churn class).  
   - **Best-performing model:** Random Forest with threshold 0.3 (highest F1 = 0.74 for churners).  

---

## Key Findings
- **High-risk churners:** Customers with high customer service calls, international plans, or heavy daytime usage.  
- **Model Insights:** Threshold-adjusted Random Forest balances precision and recall, making it ideal for retention campaigns.  
- Decision Tree offers interpretability but slightly lower F1.  
- Logistic Regression underperforms for churn detection.  

---

## Recommendations
- Deploy **Random Forest (Threshold 0.3)** for churn prediction.  
- Target high-risk customers proactively to reduce churn.  
- Monitor and retrain the model periodically with updated customer data.  
- Adjust classification thresholds based on business priorities.  
- Use key predictive features to guide marketing and retention campaigns.  

---

## Project Deliverables
- Python notebooks for EDA, preprocessing, and modeling.  
- Visualizations: correlation heatmaps, boxplots, feature importance charts, and model comparison charts.  
- Slides for presentation summarizing objectives, EDA, models, evaluation, and recommendations.  

---

## Tools & Libraries
- Python (pandas, numpy, matplotlib, seaborn, scikit-learn)  
- Jupyter Notebook / Google Colab  
- Optional: PowerPoint / Google Slides / Canva for presentation
