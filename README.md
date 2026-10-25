# People Analytics & DEIB Dashboard | Power BI

## Project Overview

This project explores workforce composition, salary differences, and inclusion and belonging indicators using Power BI, Power Query, and DAX.

The dashboard demonstrates how HR data can be transformed into interactive visualizations to support workforce reporting and descriptive analysis. It is designed as a portfolio project for People Analytics, HR Data Analytics, and Diversity, Equity, Inclusion, and Belonging (DEIB).

**Important:** The dataset is synthetic and intended for learning and portfolio demonstration. The findings do not describe a real organization.

## Interactive Power BI Dashboard

**[Open the interactive Power BI report](https://app.powerbi.com/view?r=eyJrIjoiMjFjY2U3NjQtNTc4MC00ZjMyLTg3NmYtMzJjMWI0ZmE0MWFmIiwidCI6IjU4ZTMxMjU3LWY3N2YtNGQ1OC05NzA1LWQwYjZlYTBmOWVlNCIsImMiOjh9)**

Explore the three report pages:
- Workforce Overview
- Pay Equity Analysis
- Inclusion & Belonging

*The report uses synthetic data and is intended for portfolio demonstration.*

## Business Objectives

- Monitor workforce composition and employment status.
- Examine headcount distribution across departments.
- Compare median monthly salaries across job levels and nationality groups.
- Explore descriptive salary differences within the same job level.
- Review inclusion, manager inclusion, and belonging scores.
- Demonstrate data transformation, DAX measures, data visualization, and analytical communication.

## Dashboard Pages

### 1. Workforce Overview

![Workforce Overview](01%20%E2%80%94%20Workforce%20Overview.png)

Provides an overview of employee records, active headcount, terminated employees, and terminated share.

Key visuals:
- Employee Records
- Active Headcount
- Terminated Employees
- Terminated Share %
- Active Headcount by Department
- Terminated Share by Department

### 2. Pay Equity Analysis

![Pay Equity Analysis](02%20%E2%80%94%20Pay%20Equity%20Analysis.png)

Explores median monthly salaries among active employees by job level and nationality group.

Key visuals:
- Active Median Salary by Job Level
- Active Median Salary by Nationality Group
- Median Salary by Nationality Group and Job Level
- Salary Gap % by Nationality Group and Job Level

The salary gap measure compares each group's median salary with the active-employee median benchmark for the corresponding job level.

These comparisons are descriptive. They do not, by themselves, establish discrimination, causation, or unjustified pay inequity.

### 3. Inclusion & Belonging

![Inclusion & Belonging](03%20%E2%80%94%20Inclusion%20%26%20Belonging.png)

Explores employee inclusion, manager inclusion, and belonging scores among active employees with valid responses.

Key indicators:
- Average Inclusion Score
- Average Manager Inclusion Score
- Average Belonging Index

Key visuals:
- Average Inclusion Score by Department
- Average Belonging Index by Nationality Group
- Average Manager Inclusion Score by Department

Tooltip measures provide the number of valid responses for the relevant indicators, helping users interpret averages in context.

## Key Metrics

The current dataset contains 1,500 unique employee records.

| Metric | Current result |
|---|---:|
| Employee Records | 1,500 |
| Active Headcount | 1,261 |
| Terminated Employees | 239 |
| Terminated Share | 15.93% |
| Active Median Monthly Salary | €3,790 |
| Average Inclusion Score | 3.59 |
| Average Belonging Index | 3.38 |
| Average Manager Inclusion Score | 3.50 |

The salary and inclusion figures are descriptive results from the current synthetic dataset. They may vary when report filters are applied.

## Tools and Techniques

- **Microsoft Power BI:** Interactive dashboard development and data visualization.
- **Power Query:** Data preparation and transformation.
- **DAX:** Measures, filter context, median salary calculations, percentage comparisons, and response counts.
- **Data modeling:** Relationship between employee records and the job-level salary band reference table.
- **HR analytics:** Workforce reporting, descriptive salary analysis, and inclusion metrics.

## Data Model

The model includes:
- `Employees`: employee-level workforce, salary, employment status, and survey-related data.
- `PayBandsTable`: job levels, labels, and illustrative monthly salary bands.

The relationship connects `PayBandsTable[JobLevel]` to `Employees[JobLevel]` in a one-to-many model, with single-direction filtering.

## Methodology and Limitations

- Workforce counts use distinct employee identifiers.
- Salary comparisons use median monthly salary rather than averages alone.
- Salary gap percentages compare nationality groups with the active-employee median benchmark within each job level.
- Inclusion and belonging averages use valid, non-blank scores for active employees.
- Response counts are included to provide context for survey-based averages.
- The terminated share represents the proportion of employee records classified as terminated in this dataset. It is not an annual attrition rate.
- The dataset is synthetic. Results must not be interpreted as evidence about real employees or as proof of discrimination, causation, or organizational inclusion outcomes.
- Differences within job level may still reflect other factors, such as job family, department, experience, or role-specific responsibilities.

## Skills Demonstrated

- People Analytics
- HR Data Analytics
- Microsoft Power BI
- DAX
- Power Query
- Data Cleaning and Preparation
- Data Modeling
- Workforce Analytics
- Salary and Pay Gap Analysis
- DEIB Metrics
- Data Visualization
- Analytical Communication
- Data Interpretation

## Future Improvements

Potential extensions include:
- Add a dedicated data-quality and salary-band validation page.
- Analyze hiring, retention, and turnover trends over time when suitable data is available.
- Add additional controls for response counts and missing survey data.
- Extend salary comparisons to account for job family, department, tenure, and other relevant factors.
- Improve accessibility, report navigation, and dashboard documentation.

## Disclaimer

This is an independent portfolio project using synthetic data. It is not a client engagement, an audit of a real employer, or a statistical finding about actual pay equity.

The purpose is to demonstrate Power BI reporting and descriptive People Analytics techniques.
