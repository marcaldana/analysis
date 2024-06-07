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

1. Ask Phase

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

-----------------------------------------------------------------------------------------------------------------------------------------------------------
  
# 2. How could these trends apply to Bellabeat customers?

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

Case Study Roadmap - Prepare

Guiding Questions:

+ Where is your data stored?
Both datasets are stored on Kaggle:
Fitbit Fitness Tracker Data: https://www.kaggle.com/datasets/arashnic/fitbit
Calories Burned During Exercise and Activities: https://www.kaggle.com/datasets/aadhavvignesh/calories-burned-during-exercise-and-activities
+ How is the data organized? Is it in a long or wide format?
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
+ How are you addressing licensing, privacy, security, and accessibility?
+ Licensing: Both datasets are under CC0: Public Domain licenses, allowing for unrestricted use.
+ Privacy: Fitbit data is anonymized, protecting user identities. The "Calories Burned" dataset does not contain personal information.
+ Security: Since both datasets are public, security concerns are minimal.
+ Accessibility: Both datasets are readily available on Kaggle.
+ How did you verify the data’s integrity?
+ Initial Data Checks: Both datasets will undergo the following:
+ Handling missing values: Identify and decide on the appropriate method (e.g., removal, imputation).
+ Checking for outliers: Examine extreme values and assess if they are errors or genuine data points.
+ Correcting inconsistencies: Ensure data types are consistent (e.g., dates, numeric values) and values are within expected ranges.
+ How does it help you answer your question?
Fitbit Data: Provides real-world insights into how users interact with wearable devices, their activity patterns, and health metrics, which can inform Bellabeat's product development and marketing strategies.
Calories Burned Data: Offers a reference point for understanding the relationship between different activities and calorie expenditure, helping Bellabeat refine its calorie tracking algorithms and personalize recommendations.
+ Are there any problems with the data?
Yes, both datasets have limitations (see point 3). These limitations will be addressed by:
Acknowledging biases and potential inaccuracies in the analysis.
Supplementing with additional research or data (if possible) to gain a more comprehensive understanding.
Focusing on patterns and trends rather than absolute values, given the potential limitations of the datasets.
Key Tasks:



