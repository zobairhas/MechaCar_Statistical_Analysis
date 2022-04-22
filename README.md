# MechaCar_Statistical_Analysis

## Project Overview
Assist the client by analyzing production data and calling out any issues seen to unblock the team's progress. Specifically, the client has asked for the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings

## Methodology
Tools/Programs/Languages used:

- R
- RStudio




## Linear Regression to Predict MPG
1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
  - vehicle_weight, spoiler_angle, and awd
  
![image](https://user-images.githubusercontent.com/44425379/164791170-4dc83bdb-ef2b-40bf-8a30-90f4a3708ba7.png)  

2. Is the slope of the linear model considered to be zero? Why or why not?
  - The slope of the linear model is not zero because the p-value generated from the linear regression analysis is smaller than 0.05. Therefore, we reject the null hypothesis that mpg of MechaCar prototypes can be predicted effectively by this model. 
  
3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
  - This model is not effective due to the generated R-squared value of 0.71. Although there is significance in that we can reject the null, however, half the data set (including the interept) will not provide random amounts of variance. Vehicle length and ground clearance impact miles per gallon.
  
  
## Summary Statistics on Suspension Coils
1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. 

Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
  - The design specficaitions for the suspenion coils meet this design specfiication for the most part. 
  - Looking at the ```total_summary``` table, we can see that the SD and Variance are within acceptable ranges. However, looking at the ```lot_summary``` table, we can see Lot3 with an unusually high SD and variance.
  - To avoid issues, it might be best to avoid coils from Lot3 or do an extra test to ensure quality.

<b>Total Summary:</b>
![image](https://user-images.githubusercontent.com/44425379/164791925-0e0d0270-3da3-4eae-9040-a32b28842650.png)

<b>Lot Summary:</b>
![image](https://user-images.githubusercontent.com/44425379/164791907-49a74bd9-c7f7-42a2-b2ef-aa49da892abf.png)

## T-Tests on Suspension Coils
- It would appear that Lot 1 (p-value = 0.057) is the only lot that is manufacturing products to the correct specifications as the p-value is higher than 0.05. 
- Lots 2 and 3 had p-values less than 0.05 (see SS) so we can conclude that the means are statistically different. 

<b>t-Test for Lot 1:</b>
![image](https://user-images.githubusercontent.com/44425379/164791367-46cbefec-cfc0-49b4-b0e6-6ebce809b368.png)

<b>t-Test for Lot 2:</b>
![image](https://user-images.githubusercontent.com/44425379/164791388-8b34bfd6-43c2-4a2b-b500-7eb703b0dc87.png)

<b>t-Test for Lot 3:</b>
![image](https://user-images.githubusercontent.com/44425379/164791402-fd205031-79c5-49cd-ae02-e23476b4aec5.png)

## Study Design: MechaCar vs Competition
- I think it would be interesting to test specifically if vehicle weight, spoiler angle, and all wheel drive impacts MPG across the competition. 
- If we could get our hands on that data, an ANOVA test could be used to compare multiple brands and determine what the ideal weight or spoiler angle is to produce the most optimal MPG. 
- I would assume that a lighter vehicle will always have better MPG. 
