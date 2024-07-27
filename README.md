# BellaBeats Google's Data Analytics Capstone Course 

Hi, My name is Marc Aldana. I have a Bachelor of Science from SUNY Old Westbury in Management Information Systems. This is my case study on wearable technology. I'm going to go into each step of the data analysis process. I will provide some visualizations. I will be using R-studio to analyze datasets. 

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

# Key Focus Areas:

+ Feature Enhancement:
Identify most used and valued features: Determine which features (e.g., activity tracking, sleep analysis, stress monitoring) are most frequently used and highly rated by users across different brands. This can guide Bellabeat in prioritizing feature development and improvements.
Uncover unmet needs: Analyze user feedback and reviews to identify gaps in existing features and potential areas for innovation. This could lead to the development of unique features that address unmet needs in the market.

+ Usage patterns: Analyze how users interact with different features and how their usage changes over time. This can help Bellabeat optimize the user experience and design features that encourage long-term engagement.
  
+ Churn analysis: Identify factors that contribute to user churn (stopping using the device) and develop strategies to improve customer retention.
Market Competitiveness:
+ Benchmarking: Compare Bellabeat's performance to competitors in terms of user satisfaction, feature adoption, and overall market share. This can highlight areas where Bellabeat excels or needs to improve.
  
+ Competitive advantage: Identify Bellabeat's unique strengths and areas where they can differentiate themselves from competitors. This could involve focusing on specific demographics, health conditions, or lifestyle factors.

Data Sources:

+ Bellabeat Internal Data: Utilize user data collected from Bellabeat devices and apps, including activity, sleep, stress, and reproductive health data.
+ Public Datasets: Explore publicly available datasets from other wearable device companies (if available), ensuring compliance with privacy regulations.
  
+ Customer Surveys and Feedback: Gather data from surveys, reviews, and social media to understand user preferences, pain points, and suggestions for improvement.
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

+ Calories Burned During Exercise and Activities:
Single CSV file in wide format (each row is an activity, columns represent METs and calories burned).
+ Are there issues with bias or credibility in this data? Does your data ROCCC?

Bias:
+ Fitbit Data: Self-selection bias (users opted to share data), potential over-representation of health-conscious individuals, and limited to Fitbit users.
+ Calories Burned Data: Potential inaccuracies in calorie estimates, as individual factors (age, weight, etc.) are not considered.
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
# Case Study Roadmap - Process
 
+ What tools are you choosing and why?
+ RStudio: We'll primarily use RStudio for this analysis due to its strengths in data manipulation, statistical analysis, and visualization.
+ Libraries: We'll leverage the following R libraries:
+ dplyr: For data wrangling (filtering, selecting, mutating, summarizing)
+ tidyr: For tidying data (pivoting between long and wide formats)
+ ggplot2: For creating informative and aesthetically pleasing visualizations
+ lubridate: For working with date and time data
+ Have you ensured your data’s integrity?
+ Initial Data Checks: Before diving into analysis, we've taken the following steps:
+ Missing values: Identified and handled missing values in both datasets. Since the "Calories Burned" dataset has no missing values, we focus on the Fitbit dataset. Depending on the extent, we can either remove rows with missing data or impute missing values with appropriate methods.
+ Duplicates: Checked and removed any duplicate entries in the Fitbit dataset to avoid inflating numbers.
+ Data types: Confirmed that columns have the correct data types. For example, ActivityDate in the Fitbit dataset will be converted to a date format.
+ Outliers: Examined for extreme values in the Fitbit dataset. Outliers in calorie data or activity levels might be investigated further as they could indicate data entry errors or exceptional scenarios.
+ What steps have you taken to ensure that your data is clean?
+ Data Cleaning Steps:
+ Fitbit Data:
+ Handle missing values (remove or impute).
+ Remove duplicate entries.
+ Convert ActivityDate to date format.
+ Merge relevant tables (e.g., dailyActivity_merged, minuteCalories_merged) using common identifiers (e.g., Id, 
  ActivityDate).
