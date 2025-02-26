# Excel Power Query Analysis

![Excel_Power_Query](https://github.com/user-attachments/assets/02f662bf-9100-435e-8898-981420ce0a02)

## Introduction

The data science market often lacks clear data on the best roles and necessary skills. This project investigates the skills demanded by top employers and their correlation with salary expectations.

### Questions to Analyze

To gain insights into the data science job market, we explored the following questions:

1. **Do more skills equate to higher salaries?**
2. **How do salaries vary across different regions?**
3. **What skills are most valued among data professionals?**
4. **How are the top skills compensated?**

### Excel Skills Used

Analysis was performed using the following Excel capabilities:

- **📊 Pivot Tables**
- **📈 Pivot Charts**
- **🔍 Power Query**

### Data Jobs Dataset

The dataset features extensive 2023 data science job information from an Excel-based course, covering:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## 1️⃣ Do more skills get you better pay?

### 🔍 Skill: Power Query (ETL)

#### 📥 Extract

- Initially, data was extracted using Power Query for
    - 🗃️ A complete set of job information.
    - 🔧 A list of skills associated with each job ID.

#### 🔄 Transform

- Each dataset was then refined by adjusting data types, stripping unnecessary columns, cleansing text, and trimming whitespace.
    - 📊 data_jobs_all

      <img width="187" alt="2_Project_Analysis_Screenshot1" src="https://github.com/user-attachments/assets/d4bb1c8d-1d2d-4335-a5c5-7f7ef1d65d03" />


    - 🛠️ data_job_skills

        <img width="187" alt="2_Project_Analysis_Screenshot2" src="https://github.com/user-attachments/assets/a70be0f2-37bc-489d-b50d-34308376586a" />


### 📊 Analysis

#### 💡 Insights

- Analysis shows a positive link between the diversity of requested skills in job ads and the salaries offered, especially for senior positions like Data Engineers and Scientists.
- Lower complexity roles such as Business Analysts often have reduced pay, indicating that specialized skills fetch a premium.

   <img width="466" alt="2_Project_Analysis_Chart1" src="https://github.com/user-attachments/assets/a2b3ccd2-fc7b-4dee-8e0a-ccf318c450c4" />


#### 🤔 So What

- Highlighting multiple relevant skills can significantly elevate salary prospects, especially in high-paying roles.

## 2️⃣ What’s the salary for data jobs in different regions?

### 🧮 Skills: PivotTables & DAX

#### 📈 Pivot Table

- A PivotTable was constructed using the previously created Data Model with Power Pivot, showcasing average salaries by job title and calculating median salaries for jobs in the United States:
    ```
    =CALCULATE(
        MEDIAN(data_jobs_all[salary_year_avg]),
        data_jobs_all[job_country] = "United States")
    ```

#### 🧮 DAX

- Median annual salary calculations were performed using DAX:

    ```
    Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
    ```

### 📊 Analysis

#### 💡 Insights

- Roles such as Senior Data Engineer and Data Scientist command top salaries globally, reflecting their critical importance.
- The salary gap between the US and other countries is stark, especially in tech-focused roles, influenced by the heavy presence of tech industries in the US.

    <img width="644" alt="2_Project_Analysis_Chart2" src="https://github.com/user-attachments/assets/63c630e0-eaeb-4a9b-a693-8fe249e62e05" />


#### **🤔 So What**

- These insights are vital for salary negotiations and strategic planning, allowing professionals to align expectations with the global salary landscape.

## 3️⃣ What are the top skills of data professionals?

### 🔧 Skill: Power Pivot

#### 💪 Power Pivot

- A comprehensive data model was developed by merging `data_jobs_all` and `data_jobs_skills`, which had been cleansed in earlier steps.

#### 🔗 Data Model

- Connections between the tables were established using the `job_id` column.

    <!-- Insert screenshot: 2_Project_Analysis_Screenshot5.png -->

#### 📃 Power Pivot Menu

- The Power Pivot menu facilitated the refinement of the data model and the creation of complex measures.

    <!-- Insert screenshot: 2_Project_Analysis_Screenshot6.png -->

### 📊Analysis

#### 💡Insights

- SQL and Python are the most sought-after skills, essential for robust data handling and analysis.
- Cloud technologies like AWS and Azure are increasingly prevalent, highlighting a shift towards scalable data solutions.

    <img width="406" alt="2_Project_Analysis_Chart3" src="https://github.com/user-attachments/assets/fef1fd17-3832-4920-9380-f753e71d5759" />


#### 🤔So What

- Staying updated with these critical skills is necessary for career advancement and is crucial for curriculum development in educational programs.

## 4️⃣ What’s the pay of the top 10 skills?

### 📊 Skill: Advanced Charts (Pivot Chart)

#### 📈 PivotChart

- A sophisticated PivotChart was designed to illustrate the correlation between median salary and the prevalence of skills from the data gathered.

### 📊 Analysis

#### 💡Insights

- Skills such as Python, Oracle, and SQL are linked to higher salaries, underscoring their significant value in tech-heavy roles.
- Conversely, more ubiquitous skills like PowerPoint and Word correlate with lower salaries and commonality, suggesting their generalist nature.

    <img width="461" alt="2_Project_Analysis_Chart4" src="https://github.com/user-attachments/assets/61c1a1fd-18bc-4e41-a2c9-00760cec0870" />


### 🤔So What

- The findings advocate for a focus on high-value skills that are directly correlated with enhanced earning potential in technology fields.

## Conclusion

This Excel-driven project sheds light on critical dynamics within the data science job market, illustrating how varied skills influence salary ranges. This analysis should serve as a comprehensive guide for data professionals aiming to elevate their earning potential through strategic skill development.
