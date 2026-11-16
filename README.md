# AI Usage Analysis — Who Uses AI, Which Tools, and Why

**Author:** Avadhesh Sahani  
**Tools:** Python (Pandas, NumPy, Matplotlib, Jupyter Notebook) · Power BI Desktop  

---

## Project Overview

This repository contains an end-to-end data analytics project examining how **141 users** adopt and engage with AI tools across **12 countries**. Using Python for data cleaning and exploratory data analysis (EDA) and Power BI Desktop for interactive visualization, the project evaluates AI platform popularity, primary use cases, daily usage hours, and demographic segments.

📄 **Full Report:** [AI\_Usage\_Analysis\_Report.pdf](https://www.google.com/search?q=AI_Usage_Analysis_Report.pdf)  
📓 **Analysis Notebook:** [AI\_usage\_anylisis.ipynb](https://www.google.com/search?q=AI_usage_anylisis.ipynb)


## Business Questions Answered

1. Which AI tools are most popular among users?
2. Which countries have the highest number of AI users?
3. Which AI tools have the highest average daily usage time?
4. What are the most common purposes for using AI tools?
5. How does AI usage vary across education levels, age groups, and gender?

---

## Data Cleaning & Preparation (`AI_usage_anylisis.ipynb`)

- **Dataset Dimensions:** `141` rows × `19` columns (`0` duplicate rows).
- **Missing Values Handled (`6` total across `5` columns):**
  - **Mean imputation:** `Age` (1), `Monthly_AI_Cost` (1), `Satisfaction_Score` (1), `Time_Saved_Hours_Per_Week` (1).
  - **Median imputation:** `Monthly_Income` (2) — chosen due to strong right-skew (mean `3,204.19`, median `578.00`, max `250,000.00`).
- **Export:** Saved the cleaned dataset to `AI_Usage_Cleaned.csv` for Power BI ingestion.

### Key Descriptive Statistics
| Measure | Dataset Result |
| :--- | :--- |
| Average Age | 29.93 years |
| Average Daily AI Usage | 2.97 hours *(Power BI KPI displays rounded `3.00`)* |
| Monthly AI Cost (Mean) | $10.50 |
| Productivity Score | 5.17 |
| Accuracy Rating | 3.41 |
| Satisfaction Score | 6.08 |
| Weekly Time Saved | 6.05 hours/week |

---

## Key Findings & Insights

- **Most Popular AI Tool:** **ChatGPT** leads with **61 of 141 users (43.3%)**, followed by Google Gemini (20) and Microsoft Copilot (19).
- **Highest Daily Engagement (Top 5 Tools):** **Google Gemini** ranks first at **~3.84 hours/day**, followed by Microsoft Copilot (3.00), Claude (2.93), ChatGPT (2.92), and DeepSeek (2.63) — demonstrating that user adoption and daily engagement measure different behaviors.
- **Leading Use Case:** **Coding** is the top stated purpose (**41 users, 29.1%**), followed by Research (15.6%), Writing (15.6%), and Studying (12.1%).
- **Top Countries:** **India** is the largest country group (**24 users, 17.0%**), followed by Canada (16) and the United States (15).
- **Education & Demographics:**
  - **Education Level:** Bachelor's (35), Master's (32), Undergraduate (31), High School (24), Diploma (14), PhD (5).
  - **Gender Split:** Male 72 (51.1%), Female 64 (45.4%), Other 5 (3.5%).
  - **Age Group Engagement:** Users aged 50+ average ~5.97 hrs/day (6 users), 10–19 average 3.58 hrs/day (13 users), and 20–29 average 2.78 hrs/day (70 users).

---

## Power BI Dashboard



The single-page Power BI dashboard features a dark navy theme with blue and pink accents:
- **KPI Cards:** Total Users (`141`) and Average Daily Hours (`3.00`, rounded from `2.97`).
- **Interactive Slicers:** Filter across `Country` and `AI_Tool`.
- **Visualizations:** Users by Country, Users by Gender, Total Users by AI Tool, Usage by AI Purpose, Daily AI Usage by Tool, and Users by Education Level.

---

## Data Limitations & Recommendations

### Recommendations
1. Focus product and workflow features on **coding assistance**, the #1 stated use case.
2. Track both **adoption (user count)** and **engagement (daily hours)** when benchmarking AI tools.
3. Validate India and North American market patterns with a larger, more representative sample.
4. Audit extreme values and collect more data for small subgroups before building predictive models.

### Limitations
- **Small Sample & Subgroups:** 141 total records, with small counts for PhD (5), Other gender (5), and Age 50+ (6).
- **Outliers Retained:** Extreme values (e.g., 23 hrs/day AI usage, age 97) were kept in the dataset.
- **Unparsed Free Text:** Mixed-language/encoding issues in `Tasks_Performed` were excluded from quantitative analysis.

