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
