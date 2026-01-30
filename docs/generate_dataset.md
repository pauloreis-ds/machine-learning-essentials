[Back to The Futur... I mean... Home Page](index.md)

# 📦 E-commerce Transactions Dataset (Fictitious)

## 📌 Business Context

This dataset represents a **fictitious e-commerce platform**, designed to simulate a real-world transactional environment.  
The company operates as an online marketplace connecting **customers** and **merchants**, selling products across multiple categories and countries.

The data was created for **analytical, educational, and modeling purposes**, supporting use cases such as:
- Customer behavior analysis
- Merchant performance evaluation
- Transactional analytics
- Segmentation and predictive modeling
- Data modeling and BI dashboards

All data is **synthetic** and does not represent real individuals or companies.

---

## 🎯 Dataset Objective

The main goal of this dataset is to enable analysis of:
- Customer purchasing patterns
- Distribution of transactions across merchants
- Revenue concentration
- Merchant size and geographic distribution
- Time-based transaction behavior

It follows a **star schema-friendly structure**, separating **dimensions** and **fact tables**.

---

## 🗂️ Tables Overview

The dataset is composed of the following tables:

| Table Name          | Type        | Description |
|---------------------|-------------|-------------|
| `tb_customer`       | Dimension   | Customer master data |
| `df_merchant`      | Dimension   | Merchant master data |
| `tb_transactions`  | Fact        | Transaction-level data |

---

## 🧍‍♂️ Table: `tb_customer`

### 📖 Description
Contains **unique customer records**, representing individuals who performed transactions on the e-commerce platform.

Each row corresponds to **one customer**, regardless of how many transactions they performed.

### 🧾 Columns

| Column Name     | Type        | Description |
|-----------------|-------------|-------------|
| `Customer ID`   | Integer     | Unique identifier for each customer |
| `Name`          | String      | Customer first name |
| `Surname`       | String      | Customer last name |
| `Gender`        | String      | Customer gender |
| `Birthdate`     | Date        | Customer date of birth |

### 🔍 Business Use Cases
- Customer segmentation (age, gender)
- Lifetime value analysis
- Cohort analysis
- CRM and personalization studies

---

## 🏪 Table: `df_merchant`

### 📖 Description
Contains information about **merchants (sellers)** registered on the platform.  
Merchants vary by **country** and **business size**, reflecting a realistic marketplace structure.

Each row represents **one merchant**.

### 🧾 Columns

| Column Name     | Type        | Description |
|-----------------|-------------|-------------|
| `Merchant ID`   | Integer     | Unique identifier for each merchant |
| `Merchant Name` | String      | Merchant business name |
| `Country`       | String      | Country where the merchant operates |
| `Size`          | String      | Merchant size classification (`Small`, `Medium`, `Large`) |

### 🔍 Business Use Cases
- Merchant performance analysis
- Revenue concentration by merchant size
- Geographic distribution of sellers
- Marketplace strategy and onboarding analysis

---

## 💳 Table: `tb_transactions`

### 📖 Description
This is the **fact table**, containing one record per transaction.  
It connects customers and merchants and stores transactional metrics and attributes.

### 🧾 Columns

| Column Name        | Type        | Description |
|--------------------|-------------|-------------|
| `Transaction ID`   | Integer     | Unique identifier for each transaction |
| `Customer ID`      | Integer     | Reference to the customer who made the purchase |
| `Merchant ID`      | Integer     | Reference to the merchant who sold the product |
| `Transaction Value`| Float       | Monetary value of the transaction |
| `Product Category` | String      | Category of the purchased product |
| `Date`             | Date        | Date when the transaction occurred |

### 🔍 Business Use Cases
- Revenue analysis
- Time series and seasonality analysis
- Basket and category analysis
- Customer purchase frequency
- Merchant sales performance

---

## 🧠 Data Modeling Notes

- `tb_transactions` acts as the **fact table**
- `tb_customer` and `df_merchant` act as **dimension tables**
- Keys:
  - `Customer ID` → links customers to transactions
  - `Merchant ID` → links merchants to transactions

This structure is suitable for:
- Power BI / Tableau dashboards
- SQL analytics
- Machine Learning feature engineering
- Data warehouse modeling exercises

---

## ⚠️ Disclaimer

This dataset is entirely **synthetic**, generated using probabilistic distributions to mimic real-world behavior.  
It should **not** be used for real business decisions.

---