# Excel Salary Dashboard  
![dashboard_demo](https://github.com/user-attachments/assets/3ed0295f-4408-415a-afbc-6f9b0dd10d16)  
## Introduction  
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.
The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.
## Dashboard File
My final dashboard is in [Salary_Dashboard.xlsx](Salary_Dashboard.xlsx)
## Excel Skills Used
The following Excel skills were utilized for analysis:

- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation
## Data Jobs Dataset
The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on:

- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills

# Dashboard Build
## 📉 Charts
### 📊 Data Science Job Salaries - Bar Chart
![job_title_shot](https://github.com/user-attachments/assets/15a374e4-f9e7-49a3-a356-f9bf5a8f521f)  
- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.
### 🗺️ Country Median Salaries - Map Chart
![map_demo](https://github.com/user-attachments/assets/94a519bf-17c1-4c22-8aeb-3f7707a8bad4)  
- 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.
## 🧮 Formulas and Functions
### 💰 Median Salary by Job Titles
```=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```
- 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
- 📊 Array Formula: Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.
### 🍽️ Background Table
![job_title_median_salary](https://github.com/user-attachments/assets/bf9a0d51-219e-417d-80d8-932c1c7c5a66)  
### 📉 Dashboard Implementation
![median_salary](https://github.com/user-attachments/assets/0e32b49c-84aa-4081-9839-217dc04dfbb2)  
### ⏰ Count of Job Schedule Type
`=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))`
- 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
- 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.
### 🍽️ Background Table
![schedule_type_salary](https://github.com/user-attachments/assets/dc007f19-449f-4a96-b65b-db7f55e5c8a5)  
### 📉 Dashboard Implementation:
![type_jobcount](https://github.com/user-attachments/assets/0c97848a-5292-4688-bca4-9e15fb79b1a5)  
## ❎ Data Validation
### 🔍 Filtered List
- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
  - 🎯 User input is restricted to predefined, validated schedule types
  - 🚫 Incorrect or inconsistent entries are prevented
  - 👥 Overall usability of the dashboard is enhanced

![Job_title_list](https://github.com/user-attachments/assets/e745f3a6-63a9-4928-b2d6-f09265028dca)
## Conclusion
I created this dashboard to showcase insights into salary trends across various data-related job titles. This dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.

