Unique Prompts:

“Please identify the top 3 growth KPIs for the business (e.g., 90-day revenue trend, repeat purchase rate, average order value). Compute the output using SQL strings, similar to labs 1 and 2. The results should be stored in a pandas dataframe.”

“Please use CTEs and window functions to compute trends and MoM/YoY growth for at least one KPI. Show me the MoM and YoY for orders as well.” 

“Please explain what the MoM and YoY for the revenue in the output indicate. How can this metric be valuable for the business?”

“Please explain what the MoM and YoY for the orders in the output indicate. How can this metric be valuable for the business?”

“Please conduct a deep dive into one product category and one customer segment. Show me something unique that has not been previously explored in the dataset.”

“Please use AI-assisted SQL to explore drivers (discounts, marketing channel if available, region, device). Conduct this analysis on the accessories product category picked in the previous prompt, and total items and orders by traffic source and region.”

“Please Cross-check at least two AI-generated insights with alternative queries or counterexamples. Also, show at least one case where the first answer was misleading and how you corrected it. You can use the SQL string error code for the 90-day average revenue trend.”

“In the validation section, what and how does the price_comparison_df and revenue_by_region_df help validate?”

“Please use Plotly to generate one interactive chart and other visualizations such as a Scorecard: revenue (or profit), last 30 days, Pie/Donut: sales % by region or channel, and Bar: top 5 products/categories.”

“Please generate the codes to export the dataframes that you used to build the Plotly visualizations into CSV files for Looker Studio Dashboard creation.”

“Please generate 1-2 specific recommendations using the strategist pattern based on the analysis conducted so far in the discover, investigate, and validate phases. Think from an advanced Business Analyst’s perspective and make the recommendations detailed.”

NYC Citibike Prompts:

"Act as a senior BigQuery analyst. Produce a single runnable BigQuery SQL (no commentary) for: Task: Analyze how trip duration varies by user type (Subscriber vs Customer). Table: bigquery-public-data.new_york_citibike.citibike_trips Output: Average, median, and count of trips by usertype Filter: Exclude null or zero trip durations Sort: Average trip duration in descending order Add: LIMIT 100 to control cost during exploration."

"Act as a senior BigQuery analyst. Produce a single runnable BigQuery SQL (no commentary) for: Task: Identify the most popular start and end stations, and examine how popularity changes by time of day and day of the week. Table: bigquery-public-data.new_york_citibike.citibike_trips Output: Start station, end station, hour of day, day of week, and trip count Filter: Exclude null station names Sort: By trip count in descending order Add: LIMIT 100 to control cost during exploration."

"Act as a senior BigQuery analyst. Produce a single runnable BigQuery SQL (no commentary) for: Task: Determine whether there is a significant difference in the average trip duration between weekdays and weekends. Table: bigquery-public-data.new_york_citibike.citibike_trips Logic: Extract the day of the week from starttime. Categorize each trip as ‘Weekday’ (Monday–Friday) or ‘Weekend’ (Saturday–Sunday). Output: Category (Weekday/Weekend), average trip duration, total trips. Filter: Exclude null or zero tripduration values. Sort: Average trip duration in descending order. Add: LIMIT 100 to control cost during exploration."

2 “fail then fix” examples: 

“The 90-day-average revenue trend, using the SQL string method, has been giving me an error. Show me the output using pandas calculation. The final output should be a dataframe.” 

“For the repeat purchase rate, please also include the total number of users and the number of repeat users, along with the repeat purchase rate calculated. Show all these values in a dataframe.” 

NYC Citibikes "fail then fix" examples:

"Refine the query to exclude null start_station_name and end_station_name values and remove any aggregated “total trips” rows so only valid station pairs with real trip counts appear."

"Update the query to use window functions like ROW_NUMBER() or RANK() to keep only the top record per station-hour-day group and remove duplicate or repeated station entries."

