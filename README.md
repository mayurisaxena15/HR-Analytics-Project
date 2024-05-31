# HR-Analytics-Internship-Project
This project involves performing data visualization on an HR dataset using Power BI. The aim is to gain insights into various aspects such as demographics, turnover, and employee wellness. The process includes loading and transforming data, identifying and handling null values, and creating comprehensive dashboards.
## Steps Followed:
* Data Loading and Transformation
  - Download Dataset: The dataset was downloaded from the source.
  - Upload Data: The data was uploaded into Power BI using the "Get Data" option.
  - Data Transformation: Utilized the "Transform" option in Power BI to inspect and handle null values in the dataset.
### Dashboard Overview: 
The project consists of five pages, each providing distinct insights:
* First Page: Overview
  - Provides an overview of the four detailed dashboards created in the subsequent pages: Demographics, Turnover analysis 1, Turnover analysis 2, employee Wellness.
* Second Page: Demographic Insights
  - Focuses on the demographic characteristics of the employees.
  - Visualizations created:
    - Card visual of total employees. Then we created a new column "attrition Count" which was calculated as follows:
      ``` dax
      Attrition count = IF('HR-Employee-Attrition'[Attrition]="Yes",1,0)
      ```
      This will yield the desired results: if "Attrition" is "Yes," the count is 1; if it's "No," the count is 0.
    - Sum of attrition count was calculated And subtracting this from the employee count yields the count of active employees that is 1233.
      ``` dax
      Active Employees = SUM('HR-Employee-Attrition'[EmployeeCount])-SUM('HR-Employee-Attrition'[Attrition count])
      ```
    - Data groups were created to make better visuals. Then visualizations of total attrition by work life balance, by age and by distance from home was created.
* Third page: Turnover Analysis 1
  - Investigates the factors contributing to employee turnover.
* Fourth Page: Turnover Analysis 2
  - Further analysis of turnover, building upon the insights from the third page.
* Fifth Page: Employee Wellness
  - Dedicated to understanding the wellness and satisfaction levels of employees. In this dashboard, grouping played a crucial role in organizing and presenting the data effectively. The 
    design of the dashboard is tailored to utilize the power of grouping for enhanced data visualization and analysis. For example Performance rating is grouped as low and high and 
    relationship satisfaction is grouped as dissatisfied, very dissatisfied, satisfied,very satisfied.
#### Conclusion
This project successfully leveraged Power BI to visualize and analyze an HR dataset, providing valuable insights into various aspects of employee demographics, turnover, and wellness. The created dashboards can help HR professionals and decision-makers understand and address key areas affecting employee satisfaction and retention.
