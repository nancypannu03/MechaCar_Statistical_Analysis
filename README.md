# MechaCar_Statistical_Analysis

## Part 1: Linear Regression to Predict MPG

        #Part 2: Create Visualizations for the Trip Analysis
        #2. Import and read in the Suspension_Coil.csv file as a table
        Suspension_Coil <- read.csv(file='Suspension_Coil.csv',check.names=F,stringsAsFactors = F) 

![Test Image](/Resources/linear_regression.png)

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
- According to the results, vehicle length, ground clearence and intercept provided a non- random amount of variance to the mpg values in the dataset.

2. Is the slope of the linear model considered to be zero? Why or why not?
- The slope of the linear model is not considered to be zero as p-values is much smaller than the significance level of 0.05.
3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
- As R-squared value is 0.7149, therefore the linear model predicts 71% of all the mpg predictions of MechaCar prototypes.

## Part 2: Summary Statistics on Suspension Coils
      #3. Write an RScript that creates a total_summary dataframe
      total_summary <- Suspension_Coil %>% summarize(Mean=mean(PSI), Median=median(PSI), Variance=var(PSI), SD=sd(PSI), .groups = 'keep')
      
![Test Image](/Resources/total_summary.png)

      #4.Write an RScript that creates a lot_summary dataframe 
       lot_summary <- Suspension_Coil %>% group_by(Manufacturing_Lot) %>% summarize(Mean=mean(PSI), Median=median(PSI), Variance=var(PSI), SD=sd(PSI), .groups =            'keep')
       
![Test Image](/Resources/lot_summary.png)

    
1. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.

- The data collected specifies that , variance of total_Summary is 62.29 which is less than 100 pounds. Therefore, it meets the design specification.

- for lot 1 and lot 2 variance is 0.9795 and 7.469 respectively, which is less tahn 100 pounds , which further meets the criteria of design specifications. Whereas for lot3, the variance is 170.28 which is way more than 100 pounds and lot3 fails to meet the design criteria.

## Part 3: T-Test on Suspension Coils

![Test Image](/Resources/Suspension_Coil_test.png)



![Test Image](/Resources/lot1_test.png)


![Test Image](/Resources/lot2_test.png)


![Test Image](/Resources/lot3_test.png)



![Test Image](/Resources/lot3_table.png)


### Briefly summarize your interpretation and findings for the t-test results. 

   - We willdetermine PSI across all the manufacturing lots and on the suspension coil using t.test() function.
   
   - In your MechaCarChallenge.RScript, write an RScript using the t.test() function to determine if the PSI across all manufacturing lots is statistically              different from the population mean of 1,500 pounds per square inch.
   
   - Next, write three more RScripts in your MechaCarChallenge.RScript using the t.test() function and its subset() argument to determine if the PSI for each            manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.
   
   - An RScript is written for three t-tests that compare each manufacturing lot against mean PSI of the population.
   

## Part 4: Design a Study Comparing the MechaCar to the Competition

1. A metric to be tested is mentioned 

   - MPG (fuel efficiency)

2. A null hypothesis or an alternative hypothesis is described 

   - Null hypothesis: MechaCars perform efficiently as compared to other manufacturers vehicles.

   - Alternate hypothesis: MechaCars doesnot perform efficiently as compared to the other manufacturers vehicles.

3. A statistical test is described to test the hypothesis 

   - ANOVA testing can determine the differences in order to test the hypotheseis.

