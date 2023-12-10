# Bike_Sharing_Demand_Prediction-Capstone_Project
Project Name - Bike Sharing Demand Prediction
Project Type - EDA/Regression
Contribution - Individual
Name- Pawan Kumar Singh
Project Summary -
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.
GitHub Link -
https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/blob/main/Bike_Sharing_Demand_Prediction_Capstone_ProjectML.ipynb
What all manipulations have you done and insights you found?
So we convert the "date" column into 3 different column i.e "year","month","day"
The "year" column in our data set is basically contain the 2 unique number contains the details of from 2017 december to 2018 november so if i consider this is a one year then we don't need the "year" column so we drop it.
The other column "day", it contains the details about the each day of the month, for our relevence we don't need each day of each month data but we need the data about, if a day is a weekday or a weekend so we convert it into this format and drop the "day" column
Rename the complex columns name
Changing the "Date" column into three "year","month","day" column
Convert 'Date' column to datetime format
Extract year, month, and day of the week
creating a new column of "weekdays_weekend" and drop the column "Date","day","year"
Drop 'Date', 'day', and 'year' columns
Change the int64 column into catagory column
assign the numerical columns of the DataFrame 'bike_df' to a variable,
summary of the manipulation code:

Extracting Year, Month, and Day:

You added three columns ('year', 'month', 'day') to the DataFrame 'bike_df'.
The 'year' column contains the year extracted from the 'Date' column using the 'dt.year' property.
The 'month' column contains the month extracted from the 'Date' column using the 'dt.month' property.
The 'day' column contains the day of the week (e.g., 'Sunday', 'Monday') extracted from the 'Date' column using the 'dt.day_name()' method.
Converting Date column to datetime format:

You used the 'apply()' function with a lambda function to convert the 'Date' column to a datetime format.
The lambda function utilized 'strptime()' from the 'datetime' module to parse each date string according to the format "%d/%m/%Y".
The resulting datetime objects were assigned back to the 'Date' column.
Determining Weekdays vs. Weekends:

You added a new column called 'weekdays_weekend' to the DataFrame 'bike_df'.
The values in the 'weekdays_weekend' column were determined using the 'apply()' function and a lambda function.
If the 'day' value was 'Saturday' or 'Sunday', the corresponding value in the 'weekdays_weekend' column was set to 1; otherwise, it was set to 0.
Dropping Columns:

You dropped the 'Date', 'day', and 'year' columns from the DataFrame 'bike_df' using the 'drop()' function.
The 'columns' parameter was used to specify the names of the columns to be dropped, and the 'axis' parameter was set to 1 to indicate column-wise operation.
Renaming Complex Column Names:

You renamed the complex column names in the DataFrame 'bike_df' to make them more analysis-ready.
The 'rename()' function was used with a dictionary mapping the current column names to the desired new column names.
The column names that were renamed included 'Rented Bike Count', 'Temperature(°C)', 'Humidity(%)', 'Wind speed (m/s)', 'Visibility (10m)', 'Dew point temperature(°C)', 'Solar Radiation (MJ/m2)', 'Rainfall(mm)', 'Snowfall (cm)', and 'Functioning Day'.
These manipulations demonstrate various data preprocessing steps, such as extracting date components, converting data types, creating derived features, and renaming columns.

![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/6084b0dc-3654-4ed9-91c4-fbcc8d08635f)
1. Why did you pick the specific chart?
The bar plot was chosen because it allows for a clear comparison of the count of rented bikes across different months. The categorical nature of the months is well-suited for representation on the x-axis, while the numerical count of rented bikes is represented on the y-axis. The use of different colors for each season aids in visual comparison. The bar plot enables the identification of any seasonal patterns or variations in bike rental demand and facilitates easy interpretation of the data. Overall, it is an effective and concise way to convey the count of rented bikes for each month and analyze trends over time.
2. What is/are the insight(s) found from the chart?
Seasonal Variations: The average count of rented bikes varies across seasons. Summer months (June, July, and August) have the highest average count, while winter months have relatively lower counts.

Monthly Variations: Within each season, there are variations in the average count of rented bikes across different months.

Winter Season: The winter season generally exhibits lower average counts of rented bikes, suggesting reduced demand during colder months.

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

