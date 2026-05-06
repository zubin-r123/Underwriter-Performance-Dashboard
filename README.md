# 📊 Underwriter Performance Dashboard

A Tableau workbook for monitoring and analysing loan underwriting operations across regions, loan types, and source channels. Track application volumes, approval and denial rates, underwriter efficiency, compliance, and customer satisfaction — all in one place.

---

## 🗂️ Dashboards

![Dashboard Preview](Screenshot%2026-05-06%194954.png)

### 🔍 Overview
High-level summary of the entire underwriting pipeline. At a glance, you can see:
- Total application counts, approved volumes, and rejected application counts
- Average loan amount and application distribution by status
- A **status funnel** showing drop-off at each stage of the pipeline
- A **Sankey chart** mapping the flow from loan type through to final application status

### 🏆 Performance
Underwriter-level analysis for evaluating individual and team performance:
- Approval rate broken down by underwriter
- A composite **underwriter efficiency score** (combines approval rate, defect rate, and turnaround time)
- KPI indicators for compliance score, denial ratio, and defect rate — colour-coded against thresholds
- Rankings to surface your top-performing underwriters at a glance

### 📈 Trends
Time-series view of underwriting activity over time:
- Yearly application analysis with year-on-year percentage breakdowns
- Monthly and quarterly application trends
- **TAT vs. Volume** scatter plot — spot underwriters or periods where speed and volume diverge
- Satisfaction score tracked over time
- Dynamic metric and dimension switching via parameters — swap between No. of Applications, Approval Rate, Denial Rate, and more without rebuilding the view

---

## 🗄️ Data Source

**File:** `Underwriting_applications_dataset.csv`  
**Connection type:** CSV (local flat file)  
**Locale:** en_IN &nbsp;|&nbsp; **Currency:** ₹

| Field | Type | Description |
|---|---|---|
| Application Id | String | Unique identifier for each loan application |
| Application Date | Date | Date the application was submitted |
| Underwriter | String | Name of the assigned underwriter |
| Loan Type | String | Type of loan (e.g. Home, Personal, Auto) |
| Status | String | Current application status (Approved, Denied, Pending, etc.) |
| Est. Closed Date | Date | Estimated closure date |
| Loan Amount | Integer | Loan value in ₹ |
| Region | String | Geographic region of the application |
| Source Channel | String | Channel through which the application was received |
| Approval Rate | Decimal | Approval rate for the application/underwriter |
| Denial Ratio | Decimal | Ratio of denied applications |
| Defect Rate | Decimal | Rate of errors or defects in underwriting decisions |
| Turn Around Time | Integer | Processing time in days |
| DTI (%) | Decimal | Debt-to-income ratio |
| Consistency Score | Decimal | Measure of decision consistency across similar applications |
| Re-underwriting Rate (%) | Decimal | Percentage of applications requiring re-underwriting |
| Compliance Score (%) | Decimal | Adherence to regulatory and internal compliance guidelines |
| Customer Satisfaction Score | Decimal | Customer satisfaction rating |
| Remarks | String | Free-text notes on the application |

---

## 🚀 How to Open

1. Make sure you have **Tableau Desktop 2025.1** or later installed.
2. Place `Underwriting_applications_dataset.csv` in the same folder as the `.twb` file — or note its location on your machine.
3. Open `Underwriter_new.twb` in Tableau Desktop.
4. If prompted about the data source path, click **Edit Connection** and navigate to the CSV file.
5. The **Sankey chart** on the Overview dashboard requires an active internet connection to load the Tableau Sankey Extension.
