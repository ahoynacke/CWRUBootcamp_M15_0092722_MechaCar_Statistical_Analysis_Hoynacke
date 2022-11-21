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









