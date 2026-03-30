# 🏥 Patient Health Monitoring Report
### Power BI Report

> A comprehensive patient health monitoring solution tracking risk levels, chronic conditions, visit patterns, and diagnostic summaries across 20,000 patient visits.

🔗 **[View Live Report](https://app.powerbi.com/view?r=eyJrIjoiODNmZDdkN2MtZjdmYi00MmIyLTlmOTEtMWY2M2YzOTIwNjMyIiwidCI6IjgxMTQ1ZWNkLTc5NTAtNDk4Ny1hOGFmLTJhMDY1YTgwMWVhYyJ9)** &nbsp;|&nbsp; 📃
**[Dataset](https://github.com/user-attachments/files/26335405/DATA.xlsx)** &nbsp;|&nbsp; 📖
**[Medium Article](https://medium.com/@kudehinbusamad/from-symptoms-to-strategy-how-i-built-a-patient-health-monitoring-dashboard-in-power-bi-345a7b4fdaa2)**
 &nbsp;|&nbsp; 👤 **[LinkedIn](https://www.linkedin.com/in/abdulsamad-kudehinbu/)** &nbsp;|&nbsp; 🌐 **[Portfolio](https://sites.google.com/view/abdulsamadportfolio/home)**  


---
<img width="3141" height="1876" alt="merged" src="https://github.com/user-attachments/assets/1a6bc347-70b7-492e-8281-0434e0e03e52" />

---

## 📋 Table of Contents

- [Overview](#overview)
- [Report Pages](#report-pages)
- [Data Sources](#data-sources)
- [Key Metrics](#key-metrics)
- [Insights & Recommendations](#insights--recommendations)
- [How to Use the Report](#how-to-use-the-report)
- [Filter Pane Guide](#filter-pane-guide)
- [DAX Measures](#dax-measures)
- [Disclaimer](#disclaimer)

---

## Overview

The **Patient Health Monitoring Report** is a 4-page interactive Power BI dashboard designed to give healthcare data analysts and end users a 360° view of patient health trends. It covers everything from high-level risk scoring to granular blood test results and visit history.

| Detail | Value |
|---|---|
| **Tool** | Microsoft Power BI |
| **Total Records** | 20,000 patient visits |
| **Patients** | 4,887 unique patients |
| **Date Range** | January 2024 – March 2026 |
| **Report Pages** | 4 |
| **Live Report** | [Click to view](https://app.powerbi.com/view?r=eyJrIjoiODNmZDdkN2MtZjdmYi00MmIyLTlmOTEtMWY2M2YzOTIwNjMyIiwidCI6IjgxMTQ1ZWNkLTc5NTAtNDk4Ny1hOGFmLTJhMDY1YTgwMWVhYyJ9) |

---

## Report Pages

### 1. 🔴 Risk Overview
**Quick view of patient risk levels, fever patterns, and key health indicators across visits.**

Provides a bird's-eye view of the entire patient population. Use this page to understand overall risk distribution, which fever types are most prevalent, which locations have the highest patient volumes, and how admissions break down by fever type.

<img width="1572" height="941" alt="image 1" src="https://github.com/user-attachments/assets/712567a0-6ecd-42f3-a876-ac60eb54652d" />

**Key visuals:**
- KPI cards: Total Patients, Total Visits, High-Risk Patients, High-Risk %
- Total Visits by Fever Type and Admission Required (grouped bar)
- Total Visits by Risk Level (donut chart)
- Total Patients by Age Group (bar chart)
- Top 5 Locations by Number of Patients
- Total Patients by Gender (donut chart)

---

### 2. 💚 Chronic Health Monitor
**Quick view of risk levels, fever patterns, and key health indicators focused on chronic conditions.**

Drills into chronic conditions — specifically diabetes and blood pressure — and their relationship to fever types and blood test markers (CRP, WBC, platelets, hemoglobin).

<img width="1575" height="941" alt="image 2" src="https://github.com/user-attachments/assets/7cf0f7f8-5e8f-4790-a1c5-435f51652607" />


**Key visuals:**
- KPI cards: Diabetes Patients, High Blood Pressure Patients, Avg Systolic BP, Avg Diastolic BP
- Number of Patients by Age Group and Blood Pressure Risk (clustered bar)
- Diabetes Risk Distribution (donut chart — Normal vs. Diabetic)
- Top 5 Fever Types by CRP Levels (bar chart)
- Hemoglobin Distribution (bar chart by range)
- WBC vs. Platelets by Fever Type and CRP (scatter plot)

---

### 3. 📊 Visit Analysis
**Tracking patient visit frequency, follow-up gaps, and care continuity over time.**

Focuses on how patients engage with care — identifying repeat visitors, flagging delayed follow-ups, and surfacing the patients with the most visits.

<img width="1572" height="940" alt="image 3" src="https://github.com/user-attachments/assets/80111327-9cde-4a6e-a135-9bfa8de88877" />


**Key visuals:**
- KPI cards: Total Visits, Repeat Patients, Average Visit Gap (Days), Delayed Follow-Up %
- Monthly Trends line chart (Total Visits, Repeat Patients, Avg Visit Gap, Delayed Follow-Up %)
- Visits by Visit Type (donut: Repeat vs. One-Time)
- Visits by Visit Category (bar: First Visit, Delayed Follow-Up, Moderate Gap, Regular)
- Top patients by number of visits (table)
- Visit Insight alert: flags high numbers of patients missing follow-ups

---

### 4. 📋 Summary Table
**Quick patient diagnostic summary for decision making.**

A searchable, row-level table of individual patient visits. Ideal for looking up a specific patient or cross-referencing clinical data.

<img width="1575" height="937" alt="image 4" src="https://github.com/user-attachments/assets/ef2f8eed-a751-43d9-a87e-37349b65b216" />

**Key columns:**
Patient ID · Fever Type · Visit Date · Risk Level · Systolic BP · Diastolic BP · BP Risk · Hemoglobin · CRP · WBC · Platelets · Cough · Fatigue · Body Pain

**Feature:** Search by Patient ID using the search bar at the top.

---

## Data Sources

The report is powered by a single Excel file containing 4 sheets:

| Sheet | Description | Key Fields |
|---|---|---|
| `Patient_Symptoms` | Core visit data — 20,000 rows | Visit ID, Patient ID, Visit Date, Age, Gender, Location, Fever Type, Risk Level, Symptoms, BP, Diabetes |
| `Blood_Test_Results` | Lab results linked to each visit | Hemoglobin, WBC, RBC, Platelets, Neutrophils, Lymphocytes, CRP, ESR |
| `Fever_Type_Profile` | Reference table for each fever type | Typical temperature, WBC/Platelets/CRP ranges, risk level, symptom profile |
| `Medication` | Medication reference by fever type | Drug name, typical dose, frequency, duration |

---

## Key Metrics

| Metric | Value |
|---|---|
| Total Patients | 4,887 |
| Total Visits | 20,000 |
| High-Risk Patients | 4,058 |
| High-Risk % | 83.04% |
| Diabetes Patients | 1,326 (27.13%) |
| High Blood Pressure Patients | 4,048 (82.83%) |
| Avg Systolic Blood Pressure | 130.11 mmHg |
| Avg Diastolic Blood Pressure | 85.18 mmHg |
| Repeat Patients | 4,480 |
| Average Visit Gap | 138 days |
| Delayed Follow-Up % | 40.60% |

---

## Insights & Recommendations

### 🔍 Key Findings

#### Risk Overview
- **83% of patients are classified as high risk** — an unusually high proportion that suggests the dataset skews toward patients presenting with serious or acute conditions. This warrants priority attention to triage and early intervention protocols.
- **Bacterial, COVID, and Dengue** drive the largest share of visits requiring hospital admission, while Viral fever accounts for the highest overall visit volume but fewer admissions — consistent with its lower clinical severity.
- **Adults (36–60) and Seniors (60+)** make up the largest patient age groups, indicating that middle-aged and elderly populations are the most frequent users of this health system.
- **Guntur and Nellore** are the top two locations by patient volume, suggesting these cities carry the heaviest patient load and may benefit most from resource allocation.

#### Chronic Health Monitor
- **82.83% of patients show elevated blood pressure** (average 130/85 mmHg), placing the majority in the Stage 1 hypertension range. This is a significant chronic disease burden running alongside acute fever-related visits.
- **27.13% of patients are diabetic**, with a concentration in the Adult (36–60) and Senior (60+) age groups — consistent with typical diabetes prevalence patterns.
- **COVID and Bacterial fever patients show the highest CRP levels**, confirming their association with severe systemic inflammation. This aligns with the higher admission rates observed on the Risk Overview page.
- **Hemoglobin levels are heavily concentrated in the 12–14 g/dL range**, with a notable tail of patients below 12 (mild anaemia range), particularly among dengue and malaria cases where platelet suppression is also expected.

#### Visit Analysis
- **40.60% of visits are classified as delayed follow-ups** — meaning nearly half of returning patients are not coming back within the recommended timeframe. This is a critical care continuity gap.
- **Average visit gap of 138 days** further confirms that patients are not returning regularly, which is particularly concerning for those with chronic conditions (hypertension, diabetes) who need frequent monitoring.
- **97.88% of visits are repeat visits**, meaning the majority of patient volume comes from returning patients rather than new cases — reinforcing the importance of follow-up care management.
- **Visit volume peaks in early months (Jan–Mar)** before declining through mid-year, which may reflect seasonal fever patterns (particularly dengue and malaria seasonality).

---

### ✅ Recommendations for Healthcare Teams

| # | Recommendation | Priority |
|---|---|---|
| 1 | **Strengthen follow-up protocols** — With 40.6% delayed follow-ups, implement automated SMS/call reminders for patients with chronic conditions or high-risk classifications | 🔴 High |
| 2 | **Hypertension screening programme** — Given 82.83% of patients show elevated BP, integrate BP management counselling and medication reviews into routine visit workflows | 🔴 High |
| 3 | **Seasonal resource planning** — Prepare for higher patient volume in Q1 (Jan–Mar); allocate additional clinical staff and supplies ahead of peak fever season | 🟡 Medium |
| 4 | **Targeted diabetes management** — With 27.13% diabetic patients, consider dedicated diabetic clinics or check-in touchpoints, especially in Guntur and Nellore which carry the highest volumes | 🟡 Medium |
| 5 | **Triage prioritisation for Bacterial & COVID cases** — These fever types show the highest CRP, admission rates, and severity markers; fast-track clinical assessment pathways should be considered | 🔴 High |
| 6 | **Anaemia monitoring** — Flag patients with hemoglobin below 12 g/dL (especially dengue/malaria cases) for dietary counselling and iron supplementation | 🟡 Medium |
| 7 | **Location-specific resource allocation** — Guntur, Nellore, and Visakhapatnam are the busiest locations; capacity planning (beds, staff, diagnostics) should reflect their patient load | 🟡 Medium |
| 8 | **One-time patient re-engagement** — A small but notable portion of patients only visit once (2.12%); outreach programmes may help re-engage these individuals before conditions worsen | 🟢 Low |

---

## How to Use the Report

1. 1. **Open the file** — Open `Patient_Health_Monitoring_Report.pbix` in Power BI Desktop or access via the published Power BI Service link.
2. **Navigate pages** — Use the left sidebar to switch between the 4 report pages: Risk Overview, Chronic Health, Visit Analysis, and Summary Table.
3. **Apply filters** — Use the Filter Pane on the left of each page to narrow data by Year, Month, Location, Gender, or Fever Type.
4. **Clear filters** — Click the **Clear Slicers** button at the bottom of the Filter Pane to reset all filters at once.
5. **Search a patient** — Go to the **Summary Table** page and type a Patient ID (e.g. `P00001`) into the search bar.
6. **Click to cross-filter** — Clicking a segment in one visual (e.g. a fever type in the bar chart) will automatically filter all other visuals on the page.

---

## Filter Pane Guide

Each page has a consistent Filter Pane with the following slicers:

| Filter | Options | Effect |
|---|---|---|
| **Year** | All / 2024 / 2025 / 2026| Filters all visuals to the selected year |
| **Month** | All / Jan–Dec | Narrows to a specific month |
| **Location** | All / City names | Filters by patient clinic location |
| **Gender** | All / Male / Female | Filters by patient gender |
| **Fever Type** | All / Viral / Dengue / COVID / etc. | Filters by diagnosed fever type |

> 💡 **Tip:** Filters are independent per page — changing the filter on one page does not affect other pages.

---

## DAX Measures

The following measures power the KPI cards, charts, and calculated logic throughout the report. Each entry includes the measure name, which report page it appears on, and a placeholder for the formula.

### 📌 Risk Overview

| Measure | Description | Formula |
|---|---|---|
| `Total Patients` | Count of distinct patients across all visits | ```TOTAL PATIENTS = DISTINCTCOUNT(Patient_Symptoms[Patient ID])``` |
| `Total Visits` | Total number of visit records | ```TOTAL VISITS = COUNT('Blood Test Results'[Visit ID])``` |
| `High Risk Patients` | Count of patients classified as High risk | ```HIGH RISK PATIENTS = CALCULATE(DISTINCTCOUNT(Patient_Symptoms[Patient ID]),Patient_Symptoms[Risk Level] = "High")``` |
| `High Risk %` | Percentage of patients classified as High risk | ```HIGH RISK % = DIVIDE([HIGH RISK PATIENTS],[TOTAL PATIENTS],0)``` |

---

### 📌 Chronic Health Monitor

| Measure | Description | Formula |
|---|---|---|
| `Diabetes Patients` | Count of patients with diabetic blood glucose readings | ```DIABETES PATIENTS = CALCULATE(DISTINCTCOUNT('Patient_Symptoms'[Patient ID]),'Patient_Symptoms'[Diabetes mg/dL (2hr AfterMeal)]>200)``` |
| `Diabetes %` | Percentage of patients classified as diabetic | ```DIABETES % = DIVIDE([DIABETES PATIENTS],[TOTAL PATIENTS])``` |
| `High BP Patients` | Count of patients with high blood pressure | ```HIGH BP PATIENTS = CALCULATE(DISTINCTCOUNT('Patient_Symptoms'[Patient ID]),'Patient_Symptoms'[Systolic] >= 140 OR 'Patient_Symptoms'[Diastolic] >= 90)``` |
| `High BP %` | Percentage of patients with high blood pressure | ```HIGH BP % = DIVIDE( [HIGH BP PATIENTS],[TOTAL PATIENTS])``` |
| `Avg Systolic BP` | Average systolic blood pressure across all visits | ```AVG SYSTOLIC = AVERAGE('Patient_Symptoms'[Systolic])``` |
| `Avg Diastolic BP` | Average diastolic blood pressure across all visits | ```AVG DIASTOLIC = AVERAGE('Patient_Symptoms'[Diastolic])``` |

---

### 📌 Visit Analysis

| Measure | Description | Formula |
|---|---|---|
| `Repeat Patients` | Count of patients with more than one visit | ```REPEAT PATIENTS = CALCULATE(DISTINCTCOUNT('Patient_Symptoms'[Patient ID]),FILTER(VALUES('Patient_Symptoms'[Patient ID]),CALCULATE(COUNT('Patient_Symptoms'[Visit ID])) > 1))``` |
| `Avg Visit Gap (Days)` | Average number of days between consecutive visits per patient | ```AVERAGE VISIT GAP = AVERAGE('Patient_Symptoms'[Visit Gap Days])``` |
| `Delayed Follow-Up %` | Percentage of visits categorised as delayed follow-ups | ```DELAYED FOLLOW-UP % = DIVIDE(CALCULATE(COUNTROWS('Patient_Symptoms'),'Patient_Symptoms'[Visit Category] = "Delayed Follow-up"),[Total Visits])``` |

---

### 📌 Calculated Measures

| Measure | Description | Formula |
|---|---|---|
| `Hemoglobin Ranges` | Groups hemoglobin levels into different ranges in the Blood Result Tests table | ```Hemoglobin ranges = SWITCH(TRUE(),'Blood Test Results'[Hemoglobin] < 12, "Low (<12)",'Blood Test Results'[Hemoglobin] >= 12 && 'Blood Test Results'[Hemoglobin] < 14, "12-14",'Blood Test Results'[Hemoglobin] >=14 && 'Blood Test Results'[Hemoglobin] < 16, "14-16",'Blood Test Results'[Hemoglobin] >= 16, "High (16+)")``` |
|`Age Group`|Groups patients into different age groups based on their ages|```Age Group = SWITCH(TRUE(),'Patient_Symptoms'[Age] <= 12, "Child (<13)",'Patient_Symptoms'[Age] <= 19, "Teen (13-19)",'Patient_Symptoms'[Age] <= 35, "Young Adult (20-35)",'Patient_Symptoms'[Age] <= 60, "Adult (36-60)","Senior (>60)")```|
|`Diabetes Category`|Groups patients into two categories based on their diabetes level|```Diabetes Category = IF('Patient_Symptoms'[Diabetes mg/dL (2hr AfterMeal)] > 200,"Diabetic Range","Normal Range")```|
|`BP Risk`|Groups patients into two categpoories based on the blood pressue risk using systolic and diastolic blood pressure levels|```BP Risk = IF('Patient_Symptoms'[Systolic] >= 140 OR'Patient_Symptoms'[Diastolic] >= 90,"High BP","Normal")```|
|`Previous Visit Date`|Calculates the previous visit date and returns blank it there is none|```Previous Visit Date = CALCULATE(MAX('Patient_Symptoms'[Visit Date]),FILTER('Patient_Symptoms','Patient_Symptoms'[Patient ID] = EARLIER('Patient_Symptoms'[Patient ID]) &&'Patient_Symptoms'[Visit Date] < EARLIER('Patient_Symptoms'[Visit Date])))```|
|`Visit Categories`|Categorizes visit based on the visit gap in days|```Visit Category = SWITCH(TRUE(),ISBLANK('Patient_Symptoms'[Previous Visit Date]), "First Visit",'Patient_Symptoms'[Visit Gap Days] <= 30, "Regular",'Patient_Symptoms'[Visit Gap Days] <= 90, "Moderate Gap","Delayed Follow-up")```|
|`Visit Type`|Categorizes visits as one-time or repeat|```Visit Type = IF(CALCULATE(COUNT('Patient_Symptoms'[Visit ID]),ALLEXCEPT('Patient_Symptoms', 'Patient_Symptoms'[Patient ID])) > 1,"Repeat","One-Time")```|

## Disclaimer

> ⚠️ *This report is generated using AI and demographic data; the results may not be fully accurate. It is intended for analytical and educational purposes only and should not be used as a substitute for professional medical advice or clinical decision-making.*

---

---

### 👤 About the Author

**Abdulsamad K** · Data Analyst | Power BI Developer | BI Analyst ·

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/abdulsamad-kudehinbu/)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-34A853?style=flat&logo=google)](https://sites.google.com/view/abdulsamadportfolio/home)
