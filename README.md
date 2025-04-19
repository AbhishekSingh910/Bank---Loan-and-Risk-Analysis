# 🏦 Risk Analytics in Banking Dashboard - Power BI Project

## 🎯 Objective

The primary objective of this project is to **understand risk analytics in the banking sector** by analyzing customer-level data to identify patterns among defaulters. The ultimate goal is to reduce the risk of **loan defaults** and help the bank make informed decisions by providing actionable insights and key performance indicators (KPIs).

---

## 📊 Key Use Case

- Banks provide loans to different income categories: **low, mid, and high** earners.
- Some customers fail to repay, resulting in significant financial risk.
- This analysis aims to **detect risk signals**, optimize banking decisions, and improve customer targeting strategies to **minimize defaults**.

---

## 🧾 Data Description

### 1. Personal Info
| Column | Description |
|--------|-------------|
| `Client ID` | Unique identifier for each client |
| `Name` | Client’s full name |
| `Age` | Client’s age |
| `Location ID` | City or area code |
| `Joined Bank` | Date the client joined the bank |
| `Banking Contact` | Bank staff assigned to the client |

### 2. Demographics & Profile
| Column | Description |
|--------|-------------|
| `Nationality` | Client's nationality |
| `Occupation` | Client's profession |
| `Fee Structure` | Client's fee tier (High, Mid, Low) |
| `Loyalty Classification` | Loyalty tier (Jade, Gold, Platinum, Silver) |

### 3. Financial Info
| Column | Description |
|--------|-------------|
| `Estimated Income` | Annual income estimate |
| `Superannuation Savings` | Retirement savings |
| `Amount of Credit Cards` | Number of cards owned |
| `Credit Card Balance` | Outstanding credit card balance |
| `Bank Loans` | Total loans taken |
| `Bank Deposits` | Total deposited funds |
| `Checking Accounts` | Balance in current accounts |
| `Saving Accounts` | Balance in savings accounts |
| `Foreign Currency Account` | Holdings in foreign currency |
| `Business Lending` | Loans taken for business purposes |

### 4. Assets and Risk
| Column | Description |
|--------|-------------|
| `Properties Owned` | Number of properties owned |
| `Risk Weighting` | Risk level assigned by the bank |

---

## 🔢 Categorical Mappings

- `BRId (Banking Relationship)`  
  - 1: Retail  
  - 2: Institutional  
  - 3: Private Bank  
  - 4: Commercial  

- `GenderId`  
  - 1: Male  
  - 2: Female  

- `IAId (Investment Advisor)`  
  - Mapped to advisor names (e.g., Victor Dean, Jeremy Porter)

---

## 🧮 New Calculated Columns

