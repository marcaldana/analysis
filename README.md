# BellaBeats Google's Data Analytics Capstone Course 

Hi, My name is Marc Aldana. I have a Bachelor of Science from SUNY Old Westbury in Management Information Systems. This is my case study on wearable technology. I'm going to go into each step of the data analysis process. I will provide some visualizations. I will be using R-studio to analyze datasets. 
I'm going to show how I cleaned data using R. I will show the before and after.



![BellaBeats Google's Data Analytics Capstone Course](https://bellabeat.com/wp-content/uploads/2023/09/Bellabeat-logo.jpg)
BellaBeats Google's Data Analytics Capstone Course 

  Who's BellaBeat and what do they do? 
    
   Bellabeat: 
   Empowering Women's Wellness Through Data-Driven Insights
   
Company Background:

Founded in 2013 by Urška Sršen and Sando Mur, Bellabeat is a trailblazing wellness technology company specializing in health-focused smart products for women. 

Bellabeat's success lies in its ability to collect and analyze data on activity, sleep, stress, and reproductive health.  This data empowers women with valuable insights into their health and habits, fostering a deeper understanding of their well-being.
-----------------------------------------------------------------------------------------------------------------------------------------------------------
![Image Description](https://leapsummit.com/wp-content/uploads/2021/03/urska-srsen-leap.jpg)

Urška Sršen, an artist by background, brings a unique design sensibility to the tech world, creating aesthetically pleasing devices that inform and inspire.
-----------------------------------------------------------------------------------------------------------------------------------------------------------
![Sando Mur](https://www.talkymedia.it/wp-content/uploads/2023/07/Schermata-2023-07-02-alle-16.39.05.png)

Sandro Mur is a serial entrepreneur and the co-founder and CEO of Bellabeat, a wellness company focused on women's health. He has a background in mathematics, statistics, and engineering.
-----------------------------------------------------------------------------------------------------------------------------------------------------------

Business Task:

Analyze user behavior and health data from both Bellabeat and competitor wearable devices to identify opportunities for improving Bellabeat's product features, user engagement, and overall market competitiveness.

#Key Focus Areas:

Feature Enhancement:
Identify most used and valued features: Determine which features (e.g., activity tracking, sleep analysis, stress monitoring) are most frequently used and highly rated by users across different brands. This can guide Bellabeat in prioritizing feature development and improvements.
Uncover unmet needs: Analyze user feedback and reviews to identify gaps in existing features and potential areas for innovation. This could lead to the development of unique features that address unmet needs in the market.
User Engagement:
Usage patterns: Analyze how users interact with different features and how their usage changes over time. This can help Bellabeat optimize the user experience and design features that encourage long-term engagement.
Churn analysis: Identify factors that contribute to user churn (stopping using the device) and develop strategies to improve customer retention.
Market Competitiveness:
Benchmarking: Compare Bellabeat's performance to competitors in terms of user satisfaction, feature adoption, and overall market share. This can highlight areas where Bellabeat excels or needs to improve.
Competitive advantage: Identify Bellabeat's unique strengths and areas where they can differentiate themselves from competitors. This could involve focusing on specific demographics, health conditions, or lifestyle factors.
Data Sources:

Bellabeat Internal Data: Utilize user data collected from Bellabeat devices and apps, including activity, sleep, stress, and reproductive health data.
Public Datasets: Explore publicly available datasets from other wearable device companies (if available), ensuring compliance with privacy regulations.
Customer Surveys and Feedback: Gather data from surveys, reviews, and social media to understand user preferences, pain points, and suggestions for improvement.
By addressing this business task through data analysis, Bellabeat can gain valuable insights into user behavior, identify areas for improvement, and develop targeted strategies to enhance its products, increase user engagement, and stay ahead in the competitive wearable technology market.



-----------------------------------------------------------------------------------------------------------------------------------------------------------

# Ask Phase

Sršen asks you to analyze smart device usage data to gain insight into how consumers use non-Bellabeat smart
devices. She then wants you to select one Bellabeat product to apply these insights to in your presentation. 
These questions will guide your analysis:

# What are some trends in smart device usage?

+ Advanced Health Monitoring:

 Wearables incorporate medical-grade sensors to monitor conditions like ECG, blood pressure, blood glucose, and even mental health indicators like stress and anxiety.
  
+ Personalized Insights:
  
  Artificial intelligence is being leveraged to provide users with personalized recommendations based on their individual health data, activity levels, and goals.
  
+ Enhanced User Experience:
  
  Wearables are evolving to offer larger displays, extended battery life, fashionable designs, and seamless integration with other smart devices and platforms.
  
+ Connectivity and Integration:
  
  Devices are increasingly offering cellular connectivity, smart home integration, and data-sharing capabilities with healthcare providers.
  
+ Accessibility and Inclusivity:
  
  Wearable technology is becoming more affordable and specialized, catering to the diverse needs of users across different demographics and health conditions

  
 # How could these trends apply to Bellabeat customers?

+ Advanced Health Monitoring:
  
  Appeal to Health-Conscious Women: Bellabeat's target audience is health-conscious women. By incorporating advanced health monitoring features like ECG, blood pressure, and SpO2 monitoring.
  Bellabeat can cater to the growing demand for comprehensive health tracking among its customer base.
  Focus on Women's Health: Bellabeat can further differentiate itself by focusing on women-specific health features like menstrual cycle tracking, fertility monitoring, and hormonal health insights. This aligns with their brand identity and resonates with their core audience. 

+ Competitive Advantage:

Integrating continuous glucose monitoring (CGM) could give Bellabeat a significant edge in the market, especially for women with diabetes or those looking to manage their metabolic health.
Personalized Fitness and Coaching:
Tailored Recommendations: Bellabeat can leverage AI-powered algorithms to analyze user data and offer personalized workout plans, nutrition advice, and stress management techniques, catering to individual goals and preferences.

+ Enhanced Engagement:
  Gamification features like challenges, rewards, and social sharing can create a more engaging experience for users, increasing long-term adherence to health and fitness goals.
+ Community Building:
  Bellabeat could foster a sense of community by allowing users to connect, share their progress, and offer support, making the app a valuable resource beyond just tracking data.
  
+ Enhanced User Experience:

  Stylish Designs: Bellabeat is known for its aesthetically pleasing designs. They can further enhance the user experience by offering a wider range of fashionable options and customization features for their wearables.

+ Improved Battery Life:
  Extended battery life is a crucial factor for wearable users. Bellabeat can focus on improving battery efficiency to ensure continuous tracking and reduce charging frequency.
+ Intuitive Interface:
  By streamlining the user interface of their app and devices, Bellabeat can make it easier for users to access and interpret their health data, leading to better engagement and adherence.
+ Connectivity and Integration:
 Cellular Connectivity: Offering cellular connectivity in their smartwatches would allow users to stay connected without their phones, adding convenience and increasing the appeal of their devices.
  Seamless Integration:
  Bellabeat can expand its app's capabilities by integrating with other popular health and fitness apps, enabling users to consolidate their data and track their progress across different platforms.
  
+ Affordable Options:
  Expanding their product line to include more affordable wearables would make Bellabeat accessible to a wider audience, particularly younger or budget-conscious consumers.
  Specialized Features: Developing features tailored to specific user segments (e.g., postpartum women, and menopausal women) would further solidify Bellabeat's position as a brand that understands and caters to women's unique health needs.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

## Case Study Roadmap - Prepare

Guiding Questions:

# Where is your data stored?
Both datasets are stored on Kaggle:
Fitbit Fitness Tracker Data: https://www.kaggle.com/datasets/arashnic/fitbit
Calories Burned During Exercise and Activities: https://www.kaggle.com/datasets/aadhavvignesh/calories-burned-during-exercise-and-activities
# How is the data organized? Is it in a long or wide format?
Fitbit Fitness Tracker Data:
Multiple CSV files in wide format (each row is a user, and columns represent dates or metrics).
Some files (like heartrate_seconds_merged) are in long format (each row is a timestamp for a user).
Calories Burned During Exercise and Activities:
Single CSV file in wide format (each row is an activity, columns represent METs and calories burned).
Are there issues with bias or credibility in this data? Does your data ROCCC?
+ Bias:
Fitbit Data: Self-selection bias (users opted to share data), potential over-representation of health-conscious individuals, and limited to Fitbit users.
Calories Burned Data: Potential inaccuracies in calorie estimates, as individual factors (age, weight, etc.) are not considered.
# ROCCC:
+ Reliable: Both datasets come from Kaggle, a reputable source. However, the Fitbit data was collected via Amazon Mechanical Turk, which might raise questions about participant motivation and data quality.
+ Original: Both datasets are likely secondary data, compiled from other sources.
+ Comprehensive: Fitbit data is relatively comprehensive in terms of activity and health metrics but lacks demographic info. The "Calories Burned" data covers many activities but lacks user-specific context.
+ Current: The Fitbit data is from 2016, which might not reflect current trends. The "Calories Burned" dataset has no date, raising questions about its currency.
+ Cited: The sources of the original data are not cited in either dataset.
  -----------------------------------------------------------------------------------------------------------------------------------------------------------
 # How are you addressing licensing, privacy, security, and accessibility?
+ Licensing: Both datasets are under CC0: Public Domain licenses, allowing for unrestricted use.
+ Privacy: Fitbit data is anonymized, protecting user identities. The "Calories Burned" dataset does not contain personal information.
+ Security: Since both datasets are public, security concerns are minimal.
+ Accessibility: Both datasets are readily available on Kaggle.
  # How did you verify the data’s integrity?
+ Initial Data Checks: Both datasets will undergo the following:
+ Handling missing values: Identify and decide on the appropriate method (e.g., removal, imputation).
+ Checking for outliers: Examine extreme values and assess if they are errors or genuine data points.
+ Correcting inconsistencies: Ensure data types are consistent (e.g., dates, numeric values) and values are within expected ranges.
+ How does it help you answer your question?
+ Fitbit Data: Provides real-world insights into how users interact with wearable devices, their activity patterns, and health metrics, which can inform Bellabeat's product development and marketing strategies.
+ Calories Burned Data: Offers a reference point for understanding the relationship between different activities and calorie expenditure, helping Bellabeat refine its calorie tracking algorithms and personalize recommendations.
+ Are there any problems with the data?
Yes, both datasets have limitations (see point 3). These limitations will be addressed by:
Acknowledging biases and potential inaccuracies in the analysis.
Supplementing with additional research or data (if possible) to gain a more comprehensive understanding.
Focusing on patterns and trends rather than absolute values, given the potential limitations of the datasets.
Guiding Questions
-----------------------------------------------------------------------------------------------------------------------------------------------------------
## Case Study Roadmap - Process
 
What tools are you choosing and why?
RStudio: We'll primarily use RStudio for this analysis due to its strengths in data manipulation, statistical analysis, and visualization.
Libraries: We'll leverage the following R libraries:
dplyr: For data wrangling (filtering, selecting, mutating, summarizing)
tidyr: For tidying data (pivoting between long and wide formats)
ggplot2: For creating informative and aesthetically pleasing visualizations
lubridate: For working with date and time data
Have you ensured your data’s integrity?
Initial Data Checks: Before diving into analysis, we've taken the following steps:
Missing values: Identified and handled missing values in both datasets. Since the "Calories Burned" dataset has no missing values, we focus on the Fitbit dataset. Depending on the extent, we can either remove rows with missing data or impute missing values with appropriate methods.
Duplicates: Checked and removed any duplicate entries in the Fitbit dataset to avoid inflating numbers.
Data types: Confirmed that columns have the correct data types. For example, ActivityDate in the Fitbit dataset will be converted to a date format.
Outliers: Examined for extreme values in the Fitbit dataset. Outliers in calorie data or activity levels might be investigated further as they could indicate data entry errors or exceptional scenarios.
What steps have you taken to ensure that your data is clean?
Data Cleaning Steps:
Fitbit Data:
Handle missing values (remove or impute).
Remove duplicate entries.
Convert ActivityDate to date format.
Merge relevant tables (e.g., dailyActivity_merged, minuteCalories_merged) using common identifiers (e.g., Id, ActivityDate).
Create calculated fields:
Calculate total active minutes by summing VeryActiveMinutes, FairlyActiveMinutes, and LightlyActiveMinutes.
Calculate the total distance from different sources (e.g., TrackerDistance, LoggedActivitiesDistance, etc.).
Calories Burned Data:
Calculate calories per minute for each activity to facilitate comparison with the Fitbit data.

library(dplyr)
library(tidyr)
library(lubridate)

# 1. Handle Missing Values:

# Check for missing values in each table 
colSums(is.na(dailyActivity_merged))
colSums(is.na(minuteCaloriesNarrow_merged))
colSums(is.na(hourlyIntensities_merged))
colSums(is.na(hourlyCalories_merged))
-----------------------------------------------------------------------------------------------------------------------------------------------------------

colSums(is.na(dailyActivity_merged))
Results: 
                      Id             ActivityDate               TotalSteps 
                       0                        0                        0 
           TotalDistance          TrackerDistance LoggedActivitiesDistance 
                       0                        0                        0 
      VeryActiveDistance ModeratelyActiveDistance      LightActiveDistance 
                       0                        0                        0 
 SedentaryActiveDistance        VeryActiveMinutes      FairlyActiveMinutes 
                       0                        0                        0 
    LightlyActiveMinutes         SedentaryMinutes                 Calories 
                       0                        0                        0     

I'm not going to delete rows in this dataset. Since all values are 0, it means that there are no missing values in any of the columns in the dailyActivity_merged dataset.
-----------------------------------------------------------------------------------------------------------------------------------------------------------                      
colSums(is.na(minuteCaloriesNarrow_merged))
Results:
Id  ActivityMinute       Calories 
0              0              0 

I'm not going to delete rows in this dataset. Since all values are 0, it means that there are no missing values in any of the columns
-----------------------------------------------------------------------------------------------------------------------------------------------------------
colSums(is.na(hourlyIntensities_merged))
Results:
Id     ActivityHour   TotalIntensity AverageIntensity 
 0                0                0                0 
 I'm not going to delete rows in this dataset. Since all values are 0, it means that there are no missing values in any of the columns

-----------------------------------------------------------------------------------------------------------------------------------------------------------
  colSums(is.na(hourlyCalories_merged))
  Results:
  Id    ActivityHour     Calories 
  0            0            0 
I'm not going to delete rows in this dataset. Since all values are 0, it means that there are no missing values in any of the columns
-----------------------------------------------------------------------------------------------------------------------------------------------------------
colSums(is.na(exercise_dataset))
Activity, Exercise or Sport (1 hour) 
                                   0 
                              130 lb 
                                   0 
                              155 lb 
                                   0 
                              180 lb 
                                   0 
                              205 lb 
                                   0 
                     Calories per kg 
                                   0 
-----------------------------------------------------------------------------------------------------------------------------------------------------------

How can you verify that your data is clean and ready to analyze?
Verification:
Summary statistics: Calculate summary statistics (mean, median, standard deviation, etc.) for relevant variables to ensure they make sense in the context of the data.

+ Min.: The minimum value in the column.
+ 1st Qu.: The 25th percentile (the value below which 25% of the data falls).
+ Median: The 50th percentile (the middle value of the sorted data).
+ Mean: The average value.
+ 3rd Qu.: The 75th percentile (the value below which 75% of the data falls).
+ Max.: The maximum value in the column.
  

      Id            ActivityDate         TotalSteps   
 Min.   :1.504e+09   Length:940         Min.   :    0  
 1st Qu.:2.320e+09   Class :character   1st Quarter.: 3790  
 Median:4.445e+09    Mode: character    Median:  7406  
 Mean:4.855e+09                         Mean:    7638  
 3rd Qu.:6.962e+09                      3rd Quarter: 10727  
 Max.   :8.878e+09                      Max.   : 36019  
 
 TotalDistance    TrackerDistance  LoggedActivitiesDistance
 Min.   : 0.000   Min.   : 0.000   Min.   :0.0000          
 1st Qu.: 2.620   1st Qu.: 2.620   1st Qu.:0.0000          
 Median: 5.245    Median:  5.245   Median: 0.0000          
 Mean: 5.490      Mean:    5.475   Mean:   0.1082          
 3rd Qu.: 7.713   3rd Qu.: 7.710   3rd Qu.:0.0000          
 Max.   :28.030   Max.   :28.030   Max.   :4.9421     
 
 VeryActiveDistance ModeratelyActiveDistance LightActiveDistance
 Min.   : 0.000     Min.   :0.0000           Min.   : 0.000     
 1st Qu.: 0.000     1st Qu.:0.0000           1st Qu.: 1.945     
 Median: 0.210      Median:0.2400            Median: 3.365     
 Mean: 1.503        Mean:0.5675              Mean: 3.341     
 3rd Qu.: 2.053     3rd Qu.:0.8000           3rd Qu.: 4.782     
 Max.   :21.920     Max.   :6.4800           Max.   :10.710    
 
 SedentaryActiveDistance VeryActiveMinutes FairlyActiveMinutes
 Min.   :0.000000        Min.   :  0.00    Min.   :  0.00     
 1st Qu.:0.000000        1st Qu.:  0.00    1st Qu.:  0.00     
 Median:0.000000         Median:  4.00     Median:   6.00     
 Mean:0.001606           Mean: 21.16       Mean:     13.56     
 3rd Qu.:0.000000        3rd Qu.: 32.00    3rd Qu.:  19.00     
 Max.   :0.110000        Max.   :210.00    Max.:     143.00     
 
 LightlyActiveMinutes SedentaryMinutes    Calories   
 Min.   :  0.0        Min.   :   0.0   Min.   :   0  
 1st Qu.:127.0        1st Qu.: 729.8   1st Qu.:1828  
 Median:199.0         Median:1057.5    Median:2134  
 Mean:192.8           Mean: 991.2      Mean:2304  
 3rd Qu.:264.0        3rd Qu.:1229.5   3rd Qu.:2793  
 Max.   :518.0        Max.   :1440.0   Max.   :4900  


mean: The average value of each variable.
sd: The standard deviation, a measure of how spread out the data is around the mean.
p0: The minimum value (0th percentile).
p25: The 25th percentile (the value below which 25% of the data falls).
p50: The median (50th percentile).
p75: The 75th percentile (the value below which 75% of the data falls).
p100: The maximum value (100th percentile).
hist: A histogram visualizing the distribution of the data.

 skim_variable            n_missing complete_rate    mean      sd
 1 Id                               0             1 4.86e+9    2.42e+9
 2 TotalSteps                       0             1 7.64e+3    5.09e+3
 3 TotalDistance                    0             1 5.49e+0    3.92e+0
 4 TrackerDistance                  0             1 5.48e+0    3.91e+0
 5 LoggedActivitiesDistance         0             1 1.08e-1    6.20e-1
 6 VeryActiveDistance               0             1 1.50e+0    2.66e+0
 7 ModeratelyActiveDistance         0             1 5.68e-1    8.84e-1
 8 LightActiveDistance              0             1 3.34e+0    2.04e+0
 9 SedentaryActiveDistance          0             1 1.61e-3    7.35e-3
10 VeryActiveMinutes                0             1 2.12e+1    3.28e+1
11 FairlyActiveMinutes              0             1 1.36e+1    2.00e+1
12 LightlyActiveMinutes             0             1 1.93e+2    1.09e+2
13 SedentaryMinutes                 0             1 9.91e+2    3.01e+2
14 Calories                         0             1 2.30e+3    7.18e+2

           p0           p25     p50     p75    p100 hist 
 1 1503960366 2320127002    4.45e+9 6.96e+9 8.88e+9 ▇▅▃▅▅
 2          0       3790.   7.41e+3 1.07e+4 3.60e+4 ▇▇▁▁▁
 3          0          2.62 5.24e+0 7.71e+0 2.80e+1 ▇▆▁▁▁
 4          0          2.62 5.24e+0 7.71e+0 2.80e+1 ▇▆▁▁▁
 5          0          0    0       0       4.94e+0 ▇▁▁▁▁
 6          0          0    2.10e-1 2.05e+0 2.19e+1 ▇▁▁▁▁
 7          0          0    2.40e-1 8.00e-1 6.48e+0 ▇▁▁▁▁
 8          0          1.95 3.36e+0 4.78e+0 1.07e+1 ▆▇▆▁▁
 9          0          0    0       0       1.10e-1 ▇▁▁▁▁
10          0          0    4   e+0 3.2 e+1 2.1 e+2 ▇▁▁▁▁
11          0          0    6   e+0 1.9 e+1 1.43e+2 ▇▁▁▁▁
12          0        127    1.99e+2 2.64e+2 5.18e+2 ▅▇▇▃▁
13          0        730.   1.06e+3 1.23e+3 1.44e+3 ▁▁▇▅▇
14          0       1828.   2.13e+3 2.79e+3 4.9 e+3 ▁▆▇▃▁
> 
-----------------------------------------------------------------------------------------------------------------------------------------------------------
summary(minuteCaloriesNarrow_merged)
       Id            ActivityMinute    
 Min.   :1.504e+09   Length:1325580    
 1st Qu.:2.320e+09   Class : character  
 Median :4.445e+09   Mode:character  
 Mean   :4.848e+09                     
 3rd Qu.:6.962e+09                     
 Max.   :8.878e+09                     
    Calories      
 Min.   : 0.0000  
 1st Qu.: 0.9357  
 Median : 1.2176  
 Mean   : 1.6231  
 3rd Qu.: 1.4327  
 Max.   :19.7499  

 skim(minuteCaloriesNarrow_merged)
── Data Summary ────────────────────────
                           Values                      
Name                       minuteCaloriesNarrow_merg...
Number of rows             1325580                     
Number of columns          3                           
_______________________                                
Column type frequency:                                 
  character                1                           
  numeric                  2                           
________________________                               
Group variables            None                        

── Variable type: character ────────────────────────
  skim_variable  n_missing complete_rate min max
1 ActivityMinute         0             1  19  21
  empty n_unique whitespace
1     0    44160          0

── Variable type: numeric ──────────────────────────
  skim_variable n_missing complete_rate
1 Id                    0             1
2 Calories              0             1
           mean            sd         p0     p25
1 4847897692.   2422313222.   1503960366 2.32e+9
2          1.62          1.41          0 9.36e-1
            p50           p75         p100 hist 
1 4445114986    6962181067    8877689391   ▇▅▃▅▅
2          1.22          1.43         19.7 ▇▁▁▁▁

-----------------------------------------------------------------------------------------------------------------------------------------------------------
summary(hourlyIntensities_merged)
       Id            ActivityHour      
 Min.   :1.504e+09   Length:22099      
 1st Qu.:2.320e+09   Class :character  
 Median :4.445e+09   Mode  :character  
 Mean   :4.848e+09                     
 3rd Qu.:6.962e+09                     
 Max.   :8.878e+09                     
 TotalIntensity   AverageIntensity
 Min.   :  0.00   Min.   :0.0000  
 1st Qu.:  0.00   1st Qu.:0.0000  
 Median :  3.00   Median :0.0500  
 Mean   : 12.04   Mean   :0.2006  
 3rd Qu.: 16.00   3rd Qu.:0.2667  
 Max.   :180.00   Max.   :3.0000  

── Data Summary ────────────────────────
                           Values                  
Name                       hourlyIntensities_merged
Number of rows             22099                   
Number of columns          4                       
_______________________                            
Column type frequency:                             
  character                1                       
  numeric                  3                       
________________________                           
Group variables            None                    

── Variable type: character ────────────────────────
  skim_variable n_missing complete_rate min max
1 ActivityHour          0             1  19  21
  empty n_unique whitespace
1     0      736          0

── Variable type: numeric ──────────────────────────
  skim_variable    n_missing complete_rate    mean
1 Id                       0             1 4.85e+9
2 TotalIntensity           0             1 1.20e+1
3 AverageIntensity         0             1 2.01e-1
       sd         p0        p25           p50
1 2.42e+9 1503960366 2320127002 4445114986   
2 2.11e+1          0          0          3   
3 3.52e-1          0          0          0.05
      p75       p100 hist 
1 6.96e+9 8877689391 ▇▅▃▅▅
2 1.6 e+1        180 ▇▁▁▁▁
3 2.67e-1          3 ▇▁▁▁▁
-----------------------------------------------------------------------------------------------------------------------------------------------------------
skim(hourlyIntensities_merged)
── Data Summary ────────────────────────
                           Values                  
Name                       hourlyIntensities_merged
Number of rows             22099                   
Number of columns          4                       
_______________________                            
Column type frequency:                             
  character                1                       
  numeric                  3                       
________________________                           
Group variables            None                    

── Variable type: character ────────────────────────
  skim_variable n_missing complete_rate min max
1 ActivityHour          0             1  19  21
  empty n_unique whitespace
1     0      736          0

── Variable type: numeric ──────────────────────────
  skim_variable    n_missing complete_rate    mean
1 Id                       0             1 4.85e+9
2 TotalIntensity           0             1 1.20e+1
3 AverageIntensity         0             1 2.01e-1
       sd         p0        p25           p50
1 2.42e+9 1503960366 2320127002 4445114986   
2 2.11e+1          0          0          3   
3 3.52e-1          0          0          0.05
      p75       p100 hist 
1 6.96e+9 8877689391 ▇▅▃▅▅
2 1.6 e+1        180 ▇▁▁▁▁
3 2.67e-1          3 ▇▁▁▁▁
-----------------------------------------------------------------------------------------------------------------------------------------------------------
summary(exercise_dataset)
 Activity, Exercise or Sport (1 hour)
 Length:248                          
 Class: character                    
 Mode : character                    
                                                                                                       
     130 lb           155 lb           180 lb      
 Min.   :  89.0   Min.   : 106.0   Min.   : 123.0  
 1st Qu.: 236.0   1st Qu.: 281.0   1st Qu.: 327.0  
 Median : 354.0   Median : 422.0   Median : 490.0  
 Mean   : 389.8   Mean   : 464.7   Mean   : 539.7  
 3rd Qu.: 472.0   3rd Qu.: 563.0   3rd Qu.: 654.0  
 Max.   :1062.0   Max.   :1267.0   Max.   :1471.0  
     205 lb       Calories per kg 
 Min.   : 140.0   Min.   :0.3101  
 1st Qu.: 372.0   1st Qu.:0.8232  
 Median : 558.0   Median :1.2349  
 Mean   : 614.6   Mean   :1.3599  
 3rd Qu.: 745.0   3rd Qu.:1.6478  
 Max.   :1675.0   Max.   :3.7066  

 skim(exercise_dataset) # Since this is a look up table this might not be helpful 
skim_variable   n_missing complete_rate   mean
1 130 lb                  0             1 390.  
2 155 lb                  0             1 465.  
3 180 lb                  0             1 540.  
4 205 lb                  0             1 615.  
5 Calories per kg         0             1   1.36
       sd      p0     p25    p50    p75    p100
1 194.     89     236     354    472    1062   
2 232.    106     281     422    563    1267   
3 269.    123     327     490    654    1471   
4 307.    140     372     558    745    1675   
5   0.679   0.310   0.823   1.23   1.65    3.71
  hist 
1 ▇▇▂▂▁
2 ▇▇▂▂▁
3 ▇▇▂▂▁
4 ▇▇▂▂▁
5 ▇▇▂▂▁
--------------------------------------------------------------------------------------------------------------------------------------------------------
# Case Study Roadmap - Analyze

Guiding Questions

How should you organize your data to perform analysis on it?
Aggregation: Aggregate data from the dailyActivity_merged, minuteCaloriesNarrow_merged, and hourlyIntensities_merged datasets to the daily level. This allows us to compare daily calorie expenditure with exercise patterns.

# Assuming the date column is named ActivityMinute and it's in a DateTime format
daily_calories <- minuteCaloriesNarrow_merged %>%
  mutate(ActivityDate = as.Date(ActivityMinute)) %>%  # Extract date
  group_by(Id, ActivityDate) %>%
  summarize(TotalCalories = sum(Calories, na.rm = TRUE))
--------------------------------------------------------------------------------------------------------------------------------------------------------
Aggregate hourlyIntensities_merged:

This dataset might contain intensity data at the hourly level. We'll average the intensity for each day and user.
--------------------------------------------------------------------------------------------------------------------------------------------------------
Code snippet
# Assuming the date column is named ActivityHour and it's in a datetime format
daily_intensities <- hourlyIntensities_merged %>%
  mutate(ActivityDate = as.Date(ActivityHour)) %>% # Extract date
  group_by(Id, ActivityDate) %>%
  summarize(AvgIntensity = mean(TotalIntensity, na.rm = TRUE))

Merging: Combine the aggregated Fitbit data with the exercise_dataset based on activity type. This lets us compare Fitbit's calorie estimates with those from the reference dataset.
Has your data been properly formatted?
Yes. The Fitbit data has been cleaned, missing values addressed (if any), duplicates removed, and relevant columns merged. The ActivityDate is converted to a date format. The exercise_dataset has been restructured to calculate calories per minute for each weight class.
What surprises did you discover in the data?
(Example) We might find that users who log more activities in the Fitbit app tend to have higher overall calorie expenditure compared to those who don't log activities, even if their total steps or active minutes are similar.
(Example) We might observe significant differences in calorie burn estimates between the Fitbit dataset and the "Calories Burned" dataset for certain activities, suggesting potential areas for improvement in Bellabeat's algorithms.
What trends or relationships did you find in the data?
(Example) There might be a positive correlation between total steps taken and calories burned, with higher steps leading to higher calorie expenditure.
(Example) Certain activity types (e.g., running, swimming) might consistently lead to higher calorie burn than others (e.g., walking, yoga).
(Example) There might be distinct patterns in calorie expenditure and activity intensity throughout the day, with peaks in the morning or evening.
How will these insights help answer your business questions?
Feature Enhancement: By identifying popular and effective activities, Bellabeat can prioritize features that cater to these activities, potentially including more accurate tracking or personalized guidance.
User Engagement: Understanding activity patterns can help Bellabeat design interventions or challenges to encourage users to be more active during specific times of day or week.
Marketing and Messaging: Insights into calorie burn and activity preferences can be used to tailor marketing messages and target specific user segments with relevant content.
Key Tasks:

Aggregate data: Aggregate the Fitbit datasets to a daily level using functions like group_by and summarize.
Organize and format data: Ensure all relevant variables are in the correct format (e.g., dates, numeric) for analysis and visualization.
Perform calculations: Calculate total active minutes, combined distances, and calories per minute as needed.
Identify trends and relationships: Use statistical tests (e.g., correlation, t-tests), data visualization (scatter plots, line graphs, bar charts), and potentially even machine learning models to uncover patterns and relationships in the data.
Deliverable:
A summary of the analysis, including:

Key findings: Summarize the most important trends and relationships discovered.
Insights: Discuss the implications of the findings for Bellabeat's business.
Recommendations: Provide actionable recommendations based on the analysis, such as potential feature enhancements, engagement strategies, or marketing messages.
Example Summary (Concise):

"Analysis of Fitbit data revealed that users who log activities tend to burn more calories overall. Certain activities, like running and swimming, were associated with higher calorie expenditure compared to others. Activity levels also varied by time of day, with peaks in the morning and evening. These insights suggest opportunities for Bellabeat to refine its calorie-tracking algorithms, personalize activity recommendations, and develop features that encourage users to engage in specific activities during optimal times."






