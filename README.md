# Employees Project

---
## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Recommendations](#recommendations)

---
### Project Overview

This data analysis project aims to provide insights into the project performance of a company over the past year. By analyzing various aspects of the project data, I seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's budget performance.
![employee project-1](https://github.com/user-attachments/assets/2574d2fc-710f-4929-95b6-40c0c41fb0e9)
[employee project.pdf](https://github.com/user-attachments/files/18269279/employee.project.pdf)

---
### Data Sources

Project Data: The primary dataset used for this analysis is the "Employees project.zip" file, containing detailed information about each sale made by the company.

---
### Tools
- SQL Server Management System - Data Analysis
- PowerBI - Creating reports

---
### Exploratory Data Analysis
EDA involved exploring the sales data to answer key questions, such as:

- Who are the key employees involved, and what are their roles?
- Can you provide an overview of the project distribution across teams or departments?
- How is the budget allocated across different projects or initiatives?
- How is the project cost allocated across different projects or initiatives?
- Detail table view.

---
### Data Analysis
Include some interesting code/features worked with

```sql
-- project status
WITH project_status AS
(SELECT project_id, project_name, project_budget, department_id, 'completed' AS status
FROM completed_projects
UNION ALL
SELECT project_id, project_name, project_budget, department_id, 'upcoming' AS status
FROM upcoming_projects)

-- Big Table
SELECT e.employee_id,
	   e.first_name,
	   e.last_name,
	   e.department_id,
	   e.job_title,
	   e.salary,
	   d.Department_Name,
	   d.Department_Budget,
	   d.Department_Goals,
	   ps.project_budget,
	   pa.project_id,
	   ps.project_name,
	   ps.status
FROM employees e
JOIN departments d
ON e.department_id = d.Department_ID
JOIN project_assignments pa
ON pa.employee_id = e.employee_id
JOIN project_status ps
ON ps.project_id = pa.project_id

```

---
### Connecting Database to Power BI

connecting data base from sql to power BI

---
### Results/Findings
The analysis results are summarized as follows:
1. Sales department made the biggest capital among other department.
2. Engineering had a biggest capital
3. Sales department made the biggest total salary among other department
---
### Recommendations
Based on the analysis, we recommend the following actions:
- Budget project distribution make more efficient.
- Propotion for salary made by employees monthly performance to enhance company efficiency
- 
---
### Limitations
I had to remove all zero values from budget and revenue columns because they would have affected the accuracy of my conclusions from the analysis. There are still a few outliers even after the omissions

---
### References
1. SQL for data analysis
2. [(https://stack.com)](https://github.com/Gaelim/youtube/blob/master/Data%20Analysis%20Project%20November%202024%20-%20Copy.zip)](https://github.com/Gaelim/YT_bike_share)

😄

💻

|Heading1|Heading2|
|--------|--------|
|Content|Content2|
|PowerBI|SQL|

`column_1`

