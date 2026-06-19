# Application Tracking Insight 
> *Analyzed 313 Tech Programme application records using Google Sheets to uncover course popularity trends, applicant behaviour patterns, payment status insights, and weekly submission trends.*

---

## ⚙️ Project Type Flags
> *Check what applies. This helps reviewers and collaborators understand the nature of the work at a glance. Delete this block before publishing.*

- [x] Exploratory Data Analysis (EDA)
- [ ] SQL Analysis / Querying
- [x] Dashboard / Data Visualization
- [ ] Data Pipeline / ETL
- [ ] Predictive Modelling / Machine Learning
- [x] Data Cleaning / Wrangling
- [ ] End-to-End (multiple of the above)
- [ ] Other: ___________
---

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Project Scope & Tools](#3-project-scope--tools)
4. [Repository Structure](#4-repository-structure)
5. [Data Workflow](#5-data-workflow)
6. [Data Model & Schema](#6-data-model--schema)
7. [Analysis & Metrics](#7-analysis--metrics)
8. [Key Insights](#8-key-insights)
9. [Recommendations](#9-recommendations)
10. [Deliverables](#10-deliverables)
11. [Author](#11-author)

---

## 1. Project Overview

**Context:** A Tech Training Academy runs a programme that accepts applications from prospective students across multiple courses. The Academy needed a structured analysis of its application data to understand applicant behaviour, course demand, and payment patterns.

**Problem Statement:** Application records were collected but had not been analyzed - there was no clear picture of which courses were most popular, how many applicants were repeat applicants, what the payment completion rate looked like, or how submissions varied week by week.

**Approach:** Cleaned and transformed 313 application records in Google Sheets using data cleaning techniques including deduplication, phone number normalization, date formatting, and handling of encoding errors. Conducted exploratory data analysis using Pivot Tables, COUNTIF, and charts to identify patterns across course preferences, applicant behaviour, payment status, and weekly submission trends. Built an interactive dashboard to present findings visually.

**Outcome:** Delivered a clean, interactive Google Sheets dashboard revealing key trends in course popularity, repeat applicant patterns, payment performance, and submission behaviour -findings were presented to the Internflare Academy CEO.

---

## 2. Objectives
- **Primary Objective:** Conduct exploratory data analysis on 313 Tech Programme application records to uncover meaningful patterns in course demand, applicant behaviour, and payment performance.

- **Secondary Objective 1:** Identify the most popular courses by total application count to inform future programme planning.

- **Secondary Objective 2:** Detect repeat applicants and understand their behaviour patterns across multiple application cycles.

- **Secondary Objective 3:** Analyze payment status across applicants to determine payment completion rates and outstanding balances.

- **Secondary Objective 4:** Examine weekly submission trends to identify peak and low application periods throughout the programme cycle.

> 💡 Every analysis decision in this project traces back to one of these objectives.

---

## 3. Project Scope & Tools

### Scope

| Dimension | Details |
|------------|---------|
| **In Scope** | 313 application records covering applicant names, roles applied for, form responses, and submission timestamps |
| **Out of Scope** | Applicant contact details, payment data, and post-application outcomes - these were not available in the dataset |
| **Time Period** | Application records covering January 2026 - April 2026 |
| **Granularity** | Row -level application data (one row per application submission) |

### Tools & Technologies

| Category | Tool(s) Used |
|----------|--------------|
| Data Cleaning | Google Sheets (deduplication, timestamp standardization, role name standardization, encoding fixes) |
| Data Analysis | Google Sheets (COUNTIF, Pivot Tables, sorting, filtering) |
| Data Visualization | Google Sheets (Pivot Charts, bar charts, line charts) |
| Dashboard Design | Google Sheets (interactive dashboard) |
| Documentation | Microsoft Word, GitHub |

---
## 4. Repository Structure
```
Application-Tracking-Insights/
|
├── data/
|   └── raw/              # Original, unmodified application dataset
|
├── docs/                 # Data dictionary and project notes
|
├── reports/              # Written summary report
|
├── visuals/              # Dashboard screenshots and charts
|
├── README.md             # You are here
└── project_metadata.yml  # Project metadata
```
---

## 5. Data Workflow

1. **Source:** One Google Sheets dataset containing 313 Tech Programme application records, capturing applicant names, roles applied for, form responses, and submission timestamps.
2. **Ingestion:** Dataset loaded and opened directly in Google Sheets for cleaning and analysis.
3. **Cleaning:** The following data quality issues were identified and resolved:
   - Removed duplicate application entries
   - Standardized timestamp formatting for date-based analysis
   - Resolved encoding errors in text fields
   - Identified and flagged repeat applicants across multiple submission cycles
   - Standardized role names for consistent grouping and analysis
4. **Analysis:** Conducted exploratory data analysis using Pivot Tables and COUNTIF formulas to examine role popularity, repeat applicant patterns, form response rates, and weekly submission trends.
5. **Visualization:** Built an interactive dashboard in Google Sheets using Pivot Charts, bar charts, and line charts to present findings clearly to a non-technical audience.
6. **Output:** Interactive Google Sheets dashboard, written summary report (Word document), dashboard screenshots uploaded to GitHub, and full project documentation in this repository.

---

## 6. Data Model & Schema

## Data Dictionary

| Field Name | Data Type | Description | Example Value |
|------------|-----------|-------------|---------------|
| `Timestamp` | DateTime | Date and time application was submitted | 1/27/2026 11:48:41 |
| `Full Name` | Text | Full name of the applicant | Promise Umoh |
| `Role Applied For` | Text | Role the applicant applied for | Virtual Assistant |
| `Form Response` | Text | Whether applicant confirmed details | Yes / No |

> **Row count:** 313 application records
> **Date range:** January 2026 – April 2026
> **Key note:** Dataset required cleaning before analysis — duplicates removed, encoding errors resolved, and timestamps standardized

---

## 7. Analysis & Metrics

### Analytical Approach

This project used an *exploratory data analysis* approach - examining the cleaned application dataset to identify patterns and trends across role preferences, applicant behaviour, form response rates, and submission timing. No hypothesis was tested in advance; the goal was to let the data reveal what was happening in the application cycle.

### Key Metrics Defined

| Metric | Plain-Language Definition | Why It Matters |
|--------|--------------------------|----------------|
| `Total Applications` | Count of all application records in the dataset | Measures overall programme interest and reach |
| `Role Popularity` | Number of applications per role | Identifies which roles are most in demand |
| `Repeat Applicant Count` | Count of applicants who submitted more than once | Reveals applicant persistence and programme appeal |
| `Form Response Rate` | Percentage of applicants who responded Yes vs No | Measures applicant engagement and confirmation rate |
| `Weekly Submission Trend` | Number of applications submitted per week | Identifies peak and low application periods |

### Methods Used

- Data cleaning - deduplication, timestamp standardization, role name standardization, encoding fixes
- Descriptive statistics - total counts, percentages, and distributions across key fields
- Pivot Tables - cross-tabulation of applications by role, form response, and week
- COUNTIF formulas - counting specific values across the dataset
- Trend analysis - weekly submission patterns across the application cycle
- Data visualization - charts and dashboard to present findings clearly
  
---

## 8. Key Insights

1. **Total applications received were 313 from 281 unique applicants** - indicating strong overall interest in the Tech Programme with mostly first-time applicants.

2. **Virtual Assistant is the most applied-for role with 112 applications (39.9% of total)** - dominating by a wide margin and accounting for nearly 40% of all applications confirming it as the highest demand role.

3. **Customer Support/Service (63 applications, 22.4%) and Executive Assistant (35 applications, 12.5%) are the second and third most popular roles** - together with Virtual Assistant, the top 3 roles combined account for 210 applications (74.8% of total).

4. **There are 16 total role categories** - showing a wide range of programme offerings, though demand is heavily concentrated in the top 3 roles.

5. **The least applied-for roles each received only 1 application (0.4%)** - Video Editing, IT, Design And Creative, and Backend Web Developer all tied at the bottom with 6 applications combined representing just 3% of total suggesting these roles need stronger visibility and targeted promotion.

6. **Sales & Lead Generation (18, 6.4%), Social Media Manager (14, 5%), and Copywriting/Content Writer (11, 3.9%)** form a mid-tier of roles with moderate but consistent demand.

7. **Tuesday is the peak application day** - with Monday and Tuesday together recording the highest submission volumes across the week.

8. **30 repeat applicants were recorded** - representing 9.6% of total applications indicating high unique applicant engagement.

---

## 9. Recommendations

<!--
  Action-oriented. Addressed to a real audience.
  Tied explicitly to the insight that supports each one.

  WHAT GOOD LOOKS LIKE:
  Priority: High
  Recommendation: "Conduct a fulfilment audit for home goods deliveries
                   in Region A - specifically investigating whether returns
                   correlate with a particular warehouse, carrier, or SKU batch."
  Based On: Insight 1 - return rate anomaly in Region A
  Owner: Operations / Supply Chain team

  WHAT TO AVOID:
  ❌ "Improve the return rate."
     (Not actionable. Doesn't say who, how, or where to start.)
  ❌ "Further analysis is needed."
     (This is a placeholder, not a recommendation.)
-->

| Priority | Recommendation | Based On | Suggested Owner |
|----------|---------------|----------|-----------------|
| High | [Specific, actionable step] | [Insight it comes from] | [Who should act] |
| Medium | [Specific, actionable step] | [Insight it comes from] | [Who should act] |
| Low | [Exploratory or longer-term suggestion] | [Insight it comes from] | [Who should act] |

---

## 10. Deliverables

| Deliverable | Description | Location |
|-------------|-------------|----------|
| [Name] | [What it contains] | [`/path/to/file`] |
| [Name] | [What it contains] | [`/path/to/file`] |
| [Name] | [What it contains] | [`/path/to/file`] |

---

## 11. Author

**[Your Name]**
[Your role or title - current or target]

- 🔗 [LinkedIn URL]
- 💼 [Portfolio or GitHub profile URL]
- 📧 [Email - optional]

---

*Last updated: [Month YYYY]*
*If this template helped you, consider starring the repository.*
