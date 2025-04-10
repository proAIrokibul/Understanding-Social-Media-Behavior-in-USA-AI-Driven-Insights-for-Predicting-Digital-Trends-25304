# Understanding-Social-Media-Behavior-in-USA-AI-Driven-Insights-for-Predicting-Digital-Trends-25304
## 🔍 Project Overview

This project analyzes social media usage patterns across different user demographics in the USA. The objective is to categorize users into **"Highly Aware"**, **"Moderately Aware"**, and **"Unaware"** groups based on their interaction with social platforms, preferences, and digital behaviors.

Our AI models aim to predict user awareness levels with the ultimate goal of improving **targeted content strategies**, **digital well-being initiatives**, and **platform engagement** techniques.

---

## 🛠️ Preprocessing Summary

Before modeling, we performed the following steps:

- Cleaned and standardized textual responses
- Encoded categorical features using `OneHotEncoding` and `LabelEncoding`
- Split the data into **training (80%)** and **test (20%)** sets
- Scaled numeric features using `StandardScaler` (within pipelines)
- Removed or handled missing/null values

---

## 🤖 Model Building & Fine-Tuning

We trained and tuned three classification models using `GridSearchCV`:

### 1. **Logistic Regression**
- **Best Params:** `C = 0.1`, `solver = saga`
- **Accuracy:** 0.4032

#### Classification Report:
| Class              | Precision | Recall | F1-score |
|-------------------|-----------|--------|----------|
| Highly Aware       | 0.38      | 0.42   | 0.40     |
| Moderately Aware   | 0.41      | 0.45   | 0.43     |
| Unaware            | 0.50      | 0.22   | 0.31     |

---

### 2. **Random Forest Classifier**
- **Best Params:**  
  - `n_estimators = 200`  
  - `max_depth = None`  
  - `min_samples_split = 5`  
  - `min_samples_leaf = 1`
- **Accuracy:** 0.4516

#### Classification Report:
| Class              | Precision | Recall | F1-score |
|-------------------|-----------|--------|----------|
| Highly Aware       | 0.43      | 0.42   | 0.43     |
| Moderately Aware   | 0.44      | 0.55   | 0.49     |
| Unaware            | 0.67      | 0.22   | 0.33     |

---

### 3. **XGBoost Classifier**
- **Best Params:**  
  - `learning_rate = 0.01`  
  - `max_depth = 5`  
  - `n_estimators = 200`  
  - `subsample = 0.8`  
  - `colsample_bytree = 1.0`
- **Accuracy:** 0.4355

#### Classification Report:
| Class              | Precision | Recall | F1-score |
|-------------------|-----------|--------|----------|
| Highly Aware       | 0.45      | 0.54   | 0.49     |
| Moderately Aware   | 0.43      | 0.31   | 0.36     |
| Unaware            | 0.42      | 0.56   | 0.48     |

---

## 📈 Business Impact & Insights

### 1. 🎯 **Improved Targeting for Marketing Campaigns**
Understanding digital awareness allows platforms, brands, and agencies to **segment users** based on their digital maturity.  
- *Highly Aware* users might prefer premium content, ad-free experiences.
- *Moderately Aware* users could be nudged toward curated experiences and smart reminders.
- *Unaware* users may benefit from digital literacy initiatives or onboarding guides.

---

### 2. 🧠 **Digital Well-Being and Distraction Management**
Models can predict which users are more vulnerable to digital distractions. These predictions enable:
- **Customized notifications & content filters**
- **In-app nudges** to reduce excessive usage
- **Wellness tools** and “focus mode” integrations

---

### 3. 💰 **Monetization and Subscription Prediction**
By identifying behaviors linked to premium subscriptions and content creator support:
- Streaming services (e.g., Netflix, Spotify) can **predict conversion probability**
- Platforms like Patreon or YouTube can **optimize creator support promotions**

---

### 4. 📉 **Reducing Churn through Awareness Modeling**
Lower-awareness users might churn due to overwhelming or irrelevant content. By understanding these patterns:
- Social platforms can **adjust onboarding flows**
- Deliver **custom content education**
- Drive **longer retention and loyalty**
