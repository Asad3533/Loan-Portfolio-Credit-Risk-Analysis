# Loan Portfolio & Credit Risk Analysis Dashboard

## 📊 Project Overview

This project analyzes a loan portfolio dataset using **Microsoft Power BI** to uncover insights into loan performance, borrower characteristics, credit risk, and lending trends.

The interactive dashboard provides a comprehensive view of the loan portfolio, helping users understand loan distribution, funding, interest rates, loan status, borrower profiles, and potential credit risk factors.

The project demonstrates the complete data analytics workflow, including **data cleaning, transformation, data modeling, DAX calculations, data visualization, and business insights**.

---

## 🎯 Project Objectives

The main objectives of this project are to:

* Analyze the overall loan portfolio and funding performance.
* Understand loan distribution across different grades and purposes.
* Analyze loan repayment and default patterns.
* Identify factors associated with higher credit risk.
* Analyze borrower characteristics such as income, employment, and home ownership.
* Examine interest rates across different loan grades.
* Analyze debt-to-income (DTI) levels and their relationship with loan performance.
* Identify geographic and time-based lending trends.
* Build an interactive Power BI dashboard for business decision-making.

---

## 🛠️ Tools & Technologies

* **Microsoft Power BI**
* **Power Query**
* **DAX (Data Analysis Expressions)**
* **Microsoft Excel / CSV**
* **Data Cleaning & Transformation**
* **Data Visualization**
* **Business Intelligence**

---

## 📁 Dataset

The project uses a loan portfolio dataset containing approximately **39,000+ loan records** and more than **100 attributes** related to borrowers, loans, credit history, payments, and loan performance.

### Key Data Categories

#### Loan Information

* Loan Amount
* Funded Amount
* Loan Term
* Interest Rate
* Installment
* Loan Grade
* Sub Grade
* Loan Purpose
* Loan Status

#### Borrower Information

* Annual Income
* Employment Length
* Home Ownership
* Income Verification Status
* State
* Debt-to-Income Ratio (DTI)

#### Credit Information

* Delinquencies
* Credit Inquiries
* Open Accounts
* Public Records
* Revolving Balance
* Revolving Utilization
* Total Credit Accounts

#### Loan Performance

* Total Payments
* Total Principal Received
* Total Interest Received
* Recoveries
* Outstanding Principal
* Last Payment Amount

---

## 🧹 Data Preparation

The dataset was prepared using **Power Query** before analysis.

The data preparation process included:

* Removing unnecessary columns.
* Handling missing and incomplete values.
* Checking column quality and data completeness.
* Converting columns to appropriate data types.
* Cleaning loan term values.
* Formatting interest rates and financial fields.
* Converting loan issue dates into usable date formats.
* Creating grouped loan status categories.
* Creating income and DTI groups for analysis.

---

## 📌 Key KPIs

The dashboard tracks important performance indicators, including:

* **Total Loans**
* **Total Loan Amount**
* **Total Funded Amount**
* **Average Loan Amount**
* **Average Interest Rate**
* **Default Rate**
* **Charged-Off Loans**
* **Total Interest Received**
* **Total Payments Received**
* **Average Annual Income**
* **Average Debt-to-Income Ratio**

---

## 📊 Dashboard Pages

### 1. Executive Overview

Provides a high-level summary of the loan portfolio.

Key visualizations include:

* Total Loan KPIs
* Total Funded Amount
* Average Loan Amount
* Average Interest Rate
* Default Rate
* Loan Amount Trends
* Loan Status Distribution
* Loan Grade Distribution
* Loan Purpose Analysis

---

### 2. Credit Risk Analysis

Focuses on loan performance and credit risk.

Key analysis includes:

* Charged-Off Loan Analysis
* Default Rate
* Risk by Loan Grade
* Interest Rate by Loan Grade
* Debt-to-Income Ratio Analysis
* Loan Status by Grade
* Risk Segmentation

---

### 3. Borrower Profile Analysis

Analyzes borrower demographics and financial characteristics.

Key analysis includes:

* Annual Income Distribution
* Employment Length
* Home Ownership
* Income Verification Status
* Debt-to-Income Ratio
* Borrower Segmentation
* Loan Performance by Borrower Characteristics

---

### 4. Geographic & Trend Analysis

Provides geographic and time-based insights.

Key analysis includes:

* Loan Amount by State
* Loan Count by State
* Loan Issuance Trends
* Loan Purpose Trends
* Loan Grade Trends
* Geographic Distribution of Loans

---

## 🧮 DAX Measures