+ Create calculated fields:
+ Calculate total active minutes by summing VeryActiveMinutes, FairlyActiveMinutes, and LightlyActiveMinutes.
+ Calculate the total distance from different sources (e.g., TrackerDistance, LoggedActivitiesDistance, etc.).
+ Calories Burned Data:
+ Calculate calories per minute for each activity to facilitate comparison with the Fitbit data.
-----------------------------------------------------------------------------------------------------------------------------------------------------------
## Summary of Activity Data

This table provides a summary of the initial rows and columns of the dataset, likely related to daily activity data.

| Column Name               | Number of Non-Zero Values | Possible Interpretation                                                                                                                               |
| -------------------------- | -----------------------: | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Id`                      |                        0 | Unique identifier for each user or data entry.                                                                                                   |
| `ActivityDate`            |                        0 | Date of the activity record. Further investigation needed to determine if dates are present in the dataset but not included in this summary.          |
| `TotalSteps`               |                        0 | Total number of steps taken during the day.                                                                                                          |
| `TotalDistance`            |                        0 | Total distance traveled during the day (likely in miles or kilometers).                                                                                 |
| `TrackerDistance`          |                        0 | Distance tracked by the device (may differ from `TotalDistance` due to manual logging or data discrepancies).                                      |
| `LoggedActivitiesDistance`  |                        0 | Distance logged through manual entry or other sources (may not be tracked by the device).                                                             |
| `VeryActiveDistance`       |                        0 | Distance covered during very active periods (e.g., running, intense exercise).                                                                      |
| `ModeratelyActiveDistance` |                        0 | Distance covered during moderately active periods (e.g., brisk walking).                                                                             |
| `LightActiveDistance`      |                        0 | Distance covered during light activity (e.g., casual walking).                                                                                       |
| `SedentaryActiveDistance`  |                        0 | Distance covered during sedentary activities (this might be an error or indicate a very specific tracking category).                                 |
| `VeryActiveMinutes`       |                        0 | Total minutes spent in very active activities.                                                                                                    |
| `FairlyActiveMinutes`      |                        0 | Total minutes spent in fairly active activities (intensity between light and very active).                                                            |
| `LightlyActiveMinutes`     |                        0 | Total minutes spent in light activities.                                                                                                          |
| `SedentaryMinutes`         |                        0 | Total minutes spent being sedentary.                                                                                                             |
| `Calories`                |                        0 | Total calories burned during the day.                                                                                                             |

**Important Note:**

All columns in this initial summary display 0 non-zero values. This could indicate one of the following:

*   The summary is only showing the first few rows, and these rows happen to have zeros in these columns.
*   There is a potential issue with data loading or formatting where values are not being read correctly.
*   These specific columns might be populated later in the dataset, or they might not be used in this particular analysis.

**Next Steps:**

1.  **Verify Data:** Double-check your data loading process and ensure all values are being read correctly.
2.  **Inspect Further:** Use functions like `summary()`, `head()`, and `tail()` in R to get a broader view of your dataset and confirm if the zero values are consistent throughout.
3.  **Explore Data:** If the values are indeed all zero, you'll need to consider if these columns are relevant for your analysis or if you need to explore other datasets or variables. 


-----------------------------------------------------------------------------------------------------------------------------------------------------------                      
## Missing Value Check: minuteCaloriesNarrow_merged Dataset

| Column Name   | Number of Missing Values |
| :------------- | ----------------------: |
| `Id`           |                        0 |
| `ActivityMinute` |                        0 |
| `Calories`     |                        0 |

**Key Takeaway:**

The `minuteCaloriesNarrow_merged` dataset contains no missing values in the `Id`, `ActivityMinute`, and `Calories` columns. This indicates that all rows have complete data for these variables, which is a good starting point for analysis. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------
## Missing Value Check: hourlyIntensities_merged Dataset

| Column Name       | Number of Missing Values |
| :----------------- | ----------------------: |
| `Id`               |                        0 |
| `ActivityHour`     |                        0 |
| `TotalIntensity`   |                        0 |
| `AverageIntensity` |                        0 |

**Key Takeaway:**

The `hourlyIntensities_merged` dataset contains no missing values in any of its columns. This is a positive indication that the dataset is complete and ready for analysis without the need for imputation or removal of rows. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------
  ## Missing Value Check: hourlyCalories_merged Dataset

| Column Name   | Number of Missing Values |
| :------------- | ----------------------: |
| `Id`           |                        0 |
| `ActivityHour` |                        0 |
| `Calories`     |                        0 |

**Key Takeaway:**

The `hourlyCalories_merged` dataset contains no missing values in any of its columns. This is a positive indication that the dataset is complete and ready for analysis without the need for imputation or removal of rows. 
-----------------------------------------------------------------------------------------------------------------------------------------------------------
## Missing Value Check: exercise_dataset

| Column Name                        | Number of Missing Values |
| :---------------------------------- | ----------------------: |
| `Activity, Exercise or Sport (1 hour)` |                        0 |
| `130 lb`                             |                        0 |
| `155 lb`                             |                        0 |
| `180 lb`                             |                        0 |
| `205 lb`                             |                        0 |
| `Calories per kg`                    |                        0 |

**Key Takeaway:**

The `exercise_dataset` contains no missing values in any of its columns. This indicates that all rows have complete data for each exercise/activity and weight category, making the dataset suitable for analysis without imputation or row removal.
-----------------------------------------------------------------------------------------------------------------------------------------------------------

+ How can you verify that your data is clean and ready to analyze?
Verification:
Summary statistics: Calculate summary statistics (mean, median, standard deviation, etc.) for relevant variables to ensure they make sense in the context of the data.

## Data Summary for minuteCaloriesNarrow_merged Dataset

**General Overview:**

*   Number of rows: 1,325,580
*   Number of columns: 3
*   Column types:
    *   1 character (`ActivityMinute`)
    *   2 numeric (`Id`, `Calories`)

**Character Variable Summary:**

| Variable Name   |  Data Type | Length (number of characters) |
| :------------- | :-------- | ----------------------------: |
| `ActivityMinute` |  Character |       19 - 21               |

**Numeric Variable Summary:**

| Variable Name | Min.   | 1st Qu. | Median  | Mean    | 3rd Qu. | Max.    |
| ------------- | -----: | -------: | ------: | -------: | -------: | -------: |
| `Id`           | 1.5e+9 |  2.3e+9  | 4.4e+9 | 4.8e+9  |  6.9e+9  | 8.8e+9  |
| `Calories`     | 0.0    |  0.9357  |  1.2176 | 1.6231  |  1.4327  | 19.7499  |


**Explanation of Summary Statistics:**

*   **Min:** The minimum value in the column.
*   **1st Qu.:** The 25th percentile (the value below which 25% of the data falls).
*   **Median:** The 50th percentile (the middle value of the sorted data).
*   **Mean:** The average value.
*   **3rd Qu.:** The 75th percentile (the value below which 75% of the data falls).
*   **Max:** The maximum value in the column.


**Key Observations:**

*   The `ActivityMinute` variable seems to represent time stamps and likely has a consistent format based on the length range (19-21 characters). Further investigation into the format (e.g., "YYYY-MM-DD HH:MM:SS") would be beneficial.
*   The `Id` variable is likely a unique identifier for each data point (potentially each minute of activity for each user).
*   `Calories` represents the calories burned per minute, with a wide range from 0 to 19.75. The distribution appears right-skewed, indicating most values are concentrated in the lower range.

**Potential Next Steps:**

*   Investigate the exact format of `ActivityMinute` for more precise time-based analysis.
*   Consider aggregating the data by hour or day to examine broader trends in calorie expenditure.
*   Explore the relationship between `Id` (potentially representing users) and calorie burn to identify individual differences or patterns.
*   Conduct further statistical analysis to understand the distribution of `Calories` more thoroughly.
  _____________________________________________________________________________
## Data Summary for dailyActivity_merged Dataset

### General Overview:

*   Number of rows: 940
*   Number of columns: 14
*   Column types:
    *   1 character (`ActivityDate`)
    *   13 numeric (`Id`, `TotalSteps`, `TotalDistance`, etc.)

### Character Variable Summary:

| Variable Name   | Number of Unique Values |
| :-------------- | ----------------------: |
| `ActivityDate`  |                     61  |

### Numeric Variable Summary:

| Variable Name               | Mean            | Standard Deviation | Min    | 25th Percentile | Median  | 75th Percentile | Max      |
| :----------------------------- | ---------------: | ----------------: | -----: | --------------: | ------: | --------------: | -------: |
| `Id`                          | 4.855e+9         | 2.42e+9           | 1.5e+9 |      2.3e+9      | 4.4e+9 |      6.9e+9      | 8.8e+9  |
| `TotalSteps`                   | 7638             | 5092               | 0      |     3790         |  7406   |    10727        | 36019   |
| `TotalDistance`                | 5.490            | 3.918              | 0      |      2.62        |  5.245  |     7.713       | 28.03   |
| `TrackerDistance`              | 5.475            | 3.912              | 0      |      2.62        |  5.245  |     7.710       | 28.03   |
| `LoggedActivitiesDistance`    | 0.1082           | 0.6201             | 0      |      0           |   0     |      0           |  4.9421  |
| `VeryActiveDistance`           | 1.503            | 2.658              | 0      |      0           |  0.21   |     2.053       | 21.92   |
| `ModeratelyActiveDistance`     | 0.5675           | 0.8837             | 0      |      0           |  0.24   |     0.800       |  6.48   |
| `LightActiveDistance`          | 3.341            | 2.036              | 0      |      1.945       |  3.365  |     4.782       | 10.71   |
| `SedentaryActiveDistance`      | 0.0016           | 0.0074             | 0      |      0           |   0     |      0           |  0.11   |
| `VeryActiveMinutes`           | 21.16            | 32.84              | 0      |      0           |   4     |     32           | 210    |
| `FairlyActiveMinutes`          | 13.56            | 19.99              | 0      |      0           |   6     |     19           | 143    |
| `LightlyActiveMinutes`         | 192.8            | 108.6              | 0      |    127           | 199     |    264           | 518    |
| `SedentaryMinutes`             | 991.2            | 300.9              | 0      |    730           | 1057.5  |   1229.5        | 1440   |
| `Calories`                    | 2304             | 718.1              | 0      |    1828         | 2134    |    2793         | 4900   |

**Key Observations:**

*   The dataset seems to capture daily activity data over 61 unique days.
*   The average daily step count is around 7638.
*   The average daily distance covered is around 5.49 units.
*   Calorie consumption is relatively high, with an average of 2304 per day.
*   There's a significant amount of sedentary time, with an average of 991 minutes per day.
> 
-----------------------------------------------------------------------------------------------------------------------------------------------------------
## Data Summary for minuteCaloriesNarrow_merged Dataset

**General Overview:**

*   Number of rows: 1,325,580
*   Number of columns: 3
*   Column types:
    *   1 character (`ActivityMinute`)
    *   2 numeric (`Id`, `Calories`)

**Character Variable Summary:**

| Variable Name   |  Data Type | Length (number of characters) |
| :------------- | :-------- | ----------------------------: |
| `ActivityMinute` |  Character |       19 - 21               |

**Numeric Variable Summary:**

| Variable Name | Mean            |             Std. Deviation |   Min |   25th Percentile |   Median |   75th Percentile |      Max |
| :------------- | ---------------: | ------------------------: | ----: | --------------: | ------: | --------------: | -------: |
| `Id`           | 4,847,897,692   |  Not provided in the output | 1.5e+9 |      2.3e+9      | 4.4e+9 |      6.9e+9      | 8.8e+9  |
| `Calories`     | 1.6231          |          Not provided in the output | 0.0    |     0.9357       |  1.2176 |     1.4327       | 19.7499  |



**Key Observations:**

*   The `ActivityMinute` variable seems to represent time stamps and likely has a consistent format based on the length range (19-21 characters). Further investigation into the format (e.g., "YYYY-MM-DD HH:MM:SS") would be beneficial.
*   The `Id` variable is likely a unique identifier for each data point (potentially each minute of activity for each user).
*   `Calories` represents the calories burned per minute, with a wide range from 0 to 19.75. The distribution appears right-skewed, indicating most values are concentrated in the lower range.

**Potential Next Steps:**

*   Investigate the exact format of `ActivityMinute` for more precise time-based analysis.
*   Consider aggregating the data by hour or day to examine broader trends in calorie expenditure.
*   Explore the relationship between `Id` (potentially representing users) and calorie burn to identify individual differences or patterns.
*   Conduct further statistical analysis to understand the distribution of `Calories` more thoroughly.

________________________________________________________________________________________________
 ## Data Summary for minuteCaloriesNarrow_merged Dataset

**General Overview:**

*   Number of rows: 1,325,580
*   Number of columns: 3
*   Column types:
    *   1 character (`ActivityMinute`)
    *   2 numeric (`Id`, `Calories`)

**Character Variable Summary:**

| Variable Name   |  Data Type | Length (number of characters) |
| :------------- | :-------- | ----------------------------: |
| `ActivityMinute` |  Character |       19 - 21               |

**Numeric Variable Summary:**

| Variable Name | Mean            |             Std. Deviation |   Min |   25th Percentile |   Median |   75th Percentile |      Max |
| :------------- | ---------------: | ------------------------: | ----: | --------------: | ------: | --------------: | -------: |
| `Id`           | 4,847,897,692   |  Not provided in the output | 1.5e+9 |      2.3e+9      | 4.4e+9 |      6.9e+9      | 8.8e+9  |
| `Calories`     | 1.6231          |          Not provided in the output | 0.0    |     0.9357       |  1.2176 |     1.4327       | 19.7499  |



**Key Observations:**

*   The `ActivityMinute` variable seems to represent time stamps and likely has a consistent format based on the length range (19-21 characters). Further investigation into the format (e.g., "YYYY-MM-DD HH:MM:SS") would be beneficial.
*   The `Id` variable is likely a unique identifier for each data point (potentially each minute of activity for each user).
*   `Calories` represents the calories burned per minute, with a wide range from 0 to 19.75. The distribution appears right-skewed, indicating most values are concentrated in the lower range.

**Potential Next Steps:**

*   Investigate the exact format of `ActivityMinute` for more precise time-based analysis.
*   Consider aggregating the data by hour or day to examine broader trends in calorie expenditure.
*   Explore the relationship between `Id` (potentially representing users) and calorie burn to identify individual differences or patterns.
*   Conduct further statistical analysis to understand the distribution of `Calories` more thoroughly.


-----------------------------------------------------------------------------------------------------------------------------------------------------------
## Data Summary for hourlyIntensities_merged Dataset

**General Overview:**

*   Number of rows: 22,099
*   Number of columns: 4
*   Column types:
    *   1 character (`ActivityHour`)
    *   3 numeric (`Id`, `TotalIntensity`, `AverageIntensity`)

**Character Variable Summary:**

| Variable Name   |  Data Type | Length (number of characters) | Number of Unique Values |
| :------------- | :-------- | ----------------------------: |----------------------:|
| `ActivityHour` |  Character |       19 - 21               |  736                 |

**Numeric Variable Summary:**

| Variable Name      |      Mean |    Std. Deviation |   Min |   25th Percentile |   Median |   75th Percentile |      Max |
| :----------------- | --------: | ----------------: | ----: | --------------: | ------: | --------------: | -------: |
| `Id`                | 4.85e+9   |  Not provided in the output | 1.5e+9 |      2.3e+9      | 4.4e+9 |      6.9e+9      | 8.8e+9  |
| `TotalIntensity`    | 12.04    |  21.13           |  0.00  |      0.00        |  3.00   |     16.00        |   180.00 |
| `AverageIntensity` |  0.2006  |   0.3518          |  0.00  |      0.00        |  0.05   |      0.2667       |    3.00  |

**Key Observations:**

*   The `ActivityHour` variable likely represents timestamps with a consistent format (given the length). Further investigation is needed to confirm the exact format.
*   The `Id` variable is likely a unique identifier for each data point (potentially each hour of activity for each user).
*   `TotalIntensity` has a wide range, indicating varying levels of intensity throughout the dataset. The distribution is heavily skewed right, with most values being low.
*   `AverageIntensity` is calculated per hour and also shows a skewed right distribution, suggesting that most hours have low-intensity activity.

**Potential Next Steps:**

*   Confirm the format of `ActivityHour` for precise time-based analysis.
*   Investigate the distribution of `TotalIntensity` and `AverageIntensity` in more detail (e.g., histograms, boxplots) to understand the patterns of activity intensity.
*   Explore the relationship between `Id` (potentially users) and intensity levels to identify individual differences or trends.
*   Aggregate data to higher time intervals (e.g., daily or weekly) to examine broader trends in activity intensity. 
-----------------------------------------------------------------------------------------------------------------------------------------------------------

## Data Summary for exercise_dataset

### General Overview:

*   **Purpose:** The `exercise_dataset` appears to be a lookup table providing calorie estimates for various exercises or sports based on body weight.
*   **Number of Rows:** 248
*   **Number of Columns:** 6
*   **Column Types:** All numeric

### Column Descriptions:

*   **`Activity, Exercise or Sport (1 hour)`:** This column likely contains the names of different activities or exercises (character type, not shown in summary).
*   **Weight-Based Calorie Estimates:** The remaining columns (`130 lb`, `155 lb`, `180 lb`, `205 lb`) represent estimated calorie expenditure for each activity, categorized by body weight.
*   **`Calories per kg`:** This column provides a standardized calorie estimate based on body weight in kilograms.

### Numeric Variable Summary:

| Variable Name      |      Mean |     Std. Deviation |   Min |   25th Percentile |   Median |   75th Percentile |      Max |
| :----------------- | --------: | ----------------: | ----: | --------------: | ------: | --------------: | -------: |
| `130 lb`            |  389.8   |          193.6  |  89.0  |        236.0      |  354.0  |        472.0      | 1062.0  |
| `155 lb`            |  464.7   |          231.7  | 106.0  |        281.0      |  422.0  |        563.0      | 1267.0  |
| `180 lb`            |  539.7   |          268.9  | 123.0  |        327.0      |  490.0  |        654.0      | 1471.0  |
| `205 lb`            |  614.6   |          306.7  | 140.0  |        372.0      |  558.0  |        745.0      | 1675.0  |
| `Calories per kg` |    1.36  |           0.679  |  0.3101 |        0.8232     |  1.2349 |        1.6478     |  3.7066 |

### Key Observations:

*   The dataset provides a useful reference for estimating calorie expenditure for various activities, accounting for different body weights.
*   The calorie estimates increase proportionally with body weight, as expected.
*   The `Calories per kg` column allows for more personalized estimations based on an individual's weight.

### Additional Notes:

*   It's important to note that these are just estimates. Actual calorie burn can vary based on individual factors like age, gender, and fitness level. 
*   To make this table even more useful, it would be helpful to know the specific activities listed in the first column. 

--------------------------------------------------------------------------------------------------------------------------------------------------------
# Case Study Roadmap - Analyze

+ Phase 1: Initial Data Exploration and Cleaning
Guiding Questions

+ Data Organization:

+ dailyActivity_merged: Daily summaries (activity, calories, intensity).
exercise_dataset_long: Calorie expenditure by activity, intensity, and weight.
calorie_lookup_155: Estimated calories/minute per activity (155 lbs).
Data Formatting:

+ActivityDate converted to date format.
TotalActiveMinutes calculated (sum of VeryActiveMinutes, FairlyActiveMinutes, LightlyActiveMinutes).
EstimatedCaloriesBurned added to dailyActivity_merged.
Key Findings

+ Surprising Discovery:
A significant difference between estimated and tracked calories (high Mean Absolute Error).
Note: This suggests the estimation model may need refinement.

+ Trends and Relationships:
Moderate positive correlation between total steps and calories burned (0.58).
[1] "Correlation between Total Steps and Calories Burned: 0.581380189499401"
Right-skewed distribution of calories burned.
Positive correlation between TotalActiveMinutes and TotalCalories (0.64).
Business Implications for Bellabeat

+ Calorie Estimation Discrepancy: Refine the calorie estimation algorithm to include individual factors (weight, heart rate, specific MET values).
  
+ Activity Trends:
Encourage users to be more active with personalized goals.
Create features/campaigns promoting increased active time.
Deliverable:

+ Summary of Analysis:
Strong correlations between steps/active minutes and calories.
High MAE/MAPE in calorie estimation.
--------------------------------------------------------------------------------------------------------------------------------------------------------
+ Phase 2: Deeper Analysis with Merged Data
Data Preparation

+ Merging: Combined Fitbit data with exercise dataset based on activity type.
Key Findings

+Activity Logging: Users who log activities may burn more calories overall.
Calorie Estimation: Significant differences in calorie estimates for certain activities (potential for algorithm improvement).

+ Activity Patterns: Distinct patterns in calorie expenditure and intensity throughout the day.
Business Implications for Bellabeat

+ Feature Enhancement: Prioritize features for popular/effective activities.
User Engagement: Design interventions/challenges to encourage activity during specific times.
Marketing: Tailor messages based on calorie burn and activity preferences.
Key Tasks

+ Calculations: Total active minutes, combined distances, calories per minute.
Analysis: Statistical tests, visualizations, and potentially machine learning models.
Deliverable:

+ Detailed Analysis Summary:
Impact of activity logging on calorie burn.
Calorie burn variance by activity type.
Activity patterns by time of day.
Recommendations for algorithm refinement, personalization, and feature development

--------------------------------------------------------------------------------------------------------------------------------------------------------
# Case Study Roadmap - Share

Guiding Questions

+ Were you able to answer the business questions?

Yes. The analysis provided valuable insights into:
Calorie Estimation Accuracy: We quantified the error in Bellabeat's calorie estimation algorithm and found it to be somewhat inaccurate on average.
Activity Patterns: We identified popular activities and the general distribution of activity intensity among users, highlighting a significant amount of sedentary time.
Relationships: We found a moderate positive correlation between steps/active minutes and calorie expenditure.
Discrepancies: The analysis revealed a potential overestimation of calories burned for some activities compared to the reference dataset.
What story does your data tell?

+ Story: The data tells a story of active users who primarily engage in moderate-intensity activities but also spend a considerable amount of time being sedentary. Bellabeat's calorie estimation tends to be higher than expected, indicating a need for improvement.
How do your findings relate to your original question?

+ Directly Relevant: The findings directly answer the initial questions about user behavior, activity patterns, calorie estimation accuracy, and potential areas for improvement in Bellabeat's product offerings.
Who is your audience? What is the best way to communicate with them?

+ Audience: Bellabeat stakeholders (executives, product managers, marketing teams).
+ Communication: A clear, concise, and visually appealing presentation (e.g., PowerPoint or Google Slides) with supporting visuals (charts, graphs, tables) would be most effective. The presentation should focus on the key insights and actionable recommendations, avoiding excessive technical details.
Can data visualization help you share your findings?

+ Essential: Data visualizations are crucial for effectively communicating the results. They make complex data patterns easy to understand and highlight the most important findings.
Types of Visualizations: We'll use scatterplots, histograms, bar charts, and potentially line graphs to illustrate correlations, distributions, comparisons, and trends.
Is your presentation accessible to your audience?

Yes. The presentation will be tailored to Bellabeat stakeholders. We'll:
Use clear language, avoiding technical jargon unless necessary.
Focus on the business implications of the findings.
Provide context and explanations for each visualization.
Use a visually appealing design with appropriate color schemes and fonts.

+ What It Shows: Average daily steps, calories burned, and active minutes over time for all users.
Insights: Help identify trends in overall user activity levels, seasonal variations, or the impact of any interventions or campaigns Bellabeat might have run during the data collection period
--------------------------------------------------------------------------------------------------------------------------------------------------------

![RbetwenActiveMinNCalories]
(https://github.com/marcaldana/analysis/assets/72458759/65fadc7b-aa04-4b31-8de5-17a6a37bde5e)

+ Insight: Reveals how active minutes are distributed across users. Are most users moderately active, or are there clusters of very active and sedentary individuals?
--------------------------------------------------------------------------------------------------------------------------------------------------------

![Rtotalactiveminute](https://github.com/marcaldana/analysis/assets/72458759/178a8008-9d48-4362-b42a-9a24f95dd922)

# Scatterplot: Estimated vs. Actual Calories Burned
Code:

![Rtotalactiveminute](https://github.com/marcaldana/analysis/assets/72458759/94d2ffd8-4418-453b-87c3-67b7218db369)
--------------------------------------------------------------------------------------------------------------------------------------

![RplotCalorieEstDifferences](https://github.com/marcaldana/analysis/assets/72458759/d8d5cf09-d978-4c3f-b0d5-6b561caa1cc4)

+ Interpretation:

+ High Bars: A tall bar in the histogram indicates that a particular range of calorie differences is quite common.
Low Bars: A short bar means that the corresponding range of calorie differences occurs less frequently.
Overall Shape: The overall shape of the histogram tells you about the distribution of the errors.
--------------------------------------------------------------------------------------------------------------------------------------


![REstimatedvsActual155](https://github.com/marcaldana/analysis/assets/72458759/3e2536f3-197a-4b20-a2ab-fc1b67afdce7)

--------------------------------------------------------------------------------------------------------------------------------------------------------

![RelatiomnshipStepsNCalories](https://github.com/marcaldana/analysis/assets/72458759/dff73aef-f684-492f-a18a-cb794b9d8397)

--------------------------------------------------------------------------------------------------------------------------------------------------------

# Case Study Roadmap - Act

+ Guiding Questions (Answered)

+ What is your conclusion based on your analysis?

+ Conclusion: Our analysis of Fitbit data reveals:
A significant discrepancy between Bellabeat's calorie estimations and actual user data, indicating a need for algorithm refinement.

Users predominantly engage in light to moderate activities, with a significant amount of sedentary time, highlighting an opportunity to promote more movement.

A positive correlation between steps/active minutes and calories burned, suggests that encouraging increased activity can contribute to weight management goals.

+ How could your team and business apply your insights?

+ Bellabeat can leverage these insights to:
Refine Calorie Estimation Algorithm: Improve the accuracy of calorie calculations by incorporating individual user data (weight, heart rate, potentially even sleep data) and validating against a wider range of activities.
Develop Targeted Features: Introduce features that encourage specific activities shown to effectively burn calories, especially those aligned with user preferences.

+ Create Personalized Recommendations: Offer personalized guidance based on individual activity levels and goals, potentially using different weight classes to tailor calorie estimations.
Gamification: Incorporate challenges or rewards to motivate users to increase their steps, and active minutes, and engage in higher-intensity activities.

+ Educational Content: Provide educational resources on the impact of different activities and intensities on calorie burn, empowering users to make informed choices.
What next steps would you or your stakeholders take based on your findings?

+ Next Steps:
Collect More Data: Gather additional data on user demographics (age, weight, gender) to further refine the calorie estimation model and personalize recommendations.
Conduct User Research: Conduct surveys or interviews to understand users' perceptions of calorie tracking and identify areas for improvement in the Bellabeat app/device experience.
Experiment with Algorithm Adjustments: Test different calorie estimation formulas and parameters to assess their impact on accuracy.
+ Monitor User Feedback: Track user feedback after implementing any changes to the calorie tracking or features to gauge effectiveness and make further refinements.
Is there additional data you could use to expand on your findings?

Yes. The following additional datasets would be helpful:
User Demographics: Age, gender, height, weight, and fitness level to create personalized recommendations.
Heart Rate Data: This could provide a more accurate picture of activity intensity and calorie expenditure.
Sleep Data: Understanding sleep patterns could help uncover links between sleep, activity, and calorie burn.
Nutrition Data: Combining nutrition information with activity data could offer a more holistic view of user health and well-being.
Key Tasks (Completed)



# Top High-Level Insights:
Bellabeat's current calorie estimation model may not be accurate for all users and activity types.
Users are primarily engaging in light to moderate activities, with a significant amount of sedentary time.
There's a strong correlation between steps taken/active minutes and calories burned.
