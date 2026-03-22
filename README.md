# 📊 Customer Churn Analysis & Prediction Dashboard

A Power BI-style interactive web dashboard for analyzing customer churn in a telecommunications company. Built with pure HTML, CSS, and JavaScript — no frameworks required.

---

## 🖼️ Dashboard Preview

> Open `customer_churn_dashboard.html` in any modern browser to view the full interactive dashboard.

https://prabuvenkateswaran021.github.io/customer_churn_dashboard/

---

## 📁 Repository Structure

```
📦 customer-churn-analysis/
├── 📄 customer_churn_dashboard.html       # Main interactive dashboard (open in browser)
├── 📄 Telco_Customer_Churn_Dataset.csv    # Source dataset (7,043 records)
└── 📄 README.md                           # Project documentation
```

---

## 🎯 Project Overview

This project analyzes customer churn in a telecommunications company and provides actionable insights to identify at-risk customers. The ultimate goal is to reduce churn and improve customer retention through data-driven decision making.

| Metric | Value |
|---|---|
| Total Customers | 7,043 |
| Churned Customers | 1,869 |
| **Overall Churn Rate** | **26.5%** |
| Retained Customers | 5,174 |
| Retention Rate | 73.5% |

---

## 📋 Tasks Completed

### ✅ Task 1 — Data Connection
- Imported the Telco Customer Churn dataset (7,043 records, 21 features)
- Parsed all categorical and numerical fields for visualization

### ✅ Task 2 — Data Transformation
- Cleaned and bucketed tenure into 6-month intervals (0–12, 13–24, 25–36, 37–48, 49–60, 61–72)
- Computed churn rates per segment
- Built cross-tabulations (Contract × Internet Service heatmap)
- Derived KPIs: churn rate, retention rate, high-risk segments

### ✅ Task 3 — Dashboard Components

#### A. Churn Rate Overview
- Donut chart showing 26.5% churn vs 73.5% retention
- KPI cards: Total Customers, Churn Rate, Retained Customers, High Risk Segment

#### B. Customer Demographics
- **Gender**: Pie chart — nearly equal split (Male 50.5%, Female 49.5%)
- **Partner Status**: Pie chart — customers without partners churn more (64.2% of churned)
- **Dependents**: Pie chart — customers without dependents drive 82.6% of churn

#### C. Customer Tenure Analysis
- Histogram showing customer distribution across 6 tenure buckets
- Churn rate overlay per bucket — identifies early churn risk in 0–12 month segment (47.4%)

#### D. Churn Analysis
- **Contract Type**: Stacked bar chart — Month-to-Month (42.7% churn), One Year (11.3%), Two Year (2.8%)
- **Payment Method**: Horizontal bar chart — Electronic Check highest at 45.3%
- **Internet Service**: Bar chart — Fiber Optic highest at 41.9%
- **Heatmap**: Contract × Internet Service cross-analysis

---

## 🔍 Key Findings

| # | Finding | Churn Rate | Impact |
|---|---|---|---|
| 1 | Month-to-month contract customers | 42.7% | 88.6% of all churn |
| 2 | Electronic check payment users | 45.3% | 3× higher than auto-pay |
| 3 | Fiber optic internet customers | 41.9% | Premium price, high dissatisfaction |
| 4 | Customers in first 12 months | 47.4% | Early engagement critical |
| 5 | Senior citizens | 41.7% | 1.76× the average churn rate |
| 6 | No partner + no dependents | High | Most vulnerable demographic |

---

## 💡 Actionable Recommendations

### 🔴 Contract Strategy
Month-to-month customers churn **15× more** than 2-year contract customers. Offer incentives (discounts, loyalty rewards, bundled perks) to migrate customers to annual or 2-year plans.

### 🟡 Payment Method Incentives
Electronic check users churn at 45.3%. Encourage switching to automatic payment (bank transfer or credit card) with cashback offers or monthly bill discounts.

### 🔵 Fiber Optic Service Quality
Fiber customers pay a premium yet churn at 41.9%. Audit service quality, investigate pricing vs competitors, and improve perceived value through better support and SLA guarantees.

### 🟣 Early Tenure Onboarding Program
Nearly half of all 0–12 month customers churn. Implement welcome programs, proactive check-in calls at 30/60/90 days, and first-year retention offers to reduce early drop-off.

### 🟢 Senior Citizen Focus
Senior citizens churn at 1.76× the average. Dedicated support lines, simplified billing, and senior loyalty programs could significantly improve this segment's retention.

---

## 🗂️ Dataset Description

**File:** `Telco_Customer_Churn_Dataset.csv`  
**Records:** 7,043 customers  
**Features:** 21 columns

| Column | Type | Description |
|---|---|---|
| customerID | String | Unique customer identifier |
| gender | Categorical | Male / Female |
| SeniorCitizen | Binary | 1 = Senior, 0 = Not Senior |
| Partner | Categorical | Yes / No |
| Dependents | Categorical | Yes / No |
| tenure | Numeric | Months with the company |
| PhoneService | Categorical | Yes / No |
| MultipleLines | Categorical | Yes / No / No phone service |
| InternetService | Categorical | DSL / Fiber optic / No |
| OnlineSecurity | Categorical | Yes / No / No internet |
| OnlineBackup | Categorical | Yes / No / No internet |
| DeviceProtection | Categorical | Yes / No / No internet |
| TechSupport | Categorical | Yes / No / No internet |
| StreamingTV | Categorical | Yes / No / No internet |
| StreamingMovies | Categorical | Yes / No / No internet |
| Contract | Categorical | Month-to-month / One year / Two year |
| PaperlessBilling | Categorical | Yes / No |
| PaymentMethod | Categorical | Electronic check / Mailed check / Bank transfer / Credit card |
| MonthlyCharges | Numeric | Monthly bill amount (USD) |
| TotalCharges | Numeric | Total amount charged (USD) |
| **Churn** | **Target** | **Yes / No — whether customer churned** |

---

## 🚀 How to Run

### Option 1 — Open Directly in Browser
```bash
# Simply double-click the file or open with any browser:
customer_churn_dashboard.html
```

### Option 2 — Serve Locally
```bash
# Using Python:
python -m http.server 8000

# Then open: http://localhost:8000/customer_churn_dashboard.html
```

### Option 3 — GitHub Pages
1. Push this repository to GitHub
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your dashboard will be live at: `https://<your-username>.github.io/<repo-name>/customer_churn_dashboard.html`

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| HTML5 | Structure & layout |
| CSS3 | Styling, animations, grid layout |
| SVG | Donut charts, data visualizations |
| Google Fonts (Barlow) | Typography |
| Vanilla JavaScript | Interactivity |

> No external libraries or frameworks required. Runs entirely in the browser.

---

## 📊 Dashboard Features

- **Dark theme** Power BI-inspired design
- **KPI cards** with color-coded metrics
- **Animated** chart reveals on load
- **Donut charts** for churn rate & demographics
- **Stacked bar charts** for contract analysis
- **Horizontal bar charts** for payment & internet service
- **Heatmap** for Contract × Internet Service cross-analysis
- **Insight cards** with color-coded recommendations
- **Fully responsive** layout

---

## 👤 Author

**Customer Churn Analysis & Prediction**  
Telecommunications Data Analysis Project

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

*Dashboard built with HTML/CSS/SVG — compatible with all modern browsers.*
