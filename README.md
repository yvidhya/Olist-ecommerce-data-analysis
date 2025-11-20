# 🛒 Olist E-Commerce Data Analysis & Delivery Delay Prediction

### Developer Documentation

This project is a complete end-to-end data analysis and machine-learning workflow built using the **Olist Brazilian E-Commerce Dataset**.
It covers everything from data cleaning to visualization — and finally, a **Random Forest ML model that predicts whether an order will be delayed**.

Originally created as a data exploration notebook, I expanded it into a structured, analytics-driven, machine-learning project designed for real business decision-making.

---

# 🌟 Overview

The goal of this project:

### ✔ Analyze real e-commerce business patterns

### ✔ Identify top sellers, customer behavior, revenue trends

### ✔ Understand delivery performance

### ✔ Build a **predictive ML model** for delivery delays

This documentation is written for **data analysts, ML engineers, and recruiters** who want to understand the depth of the analysis and modeling.

---

# 🔧 Requirements

### Software

* Python 3.8+
* Jupyter Notebook / Colab

### Libraries Used

```
pandas  
numpy  
matplotlib  
seaborn  
scikit-learn  
joblib  
plotly (optional)
```

Install everything:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib plotly
```

---

# ✨ Key Features

## 🔹 1. Data Cleaning & Feature Engineering

Cleaned multiple datasets:

* Orders
* Order items
* Customers
* Products

Performed:

* Datetime conversions
* Merging all datasets (order_id, customer_id)
* Handling missing values
* Removing invalid timestamps
* Creating new business features

**Feature created: Delivery Delay (days)**

```python
delivery_delay = order_delivered_customer_date - order_estimated_delivery_date
```

**Binary target created:**

* **0 = On-Time**
* **1 = Delayed**

---

## 🔹 2. Exploratory Data Analysis (EDA)

Highlights include:

### 📌 Sales Analysis

* Monthly revenue trends
* State-wise distribution
* Top-selling categories

### 📌 Customer Insights

* Customer geographic spread
* Repeat vs one-time behavior

### 📌 Operational Insights

* On-time vs delayed delivery distribution
* Seller dominance using Pareto 80/20 rule

### 📌 Visualizations

Created using **Matplotlib** + **Seaborn**:

* Monthly sales line chart
* Top 10 sellers bar chart
* Delivery performance pie chart
* Correlation heatmap

---

# 🤖 3. Delivery Delay Prediction Model (Random Forest)

The notebook includes a **full ML pipeline**.

### ✔ Feature Engineering for ML

Selected features:

* `price`
* `freight_value`
* `order_month`

### ✔ Data Preparation

```python
X_train, X_test, y_train, y_test = train_test_split(...)
StandardScaler()
```

### ✔ Model Used

**RandomForestClassifier**

```python
rf_model = RandomForestClassifier(n_estimators=200, random_state=42)
rf_model.fit(X_train_scaled, y_train)
```

### ✔ Evaluation

Generated:

* Accuracy
* Precision
* Recall
* F1-score

```python
print(classification_report(y_test, y_pred))
```

### ✔ Example Prediction

```python
features = [[5, 200, 1]]
rf_model.predict(features)
rf_model.predict_proba(features)
```

Example Output:

* **Prediction:** `[1]` → Delayed
* **Probability:** `[[0.25, 0.75]]`

### ✔ Saved Model Files

```python
joblib.dump(rf_model, "delivery_delay_model.pkl")
joblib.dump(scaler, "scaler.pkl")
```

These can be deployed into an API or other ML system.

---

# 🧭 Business Value of the ML Model

This model helps businesses predict:

* Which orders will likely be delayed
* Which customers may experience late delivery
* Which regions/products contribute to delays
* Early flagging of logistics bottlenecks

Businesses can use these predictions to:

* Notify customers proactively
* Improve route planning
* Offer compensation / priority shipping
* Optimize seller assignment

---

# 📂 Repository Structure

```
/
├── E-Commerce Analysis.ipynb          # Complete analysis + ML model
├── cleaned_olist_sales_data.csv       # Final cleaned dataset
├── delivery_delay_model.pkl           # Exported Random Forest model
├── scaler.pkl                         # Scaler for prediction pipeline
├── images/                            # All visualizations
└── README.md                          # Documentation
```

---

# 🧠 Lessons Learned

* Working with multiple relational tables improves understanding of joins
* Real-world timestamps are messy → require careful parsing
* Delivery delay patterns reveal major business inefficiencies
* Random Forest handles nonlinearities in logistics data very well

---

# 🚀 Possible Extensions

Future improvements:

* Delivery time regression model (predict number of days)
* Customer lifetime value (CLV) modeling
* Product recommender system
* Streamlit dashboard
* ARIMA/Prophet sales forecasting

---

# 👩‍💻 About Me

**VIDHYA DHARI YELURI**
📧 [vidhyay458@gmail.com](mailto:vidhyay458@gmail.com)
🔗 LinkedIn: *in/vidhya-yeluri-88432a254*
🔗 GitHub: [https://github.com/yvidhya](https://github.com/yvidhya)

⭐ If you like the project, consider starring the repo!

---
