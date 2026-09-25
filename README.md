# Presence Insights – HR Attendance Analytics Dashboard

An end-to-end HR analytics project built for **AtliQ** that turns a raw daily attendance register into an interactive **Power BI** dashboard, tracking employee **Presence %**, **Work-From-Home (WFH) %**, and **Sick-Leave (SL) %** across April–June 2022.

## 📊 Overview

HR teams often record attendance in Excel — one row per employee, one column per date — which is accurate but impossible to analyze at a glance. This project solves that by using **Power Query** to clean and unpivot the raw register, and **Power BI** to build a single-page dashboard that answers:

- What % of the workforce was present, remote, or on sick leave — and how has that trended day by day?
- Which day of the week has the strongest/weakest in-office presence?
- Which employees have unusually low presence or high leave usage, and why (remote work vs. absence)?

## 🗂️ Repository Contents

| File | Description |
|---|---|
| `Attendance-Sheet-2022-2023.xlsx` | Raw source data — one sheet per month (Apr/May/Jun 2022), daily attendance codes per employee, plus an Attendance Key sheet defining all 18 status codes (P, WFH, PL, SL, LWP, WO, HO, etc.) |
| `HR_Analytics_Presence_Insight__Dashboard.pbit` | Power BI template containing the data model, Power Query transformations, and DAX measures |
| `HR_Analytics_Presence_Insight__Dashboard.pdf` | Exported snapshot of the published dashboard |
| `Presence_Overview.PNG` | Screenshot of the dashboard's Presence Overview page |

## 🔧 Tools & Techniques

- **Excel** — raw data source and attendance register
- **Power Query** — data cleaning and unpivoting (wide date-columns → long Employee/Date/Status table), derived Day-of-Week column
- **Power BI Desktop** — data modeling, DAX measures, and report visuals (KPI cards, trend charts, matrix tables, month slicer)

## 📈 Key Metrics (Apr–Jun 2022)

| Metric | Value |
|---|---|
| Overall Presence % | 91.83% |
| Overall WFH % | 10.00% |
| Overall Sick-Leave % | 1.10% |

## ✨ Dashboard Features

- **KPI cards** for Presence %, WFH %, and SL % with a month slicer (Apr / May / Jun)
- **Trend charts** for Presence %, WFH %, and SL % by date
- **Day-of-week breakdown tables** for all three metrics, to spot weekly patterns (e.g. WFH peaks on Fridays)
- **Employee-level table** sortable by Presence %, WFH %, and SL %, to flag outliers
- **Daily attendance grid** showing each employee's status code per calendar date

## 🚀 Getting Started

1. Open `HR_Analytics_Presence_Insight__Dashboard.pbit` in Power BI Desktop.
2. When prompted, point the data source to `Attendance-Sheet-2022-2023.xlsx`.
3. Let Power Query refresh the transformations, then explore the report page.

## 📌 Notes

- Presence %, WFH %, and SL % are calculated against total working-day attendance records (Weekly Offs and Holidays are excluded from the denominator).
- The dataset covers 99 unique employees across the three monthly sheets.

## 📄 License

Add a license of your choice (e.g. MIT) if you plan to make this repository public.
