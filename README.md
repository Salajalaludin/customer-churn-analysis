# Customer Churn Analysis & Retention Strategy  
**Case Study: KKBox Subscription-Based Business**

## 📌 Project Overview
Customer churn is a critical challenge for subscription-based businesses. This project analyzes customer churn behavior using the **KKBox Churn Prediction Challenge dataset**, with the goal of identifying key churn drivers and translating insights into actionable retention strategies.

The project focuses not only on predicting churn, but more importantly on **understanding why customers churn** and **how the business can proactively reduce churn**.

---

## 🎯 Business Objectives
1. Identify key factors associated with customer churn  
2. Analyze customer behavior across subscription, payment, and engagement dimensions  
3. Provide data-driven retention strategies based on observed churn drivers  

---

## 🗂 Dataset Overview
Data sourced from the **KKBox Churn Prediction Challenge (Kaggle)**, consisting of multiple relational tables:

- **train.csv / train_v2.csv** – churn labels  
- **members.csv / members_v3.csv** – user demographics & registration info  
- **transactions.csv / transactions_v2.csv** – subscription & payment history  
- **user_logs.csv / user_logs_v2.csv** – user listening behavior  

Time window used for analysis: **October 2016 – March 2017**

---

## 🧹 Data Cleaning & Preparation
Key preprocessing steps include:
- Cleaning extreme outliers in user age (`bd`)
- Handling missing demographic values using median imputation
- Removing duplicated transaction records
- Validating transaction dates (e.g., expiration before transaction date)
- Ensuring no data leakage from post-churn information

All datasets were then integrated into a single analytical table.

---

## 🏗 Feature Engineering
Features were engineered across four main dimensions:

### 1. User Demographics & Registration
- `city`, `bd`, `gender`, `registered_via`
- `registration_init_time`

### 2. Subscription Lifecycle
- `tenure`
- `total_renewals`
- `avg_plan_duration`
- `tenure_group`

### 3. Payment & Discount Behavior
- `avg_discount_amount`
- `discount_frequency`
- `num_payment_methods`
- `favorite_payment_method`
- `discount_group`

### 4. User Activity & Engagement
- `total_listening_days`
- `total_secs_accumulated`
- `recent_secs`
- `previous_secs`
- `activity_trend`
- `days_since_last_listen`
- `last_activity_date`

**Final dataset shape:**  
- **Rows:** 1,963,891  
- **Columns:** 23  

---

## 📊 Exploratory Data Analysis (EDA)
Key analyses conducted:
- Churn rate by **tenure group**
- Churn rate by **payment method**
- Churn rate by **discount level**
- Churn rate by **city**
- Churn rate by **activity trend**

### Key Observations
- Churn peaks during **early lifecycle (1–6 months)** and **mid-loyalty phase (1–3 years)**
- Certain payment methods exhibit **significantly higher churn**
- Discount-heavy users show **substantially higher churn**, indicating price sensitivity
- Engagement momentum (activity trend) is a strong churn signal
- Geographic differences indicate localized churn behavior

---

## 🔍 Key Driver Analysis (Correlation-Based)
### Factors Increasing Churn Risk
- Longer average plan duration
- Higher discount dependency
- Longer inactivity periods
- Frequent discount usage
- Multiple payment methods

### Factors Supporting Retention
- High number of renewals (strongest signal)
- Stable favorite payment method
- High listening frequency and recency
- Deep historical engagement

**Conclusion:**  
Churn is driven primarily by **behavioral and transactional factors**, not demographics.

---

## 💡 Business Insights & Retention Strategy
Based on the findings, recommended strategies include:
- Early intervention for users with declining or flat engagement
- Reducing over-reliance on blanket discount strategies
- Improving payment experience and minimizing renewal friction
- Tenure-aware retention campaigns instead of one-size-fits-all approaches
- Geographic targeting for high-churn regions

---

## 🛠 Tools & Technologies
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook
- SQL (for data aggregation)
- Git & GitHub

---

## 📎 Deliverables
- Full exploratory and analytical notebook
- Feature-engineered dataset
- Business-oriented churn insights
- Retention strategy recommendations

---

## 📌 Notes
This project emphasizes **interpretability and business impact**, making it suitable as a real-world analytics portfolio project rather than a purely modeling-focused exercise.

---

## 👤 Author
**Sal**  
Data Analyst  
