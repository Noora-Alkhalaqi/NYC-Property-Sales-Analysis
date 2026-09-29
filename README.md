# NYC Property Sales Analysis

## Problem Statement

A real estate analytics company is preparing a market report on property sales across New York City using transaction data from September 2016 to August 2017. The results will be used to provide stakeholders with a view of patterns in the NYC property market.

## Executive Summary

This project analyzes property sales across New York City from September 2016 to August 2017. The dataset was cleaned and prepared using Python and Pandas before performing exploratory data analysis. The cleaning process included removing unnecessary columns, handling missing and invalid values, converting data types, identifying transfer transactions, mapping borough codes to borough names, and creating a building age feature.

The analysis focused on differences in property sale prices across boroughs, sales activity across neighborhoods, building age, monthly sales activity, and residential versus commercial property sales. Manhattan had the highest median property sale price at approximately $1.17 million, while the Bronx had the lowest at approximately $405,000. Flushing-North had the highest number of property sales among the neighborhoods analyzed, with 2,170 transactions. Buildings aged 97 years recorded the highest number of sales by exact building age, with 2,597 transactions. June 2017 had the highest monthly sales activity, with 5,955 transactions.

Residential-only properties were also much more common than commercial-only properties in the comparison. There were 38,791 residential-only sales compared with 1,287 commercial-only sales. Overall, the results show that property prices and sales activity varied across location, property characteristics, and time.

## File Directory

| File | Description |
|------|-------------|
| `Noora_Alkhalaqi_project2.ipynb` | Jupyter Notebook containing data cleaning, analysis, and visualizations |
| `nyc-rolling-sales.csv` | Original NYC property sales dataset |
| `nyc_property_sales_cleaned.csv` | Final cleaned dataset used for the analysis |
| `README.md` | Project overview, findings, conclusions, and documentation |

## Data and Data Dictionary

The dataset used in this project is the NYC Property Sales dataset available on Kaggle. It contains property sale transactions across the five boroughs of New York City.

The original dataset contained 84,548 rows and 22 columns. After cleaning, the final dataset contains 69,987 rows and 24 columns.

Dataset source:

https://www.kaggle.com/datasets/new-york-city/nyc-property-sales/data

### Data Dictionary

| Feature | Description |
|---------|-------------|
| `BOROUGH` | Numeric code representing the NYC borough |
| `NEIGHBORHOOD` | Neighborhood where the property is located |
| `BUILDING CLASS CATEGORY` | General category describing the property's use |
| `TAX CLASS AT PRESENT` | Current tax class of the property |
| `BLOCK` | Tax block where the property is located |
| `LOT` | Tax lot identifying the property within the block |
| `EASE-MENT` | Easement information |
| `BUILDING CLASS AT PRESENT` | Current building classification |
| `ADDRESS` | Street address of the property |
| `APARTMENT NUMBER` | Apartment number, when applicable |
| `ZIP CODE` | ZIP code of the property |
| `RESIDENTIAL UNITS` | Number of residential units |
| `COMMERCIAL UNITS` | Number of commercial units |
| `TOTAL UNITS` | Total number of residential and commercial units |
| `LAND SQUARE FEET` | Land area of the property in square feet |
| `GROSS SQUARE FEET` | Total building floor area in square feet |
| `YEAR BUILT` | Year the property was built |
| `TAX CLASS AT TIME OF SALE` | Tax class recorded at the time of sale |
| `BUILDING CLASS AT TIME OF SALE` | Building classification recorded at the time of sale |
| `SALE PRICE` | Recorded sale price of the property |
| `SALE DATE` | Date of the property transaction |
| `IS TRANSFER` | Engineered feature used to identify low-price transfer transactions |
| `BOROUGH NAME` | Engineered feature that converts borough codes into borough names |
| `BUILDING AGE` | Engineered feature representing the age of the building at the time of sale |

### Engineered Features

Three additional features were created during the data cleaning and analysis process:

- `IS TRANSFER`: Used to identify transactions with very low sale prices that were treated as transfers in this project.
- `BOROUGH NAME`: Converts the numerical borough codes into Manhattan, Bronx, Brooklyn, Queens, and Staten Island.
- `BUILDING AGE`: Calculated using the year of sale minus the year the building was built.

## Important Findings and Visualizations

### Property Sale Prices by Borough

The analysis compared property sale prices across the five NYC boroughs. Manhattan had the highest median sale price at approximately $1.17 million, while the Bronx had the lowest at approximately $405,000.

This shows that typical property sale prices differed considerably across NYC boroughs.

### Neighborhoods with the Most Property Sales

The number of property sales was compared across NYC neighborhoods. Flushing-North had the highest number of property sales, with 2,170 transactions.

This shows that property sales activity was not evenly distributed across NYC neighborhoods.

### Property Sales by Building Age

Building age was calculated using the year the property was built and the year it was sold. Properties with a building age of 97 years had the highest number of sales.

This indicates that sales activity varied across different building ages.

### Monthly Property Sales

Property sales were analyzed by month from September 2016 to August 2017. June 2017 had the highest number of property sales.

The results show that property sales activity changed throughout the period rather than remaining constant.

### Residential vs Commercial Property Sales

Residential-only and commercial-only property transactions were compared.

- Residential-only sales: 38,791
- Commercial-only sales: 1,287

Residential-only properties represented approximately 96.8% of these two groups, while commercial-only properties represented approximately 3.2%.

This shows that residential-only property transactions were much more common than commercial-only transactions in this comparison.

## Conclusions and Recommendations

The analysis shows that NYC property prices and sales activity varied based on location, property characteristics, and time during the September 2016 to August 2017 period.

Manhattan had the highest typical property sale price, while the Bronx had the lowest. Flushing-North recorded the highest number of property sales among the neighborhoods analyzed. Monthly sales activity also changed throughout the period, with June 2017 recording the highest number of transactions.

Residential-only properties had substantially more transactions than commercial-only properties. Building age also showed differences in transaction activity, although building age alone should not be used to explain property prices.

Based on these findings, stakeholders should consider borough, neighborhood, property type, and time period when studying the NYC property market. Location is especially important because areas with high sales activity do not necessarily have the highest property prices.

## Areas for Further Research/Study

Future analysis could use property sales data covering multiple years to determine whether the patterns found in this project continue over time.

Further research could also examine:

- Sale price per square foot
- Tax class changes
- Building class changes
- Relationships between property size and sale price
- Differences in market activity within each borough

Future projects could also include a larger data set to really identify the patterns.

## Sources
 
https://www.kaggle.com/datasets/new-york-city/nyc-property-sales/data

https://www.nyc.gov/assets/finance/downloads/pdf/07pdf/glossary_rsf071607.pdf

https://www.nyc.gov/assets/finance/jump/hlpbldgcode.html

https://www.nyc.gov/site/finance/property/glossary-property-sales.page#

## Articals
https://www.foxbusiness.com/features/new-york-city-commercial-real-estate-sales-slump-in-first-half-of-2017
https://www.wsj.com/articles/new-york-city-commercial-real-estate-sales-slump-in-first-half-of-2017-1502750265
https://therealdeal.com/new-york/2022/12/29/how-flushing-became-a-hotbed-for-development/
https://www.realtor.com/news/trends/manhattan-luxury-housing-market-nearly-back-to-2016-heyday/
https://www.forbes.com/sites/shimonshkury/2026/09/15/fifteen-years-of-nyc-real-estate-the-market-recovers-but-never-in-the-same-way/