The gained insights can positively impact the business by informing decisions related to seasonal demand planning, marketing strategies, and pricing. Understanding the seasonal and monthly variations in bike rental demand allows businesses to optimize resource allocation, target promotions effectively, and adjust pricing strategies. However, the lower average counts during the winter season may pose a temporary negative impact. Nonetheless, this insight can also present opportunities for diversification or focusing on alternative revenue streams during colder months. It is crucial for businesses to analyze these insights in their specific context to make informed decisions and drive positive business outcomes.
![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/0549e5eb-b6dd-4c45-963c-f81af5082007)
1. Why did you pick the specific chart?
The specific chart, a point plot with hue grouping, was chosen to visualize the count of rented bikes according to weekdays and weekends on an hourly basis. It allows for easy comparison between weekdays and weekends and provides a clear understanding of the distribution of bike counts throughout the day. The inclusion of percentage labels adds further context and insights to the chart. Overall, this chart effectively presents the desired information in a concise and visually appealing manner.

2. What is/are the insight(s) found from the chart?
The insights from the chart indicate that bike rental counts vary throughout the day. Weekdays show higher rental counts during peak commuting hours, while weekends have higher counts in the afternoon and early evening. The highest average counts are observed on weekday evenings and weekend afternoons. These insights suggest different usage patterns between weekdays and weekends and can inform resource planning and marketing strategies.

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

The insights gained from the data can have a positive impact on the business by optimizing operations and resource allocation. Understanding peak demand periods allows businesses to improve customer satisfaction and revenue. However, insights showing consistently low rental counts during certain hours may indicate a need to attract customers during off-peak times to avoid negative growth. Overall, leveraging these insights helps businesses make informed decisions to drive positive business outcomes.
![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/95ad3cec-5492-4ed2-b48a-44e972a06e82)
1. Why did you pick the specific chart?
The specific chart, a boxplot, was chosen to visualize the count of rented bikes according to seasons because it effectively displays the distribution of the data and provides insights into the variability and central tendency of the rented bike counts across different seasons. The boxplot allows for easy comparison between seasons, showing the median, quartiles, and potential outliers. It also helps identify any seasonal patterns or differences in the rented bike counts. Overall, the boxplot is a suitable choice for understanding the distribution and variability of the data across different seasons.

2. What is/are the insight(s) found from the chart?
The insights from the chart are:

There is variation in rented bike counts across different seasons.
Summer has the highest bike rental demand.
Winter has the lowest bike rental demand.
These insights highlight the seasonal trends and can guide businesses in resource allocation and planning to meet customer demand effectively.

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

The gained insights can help create a positive business impact. By understanding the seasonal variation in rented bike counts, businesses can strategically allocate resources and tailor their marketing efforts to capitalize on the peak demand during summer and other high-demand seasons. This can lead to increased customer satisfaction, improved operational efficiency, and potentially higher revenue.

There are no insights from the chart that directly indicate negative growth. However, the lower bike rental demand during winter may pose a challenge for businesses during that season. They may need to implement alternative strategies such as offering discounts, promoting indoor activities, or diversifying their services to mitigate any potential negative impact on business growth.
![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/f1c2695f-b64f-40a2-ad5e-659104c497a5)
1. Why did you pick the specific chart?
The specific chart, a scatter plot, was chosen to visualize the relationship between the "Rented_Bike_Count" and "Snowfall" variables. Scatter plots are effective in showing the distribution of data points and any potential patterns or trends between two numerical variables. In this case, the scatter plot allows us to examine how the rented bike count varies with different levels of snowfall. By plotting the "Rented_Bike_Count" on the y-axis and "Snowfall" on the x-axis, we can observe any potential correlation or relationship between these two variables.

2. What is/are the insight(s) found from the chart?
The insight from the scatter plot chart is that there appears to be a mixed relationship between the "Rented_Bike_Count" and "Snowfall" variables.

For low to moderate levels of snowfall (0-2.5), the rented bike count tends to be relatively high, indicating that people still use bikes for transportation despite the presence of snow.
However, as the snowfall increases beyond 2.5, the rented bike count starts to decrease, suggesting that severe snowfall has a negative impact on bike usage.
There are also some instances of higher rented bike counts at specific snowfall levels, such as at 0.6, 1.1, and 3.6, which may indicate unique factors or variations in customer behavior.
Overall, the scatter plot highlights the complex relationship between snowfall and bike rentals, showing a mix of positive and negative impacts depending on the level of snowfall.

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