Several DAX measures were created to support the dashboard analysis.

### Total Loans

```DAX
Total Loans = COUNTROWS('loan')
```

### Total Loan Amount

```DAX
Total Loan Amount = SUM('loan'[loan_amnt])
```

### Total Funded Amount

```DAX
Total Funded Amount = SUM('loan'[funded_amnt])
```

### Average Loan Amount

```DAX
Average Loan Amount = AVERAGE('loan'[loan_amnt])
```

### Average Interest Rate

```DAX
Average Interest Rate = AVERAGE('loan'[int_rate])
```

### Total Interest Received

```DAX
Total Interest Received = SUM('loan'[total_rec_int])
```

### Total Payments Received

```DAX
Total Payments Received = SUM('loan'[total_pymnt])
```

### Charged-Off Loans

```DAX
Charged Off Loans =
CALCULATE(
    [Total Loans],
    'loan'[loan_status] = "Charged Off"
)
```

### Default Rate

```DAX
Default Rate =
DIVIDE(
    [Charged Off Loans],
    [Total Loans],
    0
)
```

---

## 🔍 Key Business Questions

The dashboard is designed to answer questions such as:

1. How large is the overall loan portfolio?
2. How much money has been funded?
3. What percentage of loans are fully paid?
4. What percentage of loans are charged off?
5. Which loan grades have the highest credit risk?
6. Which loan purposes receive the most funding?
7. How do interest rates vary across loan grades?
8. Does a higher DTI indicate higher loan risk?
9. Which borrower income groups receive the most loans?
10. Which states have the highest loan activity?
11. How does loan issuance change over time?
12. What borrower characteristics are associated with loan performance?

---

## 💡 Key Insights

The dashboard enables analysis of:

* **Portfolio Performance:** Understand overall loan volume and funding activity.
* **Credit Risk:** Identify loan grades and borrower segments with higher risk.
* **Interest Rate Analysis:** Compare loan pricing across different risk grades.
* **Borrower Behavior:** Analyze how income, employment, and home ownership relate to lending.
* **Geographic Trends:** Identify states with higher loan activity.
* **Loan Purpose:** Understand the major reasons borrowers take loans.
* **Time Trends:** Monitor changes in loan issuance and portfolio performance over time.

---

## 📈 Dashboard Features

* Interactive KPI cards
* Dynamic charts and graphs
* Loan status analysis
* Credit risk analysis
* Loan grade comparison
* Borrower segmentation
* Geographic analysis
* Time-series analysis
* Interactive slicers and filters
* Drill-down analysis

---

## 📂 Project Structure

```text
Loan-Portfolio-Credit-Risk-Analysis/
│
├── Dataset/
│   └── loan.csv
│
├── PowerBI/
│   └── Loan_Portfolio_Credit_Risk_Dashboard.pbix
│
├── Screenshots/
│   ├── executive-overview.png
│   ├── credit-risk-analysis.png
│   ├── borrower-analysis.png
│   └── geographic-trends.png
│
└── README.md
```

---

## 🚀 How to Use

1. Clone or download this repository.
2. Open the `.pbix` file using **Microsoft Power BI Desktop**.
3. If required, update the dataset file path.
4. Refresh the data.
5. Use the interactive filters and slicers to explore the dashboard.
6. Navigate between dashboard pages to analyze different aspects of the loan portfolio.

---

## 📷 Dashboard Preview



Example:

```markdown
<img width="917" height="524" alt="Executive Overview" src="https://github.com/user-attachments/assets/496f8b87-a1c1-41a2-ae1c-b399b7af7b55" />


<img width="936" height="532" alt="Credit Risk   Loan Performance" src="https://github.com/user-attachments/assets/448b7c05-22e2-42ef-8552-e4a17e90687d" />


<img width="919" height="525" alt="Borrower Profile Analysis" src="https://github.com/user-attachments/assets/905190b5-35b5-44fd-b070-437a83000f8d" />

```

---

## 📚 Skills Demonstrated

This project demonstrates practical skills in:

* Data Cleaning
* Data Transformation
* Power Query
* DAX
* Data Modeling
* KPI Development
* Data Visualization
* Business Intelligence
* Credit Risk Analysis
* Financial Data Analysis
* Interactive Dashboard Development
* Business Insight Generation

---

## 👨‍💻 Author

**Asad Rafeeq**

Aspiring **Data Analyst** with skills in:

* Power BI
* SQL
* Python
* Excel
* Data Analysis
* Data Visualization
* Laravel & Web Development

---

⭐ If you find this project useful, feel free to give the repository a star!

