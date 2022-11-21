# CWRUBootcamp_M15_11212022_MechaCar_Statistical_Analysis_Hoynacke

# Project Overview 

A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, you’ll help Jeremy and the data analytics team do the following:

Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
Run t-tests to determine if the manufacturing lots are statistically different from the mean population
Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

# Project Requirements 

This new assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:
1. Deliverable 1: Linear Regression to Predict MPG
2. Deliverable 2: Summary Statistics on Suspension Coils
3. Deliverable 3: T-Test on Suspension Coils
4. Deliverable 4: Design a Study Comparing the MechaCar to the Competition

# Deliverable 1: 

## Linear Regression to Predict MPG

The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using your knowledge of R, you’ll design a linear model that predicts the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.csv file. Then, you’ll write a short interpretation of the multiple linear regression results in the README.md.

1. The MechaCar_mpg.csv file is imported and read into a dataframe
2. An RScript is written for a linear regression model to be performed on all six variables 
3. An RScript is written to create the statistical summary of the linear regression model with the intended p-values 

Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = mecha_mpg)

Model: 

<img width="798" alt="Screen Shot 2022-11-21 at 4 12 34 PM" src="https://user-images.githubusercontent.com/111096384/203159254-9e3856c2-b298-44f7-9b18-3fad19c01547.png">

From the above results we can infer that: 
1. vehicle length and ground clearance provide non-random amounts of variance to the model which means both have significant impact on miles per gallon. 
2. Based off the above observation, vehicle weight, spoiler angle, and AWD have p-values that indicate a random amoutn of variance with the dataset 
3. Based off the model there is sifficent evidence to reject our null hypothesis. The p-value ( is smaller than the assumed significance level of 0.05%]
4. This model has an r-squared value of 0.7149 whcih means this model does predict mpg og MechaCar prototypes effectively. 

See the below models which show what happened when we remove the less impactful independent variables 

<img width="638" alt="Screen Shot 2022-11-21 at 4 19 00 PM" src="https://user-images.githubusercontent.com/111096384/203160415-86805bca-9d08-4508-9ade-42f00fc2feda.png">

# Deliverable 2

## Summary Statistics on Suspension Coils

The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. Using your knowledge of R, you’ll create a summary statistics table to show:

The suspension coil’s PSI continuous variable across all manufacturing lots
The following PSI metrics for each lot: mean, median, variance, and standard deviation.

1. The Suspension_Coil.csv file is imported and read into a dataframe 

mecha_coil <- read.csv(file='/Users/alexahoynacke/Desktop/CWRUBootcamp/Module 15 R/Module HW/Suspension_Coil.csv',check.names=F,stringsAsFactors = F)

2. An RScript is written to create a total summary dataframe that has the mean, median, variance, and standard deviation of the PSI for all manufacturing lots 
3. An RScript is written to create a lot summary dataframe that has the mean, median, variance, and standard deviation for each manufacturing lot 

Script shown below: 

<img width="1086" alt="Screen Shot 2022-11-21 at 4 42 34 PM" src="https://user-images.githubusercontent.com/111096384/203163927-09e79421-d1c8-481a-a446-e14e74d8d267.png">

4. There is a summary that addresses the design specification requirement for all the manufacturing lots and each lot individually 

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

The variance of the coils is 62.29 which is within the 100 PSI variance requirement 

Lot 1 = 0.98 
Lot 2 = 7.47 
Lots 3 =  170.29 which offsets the variance at the full lot level 

<img width="829" alt="Screen Shot 2022-11-21 at 4 46 53 PM" src="https://user-images.githubusercontent.com/111096384/203164578-393b7d0f-4cd1-4872-a7a8-34324c7be7b2.png">

# Deliverable 3

Using your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

1. An RScript is written for t-test that compares all manufacturing lots against mean PSI of the population 
2. An RScript is written for three t-tests that compare each manufacturing lot against mean PSI of the population

<img width="399" alt="Screen Shot 2022-11-21 at 4 49 16 PM" src="https://user-images.githubusercontent.com/111096384/203164969-ebd2ff41-8b8f-418b-98e5-4722c5432d50.png">

4. There is a summary of the t-test results across all manufacturing lots and for each lot 

The true mean of the sample is 1498.78. The p-value is 0.0s higher than the common significance level of 0.05. This means there is not enough evidence to reject the null hypothesis. 

Looking at each lot individually: 
1. Lot 1 have the true sample mean of 1500. 
2. Lot 2 has a smaple mean of 1500.02 
both have sample mean that is either similar or the same to the presumed population mean
3. Lot 3 is 1496.14 with a p-value of 0.04. This p value is lower thatn the commong siginifance value of 0.05. Which means if we looked at Lot 3 individually we should reject the null hypothesis. 

If we look at the Lots as a whole we do not see issues but further looking into teh results something want wrong with lot 3. The process should be checked for failures. 

# Deliverable 4 














