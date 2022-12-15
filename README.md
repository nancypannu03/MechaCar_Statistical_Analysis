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


      
1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

## Part 3: T-Test on Suspension Coils
create a subheading ## T-Tests on Suspension Coils, then briefly summarize your interpretation and findings for the t-test results. Include screenshots of the t-test to support your summary.

## Part 4: Design a Study Comparing the MechaCar to the Competition
1. A metric to be tested is mentioned 
2. A null hypothesis or an alternative hypothesis is described 
3. A statistical test is described to test the hypothesis 
4. The data for the statistical test is described 
