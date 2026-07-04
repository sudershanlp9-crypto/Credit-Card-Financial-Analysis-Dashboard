# Credit Card Financial Analysis Dashboard

An end-to-end data analytics project analyzing credit card customer and transaction data using **Python, PostgreSQL, and Power BI** — covering data cleaning, database modeling, SQL analysis, and two interactive Power BI dashboards for business reporting.

## 📌 Project Overview

This project analyzes credit card customer demographics and weekly transaction data to uncover insights on revenue, spending behavior, customer segments, and risk indicators (delinquency, utilization ratio). It simulates a real-world analytics workflow: raw data → cleaned & structured database → SQL analysis → executive dashboards.

## 📁 Project Structure

| File | Description |
|---|---|
| `customer.csv` | Customer demographic data — Age, Gender, Education, Marital Status, State, Income, Job, Satisfaction Score |
| `cust_add.csv` | Additional/incremental customer records (appended data) |
| `credit_card.csv` | Weekly credit card transaction data — Card Category, Credit Limit, Revolving Balance, Transaction Amount/Count, Utilization Ratio, Interest Earned, Delinquency |
| `cc_add.csv` | Additional/incremental credit card transaction records (appended data) |
| `CCDB.sql` | SQL script to create the `cc_detail` and `cust_detail` tables in PostgreSQL and load the data |
| `Customer Credit Card Report.pdf` | Power BI report — customer-focused view (revenue by age group, job, education, gender) |
| `Credit Card Financial Weekly Dashborad.pdf` | Power BI report — transaction-focused view (revenue by card category, quarterly trends, interest earned) |
| `Credit Card Financial Weekly Dashboard Report (1)_removed.pdf` | Combined/exported dashboard report |

## 🗄️ Data Model

Two core tables built in PostgreSQL:

- **`cust_detail`** — one row per customer (`Client_Num` as key): demographics, occupation, income, and satisfaction score.
- **`cc_detail`** — one row per customer per week (`Client_Num` as foreign key): card category, credit limit, revolving balance, transaction amount/count, utilization ratio, interest earned, and delinquency flag.

The two `*_add.csv` files represent incremental weekly loads, simulating how new transaction batches would be appended to the database over time.

## 🛠️ Workflow

1. **Data Cleaning & Preparation (Python)** — Cleaned and transformed the raw customer and transaction CSVs (data types, missing values, formatting) before loading.
2. **Database Setup (PostgreSQL)** — Created `cust_detail` and `cc_detail` tables via `CCDB.sql` and loaded the cleaned data using SQL queries.
3. **Data Analysis (SQL)** — Queried the database to analyze revenue, transaction volume, and customer segments across demographics and card categories.
4. **Visualization (Power BI)** — Built two interactive dashboards:
   - **Customer Report**: revenue by age group, gender, customer job, and education level.
   - **Weekly Transaction Report**: revenue and transaction trends by quarter, card category (Blue/Silver/Gold/Platinum), and interest earned.
5. **Reporting** — Exported dashboard views as PDF reports for stakeholder sharing.

## 📊 Key Insights

- Total revenue across all customers: **₹5.53 Cr**, from **~6.56L transactions**.
- **Blue** card holders drive the largest share of revenue and transaction volume, followed by Silver, Gold, and Platinum.
- Revenue varies notably by customer occupation, with Businessman and White-collar segments contributing the most.
- Revenue and transaction counts show clear quarterly and weekly seasonality across 2023.

## 🚀 How to Run This Project

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd credit-card-financial-analysis-dashboard
   ```
2. **Set up PostgreSQL**
   - Create a new database.
   - Run `CCDB.sql` to create the `cc_detail` and `cust_detail` tables.
3. **Load the data**
   - Import `customer.csv` / `cust_add.csv` into `cust_detail`.
   - Import `credit_card.csv` / `cc_add.csv` into `cc_detail`.
4. **Explore the dashboards**
   - Open the PDF reports to view the pre-built Power BI dashboards, or connect Power BI Desktop to your PostgreSQL database to rebuild/extend them.

## 🧰 Tech Stack

- **Python** — Pandas, NumPy, data cleaning & EDA
- **PostgreSQL** — schema design, data loading, SQL analysis
- **Power BI** — DAX, data modeling, dashboard development

## 👤 Author

Sudarshan Pulgamwar
📧 sudarshanpulgamwar07@gmail.com
🔗 [GitHub](https://github.com/sudershanlp9-crypto)
