# Queensland Fuel Price Data Analysis Project

## Project Overview

This project is focused on analyzing fuel prices in Queensland, Australia, and examining the relationships between fuel prices, crude oil prices, and Terminal Gate Pricing (TGP). The analysis aims to provide insights into price trends, site and brand distribution, and real-time snapshots of fuel prices, with visualizations including maps and charts.

## Data Sources

1. **Queensland Fuel Price Data (2024)**
   - Source: [Queensland Government Open Data Portal](https://www.data.qld.gov.au/dataset/fuel-price-reporting-2024)
   - This dataset provides real-time and historical fuel price data for various fuel types across Queensland. The data includes details such as site information, fuel type, prices, and geographic location.

2. **Crude Oil Prices**
   - Source: [Investing.com Crude Oil Historical Data](https://www.investing.com/commodities/crude-oil-historical-data)
   - This data provides daily crude oil prices, which are used to analyze the relationship between global oil prices and local fuel prices.

3. **Australian Terminal Gate Pricing (TGP)**
   - Source: [Australian Institute of Petroleum](https://www.aip.com.au/historical-ulp-and-diesel-tgp-data)
   - TGP data includes wholesale fuel prices for unleaded petrol (ULP) and diesel across various Australian cities. This data helps to compare wholesale pricing trends with retail prices at fuel stations.

## Project Workflow

### 1. Data Collection and Preprocessing
   - **Queensland Fuel Data** is retrieved via CSV files and API calls, cleaned to remove invalid values (e.g., price marked as 9999, which indicates no stock), and formatted for analysis.
   - **Crude Oil Prices** are fetched and cleaned to ensure date alignment with fuel price data for time series comparison.
   - **TGP Data** is downloaded and cleaned for integration with fuel prices, helping to track the impact of wholesale fuel costs.

### 2. Preprocessing for Data Analysis
   - Remove price outliers using the interquartile range (IQR) method.
   - Convert transaction timestamps to a common datetime format to facilitate time series analysis.
   - Aggregate daily fuel prices (min, median, max) per fuel type and combine the data with crude oil and TGP data.

### 3. Data Analysis
   - **Price Trend Analysis**: Analyze and visualize price trends for different fuel types over time, alongside crude oil and TGP price trends.
   - **Brand and Site Analysis**: Identify major fuel brands and examine site-level price variations across Queensland.
   - **Geospatial Analysis**: Create interactive maps to visualize fuel prices across the region, showing price distributions per site and allowing comparison by fuel type and brand.
   - **Current Price Snapshot**: Display the most recent prices, with color-coded price levels across Queensland fuel stations.

### 4. Visualizations
   - **Price Trend Charts**: Show historical trends in fuel prices, crude oil prices, and TGP data.
   - **Geospatial Maps**: Interactive maps displaying price ranges and fuel stations, with color coding to indicate price variations.
   - **Current Price Distribution**: Provide a snapshot of current fuel prices across regions, with prices color-coded to highlight high and low price areas.

## How to Run the Project

1. Clone the repository and install required dependencies (`requirements.txt`).
2. Retrieve fuel price data from the Queensland Government API, crude oil prices from Investing.com, and TGP data from AIP.
3. Run the analysis scripts to generate charts and maps, and review the results in your browser.

---

This project demonstrates a robust approach to fuel price analysis, integrating multiple data sources for comprehensive insights.
