# PALMORIA-GROUP-HR-ANALYSIS
A comprehensive project analysis of Palmoria employee data using Power BI. This analysis provides insights into gender distribution, the salary structure, performance ratings and bonus allocation across various department and regions which will enable the management team to identify key areas of adjustment and make a wise decision.

## Project Objectives
- Analyse gender distribution
- Performance rating based on gender
- Analyse company's salary structure
- Identify the resence of gender gap pay
- To check if Palmoria comply with the minimun salary regulation

  ## Tools & Techniques used
  - Power BI Desktop
  - Data Cleaning & Transformation to remove null values
  - Dax Measures (for averaage salary, average rating, gender pay gap)
  - Calculated Columns(salary band, total salary paid, ...)
  - Interactive Visualizations (Cards, Charts, Slicers)

     ## Key Performance Indicators
    1. Gender distribution
       - Visualized the gender distribution by region
       - Visualized the overall gender distribution using a pie pie chart
    2. Rating by gender
       - Visualized the rating distribution by gender and ratying comparison by gender across all regions
       - A measure was calculated to obtain nthe average rating by gender
    3. Salary Structure and Gender Pay Gap
       - A card was used to show the average salary
       - Charts were used to visualise the average nsalary by department, regions and gender
       - Measures was created to calaculate the gender pay gap
    4. Minimum salary Requirement
       - A column chart is used to show the salary band increment
       - A dax measure to calculate the employees receiving below the minimum salary ($90,000)
       - Card is used to show the counts of employees receiving below the minimum salary
    5. Bonus Payment & Total Salary
       - Visualised Bar the ntotal bonus payout by Regions
       - Created a table to show individual employee bonus amount and the top 5 employee wuith the highest pay
      
      ## Visualizations
    1. A dashboard showing difeferent KPIs     
     ![Palmoria Dashboard 1](https://github.com/user-attachments/assets/de6afd2d-0e3b-4b5a-89f1-bc249185473b)

    2. Performance Rating in the Organisation
     ![Palmororia Dashboard 2](https://github.com/user-attachments/assets/acd21a20-410b-4617-9fa7-9694313ca725)

    3 Cards showing important details such as gender count, average salary , gender pay gap
     ![Cards](https://github.com/user-attachments/assets/6c3ca78b-82fb-4964-92c9-d5e1864bea52)

   4  A Bar Chart Showing Rating Distribution by gender

     ![Bar Chart - Rating distribution](https://github.com/user-attachments/assets/b109ee40-affc-4e6e-b6e2-24f9cae36bf2)

     ## DAX Measures
        To achieve a better analysis of the data, several dax measures were created. Below are a few key examples used to calculate metrices.
       a. Average Salary
         - Average Salary = AVERAGE ('palmoria Employee[Salary])

        b. Gender Pay Gap (%)
          - Gender Pay Gap (%) = VAR MaleAvg = CALCULATE(AVERAGE('Palmoria Employee'[Salary]),'Palmoria Employee'[Gender] = "Male") VAR FemaleAvg = CALCULATE(AVERAGE('Palmoria Employee'[Salary]), 'Palmoria Employee'[Gender] = "Female") RETURN DIVIDE(MaleAvg - FemaleAvg, MaleAvg)

      c. Total Bonus Payout
        - Total Bonus Payout = SUM('Palmoria Employee'[Annual Bonus Amount])

   ## Recommendations
            - Salariew review
            - Update of company's Policy
            - Unbiasedness in terms of gender in the company 
    

    
