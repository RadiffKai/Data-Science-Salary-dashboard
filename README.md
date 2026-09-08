
# Data-Science-Salary-dashboard
Analysis of raw data science work sheet ,for purpose of visualizing top paying data science jobs based on their country and schedule type  

<img width="948" height="410" alt="Screenshot 2026-09-07 093738" src="https://github.com/user-attachments/assets/fd682cd5-07f3-4e84-b187-5ca5e151b354" />

## Introduction
This project aim to help youth seeking to enter in different data jobs ,in identifying not only the various feilds they can pursue but also their salary and schedule type.  
The dataset is from   [data_jobs_salary_monthly.xlsx](data_jobs_salary_monthly.xlsx)  
The salary dashboard is in [Salary_dashboard.xlsx](Salary_dashboard.xlsx)


### Charts  
 Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.Horizontal bar chart for visual comparison of median salaries. Sorted values from the largest to the smallest ,making it easier to see engineers and senior roles are the most paying  
<img width="336" height="275" alt="Screenshot 2026-09-08 181356" src="https://github.com/user-attachments/assets/8dea3262-9edd-46df-bbde-2fdb15c31000" />  
Utilized Excel's map chart feature to plot median salaries globally. Used the color-coded map to visualize disparity in median salaries in different countries  
<img width="302" height="260" alt="Screenshot 2026-09-08 181412" src="https://github.com/user-attachments/assets/322bc222-fafe-40a3-9d13-da3c3151da88" />  
Data science salary varying with different schedule types ,fulltime are most compensated compared to other schedule type  

<img width="241" height="281" alt="Screenshot 2026-09-08 181437" src="https://github.com/user-attachments/assets/d9813842-42ec-4b47-835c-a0b0f3ebd0cc" />  

Data validation allows users to only input specified values ,could for instance be in a list ,this allowsonly permitted values to be placed and increased usability of the dashboard  
Various formulas used included 
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
This formula checks for median salary if based on the current values on the data validation cells.  
Other functions such as filter(), sort() were used for better analysis and visualisation.  
Other small KPI card indicate median salary for the selected value,the top job platform with the most listing and the job markert count.


