# 💳 Credit Card Transaction Analysis

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![CSV Data](https://img.shields.io/badge/CSV%20Data-217346?style=for-the-badge&logo=files&logoColor=white)

> **Data-Driven Insights for Strategic Decision Making**  
> Reporting Period: January 2023 – December 2023 | Dataset: 10,108 Customer Records

---

## 📌 Project Overview

This end-to-end data analytics project analyzes credit card transaction data and customer demographics to surface actionable business insights. The project covers revenue performance, customer segmentation, geographic distribution, spending behavior, and risk exposure across a full fiscal year.

**Developed by:** Nitin Shani

---

## 📊 Power BI Dashboards

### Page 1 — Credit Card Transaction Dashboard
![Credit Card Transaction Dashboard](dashboard1.png)

### Page 2 — Credit Card Customer Dashboard
![Credit Card Customer Dashboard](dashboard2.png)

---

## 📈 Key Metrics at a Glance

| Metric | Value |
|---|---|
| 💰 Total Transaction Revenue | $55M |
| 📈 Total Interest Earned | $8M |
| 👥 Total Customers | 10,108 |
| ⭐ Avg Customer Satisfaction | 3.19 / 5.0 |
| ⚠️ Delinquent Accounts | 614 (6.1%) |
| 📊 Avg Credit Utilization | 27.5% |

---

## 🗂️ Project Structure

```
credit-card-analysis/
│
├── 📁 data/
│   ├── credit_card2.csv              # Credit card transaction records
│   └── customer.csv                  # Customer demographic data
│
├── 📁 sql/
│   └── Table_creation_and_Load.sql   # SQL schema + data loading scripts
│
├── 📁 reports/
│   ├── Credit_Card_Report.pbix           # Power BI dashboard file
│   └── Credit_Card_Analysis_Report.pdf   # Full analysis report (PDF)
│
├── dashboard1.png                    # Transaction dashboard screenshot
├── dashboard2.png                    # Customer dashboard screenshot
└── README.md
```

---

## 🛠️ Tech Stack

- **Database:** Microsoft SQL Server (T-SQL, BULK INSERT)
- **Visualization:** Power BI Desktop (.pbix)
- **Data Format:** CSV
- **Reporting:** PDF

---

## ⚙️ Setup & Usage

### 1. Database Setup

Run the SQL script to create the tables and load data:

> ⚠️ **Important:** Update the file paths in `Table_creation_and_Load.sql` to match your local machine before executing.

```sql
BULK INSERT cc_detail
FROM 'YOUR_PATH\credit_card2.csv'
WITH (FORMAT = 'CSV', FIRSTROW = 2, FIELDTERMINATOR = ',', TABLOCK);

BULK INSERT cust_detail
FROM 'YOUR_PATH\customer.csv'
WITH (FORMAT = 'CSV', FIRSTROW = 2, FIELDTERMINATOR = ',', TABLOCK);
```

### 2. Power BI Dashboard

1. Open `Credit_Card_Report.pbix` in Power BI Desktop
2. Update the data source connection to your SQL Server instance
3. Refresh the data model

---

## 📈 Key Findings

### Revenue by Card Category
| Card | Customers | Revenue | Revenue Share |
|---|---|---|---|
| Blue | 9,214 | $46.1M | 83.0% |
| Silver | 639 | $5.6M | 10.3% |
| Gold | 188 | $2.5M | 4.6% |
| Platinum | 67 | $1.1M | 2.1% |

### Revenue by Age Group
| Age Group | Revenue | Share |
|---|---|---|
| 40–49 | $19.51M | 43.8% |
| 50–59 | $14.72M | 33.1% |
| 30–39 | $7.70M | 17.3% |
| 60+ | $1.75M | 3.9% |
| 20–29 | $0.84M | 1.9% |

### Top 5 States by Revenue
| State | Revenue |
|---|---|
| Texas (TX) | $10.31M |
| New York (NY) | $10.26M |
| California (CA) | $10.12M |
| Florida (FL) | $7.80M |
| New Jersey (NJ) | $3.44M |

---

## 🔍 Strategic Recommendations

1. 🔐 **Migrate swipe transactions to chip/online** — Reduce fraud exposure (swipe = 62.7% of volume, highest risk)
2. 💎 **Improve Platinum & Gold customer experience** — Satisfaction score of 2.72/5.0 risks premium churn
3. 🧑‍💻 **Target 20–39 age segment** — Currently only 19.2% of revenue; high future earning potential
4. ✈️ **Launch travel & entertainment reward tiers** — Lowest category ($4.85M) but highest margin potential
5. 🛍️ **Q4 seasonal campaign** — Weakest quarter ($10.69M) despite holiday season; cashback offers recommended
6. 📉 **Proactive delinquency monitoring** — 614 accounts at risk; early intervention could protect $1.5–2M
7. 🗺️ **Geographic expansion** — 5 states = 94.2% of revenue; diversification needed for resilience

---

## 📋 Data Dictionary

### `cc_detail` Table
| Column | Description |
|---|---|
| `Client_Num` | Unique customer identifier |
| `Card_Category` | Blue / Silver / Gold / Platinum |
| `Annual_Fees` | Annual card fee (USD) |
| `Credit_Limit` | Customer credit limit |
| `Total_Trans_Amt` | Total transaction amount |
| `Total_Revolving_Bal` | Outstanding revolving balance |
| `Avg_Utilization_Ratio` | Credit utilization ratio |
| `Interest_Earned` | Interest earned on account |
| `Delinquent_Acc` | Delinquency flag (Yes/No) |
| `Use_Chip` | Transaction method (Swipe/Chip/Online) |
| `Exp_Type` | Expenditure category |

### `cust_detail` Table
| Column | Description |
|---|---|
| `Client_Num` | Unique customer identifier (FK) |
| `Customer_Age` | Customer age |
| `Gender` | M / F |
| `Income` | Annual income (USD) |
| `Education_Level` | Highest education attained |
| `Marital_Status` | Marital status |
| `State_cd` | US state code |
| `Customer_Job` | Occupation type |
| `Cust_Satisfaction_Score` | Satisfaction score (1–5) |

---

## 📄 License

This project is for educational and portfolio purposes.

---

*Prepared by **Nitin Shani** | Data Analytics Division*
