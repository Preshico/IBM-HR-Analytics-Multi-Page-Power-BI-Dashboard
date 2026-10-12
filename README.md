HR Analytics Dashboard | Turning Data into Insights and Insights into Impact
Project Overview

Employee turnover is more than an HR concern. It affects productivity, increases recruitment costs, reduces team stability, and impacts business performance.

This project was developed to help HR professionals and business leaders understand their workforce through data. Rather than simply presenting metrics, the goal was to answer meaningful business questions, uncover patterns, and provide recommendations that support better decision-making.

Business Objectives

This project seeks to answer questions such as:

What is the overall state of the workforce?
Which departments and job roles experience the highest attrition?
What factors appear to influence employee turnover?
Does employee satisfaction affect retention?
Are compensation and career progression linked to attrition?
Which employee groups should HR prioritize for retention efforts?
What actions can management take to improve employee retention?

Dashboard Pages
Page 1 — HR Executive Overview

A high-level snapshot of the entire workforce with key metrics and department-level breakdowns.

KPIs: Total Employees · Active Employees · Employees Left · Attrition Rate · Average Age · Average Years at Company · Average Job Satisfaction · Average Monthly Income

Charts:

Workforce by Department
Workforce by Gender
Attrition by Department
Employees by Age Group
Employees by Education
Business Travel Distribution
Workforce Composition by Job Role
Page 2 — HR Attrition Analysis

A deep dive into attrition patterns across multiple dimensions to identify key drivers of employee turnover.

KPIs: Total Employees · Employees Left · Attrition Rate · Active Employees · Avg Years at Company (Left) · Avg Age (Left)

Charts:

Attrition by Department
Attrition by Job Role
Attrition by Overtime
Attrition by Marital Status
Attrition by Education Field
Attrition by Gender
Attrition by Age Group
Attrition by Income Band
Attrition by Years at Company
Attrition by Distance from Home
Page 3 — Performance, Compensation & Satisfaction

An analysis of how performance ratings, compensation levels, and satisfaction scores relate to employee retention.

KPIs: Avg Job Satisfaction · Avg Environment Satisfaction · Avg Relationship Satisfaction · Avg Work-Life Balance · Avg Performance Rating · Avg Monthly Income

Charts:

Average Monthly Income by Job Role
Performance Rating Distribution
Satisfaction Scores (out of 5)
Salary vs Attrition Rate
Training Times Last Year
Years Since Last Promotion
Years with Current Manager
Work-Life Balance vs Attrition Rate
Attrition Rate by Job Satisfaction

Key Takeaway Metrics:

High Satisfaction Attrition Rate
Recent Promotion Attrition Rate
High Training Attrition Rate
High Income Attrition Rate
Page 4 — Workforce Demographics & Strategic Insights

A workforce composition and tenure analysis providing strategic insights for HR planning and decision-making.

KPIs: Total Employees · Active Employees · Avg Years at Company · Avg Years in Current Role · Avg Years with Manager · Avg Salary Hike · Stock Option Employees

Charts:

Employees by Education Field
Employees by Job Level
Employees by Stock Option Level
Average % Salary Hike by Job Level
Years at Company (Tenure)
Years in Current Role
Years with Current Manager
Distance from Home
Workforce by Age Group
Department Composition
Employee Segment Insights (Table)
🛠️ Tools & Techniques
Tool	Usage
Power BI Desktop	Dashboard design and development
DAX	Calculated measures and columns
Power Query	Data cleaning and transformation
Data Modelling	Relationships and schema design
📐 DAX Measures Created
DAX
-- Core KPI Measures
Total Employees = COUNTROWS('IBM_HR_DATASET')
Active Employees = CALCULATE(COUNTROWS('IBM_HR_DATASET'), 'IBM_HR_DATASET'[Attrition] = "No")
Employees Left = CALCULATE(COUNTROWS('IBM_HR_DATASET'), 'IBM_HR_DATASET'[Attrition] = "Yes")
Attrition Rate = DIVIDE([Employees Left], [Total Employees], 0)

-- Attrition Analysis Measures
Group Attrition Rate = DIVIDE(CALCULATE(COUNTROWS('IBM_HR_DATASET'), 'IBM_HR_DATASET'[Attrition] = "Yes"), COUNTROWS('IBM_HR_DATASET'), 0)
Avg Age (Left) = CALCULATE(AVERAGE('IBM_HR_DATASET'[Age]), 'IBM_HR_DATASET'[Attrition] = "Yes")
Avg Years at Company (Left) = CALCULATE(AVERAGE('IBM_HR_DATASET'[YearsAtCompany]), 'IBM_HR_DATASET'[Attrition] = "Yes")

-- Satisfaction Measures
Avg Satisfaction Score = SWITCH(SELECTEDVALUE('Satisfaction Categories'[Category]), ...)
Avg Environment Satisfaction = AVERAGE('IBM_HR_DATASET'[EnvironmentSatisfaction])
Avg Work Life Balance = AVERAGE('IBM_HR_DATASET'[WorkLifeBalance])

-- Key Takeaway Measures
High Satisfaction Attrition = CALCULATE(DIVIDE(...), 'IBM_HR_DATASET'[JobSatisfaction] >= 4)
Recent Promotion Attrition = CALCULATE(DIVIDE(...), 'IBM_HR_DATASET'[YearsSinceLastPromotion] <= 2)
High Training Attrition = CALCULATE(DIVIDE(...), 'IBM_HR_DATASET'[TrainingTimesLastYear] >= 3)
High Income Attrition = CALCULATE(DIVIDE(...), 'IBM_HR_DATASET'[MonthlyIncome] >= 10000)
📊 Calculated Columns Created
Column	Purpose
Age Group	Groups employees into 5 age bands
Age Group Sort	Ensures correct sort order
Education Label	Converts numeric codes to readable labels
Income Band	Groups monthly income into ranges
Distance Band	Groups commute distance into ranges
Years Promotion Band	Groups years since last promotion
Career Stage	Classifies Early/Mid/Senior career
Tenure Band	Groups years at company into ranges
Current Role Band	Groups years in current role
Manager Years Band	Groups years with current manager
WLB Label	Converts Work-Life Balance scores to labels
JobSat Label	Converts Job Satisfaction scores to labels
Performance Label	Converts performance ratings to labels
Job Level Label	Converts job level codes to labels
Stage Criteria	Describes Career Stage criteria

📁 Dataset

Source: IBM HR Analytics Employee Attrition Dataset Available on: Kaggle

Property	Detail
Rows	1,470 employees
Columns	35 features
Target Variable	Attrition (Yes/No)
Format	CSV
💡 Key Findings
Overall attrition rate is 16.12% with Sales department showing the highest at 20.63%
Early career employees (0-2 years) have the highest attrition at 29.82%
Employees with poor work-life balance (Level 1) leave at 31.25%
Low job satisfaction (Level 1) drives attrition to 22.84% vs 11.33% for very satisfied employees
Employees earning below 5K USD monthly have the highest attrition at 28.12%
42.18% of the workforce is aged 25-34 — the largest and most at-risk group
631 employees (42.93%) have no stock options — a potential retention lever

👩‍💻 Author
Ifeoma Precious Ugwu Data Analyst | Power BI Developer

📌 How to Use
Download the .pbix file from this repository
Open with Power BI Desktop (free download from Microsoft)
All data is embedded — no additional setup required
Use the slicers on the left sidebar to filter by Department, Job Role, Gender, Education, Age Group and more
Click any visual to cross-filter the entire page

Built with Power BI Desktop | IBM HR Analytics Dataset | August 2026