The gained insights from the scatter plot can potentially help create a positive business impact.

Positive Impact:

The insight that bike rentals remain relatively high during low to moderate levels of snowfall suggests that businesses can promote biking as a viable transportation option even in winter conditions. This can lead to increased revenue and customer engagement.
Negative Impact:

The insight that severe snowfall leads to a decrease in bike rentals indicates a potential negative impact on business growth during extreme weather conditions. In such situations, it may be challenging to attract customers and maintain regular bike rental activities.
To mitigate the negative impact, businesses can focus on alternative services or promotions during periods of heavy snowfall, such as offering indoor cycling classes or maintenance services. By diversifying their offerings and adapting to changing weather conditions, businesses can minimize the negative effects and maintain a positive business impact overall.
![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/b26c59a2-9900-47f1-bf22-ada5d281b685)
1. Why did you pick the specific chart?
A scatter plot was chosen because it is a common and effective way to visualize the relationship between two continuous variables and observe patterns, dispersion, and outliers in the data.

2. What is/are the insight(s) found from the chart?
at temperature 20 to 30 rente demand is high

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

the gainded insight of incresed rental demand when the temperature is between 20 to 30 can potentially create a positive business impact. it allow businesses to optimize opertions and resources during periods of high demand. however , negative growth can occur due to factors such as extrme temperatures change customer preferncess. a comprehesive analysis considering various is nacessary to understande the spesific reasone for negative growth.
![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/94754a5e-f96e-4bf6-ba30-d0cbb582b461)
1. Why did you pick the specific chart?
The line plot was chosen for the relationship between 'Solar_Radiation' and 'Rented_Bike_Count' because it effectively displays the continuous relationship between the variables, allows for visualizing trends over time, and showcases the quantitative representation of the data. Additionally, the line plot connects the data points, highlighting the continuity and direction of the relationship.

2. What is/are the insight(s) found from the chart?
solar rediation show positive correlation with ranta count but correlation is very week.

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

solar radiation is highly fltuating value The gained insight of a weak positive correlation between 'Solar_Radiation' and 'Rented_Bike_Count' may have limited impact in creating a positive business impact. It is essential to consider additional factors and insights to drive significant improvements. No specific insights were identified that would directly lead to negative growth. but people like sunny days.
![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/69dbdae7-8ef0-407f-b30f-1b89feddb88d)

1. Why did you pick the specific chart?
The specific chart, an area plot, was chosen to visualize the relationship between 'Wind_speed' and the average 'Rented_Bike_Count'. It was selected because it effectively represents the continuous data, allows for comparison and assessment of magnitude, shows the distribution of the average bike count, and provides visual appeal.

2. What is/are the insight(s) found from the chart?
Distribution of Average Rented Bike Count: positive distribution approx 6

Trends or Patterns: rented bike count is highr between .5 to 4

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

Based on the insights gained from the area plot, the relationship between wind speed and the average rented bike count indicates potential opportunities for creating a positive business impact. The higher bike demand observed within the wind speed range of 0.5 to 4 suggests that focusing on promoting bike rentals during these moderate wind conditions could lead to increased customer demand and potentially generate positive business outcomes.

Regarding insights that may lead to negative growth, based on the provided information, there are no specific insights that directly suggest negative growth. However, it's important to consider that the analysis is based on the relationship between wind speed and bike count, and there may be other factors and considerations that could impact business outcomes. It's recommended to conduct a comprehensive analysis that incorporates multiple variables and factors to better assess potential negative impacts or risks to business growth.
![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/7b76e93e-901f-4c53-a00b-dceb8b7abb2f)
1. Why did you pick the specific chart?
The specific chart, a scatter plot with regression lines, was chosen because it allows for visualizing the relationship between numerical features and the 'Rented_Bike_Count'. It helps in understanding the correlation or pattern between these variables and facilitates comparisons among different features. The inclusion of regression lines provides an estimate of the overall trend.

2. What is/are the insight(s) found from the chart?
Positive correlations:

Temperature, wind speed, visibility, and solar radiation are positively correlated with the number of rented bikes.

Negative correlations:

Rainfall, snowfall, and humidity are negatively correlated with the number of rented bikes.

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

the gained insights regarding the positive correlations between temperature, wind speed, visibility, and solar radiation with the number of rented bikes can help create a positive business impact. These insights allow businesses to identify favorable conditions for bike rentals and tailor their strategies accordingly, resulting in increased revenue and customer satisfaction.

