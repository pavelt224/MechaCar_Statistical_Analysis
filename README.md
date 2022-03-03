# MechaCar_Statistical_Analysis
Manufacturing Datasets: Designed Hypothesis Testing with R.

## Challenge Overview

A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

1. Deliverable 1: Linear Regression to Predict MPG
    Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes

    Mecha Car Linear Model Summary![D1 Linear Regression to Predict MPG](https://user-images.githubusercontent.com/93852380/156665732-039331f5-8a59-4412-a4a6-00c4b8325556.png)

    Summary of Findings
Data scientists can estimate future observations and measurements of a continuous, dependent variable of interest based on various independent factors using the above exercise of developing a predictive, multiple linear regression modeling tool. We can deduce the following from the overall results of our analysis:

    * Because their p-values are substantially smaller than our significance level of 0.05 percent, the vehicle length, ground clearnace, and y intercept coefficent are statistically likely to add a non-random amount of variance to the mpg values in the dataset. Furthermore, if the intercept has a significant predictive impact, there may be other variables of interest that are not included in the model that can better explain mpg variability, or we may need to transform the current regression model (i.e. remove variables with little to no predictive power) to improve the model (vehicle weight, spoiler angle, and AWD (All Wheel Drive)).

    * The null hypothesis of our regression analysis test, that the linear model's slope is not zero, can be rejected. This view is based on the fact that the Mecha Car's mpg is significantly predicted by at least two known independent variables. To back this up, our regression model's p-value is 5.35 x 10-11, which is substantially lower than the stated significance level of 0.05 percent, showing that there is enough evidence to reject the null hypothesis.

    * The linear model has an r-squared value of 0.7149, which suggests that it will correctly predict 71.5 percent of all mpg predictions. As a result, we can confirm that the Mecha Car prototypes' mpg can be accurately predicted using multiple linear regression. To further evaluate the efficiency of our model, we may make more changes to our analysis by deleting variables with little to no predictability of variance, which would be determined by the updated r-squared value.

2. Deliverable 2: Create Visualizations for the Trip
    Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots

3. Deliverable 3: T-Tests on Suspension Coils (20 points)
    Run t-tests to determine if the manufacturing lots are statistically different from the mean population

4. Deliverable 4: Design a Study Comparing the MechaCar to the Competition
    Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each 
    statistical analysis, you’ll write a summary interpretation of the findings.
