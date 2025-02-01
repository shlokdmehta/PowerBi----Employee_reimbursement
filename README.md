# Employee Reimbursement Analysis with Power BI

This project demonstrates the use of Power BI for analyzing employee reimbursement data. It covers data cleaning, transformation, and visualization techniques to extract meaningful insights.

## Project Objective

This project was a practice exercise to gain hands-on experience with Power BI. The goal was to analyze employee reimbursement data, create visualizations, and derive insights.

## Dataset

The dataset used for this analysis is `Employee_reimbursement_dataset.xlsx` - https://github.com/shlokdmehta/PowerBi----Employee_reimbursement/blob/main/Employee_reimbursement_dataset.xlsx.

## Task Breakdown

The following tasks were performed in this project:

**Data Cleaning and Transformation (Power Query)**

* Corrected spelling and punctuation errors in the `Expense Type` column.
* Standardized `Project` names for consistency.
* Created a new `Currency` column to fill missing values based on the `Amount` column using the following formula:
    ```
    (if [Currency] = null and [Amount] >= 1000 then "INR" else if [Currency] = null and [Amount] < 1000 then "USD" else [Currency] )
    ```
* Converted the `Amount` column to INR based on the `Currency` column, using appropriate exchange rates for USD and Euro.

**DAX Measures**

* Created a measure to calculate the sum of reimbursed amount in INR.
* Used the `CALCULATE` function to determine the total reimbursed amount for Project_B.
* Created a measure to count the number of declined requests.

**Visualizations**

* Created slicer visuals for `Project` and `Employee`.
* Created a bar chart visualizing employee-wise reimbursement amounts.
* Created a pie chart showing the distribution of reimbursement amounts by project.

## Insights

* Project A had highest Reimbursement amount - 55% of total reimbursements
* Through all 3 projects Silva claimed highest reimbursement amount - 133K INR
* Throgh all 3 projects Dhoni claimed the lowest amount of reimbursement - 13% of total reimbursement amount - roughly 62% less than Silva

## Files

* `(Employee_reimbursement_dataset.xlsx)`: The original dataset. - https://github.com/shlokdmehta/PowerBi----Employee_reimbursement/blob/main/Employee_reimbursement_dataset.xlsx
* `(Employee_reimbursement_dataset_powerBi.pbix)`: The Power BI file containing the data transformations, measures, and visualizations. - https://github.com/shlokdmehta/PowerBi----Employee_reimbursement/blob/main/Employee_reimbursement_dataset_powerBi.pbix

## Tools Used

* Microsoft Power BI Desktop

## Skills Demonstrated

* Data cleaning and transformation using Power Query
* DAX measure creation
* Data visualization
* Data analysis and interpretation

## Next Steps

* Continue with current data set, exhaust all possible analysis
* move onto new data sets and perform analysis while learning PowerBi
