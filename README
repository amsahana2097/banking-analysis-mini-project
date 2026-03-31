# Analysis of Banking Penetration and Financial Inclusion in India

![Banking Analysis](https://img.shields.io/badge/Data_Analysis-Excel_%26_Power_BI-blue)
![Financial Inclusion](https://img.shields.io/badge/Focus-Financial_Inclusion-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview
This project examines the distribution of **Scheduled Commercial Banks (SCBs)** across India to identify structural and geographical imbalances. By analyzing trends in bank offices, accounts, and deposit patterns from 2019 to 2022, the study highlights the gap between metropolitan hubs and underbanked rural regions.

## 🎯 Project Objectives
* **Trend Analysis:** Track growth in SCB offices, accounts, and deposits over time.
* **Gap Identification:** Identify underbanked districts and regions with low banking usage.
* **Regional Comparison:** Benchmark banking access across Western, Eastern, Northern, Southern, Central, and North-Eastern regions.
* **Efficiency Metrics:** Analyze "Accounts per Office" and "Deposit per Account" to measure banking depth.

---

## 📊 Data Source
* **Source:** India Data Portal (IDP)
* **Domain:** Banking and Financial
* **Dataset:** Population-group Wise Deposits

### Data Attributes
| Attribute Name | Description | Data Type |
| :--- | :--- | :--- |
| **Year** | Reference year for the record (2019–2022) | Date |
| **State Name** | The Indian state to which the district belongs | Text |
| **District Name** | Administrative unit for data collection | Text |
| **Region** | Geographical region of India | Text |
| **Population Group** | Area classification (Rural, Semi-Urban, Urban, Metro) | Text |
| **No. of SCB Offices** | Total bank branches operating in the district | Number |
| **No. of Accounts** | Total bank accounts held with SCBs | Number |
| **Amount Deposited** | Average deposit amount per bank account | Currency |

---

## 🛠️ Tools & Technologies
* **Excel:** Used for data cleaning, transformation, and descriptive statistics (Analysis Toolpak).
* **Power BI:** Used for data modeling, DAX calculations, and interactive dashboard creation.

---

## ⚙️ Data Pre-processing & Modeling

### 1. Excel (Cleaning & Transformation)
* **Standardization:** Applied `CLEAN` and `TRIM` functions to State, District, and Region names.
* **Calculated Columns:** * `Account per office` = Number of accounts / Number of offices
    * `Deposit per account` = Amount Deposited / Number of accounts
    * `Deposit Category` = Conditional logic (IF) to group accounts into *Very Low, Low, Medium, and High*.

### 2. Descriptive Statistics
Generated key metrics using Excel’s **Analysis Toolpak**:
* Mean, Median, Mode, Standard Deviation, Kurtosis, and Skewness.
* Summary statistics for total SCB offices and average deposits.

### 3. Power BI (DAX & Modeling)
Established a Star Schema by creating **District_DIM** and **State_DIM** tables.
**Key DAX Measures:**
```dax
Total_Deposits = SUM('Table'[Amount deposited])

Deposit_growth = 
DIVIDE([Total_Deposits] - [Previousyear_deposit], [Previousyear_deposit])

Accountper_office = 
DIVIDE([Totalnumber_of_accounts], [Totalnumberof_offices])