On the other hand, the insights indicating negative correlations between rainfall, snowfall, and humidity with the number of rented bikes can lead to negative growth. During periods of unfavorable weather, bike rental demand may decrease, impacting business growth negatively.

In summary, the gained insights have the potential to create a positive business impact by capitalizing on favorable conditions and mitigating the negative impact of unfavorable weather conditions on bike rental demand.
![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/183291c7-af24-4361-9a4a-0892f0f1e31c)
1. Why did you pick the specific chart?
The distribution plots were chosen because they provide a visual representation of the distribution of values for each numerical column in the dataset. This helps in understanding the range, shape, and central tendency of the data, allowing for insights into the overall characteristics of the variables.

2. What is/are the insight(s) found from the chart?
The rented bike count, wind speed, solar radiation, rainfall, and snowfall are left-skewed data, while temperature, humidity, and visibility have normal distributions.

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

The gained insights have the potential to create a positive business impact by leveraging optimal weather conditions (temperature, humidity) and adjusting strategies based on solar radiation. However, the left-skewed distribution of rented bike count indicates the presence of limiting factors that may lead to negative growth. Businesses need to address these factors to mitigate their impact and stimulate demand for bike rentals.

1. Why did you pick the specific chart?
The specific chart of a box plot was chosen to visually compare the distribution of the "Rented_Bike_Count" across different categories of the categorical variables. It allows for easy comparison, identification of outliers, and understanding of the central tendency and spread within each category.

2. What is/are the insight(s) found from the chart?
The insights from the box plots suggest that:

Hour: There is one outlier at x=2 and y=1300, indicating a high bike rental count at that hour.
Seasons: Summer has the highest bike demand among the four seasons.
Holiday: Non-holiday periods have higher bike demand compared to holidays.
Functioning Day: "Yes" (functioning day) has more data points and outliers, indicating higher bike demand compared to "No" (non-functioning day).
Outliers: There are outliers present in each category, suggesting variations in bike rental counts within each category.
3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

Yes, the gained insights can potentially create a positive business impact by allowing businesses to understand and cater to the high demand during summer seasons, non-holiday periods, and functioning days. However, the presence of outliers suggests the need for further investigation to address any potential negative growth factors and ensure a positive customer experience.
1. Why did you pick the specific chart?
The specific line plot with multiple categorical variables over time was chosen to examine trends and patterns in the scaled rented bike count across different categories and understand the factors that influence bike rental demand.

2. What is/are the insight(s) found from the chart?
The insights gained from the plot indicate that all seasons exhibit similar time patterns in terms of bike rental demand. Specifically, there is a higher demand for bikes during the hours of 5 to 10 and 16 to 20.

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

