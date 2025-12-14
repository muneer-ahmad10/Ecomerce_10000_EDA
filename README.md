# 📊 Exploratory Data Analysis (EDA) – E-commerce Dataset

## 📌 Overview

This project presents a comprehensive **Exploratory Data Analysis (EDA)** on an e-commerce transactional dataset. The goal of this analysis is to deeply understand the data, identify patterns, validate assumptions, detect anomalies, and derive meaningful insights that can support **business decisions** and **machine learning modeling**.

The analysis focuses on understanding **products, pricing, customer behavior, sales trends, and revenue patterns**.

---

## 🧾 Dataset Description

The dataset contains **order-level e-commerce data** with the following columns:

* **OrderID** – Unique identifier for each order
* **Product** – Product name
* **Category** – Product category (Electronics, Fashion, etc.)
* **Brand** – Brand name
* **Platform** – E-commerce platform
* **City** – City of purchase
* **Price** – Price per unit
* **Quantity** – Units purchased per order
* **TotalAmount** – Total transaction value (Price × Quantity)
* **Rating** – Customer rating
* **Reviews** – Number of customer reviews
* **OrderDate** – Date of order

---

## 🔍 Key EDA Steps & Insights

### 1️⃣ Data Structure & Quality

* Dataset is **clean and well-structured**
* No critical missing values impacting analysis
* Numerical and categorical columns are clearly defined
* Date column successfully parsed for time-based analysis

---

### 2️⃣ Product-Level Analysis

* Product distribution is **fairly balanced**, with no single product dominating the dataset
* Product counts range narrowly, indicating **minimal sampling bias**
* Quantity distribution per product is **identical and stable**

📌 **Insight:** Customer purchasing behavior (quantity per order) is consistent across products

---

### 3️⃣ Category Analysis

* **Electronics and Fashion** dominate the dataset
* Other categories are comparatively underrepresented

📌 **Insight:** Overall dataset trends are likely influenced mainly by Electronics and Fashion

---

### 4️⃣ Brand & Platform Analysis

* Brands and platforms show **balanced representation** in terms of product count
* No brand or platform dominates purely by frequency

📌 **Insight:** Minimal brand/platform-level sampling bias; safe to include these as ML features

---

### 5️⃣ Price Analysis

* Price range: **~₹0 – ₹20,000**
* Median price ≈ **₹10,000**
* No extreme outliers detected using IQR
* Distribution is **fairly symmetric**

📌 **Insight:** Pricing behavior is stable and suitable for modeling without heavy transformations

---

### 6️⃣ Quantity Analysis

* Quantity values range between **1 to 5 units**
* Near-uniform distribution across all values

```
Quantity  Count
1         2002
2         1980
3         1972
4         2046
5         2000
```

📌 **Insight:** Quantity per order is controlled and non-skewed; bulk ordering is limited

---

### 7️⃣ Total Amount Analysis

* **Right-skewed distribution** with high-value outliers above ~₹95,000
* Outliers are present for most products
* These outliers are **price-driven**, not quantity-driven

📌 **Insight:** High-value transactions represent premium or bulk purchases and should not be blindly removed

---

### 8️⃣ Rating & Review Analysis

* Brand-wise rating averages show meaningful variation
* Reviews vary significantly across brands and platforms

📌 **Insight:** Customer perception differs across brands despite balanced representation

---

### 9️⃣ Time-Based Analysis

#### 📆 Monthly Revenue (2024)

* Revenue remains relatively stable throughout the year
* Minor peaks observed in **July, September, and January**
* December shows a slight dip

#### 📅 Yearly Revenue

* **Total revenue (2024): ~₹302 million**

📌 **Insight:** Sales are consistent across months, indicating stable demand

---

## 🧠 Key Takeaways

* Dataset is **balanced, clean, and ML-ready**
* Quantity behavior is uniform; price drives revenue variability
* Category dominance must be considered during modeling
* Outliers in total amount are **informative, not erroneous**
* Strong foundation for predictive modeling and business analytics

---

## 🚀 Next Steps

* Feature engineering (log-transform TotalAmount if required)
* Category-wise or brand-wise modeling
* Demand forecasting or revenue prediction
* Customer segmentation

---

## 📁 Project Goal

This EDA was performed to build **strong data intuition** before modeling, ensuring that future machine learning results are **meaningful, interpretable, and reliable**.

---

✨ *EDA is not about plots — it’s about understanding the story behind the data.*
