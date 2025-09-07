# My Excel Data Analytics Projects

![Adobe Express - Screen Recording 2025-09-07 at 00 29 59](https://github.com/user-attachments/assets/0288923b-54ce-44b4-aa88-2b92e4546c97)

## Introduction
This salary dashboard for data jobs was created to help job seekers research salaries for their desired positions and ensure they are being adequately compensated.

The data was sourced from Luke Barousse's Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
My final dashboard is in [Salary_Dashboard_Excel](https://github.com/nzubehenry/Excel_Project_Data_Analysis/blob/main/Book1.xlsx)

### Excel Skills Used
The following Excel skills were utilized for analysis:

- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation

### Data Jobs Dataset
The dataset used for this project contains real-world data on job information in data science from 2023. The dataset is a combination of job postings scraped from different job sites. It includes detailed information on:

- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills

# Dashboard Build
## 📉 Charts
### 📊 Data Science Job Salaries - Bar Chart
<img width="600" height="430" alt="Screenshot 2025-09-07 at 17 09 15" src="https://github.com/user-attachments/assets/82fb5fef-619a-437a-a595-249eec5e0a8b" />



- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

### 🗺️ Country Median Salaries - Map Chart

<img width="600" height="430" alt="image" src="https://github.com/user-attachments/assets/150f3626-0aa5-4a55-89e0-cb06884662b1" />



- 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions
### 💰 Median Salary by Job Titles

```
=MEDIAN(
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
- 📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
- 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.

### 🍽️ Background Table

<img width="265" height="220" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/b6d10ba3-ddc6-4100-b8fe-0b8d9c797aa8" />


### 📉 Dashboard Implementation

<img width="430" height="430" alt="1_Salary_Dashboard_Job_Title" src="https://github.com/user-attachments/assets/3d0aa842-7c79-48d1-ad26-eb9fd9d153dd" />



⏰ Count of Job Schedule Type

``` =FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0)) ```

- 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
- 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.

### 🍽️ Background Table

<img width="265" height="220" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/00ee58fa-a055-435d-bd7a-1b42e98198bf" />


### 📉 Dashboard Implementation:

<img width="430" height="430" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/aa13b187-1a3e-468a-b140-d829fc5bca86" />


## ❎ Data Validation
### 🔍 Filtered List
- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type options in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced
 
  ![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/353ec91e-869a-4f40-8ba7-653af6359c53)


# Conclusion
I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing the dataset, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.



