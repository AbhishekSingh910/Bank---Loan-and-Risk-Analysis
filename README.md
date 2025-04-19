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
