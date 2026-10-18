# HR Analytics Dashboard | Understanding Employee Attrition and Retention

## 1. Business Problem

Employee turnover affects productivity, recruitment costs, team stability, and overall business performance. When employees leave, organizations need to understand where attrition is concentrated and which workforce patterns may be associated with their decisions to leave.

This project uses Power BI to analyze employee attrition across departments, job roles, tenure, job satisfaction, work-life balance, compensation, and other workforce characteristics.

The goal is to help HR professionals and business leaders identify employee groups that may require attention and develop evidence-based strategies to improve retention.

**Key Business Question:** Where is employee attrition highest, which workforce patterns are associated with turnover, and what actions can HR take to improve employee retention?

## 2. Data

- **Dataset:** IBM HR Analytics Employee Attrition Dataset
- **Source:** Kaggle
- **Records:** 1,470 employees
- **Features:** 35 columns
- **Target Variable:** Attrition (Yes/No)
- **File Format:** CSV

The dataset contains employee information covering demographics, departments, job roles, monthly income, job satisfaction, performance ratings, work-life balance, training, promotions, and tenure.

These variables provide a basis for examining workforce composition and comparing attrition rates across employee groups.

## 3. Method

The project followed a structured data analysis and visualization process.

### Data Preparation
Used Power Query to clean and transform the dataset, prepare analytical fields, and create categories suitable for comparison.

### Data Modelling
Organized the data model to support consistent calculations and interactive analysis in Power BI.

### DAX Measures
Developed measures to calculate workforce size, active employees, employee exits, attrition rates, average income, tenure, and satisfaction metrics.

### Workforce Segmentation
Created calculated columns to group employees by age, income, commuting distance, tenure, career stage, job level, years since promotion, and other relevant characteristics.

### Exploratory Analysis
Compared attrition rates across departments, job roles, age groups, income bands, tenure, job satisfaction, work-life balance, and other workforce characteristics.

### Dashboard Development
Built a four-page interactive Power BI dashboard to present workforce metrics, examine attrition patterns, and support HR decision-making.

## 4. Three Key Findings

### Finding 1: Sales Has the Highest Departmental Attrition Rate

The overall attrition rate is **16.12%**, while the Sales department records the highest departmental attrition rate at **20.63%**.

**Business implication:** Sales deserves closer examination to understand whether workload, overtime, management practices, compensation, career development, or other working conditions may be contributing to employee turnover.

### Finding 2: Early-Career Employees Have the Highest Attrition Rate

Employees with **0 to 2 years at the company** have an attrition rate of **29.82%**.

**Business implication:** The early stages of employment may represent an important retention period. HR should investigate onboarding, role expectations, manager support, training, and career progression opportunities for newer employees.

### Finding 3: Poor Work-Life Balance Is Associated with Higher Attrition

Employees reporting the lowest work-life balance score, Level 1, have an attrition rate of **31.25%**.

**Business implication:** HR should examine workload distribution, overtime, scheduling, and employee feedback to identify possible sources of work-life balance difficulties and determine where targeted improvements may be appropriate.

### Additional Finding: Compensation Warrants Further Investigation

Employees earning below **$5,000 per month** have the highest attrition rate at **28.12%**. The analysis also shows that employees with low job satisfaction, Level 1, have an attrition rate of **22.84%**, compared with **11.33%** among employees with the highest job satisfaction, Level 4.

These additional patterns provide useful context for HR teams investigating compensation and employee experience alongside the three principal findings.

**Interpretation note:** These figures describe associations observed in the dataset. They do not establish that any single characteristic independently causes employee turnover.

## 5. Recommendations

### 1. Investigate Attrition in Sales

Review exit records, employee feedback, workload, overtime, compensation, and management practices within the Sales department. Compare these patterns with departments that have lower attrition to identify potential areas for improvement.

### 2. Strengthen Early-Career Retention

