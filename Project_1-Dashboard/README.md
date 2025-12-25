# Excel Salary Dashboard

![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/db6b65e1-a92c-4f52-b690-d54a925f92ae)


## Introduction

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated. 

The data is from an Excel course by Luke, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
My final dashboard is in [1_Salary_Dashboard-by_Nimra.xlsx](https://github.com/user-attachments/files/24339566/1_Salary_Dashboard-by_Nimra.xlsx).

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. The dataset is available via his Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

<img width="1336" height="867" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/10384a30-af73-4115-801a-5e13cce1c0e2" />


- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart

![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/dce9972a-ed42-4e1c-8765-dfa94881e793)


- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

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

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

<img width="265" height="220" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/a27ccc85-d006-4ed8-9cc0-8287f65ea436" />


📉 Dashboard Implementation

<img width="400" height="500" alt="1_Salary_Dashboard_Job_Title" src="https://github.com/user-attachments/assets/c9d882bf-d8b4-4b8a-ba5e-0d5d33a8e5cb" />


#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

<img width="195" height="119" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/375936bb-0a57-46a7-93f4-e8298e6fe53a" />


📉 Dashboard Implementation:

<img width="400" height="500" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/f3a24116-a95f-4cfa-b5fd-407160805af6" />


### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/65368c60-c7ee-4f02-9e6d-a25a351b8c49)<img src="mygif.gif" width="420" height="400" />

## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from his Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries. 

(All background data sheets are in hidden sheets)
