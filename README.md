## Business Problem
### Swiggy Restaurant Analysis - Kaggle Dataset

1. **Restaurant Performance**: Identify trends in ratings and pricing to help restaurants improve their offerings.
2. **Pricing Strategy**: Analyze how pricing affects ratings to guide restaurant owners in setting competitive prices.
3. **Food Type Popularity**: Understand regional food preferences to help Swiggy and restaurants tailor their menus.
4. **Customer Satisfaction Drivers**: Explore factors that influence customer ratings, like price and service quality.

This Jupyter Notebook contains an analysis of a **Swiggy Restaurant Dataset** to explore and gain insights into restaurant performance on Swiggy. The dataset includes multiple features like price, ratings, food types, area, and more. Through this analysis, various patterns, correlations, and trends within the data are identified.

## 1. **Overview of the Notebook**
   - The notebook starts with importing necessary libraries: `pandas`, `numpy`, `plotly`, `matplotlib`, and `seaborn`, which are used for data analysis and visualization.
   - The dataset is loaded from a CSV file named `swiggy.csv`, which contains data on different Swiggy restaurants.

## 2. **Data Inspection and Cleaning**
   - **Basic Data Information**: The dataset is first examined using `df.info()` to understand its structure (number of rows, columns, and data types).
   - **Missing Values**: We check for missing values in the dataset with `isnull().sum()`. Missing data is then handled either by filling or dropping them, as per the analysis requirements.
   - **Duplicates**: Duplicate rows are identified and removed by checking `df.duplicated().sum()`.

## 3. **Data Overview**
   - **First Rows**: The first few rows of the dataset are displayed using `df.head()` to get a sense of the data.
   - **Missing Values After Cleaning**: After cleaning the data, we check again for any remaining missing values.
   - **Dataset Size**: We print the number of records and columns to understand the dataset’s size.

## 4. **Data Analysis**
   - **Price Range Distribution**: We create a pie chart to visualize the distribution of restaurants across different price ranges, helping us understand the general pricing trends on Swiggy.
   - **Top 10 Areas with Most Restaurants**: A bar chart is created to show the areas with the highest number of Swiggy restaurants.
   - **Most Popular Food Types by City**: A bar chart is plotted to show the most popular food types in various cities. This helps identify trends in consumer preferences across different regions.
   - **Rating Distribution**: A pie chart displays the distribution of restaurant ratings. We segment the ratings into those above 4.5 and those below to highlight top-rated restaurants.
   - **Price Distribution**: A histogram is used to explore the distribution of restaurant prices, with a red color scheme to emphasize the visualization.

## 5. **Correlation Analysis**
   - **Correlation Matrix**: We generate a heatmap to visualize the correlation between numeric features like `Price`, `Avg ratings`, and others. This helps in understanding the relationships between various restaurant features and their ratings.

## 6. **Price vs Average Rating**
   - A scatter plot is created to explore the relationship between restaurant prices and their average ratings. The scatter plot helps in understanding whether higher-priced restaurants tend to have better or worse ratings.

## Key Insights:
- **Top-Rated Restaurants**: A substantial percentage of restaurants have ratings above 4.5, indicating customer satisfaction is generally high.
- **Price Distribution**: The price distribution indicates that there are a range of affordable and expensive restaurants.
- **Food Preferences by City**: Some cities have distinct food preferences, which can be beneficial for restaurant owners and Swiggy for marketing and inventory decisions.
- **Price and Rating Correlation**: The scatter plot suggests that while higher prices don’t necessarily guarantee better ratings, they may correlate with certain food types or specific market segments.

## Dataset Details:
This dataset is sourced from Kaggle and includes the following key features:
- `ID`: Unique identifier for the restaurant.
- `Name`: Restaurant name.
- `City`: City where the restaurant is located.
- `Area`: Area of the city where the restaurant is located.
- `Price`: Price range of the restaurant.
- `Food type`: Type of food served by the restaurant (e.g., Indian, Chinese, Italian).
- `Avg ratings`: Average ratings from customers (on a scale of 1-5).
- `Reviews`: Number of reviews received by the restaurant.
- `Delivery time`: Average delivery time for the restaurant (if available).
