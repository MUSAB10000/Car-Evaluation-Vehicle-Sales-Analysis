# Car Evaluation & Vehicle Sales Analysis

This project applies real-world data wrangling techniques to two automotive-related datasets — one from the UCI Machine Learning Repository and one from Kaggle — to explore how evaluation features influence used vehicle sales. The goal is to clean, combine, and analyze these datasets to answer a specific research question about factors affecting used car prices across manufacturers.

## Problem Statement

This project investigates:  
**"What are the key factors that affect the selling price of used cars, and how do these factors vary by car manufacturer?"**

By combining evaluation criteria (like safety and capacity) with real-world vehicle sales data (like price, odometer reading, and manufacturer), this analysis uncovers insights into the automotive market and consumer behavior.

## Technologies Used

- **Python**
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
- **ucimlrepo** (to programmatically fetch UCI data)
- **Kaggle** (for real-world used car sales dataset)

## Data Gathering

- **Dataset 1: Car Evaluation Dataset (UCI Repository)**
  - Attributes include: buying price, maintenance cost, doors, capacity, boot size, safety.
  - Fetched programmatically using `ucimlrepo`.

- **Dataset 2: Craigslist Vehicle Sales Dataset (Kaggle)**
  - Contains used car listings with price, manufacturer, odometer, fuel type, etc.
  - Manually downloaded in CSV format.

##  Data Wrangling Process

- **Assessing Data**
  - Identified and documented quality and tidiness issues including:
    - Missing values in the Kaggle dataset
    - Ambiguous column names
    - Data type inconsistencies
    - Separated feature and target variables in UCI dataset

- **Cleaning Data**
  - Dropped useless columns (e.g., `county`)
  - Converted string-based numeric columns to integers
  - Renamed columns for clarity (`persons` → `num_persons`)
  - Merged UCI features and targets into a single dataframe
  - Combined both datasets for unified analysis

- **Data Storage**
  - Saved versions of raw, intermediate, and cleaned datasets (`raw_car_data.csv`, `raw_xy_data.csv`, `combined_car_data.csv`)

## Analysis & Visualizations

### Research Question:
> What are the key factors that affect the selling price of used cars, and how do these factors vary by car manufacturer?

### Insights:
- **Average Price by Manufacturer**  
  A bar chart showed that certain manufacturers like Mercedes-Benz have significantly higher average used car prices.

- **Odometer vs. Price**  
  A scatter plot revealed a strong negative correlation between mileage and car price — higher odometer readings often mean lower prices.

## Conclusion

Integrating car evaluation metrics with real-world pricing data revealed relationships between safety, capacity, and selling price. Manufacturer-specific trends also emerged, showing brand impact on used car value.

## Reflection

Given more time, further data cleaning (e.g., standardizing string labels like `'vhigh'` to `'very high'`) and deeper feature engineering would enhance this analysis. Additional questions such as “Which model has the highest average price?” or “How does condition affect depreciation rate?” could also be explored.

## License & Credits

- This project was completed as part of the **Udacity Data Analyst Nanodegree**.
- Datasets:
  - [Car Evaluation Dataset - UCI](https://archive.ics.uci.edu/dataset/19/car+evaluation)
  - [Craigslist Car Sales - Kaggle](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data)

