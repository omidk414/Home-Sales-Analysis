# Home Sales Analysis

## Project Overview

In this challenge, we use SparkSQL to determine key metrics about home sales data. The project involves creating temporary views, partitioning the data, caching and uncaching a temporary table, and verifying that the table has been uncached. This analysis provides insights into home pricing trends based on various criteria and demonstrates the performance benefits of different data handling techniques in Spark.

## Table of Contents

1. [Technologies Used](#technologies-used)
2. [Key Findings](#key-findings)
   - [Four-Bedroom House Prices](#four-bedroom-house-prices)
   - [Three-Bedroom, Three-Bathroom Home Prices](#three-bedroom-three-bathroom-home-prices)
   - [Specific Home Criteria Prices](#specific-home-criteria-prices)
   - [View Rating Impact on Prices](#view-rating-impact-on-prices)
3. [Performance Optimization](#performance-optimization)
4. [Conclusion](#conclusion)

## Technologies Used

- Google Colab
- PySpark
- SparkSQL
- Python
- Jupyter Notebook

## Key Findings

### Four-Bedroom House Prices

The average price of four-bedroom houses remained relatively stable from 2019 to 2022:

| Year | Average Price |
|------|---------------|
| 2022 | $296,363.88   |
| 2021 | $301,819.44   |
| 2020 | $298,353.78   |
| 2019 | $300,263.70   |

### Three-Bedroom, Three-Bathroom Home Prices

For homes with 3 bedrooms and 3 bathrooms, there was a slight trend of newer builds having higher average prices:

| Year Built | Average Price |
|------------|---------------|
| 2017       | $292,676.79   |
| 2016       | $290,555.07   |
| 2015       | $288,770.30   |
| 2014       | $290,852.27   |
| 2013       | $295,962.27   |
| 2012       | $293,683.19   |
| 2011       | $291,117.47   |
| 2010       | $292,859.62   |

### Specific Home Criteria Prices

For homes with 3 bedrooms, 3 bathrooms, 2 floors, and ≥2,000 sqft:

| Year Built | Average Price |
|------------|---------------|
| 2017       | $280,317.58   |
| 2016       | $293,965.10   |
| 2015       | $297,609.97   |
| 2014       | $298,264.72   |
| 2013       | $303,676.79   |
| 2012       | $307,539.97   |
| 2011       | $276,553.81   |
| 2010       | $285,010.22   |

### View Rating Impact on Prices

Homes with higher view ratings showed significantly higher prices:

| View Rating | Average Price |
|-------------|---------------|
| 51          | $788,128.21   |
| 54          | $798,684.82   |
| 69          | $750,537.94   |
| 87          | $1,072,285.20 |
| 73          | $752,861.18   |
| ...         | ...           |

## Performance Optimization

Data caching was used to improve query performance:

- Cached runtime: 0.7509136199951172 seconds

This demonstrates a significant improvement in query execution time when using cached data.

## Conclusion

The analysis of home sales data using SparkSQL has provided valuable insights into pricing trends and the impact of various home features on sale prices. Key observations include:

1. **Price Stability**: The average price of four-bedroom houses remained relatively stable from 2019 to 2022, with only minor fluctuations.

2. **Build Year Influence**: For three-bedroom, three-bathroom homes, there was a slight trend of newer builds (2013-2017) having higher average prices compared to older ones (2010-2012).

3. **Size and Features Premium**: When considering homes with specific criteria (3 bedrooms, 3 bathrooms, 2 floors, ≥2,000 sqft), we observed a noticeable price premium, particularly for homes built between 2012-2014.

4. **View Rating Significance**: Homes with higher view ratings (51 and above) commanded significantly higher prices, with some ratings associated with average prices over $1 million.

5. **Performance Optimization**: Caching the data resulted in a significant performance improvement, with query runtime reduced to approximately 0.75 seconds. This demonstrates the importance of proper data management techniques in big data analysis.

These findings can be valuable for real estate professionals, homebuyers, and investors in understanding market trends and the factors that influence home prices. The use of SparkSQL for this analysis showcases its efficiency in handling and querying large datasets, while techniques like caching demonstrate how performance can be optimized for big data operations.
