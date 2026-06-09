<div align="center">

# 🏦 Bank Loan Analysis

<img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
<img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
<img src="https://img.shields.io/badge/Plotly-Interactive%20Viz-3F4F75?style=for-the-badge&logo=plotly&logoColor=white"/>
<img src="https://img.shields.io/badge/Matplotlib-Seaborn-11557C?style=for-the-badge&logo=python&logoColor=white"/>

<br/>

> **A comprehensive end-to-end exploratory data analysis of a bank's loan portfolio — uncovering trends in funding, repayment, risk, and borrower demographics across 38,000+ loan records.**

<br/>

```
📊 38,576 Loans   ·   💰 $435.76M Funded   ·   ✅ 86.18% Good Loans   ·   📅 Full Year 2021
```

</div>

---

## 📑 Table of Contents

- [📌 Project Overview](#-project-overview)
- [📂 Dataset](#-dataset)
- [🔢 Key Metrics at a Glance](#-key-metrics-at-a-glance)
- [✅ Good Loan vs ❌ Bad Loan Analysis](#-good-loan-vs--bad-loan-analysis)
- [📈 Analyses Performed](#-analyses-performed)
- [🛠️ Tech Stack](#️-tech-stack)
- [🚀 Getting Started](#-getting-started)
- [📁 Project Structure](#-project-structure)

---

## 📌 Project Overview

This project performs a **thorough exploratory data analysis (EDA)** on a bank's lending dataset covering the full year of 2021. The goal is to extract actionable insights about loan performance, borrower behavior, and funding patterns — helping financial analysts and decision-makers understand portfolio health at a glance.

The analysis covers:

- 📆 **Month-over-month trends** in loan applications, funded amounts, and repayments
- 🗺️ **Regional breakdowns** by U.S. state
- 🏠 **Borrower demographics** — home ownership, employment length, income
- 🎯 **Loan purpose segmentation** — debt consolidation, home improvement, credit cards, and more
- ⚖️ **Risk classification** — distinguishing good loans (Fully Paid / Current) from bad loans (Charged Off)

---

## 📂 Dataset

| Property | Details |
|---|---|
| **File** | `financial_loan.xlsx` |
| **Rows** | 38,576 |
| **Columns** | 24 |
| **Time Period** | January 2021 – December 2021 |
| **Granularity** | Individual loan applications |

### 📋 Feature Overview

| Column | Type | Description |
|---|---|---|
| `id` | int | Unique loan identifier |
| `loan_amount` | int | Principal amount funded |
| `loan_status` | object | Fully Paid / Current / Charged Off |
| `int_rate` | float | Annual interest rate |
| `dti` | float | Debt-to-income ratio |
| `annual_income` | float | Borrower's annual income |
| `installment` | float | Monthly payment amount |
| `total_payment` | int | Total amount received from borrower |
| `grade` / `sub_grade` | object | Risk grading (A–F) |
| `purpose` | object | Reason for loan |
| `term` | object | 36 or 60 months |
| `home_ownership` | object | RENT / MORTGAGE / OWN |
| `emp_length` | object | Employment duration |
| `address_state` | object | U.S. state of applicant |
| `issue_date` | datetime | Date loan was issued |
| `verification_status` | object | Income verification level |

---

## 🔢 Key Metrics at a Glance

<div align="center">

| Metric | Value |
|:---:|:---:|
| 📋 **Total Loan Applications** | 38,576 |
| 📋 **MTD Applications** *(Dec 2021)* | 4,314 |
| 💵 **Total Funded Amount** | **$435.76M** |
| 💵 **MTD Funded Amount** | $53.98M |
| 💰 **Total Amount Received** | **$473.07M** |
| 💰 **MTD Amount Received** | $58.07M |
| 📈 **Average Interest Rate** | **12.05%** |
| ⚖️ **Average DTI** | **13.33%** |

</div>

> 💡 **Insight:** The portfolio received **$37.31M more** than it funded — indicating healthy net positive cash flows from interest collections.

---

## ✅ Good Loan vs ❌ Bad Loan Analysis

The portfolio was segmented by loan status to assess credit risk:

### ✅ Good Loans *(Fully Paid + Current)*

| Metric | Value |
|---|---|
| Applications | 33,243 |
| **% of Total** | **86.18%** |
| Funded Amount | $370.22M |
| Total Received | $435.79M |

### ❌ Bad Loans *(Charged Off)*

| Metric | Value |
|---|---|
| Applications | 5,333 |
| **% of Total** | **13.82%** |
| Funded Amount | $65.53M |
| Total Received | $37.28M |

> ⚠️ **Risk Alert:** Bad loans resulted in a **$28.25M shortfall** ($65.53M funded vs. $37.28M recovered) — highlighting the financial cost of defaults and the need for improved credit screening.

---

## 📈 Analyses Performed

### 1. 📅 Monthly Trends

Three time-series area charts track the evolution of the portfolio throughout 2021:

- **Total Funded Amount by Month** — Tracks how lending volume grew month-over-month
- **Total Received Amount by Month** — Shows repayment velocity across the year  
- **Total Loan Applications by Month** — Visualizes application demand seasonality

> The portfolio shows a **consistent upward trend** across all three metrics, peaking in December 2021 with 4,314 applications and $53.98M funded.

---

### 2. 🗺️ Regional Analysis by State

A horizontal bar chart ranks all U.S. states by total funded amount (in PKR thousands). This reveals:

- Which states drive the **highest loan demand**
- Geographic concentration of credit risk
- Opportunity markets with growing borrower bases

---

### 3. 🕐 Loan Term Analysis

A **donut chart** breaks down funding by loan term:

| Term | Share of Portfolio |
|---|---|
| 36 Months | Majority |
| 60 Months | Minority |

> Shorter-term loans dominate, suggesting borrowers prefer faster payoff schedules.

---

### 4. 👔 Employment Length Analysis

A horizontal bar chart maps total funded amounts across employment tenure buckets:

- `< 1 year` through `10+ years`
- Reveals whether **job stability correlates** with borrowing volume
- Helps profile the typical borrower's employment background

---

### 5. 🎯 Loan Purpose Breakdown

A horizontal bar chart segments funded amounts by purpose category, including:

- 🔁 Debt consolidation
- 🏠 Home improvement
- 💳 Credit card refinancing
- 🚗 Major purchases
- 🏥 Medical expenses
- 🎓 Education
- And more...

> **Debt consolidation** is by far the dominant purpose, reflecting broad consumer demand for financial restructuring.

---

### 6. 🏠 Home Ownership Analysis

An interactive **Plotly treemap** visualizes funding distribution across home ownership categories:

- `RENT` — Largest borrower segment
- `MORTGAGE` — Second largest
- `OWN` — Smallest segment

> Renters represent the largest borrower group, suggesting they seek loans for liquidity that homeowners may access through equity.

---

## 🛠️ Tech Stack

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, aggregation |
| `numpy` | Numerical operations |
| `matplotlib` | Static charts (area, bar, donut) |
| `seaborn` | Statistical visualization styling |
| `plotly.express` | Interactive treemap |

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn plotly openpyxl
```

### Run the Notebook

1. **Clone / download** this repository
2. Place `financial_loan.xlsx` in the same directory (or update the path in cell 1)
3. Open the notebook:

```bash
jupyter notebook BANK_LOAN_ANALYSIS.ipynb
```

4. Run all cells (`Kernel → Restart & Run All`)

> 💡 If running in **Google Colab**, upload `financial_loan.xlsx` to `/content/` — the default path in the notebook will work as-is.

---

## 📁 Project Structure

```
Bank_Loan_Analysis-main/
│
├── 📓 BANK_LOAN_ANALYSIS.ipynb     # Main analysis notebook
└── 📄 README.md                    # Project documentation
```

---

<div align="center">

**Built with Python · Powered by Data · Driven by Insight**

<br/>

*If you find this project useful, consider giving it a ⭐*

</div>
