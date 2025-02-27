# Excel Salary Dashboard

![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/adafbdea-5b21-4ee3-bad6-ff58c583d022)


## Introduction

This dashboard provides a detailed look at salaries within the data job sector, designed to assist job seekers in evaluating potential earnings accurately.

The information is derived from a specialized Excel course and showcases extensive data on professional roles, compensation, geographic locations, and necessary skills.

### Dashboard File
Access the complete dashboard here: [1_Salary_Dashboard.xlsx](1_Salary_Dashboard.xlsx).

### Excel Skills Used

Skills applied in this analysis include:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

Our dataset encompasses a wide array of 2023 data science job information, accessible through our Excel course. This includes:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/b5d7d1d2-4461-4505-8608-0512158eec47)


- 🛠️ **Excel Features:** The bar chart function is used here to display salary data effectively.
- 🎨 **Design Choice:** A horizontal layout is selected to facilitate easy comparison of median salaries.
- 📉 **Data Organization:** Salaries are organized in descending order to highlight top earners.
- 💡 **Insights Gained:** This visualization quickly demonstrates salary trends, with senior roles and engineers earning more than analysts.

#### 🗺️ Country Median Salaries - Map Chart

![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/31089c0b-95cf-465d-915f-ce1a9a032cc6)


- 🛠️ **Excel Features:** The map chart tool is used to depict global salary data.
- 🎨 **Design Choice:** A color-coded approach differentiates salary levels across countries.
- 📊 **Data Representation:** Each country's median salary is displayed.
- 👁️ **Visual Enhancement:** The map enhances readability and comprehension of global salary trends.
- 💡 **Insights Gained:** This chart provides a clear view of international salary variations, highlighting regions with higher and lower earnings.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)