The gained insights, such as the identified time patterns and trends, can help businesses create a positive impact by enabling them to allocate resources more efficiently and optimize their operations. By understanding the high-demand periods during weekdays and the lower demand on weekends, businesses can adjust their staffing, bike availability, and marketing strategies accordingly. However, neglecting the lower demand on weekends without appropriate strategies to stimulate demand could lead to negative growth in terms of lower utilization rates and potential revenue loss. It is crucial for businesses to consider these insights and implement appropriate measures to address the weekend demand and ensure a positive business impact overall.
![image](https://github.com/Pawanme9034/Bike_Sharing_Demand_Prediction-Capstone_Project/assets/122411441/7f8bfa7e-775d-443d-b799-b7b693e36ff8)
1. Why did you pick the specific chart?
The line plot was chosen to visually analyze the relationship between the scaled numerical features and the scaled rented bike count. It allows for a clear comparison and interpretation of the impact of each feature on the bike count.

2. What is/are the insight(s) found from the chart?
when scale the data, the line plot shows patterns in the relationship between the scaled numerical features and the scaled rented bike count. From the plot, observe that:

The demand for rented bikes is high when the humidity is between 0.0 and 0.1.
The demand for rented bikes is higher when the wind speed is between 0.2 and 0.5.
The demand for rented bikes is higher when the snowfall is between 0.0 and 0.4.
The demand for rented bikes is higher when the temperature is between 0.5 and 0.9.
These patterns suggest that these specific ranges of values for these features have a positive impact on the rented bike count.

3. Will the gained insights help creating a positive business impact?
Are there any insights that lead to negative growth? Justify with specific reason.

Yes, the gained insights can help create a positive business impact by identifying ranges of humidity, wind speed, snowfall, and temperature that are associated with higher bike demand. However, there are no specific insights indicating negative growth in the data analyzed.
1. Why did you pick the specific chart?
The correlation matrix heatmap is selected because it provides a clear and concise visual representation of the correlations between variables in the dataset. It allows for quick identification of the strength and direction of the relationships, making it an effective tool for understanding the interdependencies among the variables.

2. What is/are the insight(s) found from the chart?
The "Rented_Bike_Count" shows a positive correlation with "Temperature", "Dew_point_temperature", and "Solar_Radiation". This means that as these variables increase, the demand for rented bikes tends to increase.

On the other hand, there is a negative correlation between "Rented_Bike_Count" and "Humidity", "Rainfall", and "Snowfall". This implies that as humidity, rainfall, and snowfall increase, the demand for rented bikes tends to decrease.

The variables "Wind_speed" and "Visibility" have relatively weaker correlations with "Rented_Bike_Count".

These insights can help businesses understand the factors that affect bike rental demand and make data-driven decisions to create a positive business impact.
![Uploading image.png…]()
1. Why did you pick the specific chart?
The pairplot allows us to visualize the relationships between different numerical variables in the dataset, with each plot showing the relationship between two variables. The "hue" parameter is set to "Seasons" to differentiate the data points based on the seasons.

By using the pairplot, we can gain insights into the relationships and distributions of variables across different seasons. The diagonal plots represent the distributions of individual variables, while the off-diagonal plots show the scatter plots of variable pairs.

2. What is/are the insight(s) found from the chart?
From the pairplot chart, we can derive several insights:

Temperature and Rented_Bike_Count: There is a positive correlation between temperature and the number of rented bikes. As temperature increases, the bike count tends to increase as well.

Humidity and Rented_Bike_Count: There appears to be a negative correlation between humidity and the number of rented bikes. Higher humidity levels are associated with slightly lower bike counts.

Wind_speed and Rented_Bike_Count: There seems to be a weak positive correlation between wind speed and the number of rented bikes. Higher wind speeds are generally associated with slightly higher bike counts.

Visibility and Rented_Bike_Count: There is a positive correlation between visibility and the number of rented bikes. As visibility increases, the bike count tends to increase as well.

Dew_point_temperature and Rented_Bike_Count: There is a positive correlation between dew point temperature and the number of rented bikes. Higher dew point temperatures are associated with higher bike counts.

Solar_Radiation and Rented_Bike_Count: There is a positive correlation between solar radiation and the number of rented bikes. Higher levels of solar radiation are associated with higher bike counts.

Rainfall and Rented_Bike_Count: There appears to be a weak negative correlation between rainfall and the number of rented bikes. Higher rainfall amounts are associated with slightly lower bike counts.

Snowfall and Rented_Bike_Count: There seems to be a weak negative correlation between snowfall and the number of rented bikes. Higher snowfall amounts are generally associated with slightly lower bike counts.

These insights suggest that weather-related factors such as temperature, humidity, wind speed, visibility, dew point temperature, solar radiation, rainfall, and snowfall have some influence on the demand for rented bikes. Businesses can consider these factors when making operational decisions, such as bike availability, pricing, and marketing strategies, to optimize bike rentals and cater to customer preferences based on weather conditions.

Conclusion
In conclusion, data visualization and exploratory data analysis play a crucial role in understanding and gaining insights from datasets. By using various charts and visualizations, we can analyze the distribution of variables, identify patterns, detect outliers, explore relationships between variables, and uncover trends or correlations.

These insights can have a positive impact on businesses by providing valuable information for decision-making, strategy formulation, and optimization. For example, understanding the factors that influence bike rental demand can help businesses optimize their inventory, pricing, and marketing strategies to meet customer needs and maximize revenue. Identifying negative growth factors can also guide businesses in mitigating risks, addressing issues, and improving their offerings.

Additionally, model evaluation metrics and feature importance analysis can aid in assessing the performance and interpretability of machine learning models. Metrics such as mean squared error (MSE), root mean squared error (RMSE), mean absolute error (MAE), and R-squared (R2) can provide insights into the accuracy and predictive power of the models. Feature importance analysis helps in identifying the most influential features that contribute to model predictions, allowing businesses to prioritize resources and focus on the most impactful variables.
