# 🎧 Customer Churn Prediction in a Leading Music App

## 🧾 Overview

This project tackles **customer churn prediction** for a leading freemium music streaming service. By analyzing user interactions and behaviors through event logs, the goal is to develop a predictive model that identifies users at risk of churn and provides **actionable insights** to drive **user retention**.

---

## 👥 Team

**Final Project – MGMT 59000 (Spring 2025)**  
Namra Shah & Swanand Gaikwad

---

## 🎯 Objectives

- Identify behavioral patterns associated with churn.
- Develop machine learning models to predict churn.
- Evaluate models using **F1-score** for handling class imbalance.
- Recommend **business strategies** to retain users.

---

## 📊 Dataset Overview

- **Source**: Event logs of user activity in a music app.
- **Rows**: User-session-level logs
- **Key Features**:
  - User ID
  - Session count & duration
  - Device type
  - Page interaction (e.g., “Next Song”, “Thumbs Up”)
  - Subscription level (Free/Paid)
  - Churn indicator (target variable)

---

## 🔍 Exploratory Data Analysis (EDA)

- **Churn Rate**: ~24% of users churned
- **Gender Effect**: Males churned at a higher rate (26%) than females (19%)
- **Behavioral Patterns**:
  - High engagement with “Thumbs Up” and “Add to Playlist” = lower churn
  - Skipping songs and less social interaction = early churn signals
- **Device Trends**: Windows users showed the highest churn
- **Location Trends**: Urban areas like Los Angeles and New York had higher churn rates
- **Failed Payments**: Strong indicator of churn

---

## 🧠 Feature Engineering

| Feature                    | Description                              | Type      |
|---------------------------|------------------------------------------|-----------|
| Gender                    | Male/Female                              | Binary    |
| Churn                     | Subscription cancellation indicator      | Binary    |
| User Level                | Free or Paid                             | Binary    |
| Total Length of Songs     | Total listening duration                 | Float     |
| Avg Session Duration      | Time per session                         | Float     |
| Page Interactions         | Thumbs Up, Playlist, etc.                | Integer   |
| Time Since Registration   | Days since signup                        | Integer   |
| Total Sessions            | Session count                            | Integer   |
| Total Songs Played        | Song count                               | Integer   |
| Device Type               | Windows, Mac, iPhone, Android            | Categorical |

---

## 🤖 Models Built

- **Logistic Regression**
- **Decision Tree**
- **Random Forest**
- **Gradient Boosting**

### 🏆 Model Performance

| Model               | F1-Score | Accuracy |
|--------------------|----------|----------|
| Gradient Boosting  | **0.9915** | Highest  |
| Random Forest      | 0.9871   |          |
| Logistic Regression| 0.9558   |          |
| Decision Tree      | 0.9523   |          |

- **Evaluation Metric**: F1-score (preferred due to class imbalance)
- **Tuning**: GridSearch for hyperparameter optimization
- **Feature Importance**:
  - Page Settings
  - Home Page Visits
  - Thumbs Up Count
  - Total Time Spent
  - Error Page Visits

---

## 💼 Business Recommendations

1. **Target High-Risk Segments**
   - Offer incentives to Windows users & users in high-churn cities (e.g., LA, NYC).

2. **Enhance Engagement**
   - Push users toward features like “Thumbs Up” and “Add to Playlist”.

3. **Optimize Payment Processes**
   - Add flexible billing, retries, and proactive payment reminders.

4. **Boost Social Interaction**
   - Promote collaborative playlists, social sharing, and friend invites.

5. **Experiment & Personalize**
   - A/B test onboarding, UI, and promotional offers.
   - Use AI to drive personalized playlists and content discovery.

---

## 🔮 Future Work

- Incorporate **demographic data**, advanced logs, and **time-based metrics**
- Experiment with **XGBoost**, **LightGBM**, and **deep learning**
- Build a **Recommendation Engine** for music personalization
- Explore **Reinforcement Learning** for retention decision-making

---

## 🛠️ Tools & Technologies

- Python (Pandas, NumPy, Scikit-learn)
- Matplotlib / Seaborn for EDA
- GridSearchCV for tuning
- Classification models from `sklearn`

---

> _“Retention is not just about prediction—it’s about action. Our model helps music apps anticipate churn and re-engage users before it's too late.”_