### ➕ Engagement Days
```DAX
Engagement Days = DATEDIFF(Banking_Clients[Joined Bank], TODAY(), DAY)




## 📌 Key KPIs

| KPI                        | Description                                         |
|----------------------------|-----------------------------------------------------|
| **Total Clients**          | Number of active banking clients                    |
| **Total Loan**             | Sum of Bank Loans + Business Lending + Credit Card Balance |
| **Bank Loan**              | Individual bank loan amount                         |
| **Business Lending**       | Loans issued for businesses                         |
| **Total Deposit**          | Total client deposits                               |
| **Total Fees**             | Aggregated banking service fees                     |
| **Bank Deposit**           | Deposits in standard accounts                       |
| **Checking Account Amount**| Funds available in checking                         |
| **Savings Account Amount** | Total funds in savings                              |
| **Credit Card Balance**    | Total outstanding credit usage                      |
| **Engagement Account**     | Count of active engagement clients                  |

---


---

## 📊 Power BI Dashboards

### 🔷 1. Banking Overview Dashboard

| Metric | Value |
|--------|-------|
| Total Clients | 2940 |
| Total Loan | $4.38 Billion |
| Total Deposit | $3.77 Billion |
| Total Fees | $158.2 Million |
| Total Credit Card Balance | $9.53 Million |
| Savings Account Amount | $698.7 Million |

**Filters Available:**
- Year: 2013, 2014, 2018, 2019, 2020, 2021
- Gender: Male / Female

---

### 🔷 2. Loan Analysis Dashboard

#### 📌 Breakdown by Banking Relationship

| Relationship | Bank Loan |
|--------------|-----------|
| Private Bank | $0.81B |
| Retail | $0.38B |
| Commercial | $0.30B |
| Institutional | $0.28B |

#### 📌 Breakdown by Nationality

| Nationality | Bank Loan |
|-------------|-----------|
| European | $777.62M |
| Asian | $436.19M |
| American | $306.03M |
| Australian | $154.19M |
| African | $100.12M |

#### 📌 By Income Band

| Income Band | Bank Loan |
|-------------|-----------|
| High | $942.49M |
| Low | $448.19M |
| Medium | $383.47M |

#### 📌 By Engagement Timeframe

| Timeframe | Total Loan |
|-----------|------------|
| < 20 Years | ~$1.6B |
| > 20 Years | ~$1.3B |
| < 10 Years | ~$1.0B |
| ≤ 5 Years | ~$0.5B |

---

### 🏦 3. Deposit Analysis Dashboard

| Metric | Value |
|--------|-------|
| Total Deposit | $3.77 Billion |
| Bank Deposit | $2.01 Billion |
| Savings Account | $698.7 Million |
| Checking Account | $963 Million |
| Foreign Currency Account | $89.65 Million |

#### 📌 Deposit by Engagement Timeframe

| Timeframe | Total Deposit |
|-----------|----------------|
| < 20 Years | $1.41B |
| > 20 Years | $1.09B |
| < 10 Years | $0.79B |
| < 5 Years | $0.48B |

#### 📌 Bank Deposit by Income Band

| Income Band | Bank Deposit |
|-------------|--------------|
| Medium | $1.09B |
| Low | $0.50B |
| High | $0.42B |

#### 📌 Total Deposit by Nationality

| Nationality | Total Deposit |
|-------------|----------------|
| European | ~$3.2B |
| Asian | ~$1.5B |
| American | ~$0.9B |
| Australian | ~$0.6B |
| African | ~$0.5B |

---

### 💸 4. Fees Analysis Dashboard

#### 📌 By Loyalty Classification

| Loyalty Tier | Total Fees |
|--------------|------------|
| Jade | $72M |
| Silver | $40M |
| Gold | $30M |
| Platinum | $16M |

#### 📌 By Nationality

| Nationality | Total Fees |
|-------------|------------|
| European | $69M |
| Asian | $40M |
| American | $26M |
| Australian | $14M |
| African | $10M |

---

## 🧠 Key Insights

- **Private Bank** clients hold the highest volume of loans.
- **European** clients dominate both in **loan volumes and deposits**.
- **High-income** clients take larger loans, but **medium-income** clients deposit more.
- Clients engaged for **< 20 years** hold the highest **deposits and loans**.
- **Jade tier** clients generate the most banking fees, likely due to **premium services**.
"""

# Save both parts into README.md
with open("/mnt/data/README.md", "w") as f:
    f.write(markdown_content)
    f.write(more_markdown_content)
"/mnt/data/README.md"


# Define the initial markdown content (reused from previous context)
markdown_content = """
# 🏦 Banking Risk Analytics Dashboard

This project focuses on analyzing and visualizing key risk metrics in a banking environment using Power BI. It includes insights from loans, deposits, client demographics, and bank-generated fees to detect risk patterns and uncover business opportunities.

---

## 📁 Dataset Overview

The dataset contains detailed client banking information across multiple dimensions:

| Column | Description |
|--------|-------------|
| Client ID | Unique identifier for each client |
| Estimated Income | Estimated annual income of the client |
| Superannuation Savings | Retirement savings balance |
| Credit Card Balance | Outstanding credit card balance |
| Banking Relationship | Type of client relationship (e.g., Private, Retail) |
| Investment Advisor | Presence of an assigned investment advisor |
| Total Loan | Combined bank + business + credit card loans |
| Loan Risk Category | Risk classification (Low, Medium, High) |
| Total Deposit | Sum of client deposits |
| Deposit Tier | Client deposit category |
| Loyalty Classification | Banking loyalty level (Jade, Silver, etc.) |
| Total Fees | Fees paid by the client |
| Engagement Timeframe | Length of client-bank relationship |
| Checking & Savings Amount | Individual account fund balances |
| Foreign Currency Account | International account value |
| Gender, Nationality, Age Group | Demographic indicators |

---
"""

# Define the additional content containing KPIs, dashboards, and insights
more_markdown_content = """
## 📌 Key KPIs

| KPI | Description |
|-----|-------------|
| **Total Clients** | Number of active banking clients |
| **Total Loan** | Sum of Bank Loans + Business Lending + Credit Card Balance |
| **Bank Loan** | Individual bank loan amount |
| **Business Lending** | Loans issued for businesses |
| **Total Deposit** | Total client deposits |
| **Total Fees** | Aggregated banking service fees |
| **Bank Deposit** | Deposits in standard accounts |
| **Checking Account Amount** | Funds available in checking |
| **Savings Account Amount** | Total funds in savings |
| **Credit Card Balance** | Total outstanding credit usage |
| **Engagement Account** | Count of active engagement clients |

---

## 📊 Power BI Dashboards

### 🔷 1. Banking Overview Dashboard

| Metric | Value |
|--------|-------|
| Total Clients | 2940 |
| Total Loan | $4.38 Billion |
| Total Deposit | $3.77 Billion |
| Total Fees | $158.2 Million |
| Total Credit Card Balance | $9.53 Million |
| Savings Account Amount | $698.7 Million |

**Filters Available:**
- Year: 2013, 2014, 2018, 2019, 2020, 2021
- Gender: Male / Female

---

### 🔷 2. Loan Analysis Dashboard

#### 📌 Breakdown by Banking Relationship

| Relationship | Bank Loan |
|--------------|-----------|
| Private Bank | $0.81B |
| Retail | $0.38B |
| Commercial | $0.30B |
| Institutional | $0.28B |

#### 📌 Breakdown by Nationality

| Nationality | Bank Loan |
|-------------|-----------|
| European | $777.62M |
| Asian | $436.19M |
| American | $306.03M |
| Australian | $154.19M |
| African | $100.12M |

#### 📌 By Income Band

| Income Band | Bank Loan |
|-------------|-----------|
| High | $942.49M |
| Low | $448.19M |
| Medium | $383.47M |

#### 📌 By Engagement Timeframe

| Timeframe | Total Loan |
|-----------|------------|
| < 20 Years | ~$1.6B |
| > 20 Years | ~$1.3B |
| < 10 Years | ~$1.0B |
| ≤ 5 Years | ~$0.5B |

---

### 🏦 3. Deposit Analysis Dashboard

| Metric | Value |
|--------|-------|
| Total Deposit | $3.77 Billion |
| Bank Deposit | $2.01 Billion |
| Savings Account | $698.7 Million |
| Checking Account | $963 Million |
| Foreign Currency Account | $89.65 Million |

#### 📌 Deposit by Engagement Timeframe

| Timeframe | Total Deposit |
|-----------|----------------|
| < 20 Years | $1.41B |
| > 20 Years | $1.09B |
| < 10 Years | $0.79B |
| < 5 Years | $0.48B |

#### 📌 Bank Deposit by Income Band

| Income Band | Bank Deposit |
|-------------|--------------|
| Medium | $1.09B |
| Low | $0.50B |
| High | $0.42B |

#### 📌 Total Deposit by Nationality

| Nationality | Total Deposit |
|-------------|----------------|
| European | ~$3.2B |
| Asian | ~$1.5B |
| American | ~$0.9B |
| Australian | ~$0.6B |
| African | ~$0.5B |

---

### 💸 4. Fees Analysis Dashboard

#### 📌 By Loyalty Classification

| Loyalty Tier | Total Fees |
|--------------|------------|
| Jade | $72M |
| Silver | $40M |
| Gold | $30M |
| Platinum | $16M |

#### 📌 By Nationality

| Nationality | Total Fees |
|-------------|------------|
| European | $69M |
| Asian | $40M |
| American | $26M |
| Australian | $14M |
| African | $10M |

---

## 🧠 Key Insights

- **Private Bank** clients hold the highest volume of loans.
- **European** clients dominate both in **loan volumes and deposits**.
- **High-income** clients take larger loans, but **medium-income** clients deposit more.
- Clients engaged for **< 20 years** hold the highest **deposits and loans**.
- **Jade tier** clients generate the most banking fees, likely due to **premium services**.
"""


