Introduce structured onboarding, regular manager check-ins, mentoring, clear performance expectations, and early career development discussions. Monitor attrition by tenure to assess whether these measures are associated with improved retention.

### 3. Address Work-Life Balance Concerns

Examine workloads, overtime patterns, scheduling practices, and employee feedback. Where problems are identified, test targeted changes and compare subsequent attrition rates with previous results.

### 4. Review Compensation and Job Satisfaction

Investigate whether compensation levels, career progression, job responsibilities, and employee satisfaction differ between employees who stay and those who leave. Use the findings to guide targeted retention measures rather than assuming salary alone explains turnover.

### 5. Monitor Workforce Trends Regularly

Use the dashboard to track attrition by department, job role, tenure, satisfaction, income, and other relevant characteristics. Review these indicators regularly to identify emerging patterns and assess the results of retention initiatives.

## 6. Dashboard Overview

The dashboard consists of four interactive pages.

### Page 1: HR Executive Overview

Provides a high-level view of workforce composition and headline HR metrics.

**Key Performance Indicators**
- Total Employees
- Active Employees
- Employees Left
- Attrition Rate
- Average Age
- Average Years at Company
- Average Job Satisfaction
- Average Monthly Income

**Visualizations**
- Workforce by Department
- Workforce by Gender
- Attrition by Department
- Employees by Age Group
- Employees by Education
- Business Travel Distribution
- Workforce Composition by Job Role

### Page 2: HR Attrition Analysis

Examines how employee turnover varies across workforce groups.

**Key Performance Indicators**
- Total Employees
- Employees Left
- Attrition Rate
- Active Employees
- Average Years at Company for Employees Who Left
- Average Age of Employees Who Left

**Visualizations**
- Attrition by Department
- Attrition by Job Role
- Attrition by Overtime
- Attrition by Marital Status
- Attrition by Education Field
- Attrition by Gender
- Attrition by Age Group
- Attrition by Income Band
- Attrition by Years at Company
- Attrition by Distance from Home

### Page 3: Performance, Compensation and Satisfaction

Examines relationships between employee retention, compensation, performance, and workplace experience.

**Key Performance Indicators**
- Average Job Satisfaction
- Average Environment Satisfaction
- Average Relationship Satisfaction
- Average Work-Life Balance
- Average Performance Rating
- Average Monthly Income

**Visualizations**
- Average Monthly Income by Job Role
- Performance Rating Distribution
- Satisfaction Scores on a Five-Point Scale
- Salary vs. Attrition Rate
- Training Times Last Year
- Years Since Last Promotion
- Years with Current Manager
- Work-Life Balance vs. Attrition Rate
- Attrition Rate by Job Satisfaction

**Additional Analytical Measures**
- High Satisfaction Attrition Rate
- Recent Promotion Attrition Rate
- High Training Attrition Rate
- High Income Attrition Rate

These measures allow users to investigate attrition patterns within selected employee groups.

### Page 4: Workforce Demographics and Strategic Insights

Provides a deeper view of workforce composition, career progression, and tenure to support HR planning.

**Key Performance Indicators**
- Total Employees
- Active Employees
- Average Years at Company
- Average Years in Current Role
- Average Years with Manager
- Average Salary Hike
- Employees with Stock Options

**Visualizations**
- Employees by Education Field
- Employees by Job Level
- Employees by Stock Option Level
- Average Percentage Salary Hike by Job Level
- Years at Company
- Years in Current Role
- Years with Current Manager
- Distance from Home
- Workforce by Age Group
- Department Composition
- Employee Segment Insights Table

## 7. Tools and Techniques

| Tool or Technique | Application |
|---|---|
| Power BI Desktop | Dashboard design and development |
| Power Query | Data cleaning and transformation |
| DAX | Measures, calculated columns, and analytical indicators |
| Data Modelling | Data structure and relationship management |
| Exploratory Data Analysis | Workforce segmentation and attrition comparisons |

## 8. DAX Measures

