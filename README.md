# Dublin Airbnb Data Analysis Dashboard
This repository contains a Tableau dashboard project that visualizes and analyzes Airbnb listings data for Dublin. The project aims to provide insights into Airbnb property trends, including geographic distribution, pricing, reviews, and revenue generation over time. The data is sourced from Inside Airbnb, a website that compiles publicly available data on Airbnb listings across various cities.

<h2> Data Source </h2>
The dataset used in this analysis was downloaded from [Inside Airbnb](https://insideairbnb.com/get-the-data.html). This dataset contains detailed information about Airbnb listings in Dublin, including fields such as:

- Listing ID
- Host Since Date
- Price
- Property Type
- Reviews
- Availability Calendar
- Location (Latitude/Longitude)

<h2> Data Connection and Structure </h2>
The dataset is structured across multiple tables: listings, calendar, and reviews, which were joined using the Listing ID to analyze price trends, availability, and review data across Dublin.

<h2> Dashboard Overview </h2>
The Tableau dashboard is divided into four key sections, each providing different insights into the Dublin Airbnb market:

<h3> Dublin Airbnb Geographic Data (Map) </h3>
- Description: A color-coded map displaying Airbnb listings based on Neighborhood Cleansed. Each point on the map represents a property listing, and the points are color-coded by neighborhood (e.g., Dublin City, Fingal, South Dublin, Dún Laoghaire-Rathdown).
- Filters: Users can filter by:
    - Property Type (e.g., Entire Home, Private Room)
    - Price Range (via a slider to set minimum and maximum prices)
    - Neighborhood (Color-coded regions)
  - Interaction: Clicking on a specific neighborhood dynamically filters the other graphs in the dashboard, allowing users to drill down into properties in specific areas.
<h3> Reviews Per Property Type (Bar Chart) </h3>
- Description: A bar chart that shows the number of reviews per property type. This visualization helps to identify the most popular types of properties in terms of user engagement.
- Details: The chart lists property types such as "Entire rental unit", "Private room in home", "Entire condo", and more, displaying the count of reviews for each type.
3. Average Price Over Time (Line Chart)
Description: A line chart depicting the average price of Airbnb listings over time, based on the Host Since year. It tracks pricing trends from 2009 to 2024.
Insights: Users can see how Airbnb pricing has fluctuated over the years, with notable dips and peaks during specific years.
4. Average Revenue Per Month (Line Chart)
Description: A line chart showing the Average Revenue Per Month for the year 2024.
Revenue Calculation:
The formula used to calculate revenue is:
makefile
Copy code
Revenue = Price * (365 - Availability_365)
This calculation estimates the revenue a host can generate based on their listing price and the number of days the property is available in a year.
Filters and Interactivity
The dashboard is designed with interactive filters that allow users to dynamically explore the data:

Property Type Filter: Allows users to select one or more property types (e.g., Entire home, Private room).
Price Range Slider: A slider to filter properties within a specific price range.
Neighborhood Cleansed Filter: Users can filter data by specific neighborhoods, which are color-coded and linked to the map visualization.
Dynamic Interaction
The map is fully interactive, allowing users to zoom in on specific areas of Dublin.
Filters are synchronized across all sheets in the dashboard, enabling users to apply filters (such as neighborhood and property type) globally.
Key Calculations Used
Average Revenue Per Month:

css
Copy code
Revenue = [Price] * (365 - [Availability 365])
This calculation estimates monthly revenue by multiplying the price by the total number of days booked (365 minus days available).

Average Price: The dashboard uses a simple aggregation of listing prices to compute average prices over time and across different dimensions like property type and neighborhood.

How to Use
Download the Dataset: If you want to replicate or extend the dashboard, you can download the data from Inside Airbnb.
Open the Tableau Dashboard: Open the .twb or .twbx file in Tableau to view and interact with the dashboard.
Explore the Visuals: Use the interactive filters to explore Airbnb data based on your interest (e.g., property types, neighborhoods, and price ranges).
Analyze Trends: Use the charts to analyze trends in average pricing, review counts, and revenue over time.
Conclusion
This Tableau project offers a comprehensive and interactive analysis of Airbnb listings in Dublin. By leveraging multiple data visualizations and filters, users can gain valuable insights into property trends, pricing, and revenue potential in the Airbnb market. The dashboard's dynamic interactivity provides an engaging way to explore various aspects of Airbnb listings across Dublin neighborhoods.

Additional Notes
This is a mini-project aimed at developing Tableau dashboarding skills for real-world datasets.
Please ensure that you have the latest version of Tableau Desktop to open the dashboard files provided in this repository.
