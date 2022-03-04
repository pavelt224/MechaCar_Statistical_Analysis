# MechaCar_Statistical_Analysis
Manufacturing Datasets: Designed Hypothesis Testing with R.

## Challenge Overview

A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

# 1. Deliverable 1: Linear Regression to Predict MPG
    Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes

 Mecha Car Linear Model Summary

![D1 Linear Regression to Predict MPG](https://user-images.githubusercontent.com/93852380/156688199-f792aefc-9acf-47d3-9318-24d1df0927bc.png)

    Summary of Findings
Data scientists can estimate future observations and measurements of a continuous, dependent variable of interest based on various independent factors using the above exercise of developing a predictive, multiple linear regression modeling tool. We can deduce the following from the overall results of our analysis:

    * Because their p-values are substantially smaller than our significance level of 0.05 percent, the vehicle length, ground clearnace, and y intercept coefficent are statistically likely to add a non-random amount of variance to the mpg values in the dataset. Furthermore, if the intercept has a significant predictive impact, there may be other variables of interest that are not included in the model that can better explain mpg variability, or we may need to transform the current regression model (i.e. remove variables with little to no predictive power) to improve the model (vehicle weight, spoiler angle, and AWD (All Wheel Drive)).

    * The null hypothesis of our regression analysis test, that the linear model's slope is not zero, can be rejected. This view is based on the fact that the Mecha Car's mpg is significantly predicted by at least two known independent variables. To back this up, our regression model's p-value is 5.35 x 10-11, which is substantially lower than the stated significance level of 0.05 percent, showing that there is enough evidence to reject the null hypothesis.

    * The linear model has an r-squared value of 0.7149, which suggests that it will correctly predict 71.5 percent of all mpg predictions. As a result, we can confirm that the Mecha Car prototypes' mpg can be accurately predicted using multiple linear regression. To further evaluate the efficiency of our model, we may make more changes to our analysis by deleting variables with little to no predictability of variance, which would be determined by the updated r-squared value.

# 2. Deliverable 2: Create Visualizations for the Trip
    Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots

## Output of Results

Total Summary:

![Total Summary Statistics](https://user-images.githubusercontent.com/93852380/156678180-be769801-7776-4f43-a06b-977271600f1d.png)


Lot Summary:

![Lot Summary ](https://user-images.githubusercontent.com/93852380/156678230-b27ec6bc-e661-46f4-843e-e3a3f2762b3d.png)


## Summary of Results:

The variation of the MechaCar suspension coils must not exceed 100 pounds per square inch, according to the design parameters (PSI). We can draw the following conclusions based on the technical study above, which summarizes the findings of testing the weight capabilities of various suspension coils from multiple production lots:

* The suspension coil PSI variance of the sample population of manufacturing lots is 62.3, which is comfortable within the range of the 100 PSI variance requirement.

* Individual lots 1 and 2 both pass the required suspension coil variance of 100 PSI with even tighter variability and are statistically more consistent than the whole sample population (within 1 PSI and 7.5 PSI, respectively)

* However, with a variance of 170.30, lot 3 fails to meet the suspension coil PSI variance threshold. We can deduce that lot 3 is skewing the total manufacturer's variance to the right in an unproportional way. Because the SD from the mean is 13 pounds per square inch, we can anticipate that some data points from lot 3 will be considered outliers.


# 3. Deliverable 3: T-Tests on Suspension Coils 
    Run t-tests to determine if the manufacturing lots are statistically different from the mean population
  
  
  All Manufacturing Lots
  
![All Manufacturing Lots](https://user-images.githubusercontent.com/93852380/156683603-826d51aa-0709-4a2e-8f96-06b7afe11dc2.png)



  T.test by lots

![T test by lots](https://user-images.githubusercontent.com/93852380/156683786-14ab3207-1a6b-4608-997b-133ff2d3ca04.png)

## Summary
The null hypothesis, which asserts that the true mean of the sample population's PSI is statistically similar to that of the overall population's PSI (mu=1500), is tested using the above t-tests.

* The true mean of the sample is 1498.78 with a p-value of 0.06 according to the first t-test, which summarizes data across all manufacturing lots. We might conclude that there is insufficient evidence to reject the null hypothesis because this is larger than the anticipated significance level of 0.05. To put it another way, the average PSI of all three manufacturing lots is statistically similar to the population mean of 1500.

* Lot1 has a p-value of 1, which is substantially higher than the 0.05 significance limit we assumed. That indicates there is a 100 percent chance that another sample prototype will produce the same PSI measurement as lot 1. There is also a 0% chance that another sample population from lot 1 will be statistically different from the population mean.

* Lot 2 has a p-value of 0.61, which is similar to the initial t-test done on all manufacturing lots. As a result, there isn't enough evidence to rule out the null hypothesis, and the sample mean is statistically comparable to the population mean of 1500.

* The t-test results for Lot 3 differ from those of Lots 1 and 2, but this is not surprising given our assessment of the suspension coil's PSI summary data. The p-value generated is 0.04, which is less than the 0.05 significance limit we assumed. As a result, we can conclude that there is sufficient evidence to reject our null hypothesis, and that the sample population mean PSI is not statistically similar to the population mean.

The production division will benefit from this information: The suspension coils on Lot 3's Mecha Car prototypes do not meet quality assurance requirements, and the manufacturing process for these automobiles needs to be rigorously examined moving forward.


# 4. Deliverable 4: Design a Study Comparing the MechaCar to the Competition
    Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each 
    statistical analysis, you’ll write a summary interpretation of the findings.
    
When comparing the Mecha Car to its competitors, a consumer would be interested in learning about the car's maintenance costs before making a purchase choice. As a result, we may do a statistical analysis to determine how the Mecha Car's repair/maintenance cost, which is a KPI performance indicator, compares to the competitors. If we can show that the Mecha Car's repair costs are cheaper than those of its competitors, we can use that knowledge when marketing the car, which will help boost sales once it hits the market.

Questions to consider: When considering how to test for maintenance cost as a continuous variable, it's necessary to evaluate whether a complementary variable should be included to express the true worth of lower repair costs as a "performance metric." Cost should be connected with miles driven as a continuous variable, and miles driven can be used to quantify "vehicle utilization lifespan." In principle, as a car is driven more, it should require only minor repairs.

Question: Is there a statistical difference in the MechaCar's maintenance cost compared to its competitors based on mileage intervals?

A two-way ANOVA test would be used as the testing method.

1- Miles Driven, but as categorical datatypes, divided into buckets that indicate various ranges of miles driven based on the car's lifecycle (i.e Intervals of 10k miles).

2- Car Manufacturer is the second independent variable (categorical)

3- Maintenance Cost is a dependent variable.


Data Needed:

1- A great number of cars were tested, including the Mecha Car and its rivals.

2- Miles Driven Summary Statistics to Divide into Quartiles for Categorical Use

3- Car Maintenance Costs Over Time



H0: Over the lifecycle of a car (measured in ranges of miles driven), the average maintenance expenses of each automobile manufacturer are equal.

At least one of the means differs from the others (the cost of a Mecha automobile is lower).


The results of Technical Analysis would be generated using R's aov() and summary() functions. This would need first going into the summary statistics of each car's Miles Driven in order to appropriately arrange the bucket ranges by quartile, essentially creating a new summary dataframe from which the aov() test could be performed.










RStudio

![RStudio](https://user-images.githubusercontent.com/93852380/156686857-5612eb5e-5006-4d67-94e1-f2818cb1f11d.png)