The following are examples of the core measures used in the dashboard.

### Core Workforce Metrics

```dax
Total Employees =
COUNTROWS('IBM_HR_DATASET')

Active Employees =
CALCULATE(
    COUNTROWS('IBM_HR_DATASET'),
    'IBM_HR_DATASET'[Attrition] = "No"
)

Employees Left =
CALCULATE(
    COUNTROWS('IBM_HR_DATASET'),
    'IBM_HR_DATASET'[Attrition] = "Yes"
)

Attrition Rate =
DIVIDE(
    [Employees Left],
    [Total Employees],
    0
)
```

### Attrition Analysis Measures

```dax
Group Attrition Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS('IBM_HR_DATASET'),
        'IBM_HR_DATASET'[Attrition] = "Yes"
    ),
    COUNTROWS('IBM_HR_DATASET'),
    0
)

Avg Age (Left) =
CALCULATE(
    AVERAGE('IBM_HR_DATASET'[Age]),
    'IBM_HR_DATASET'[Attrition] = "Yes"
)

Avg Years at Company (Left) =
CALCULATE(
    AVERAGE('IBM_HR_DATASET'[YearsAtCompany]),
    'IBM_HR_DATASET'[Attrition] = "Yes"
)
```

### Satisfaction Measures

```dax
Avg Environment Satisfaction =
AVERAGE(
    'IBM_HR_DATASET'[EnvironmentSatisfaction]
)

Avg Work Life Balance =
AVERAGE(
    'IBM_HR_DATASET'[WorkLifeBalance]
)
```

Additional measures were created for satisfaction categories and attrition among employees meeting selected criteria, including job satisfaction levels, recent promotions, training frequency, and monthly income thresholds.

## 9. Calculated Columns

The dashboard uses calculated columns to support consistent grouping, sorting, and interpretation.

| Calculated Column | Purpose |
|---|---|
| Age Group | Groups employees into five age bands |
| Age Group Sort | Maintains the correct age-band order |
| Education Label | Converts education codes into readable labels |
| Income Band | Groups monthly income into ranges |
| Distance Band | Groups commuting distances into ranges |
| Years Promotion Band | Groups years since last promotion |
| Career Stage | Classifies employees into career stages |
| Tenure Band | Groups years at the company |
| Current Role Band | Groups years in the current role |
| Manager Years Band | Groups years with the current manager |
| WLB Label | Converts work-life balance scores into labels |
| JobSat Label | Converts job satisfaction scores into labels |
| Performance Label | Converts performance ratings into labels |
| Job Level Label | Converts job level codes into readable labels |
| Stage Criteria | Describes the criteria used for career-stage classification |

## 10. Business Value

This project demonstrates how employee data can be transformed into an interactive analytical tool that supports workforce planning and retention decisions.

The dashboard helps HR professionals and business leaders:

- Monitor workforce composition and employee turnover.
- Identify departments and employee groups with elevated attrition.
- Examine patterns associated with satisfaction, compensation, tenure, and working conditions.
- Prioritize areas for further investigation.
- Track workforce indicators to support more informed retention decisions.

The central value of the project is the connection between workforce metrics, analytical findings, and practical recommendations.

## 11. How to Use the Dashboard

1. Download the `.pbix` file from this GitHub repository.
2. Open it using Power BI Desktop.
3. Use the slicers on the left sidebar to filter by department, job role, gender, education, age group, and other available categories.
4. Select charts or data points to cross-filter the visuals on the relevant page.
5. Compare employee groups and examine the measures to explore the patterns behind the overall workforce figures.

The dashboard file contains the data required for the report, so no separate dataset setup should be necessary.

## Author

**Ifeoma Precious Ugwu**  
Data Analyst | Power BI Developer

**Tools:** Power BI Desktop, DAX, Power Query  
**Dataset:** IBM HR Analytics Employee Attrition Dataset  
**Project Date:** August 2026
