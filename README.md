# E-Commerce Delivery Delay Prediction

## 📌 Project Overview
This project analyzes e-commerce sales and operational data to understand customer behavior, product performance, and delivery efficiency. It combines business-focused insights with data analytics and machine learning to support better decision-making in sales planning and logistics operations.

The analysis covers the full data lifecycle — from raw data integration and cleaning to exploratory analysis and predictive modeling.

---

## 🎯 Business Objective
E-commerce platforms generate large volumes of transactional data daily. However, raw data alone does not explain:
- Why certain months have higher or lower sales
- Which product categories drive most revenue
- How delivery delays impact customer experience
- Whether delays can be predicted in advance

**This project aims to:**
- Identify monthly sales trends and seasonality
- Highlight top revenue-generating product categories
- Analyze delivery time behavior and operational bottlenecks
- Predict whether an order is likely to be delayed

---

## 📊 Business Value Delivered
- Enabled visibility into **monthly sales performance**, helping with seasonal planning
- Identified **top-performing product categories**, supporting inventory and pricing strategies
- Analyzed **delivery delays**, helping operations teams understand fulfillment efficiency
- Built a **delay prediction model** to proactively flag risky orders

---

## 🗂️ Data Sources
The analysis uses multiple relational datasets:
- Orders
- Customers
- Order Items
- Products
- Sellers
- Payments

All datasets are merged into a single analytical table using **left joins**, keeping orders as the primary reference to avoid losing transaction records.

---

## 🧹 Data Cleaning & Preparation
Key data preparation steps:
- Converted timestamp columns to datetime format
- Created a new feature: `delivery_time` (in days)
- Removed invalid or negative delivery records
- Handled missing numeric values using median imputation
- Ensured data consistency for analysis and modeling

---

## 🔍 Exploratory Data Analysis (EDA)
EDA was performed to understand patterns and trends:
- Monthly sales trend analysis to detect seasonality
- Distribution of delivery times to identify delays and outliers
- Revenue contribution by product category
- Summary statistics (mean, median, max delivery time)

Visualizations were created using Matplotlib and Seaborn to support clear business interpretation.

---

## 🧠 Feature Engineering
- Created a binary target variable `is_delayed`
- Orders with delivery time greater than the median were labeled as delayed
- Selected key predictive features such as product price and freight value

---

## 🤖 Machine Learning Model
- Model Used: **Random Forest Classifier**
- Reason: Handles non-linear relationships well and performs reliably on structured data
- Data Split: 80% training, 20% testing
- Evaluation Metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Classification Report

The model predicts whether an order is likely to be delayed based on order and shipping attributes.

---

## 📈 Model Evaluation
Performance was evaluated using:
- **Accuracy** to measure overall correctness
- **Precision** to assess prediction reliability
- **Recall** to measure how many actual delays were detected
- **F1-score** to balance precision and recall

These metrics provide a complete view of model effectiveness beyond accuracy alone.

---

## 🛠️ Tools & Technologies
- **Python**
- **Pandas & NumPy** – Data manipulation and cleaning
- **Matplotlib & Seaborn** – Data visualization
- **Scikit-learn** – Machine learning and evaluation
- **Google Colab**
