# EDA-Project-Airbnb-Market-Trends-main
EDA-Project-Airbnb-Market-Trends-main SMIT assignments'

Introduction
As a consultant working for a real estate start-up, you have collected Airbnb listing data from various sources to investigate the short-term rental market in New York. This assignment focuses on analyzing this data to provide insights to your client. The goal is to use exploratory data analysis (EDA) techniques to extract meaningful trends, perform data transformations, and visualize findings effectively.
Files Available in the data Folder
1.	airbnb_price.csv: Contains data on Airbnb listing prices and locations.
o	listing_id: Unique identifier of the listing.
o	price: Nightly listing price in USD.
o	nbhood_full: Name of borough and neighborhood where the listing is located.
2.	airbnb_room_type.xlsx: Contains data on listing descriptions and room types.
o	listing_id: Unique identifier of the listing.
o	description: Listing description.
o	room_type: Type of room (shared room, private room, entire home/apartment).
3.	airbnb_last_review.tsv: Contains data on Airbnb host names and review dates.
o	listing_id: Unique identifier of the listing.
o	host_name: Name of the listing host.
o	last_review: Date when the listing was last reviewed.
________________________________________
Assignment Guidelines
This assignment is open-ended, meaning you can refer to internet resources, documentation, and tutorials for assistance. However, for each solution, you must include 2 to 3 sentences of justification or reasoning explaining:
•	How you arrived at the solution.
•	What steps you took to achieve the solution.
Additionally:
•	Your submission file should include all steps in the process, not just the final answer. Each question should have a complete code workflow.
•	Visualization questions require well-labeled and aesthetically pleasing charts.
________________________________________
Questions
Basic Analysis
1.	Dates of Reviews
o	What are the dates of the earliest and most recent reviews?
	Store these values as two separate variables, earliest_review and most_recent_review.
2.	Private Room Listings
o	How many of the listings are private rooms?
	Save this count into a variable called nb_private_rooms.
3.	Average Price Calculation
o	What is the average listing price?
	Round to the nearest two decimal places and store it in a variable called avg_price.
4.	Summary Table
o	Combine the calculated values into a new DataFrame called review_dates with the following columns (in order): first_reviewed, last_reviewed, nb_private_rooms, and avg_price. The DataFrame should contain only one row of values.
________________________________________
Intermediate Analysis
5.	Neighborhood Trends
o	Which neighborhoods have the highest and lowest average listing prices?
	Create a DataFrame with columns neighborhood, average_price, and number_of_listings for the top 5 most expensive neighborhoods.
6.	Word Analysis in Descriptions
o	Find the top 10 most frequently used words in the description column (excluding stopwords like "the," "and," etc.).
	Use pandas.Series.str.split and explore the Counter class from the collections module.
________________________________________
Advanced Analysis
7.	Room Type Comparison
o	Compare the average prices for each room_type (shared rooms, private rooms, entire homes/apartments).
	Create a bar chart visualizing the differences.
8.	Trend Over Time
o	Analyze the number of reviews over time for all listings.
	Plot a line graph showing the trend of reviews per month over the years. (Hint: Use pandas.to_datetime and groupby.)
9.	Exploring Unique Matplotlib Functions
o	Create a scatter plot with a regression line showing the relationship between price and the length of the description.
	Use matplotlib.axes.Axes.annotate to highlight outliers in the graph. (Note: Students should explore this function independently.)
10.	Exploring Unique Seaborn Functions
o	Generate a strip plot for prices grouped by room_type using the hue parameter to distinguish neighborhoods.
	Students should explore the seaborn.stripplot function.
________________________________________
Visualization Questions
11.	Bar Chart
o	Create a bar chart showing the count of listings for each room type.
	Add proper labels, titles, and a legend.
12.	Heatmap
o	Generate a heatmap to show the correlation (if any) between listing price and the frequency of reviews.
	Use the sns.heatmap function.
o	Pie Chart
o	Create a pie chart to visualize the proportion of room types available.
	Use a custom color palette and annotate the chart with percentages.
13.	Histogram
o	Plot a histogram showing the distribution of listing prices.
	Use bins to group prices in increments of $50.
14.	Violin Plot
o	Create a violin plot to compare price distributions across neighborhoods.
________________________________________
Submission Requirements
•	Your notebook should include:
i.	Step-by-step solutions for each question.
ii.	Explanations for each solution in 2-3 sentences.
iii.	Properly labeled graphs and visualizations.
•	Ensure all code cells are executed, and the outputs are visible.
•	Submit the .ipynb file with the name format: EDA_Project1_<YourName>.ipynb.
________________________________________
Bonus Questions
1.	Outlier Detection
o	Identify listings with unusually high prices (outliers) using the interquartile range (IQR) method.
	Highlight these listings in a scatter plot.
2.	Interactive Visualization
o	Explore plotly or altair to create an interactive visualization for price trends by neighborhood.
	Include tooltips to display additional information such as room_type and description.
