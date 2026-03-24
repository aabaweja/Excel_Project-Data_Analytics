# Excel Salary Dashboard
<img width="1891" height="777" alt="Main_Dashboard" src="https://github.com/user-attachments/assets/f360dd3a-2a65-481f-9c08-be72909d96ab" />

## Introduction

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated. 

The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
My final dashboard is in [Project1-Dashboard](https://github.com/aabaweja/Excel_Project-Data_Analytics/blob/main/Project_1%20-%20Data_Science_Salary_Dashboard/Project_1-Dashboard.xlsx)

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart
<img width="1134" height="566" alt="proj1_job_title_Barchart1" src="https://github.com/user-attachments/assets/b09a91ff-c9ca-4924-ae80-2944055052d2" />

- 🛠️ **Excel Features:** Utilized bar chart feature and optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries(salaries are in $USD).
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart

![proj1_country_mapchart](https://github.com/user-attachments/assets/89155cb7-fda6-43bc-a8f2-f919e82a33b0)

- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=MEDIAN(IF(
(data[job_title_short]=$A2)*
(data[job_country]=country_input)*
(ISNUMBER(SEARCH(job_schedule_input,data[job_schedule_type])))*
(data[salary_year_avg]<>0),
data[salary_year_avg]
))
```

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

<img width="606" height="494" alt="proj1_job_title_back_table" src="https://github.com/user-attachments/assets/61f59324-5e2e-4d61-8460-71fa8c017da8" />


📉 Dashboard Implementation

<img width="600" height="681" alt="proj1_job_title_chart_plus_median_salary_KPI" src="https://github.com/user-attachments/assets/bcabfbf7-7eb2-4ec7-ac39-ffbe8b35e4ad" />  

#### ⏰ Count of Job Schedule Type

```
=FILTER(A2#,(NOT(ISNUMBER(SEARCH("and",A2:A33))))*(A2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

<img width="408" height="250" alt="proj1_job_type_background_im" src="https://github.com/user-attachments/assets/1980dc33-6a6d-4b2d-8d2d-fbd529216b02" />


📉 Dashboard Implementation:

<img width="901" height="589" alt="proj1_job_type_dashboard" src="https://github.com/user-attachments/assets/64503851-5a74-4156-8e32-a357ef8bdf9f" />

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

![proj1_data_job_validation](https://github.com/user-attachments/assets/fa61e858-d68d-47bd-95fb-c25f690a2dee)

## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.

