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
  
  Wearable technology is becoming more affordable and specialized, catering to the diverse needs of users across different demographics and health conditions.
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Using the Fitbit Dataset I got off Kaggle I noticed a few things.
- Item 1 Calories Burned in an Hour
  I just wanted to see the frequency of how people are burning calories in an hour. This type of data can be marketable. Just to learn more about ggplot2. Here's the code I used in R-Studio.
-----------------------------------------------------------------------------------------------------------------------------------------------------------
+ ggplot(hourlyCalories_merged, aes(x = Calories)) +
+   geom_histogram(binwidth = 50, fill = "skyblue", color = "black") +
+    labs(title = "Distribution of Calories Burned per Hour",
+    x = "Calories Burned",
+   y = "Frequency") +
+    theme_minimal()
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Here's what the plot looks like.
![CaloriesBurnedperHourFitbit](https://github.com/marcaldana/analysis/assets/72458759/35603e81-616d-4fa2-8b8b-36521d765a55)
 
Here you can see most people burn around up to 500 calories in an hour.

Here's a relationship between steps and calories using this code in R-Studio.
-----------------------------------------------------------------------------------------------------------------------------------------------------------
library(ggplot2)

+ Convert 'ActivityDate' to date format if needed (assuming MM/DD/YYYY)

+  dailyActivity_merged$ActivityDate <- as.Date(dailyActivity_merged$ActivityDate, "%m/%d/%Y")
+  ggplot(dailyActivity_merged, aes(x = TotalSteps, y = Calories)) +
+  geom_point(alpha = 0.7, color = "blue") +  # Scatterplot with transparency
+  geom_smooth(method = "lm", se = FALSE, color = "red") +   # Add a linear regression line
+  labs(title = "Relationship Between Total Steps and Calories Burned",
+  x = "Total Steps",
+  y = "Calories Burned") +
+  theme_minimal()
-----------------------------------------------------------------------------------------------------------------------------------------------------------
  Here is a visualization of the code to understand it more. 

  ![TotalSteps_CalorieBurned](https://github.com/marcaldana/analysis/assets/72458759/066c716f-b48e-4320-a031-36ea411582f4)
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

1. Where is your data stored?

The primary data is stored in the Fitbit Fitness Tracker Data dataset on Kaggle. It's available under the CC0: Public Domain license, meaning it's free to use for any purpose.
You can access the dataset here: https://www.kaggle.com/datasets/arashnic/fitbit
It's important to note that this dataset was collected through Mobius, and Fitbit users consented to share their anonymized data.
2. How is the data organized? Is it in a long or wide format?

The Fitbit dataset is comprised of 18 CSV files, each focusing on different aspects of user activity, such as daily activity summaries, sleep data, weight logs, etc.
The files are generally in wide format, with each row representing a single user and columns representing different variables or time points.
For analysis using tools like R and its tidyverse, we'll likely need to reshape some of the data into a long format for easier manipulation and visualization.
3. Are there issues with bias or credibility in this data? Does your data ROCCC?

Bias:
Self-selection bias: The dataset is based on voluntary participation from Fitbit users, so it may not be representative of the entire population or all wearable device users. Users who are more health-conscious or active might be overrepresented.
Device-specific bias: The data is limited to Fitbit users, so it may not reflect the usage patterns or behaviors of users with other brands of wearables.
ROCCC:
Reliable: The data comes from a reputable source (Fitbit) and was collected with user consent. However, potential biases should be acknowledged.
Original: The dataset is original, primary data collected directly from Fitbit devices.
Comprehensive: It includes a wide range of activity and health metrics, making it fairly comprehensive for this analysis.
Current: The dataset was collected in 2016, so it might not reflect the latest trends in wearable technology usage.
Cited: The data source (Mobius) and licensing (CC0) are clearly stated.
4. How are you addressing licensing, privacy, security, and accessibility?

Licensing: The dataset is in the public domain (CC0), allowing free use without restriction.
Privacy: The data is anonymized, ensuring that individual users cannot be identified.
Security: Since the data is already public, security is not a major concern in this context. However, if you were to combine this data with other sources, additional security measures might be needed.
Accessibility: The dataset is readily accessible on Kaggle, making it easy for others to use and replicate the analysis.
5. How did you verify the data’s integrity?

Data Cleaning: Preliminary checks would involve:
Handling missing values: Identify and decide on how to deal with missing entries.
Identifying and addressing outliers: Extreme values could be errors or genuine but might need special handling.
Checking for inconsistencies: Verify that data types are correct and values are within expected ranges.
6. How does it help you answer your question?

The Fitbit dataset directly addresses the business task by providing insights into:
Feature Usage: We can analyze which features are most frequently used by Fitbit users to inform Bellabeat's product development decisions.
User Engagement: We can examine usage patterns over time to understand how users interact with the device and identify potential areas for improvement in Bellabeat's app or device interface.
Health Trends: Analyzing the health metrics (steps, heart rate, sleep) can reveal insights into user behavior and health outcomes that can inform Bellabeat's marketing and messaging strategies.
7. Are there any problems with the data?

Limitations:
Limited Demographic Information: The dataset lacks detailed demographic information about the users (age, gender, location), which could limit the ability to segment users and tailor recommendations.
Potentially Outdated: The data is from 2016 and might not fully reflect current user behaviors or the latest features in wearable technology.
Fitbit-Specific: The data only represents Fitbit users, which might not generalize to Bellabeat's target audience.
Addressing these limitations could involve:

Supplementing with Additional Data: Look for other public datasets or research on wearable device usage to gain a broader perspective.
Conducting Surveys/Interviews: Collect additional data from Bellabeat users to understand their specific needs and preferences.
