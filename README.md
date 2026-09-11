# Placement_Analysis


An end-to-end data analysis project exploring campus placement outcomes across branches, CGPA, and academic backlogs, built with **SQL (PostgreSQL)** and **Power BI**.

> **Note on the data:** This project uses a simulated dataset (1,324 records) modeled on real campus placement patterns, generated to reflect realistic relationships between CGPA, backlogs, branch, and placement outcomes. It is not real institutional data.

---

## 🎯 Objective

Analyze 3 years of student placement records to answer:
- Which branches place the most students, and which pay the best?
- Does CGPA actually predict placement outcomes?
- How much do academic backlogs hurt placement chances?
- Who are the top recruiters, and how do packages vary by company tier?

---

## 🛠️ Tools Used
- **PostgreSQL** — data storage and analysis via SQL queries
- **Power BI** — interactive dashboard and visualization
- **Excel** — initial data cleaning

---

## 📊 Dashboard

![Dashboard Screenshot](dashboard_screenshot.png)



The dashboard includes:
- KPI summary cards (placement rate, total placed, avg/highest package)
- Placement rate by branch
- Placement rate by CGPA band and backlog status
- Year-over-year placement and package trends
- Top 10 recruiting companies

---

## 🔍 Key Findings

| Finding | Result |
|---|---|
| Overall placement rate | **51.74%** |
| Best-performing branches | IT (59.48%) and CSE (59.23%) |
| Weakest-performing branch | Electrical (44.89%) |
| CGPA 9+ vs. Below 6 placement rate | **75.00% vs. 38.38%** |
| No backlogs vs. has backlogs placement rate | 58.09% vs. 40.46% (**18-point gap**) |
| Highest-volume recruiter | Accenture (94 students hired) |
| Highest-paying recruiter | Google (₹33.00L avg package) |
| Avg package by tier | Tier 1: ₹30.80L · Tier 2: ₹6.57L · Tier 3: ₹3.52L |
| 3-year package trend | ₹8.27L (2022) → ₹7.42L (2024), a ~10% decline |

### Takeaways
- **CGPA is one of the strongest single predictors of placement** in this dataset — placement rate nearly doubles moving from the lowest to highest CGPA band.
- **Backlogs matter almost as much as CGPA** — an 18-point placement rate gap between students with and without backlogs.
- **Branch affects placement rate more than package size in some cases** — Civil had a below-average placement rate but the highest average package among placed students, suggesting fewer but higher-paying offers.
- **A small number of Tier 1 recruiters (e.g. Google) pull the overall average package up significantly**, while the bulk of placements happen through Tier 2 companies at more moderate packages.
- Average package has **trended slightly downward** over the 3-year window even as placement volume stayed stable — worth monitoring in future years.

---

## 📁 Repository Structure

```
├── README.md
├── data/
│   └── riverdale_university_placements.csv
├── sql/
│   └── placement_queries.sql
├── dashboard/
│   └── dashboard_screenshot.png
└── placements.pbix          # Power BI file (optional, if under GitHub's file size limit)
```

---



---

## 📌 Future Improvements
- Add a predictive model (logistic regression) to estimate placement probability for a given CGPA/backlog/branch combination
- Incorporate soft-skill or aptitude test scores if available, to see if they add predictive power beyond CGPA
- Expand to more years of data to validate the declining-package trend
