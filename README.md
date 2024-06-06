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
1. Ask Phase

Sršen asks you to analyze smart device usage data to gain insight into how consumers use non-Bellabeat smart
devices. She then wants you to select one Bellabeat product to apply these insights to in your presentation. These questions
will guide your analysis:


1. What are some trends in smart device usage?
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

