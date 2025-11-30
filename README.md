# Soft Drink Market Insight: Alimosho, Lagos

_The Battle for the Streets: Uncovering the Informal Economy of Soft Drinks_

 ![](https://github.com/hamadkamorudeen/Alimosho-Soft-Drink-Analysis/blob/main/Alimosho.jpg)

 ## 📖 Project Overview

The Soft Drink Market Insight Challenge focused on analyzing real-world survey data from Alimosho Local Government Area, Lagos. The goal was to explore soft drink availability, packaging trends, and outlet distribution to uncover the "ground reality" of the market.

This repository contains the full data analysis pipeline, from data cleaning to advanced visualization, revealing how brands like Coca-Cola and Pepsi compete in the informal economy.

## 📂 Dataset Description

The dataset consists of 1,500 rows and 38 columns representing individual soft drink outlets.

Source: Field survey data from Alimosho LGA.

### Key Features:

- Type of Outlet: (Shop, Kiosk, Supermarket, etc.)

- Brand Availability: (Coca-Cola, Pepsi, Bigi, etc.)

- Stock Condition: (Well stocked, Partially stocked, etc.)

- GPS Coordinates: (Latitude/Longitude)

### ⚙️ Methodology: From Raw Data to Insights

_1. Data Acquisition & Loading_

- The raw data (Product Visibility Challenge Data.csv) contained a structural inconsistency where the header spanned two rows.

- Technique Used: Loaded data using header=1 in Pandas to correctly align column names.

- Result: Successfully indexed 1,500 rows of data.
  

_2. Data Cleaning_

- Real-world data is messy. I implemented a robust cleaning pipeline:

Missing Values (Nulls):

- Numerical Columns: Filled NaN with 0 (interpreting null availability as "Not Available").

- Categorical Columns: Filled NaN with "Not Specified" to preserve data integrity.

-  Duplicate Check: Verified that the dataset contained 0 duplicate records to ensure analysis accuracy.

- Column Drop: Removed the S/N (Serial Number) column as it provided no analytical value.
  

_3. Exploratory Data Analysis (EDA)_

I focused on five key metrics to tell the story of the market:

- Brand Dominance: Frequency count of all major brands.

- Outlet Types: Distribution of where drinks are sold.

- Packaging Preferences: Comparison of PET vs. Glass vs. Cans.

-  Stock Levels: Analysis of supply chain efficiency.

- Geospatial Analysis: Mapping outlets by location.
  

## 📊 Key Findings & Visualizations

### 1. The "David vs. Goliath" Battle

While Coca-Cola (1,028 outlets) and Pepsi (977 outlets) dominate the market, the data revealed a shocking contender. American Cola secured the #4 spot, surpassing established legacy brands like 7Up. This indicates a shift toward value-driven challenger brands.

 ![](https://github.com/hamadkamorudeen/Alimosho-Soft-Drink-Analysis/blob/main/Market%20Dominance%20-%20Most%20Available%20Soft%20Drink%20Brands.png)


### 2. The Informal Economy Rules

Contrary to modern retail expectations, 86% of soft drinks in Alimosho are sold in small, informal Shops. Supermarkets and modern trade outlets are statistically negligible.

![](https://github.com/hamadkamorudeen/Alimosho-Soft-Drink-Analysis/blob/main/Distribution%20of%20Outlet%20Types.png)

Insight: Brands focusing on supermarket shelf space are missing the actual battlefield.


### 3. Packaging: The Reign of PET

_76% of all available products are PET (Plastic) bottles._

- Glass: 20%

- Cans: Only 3%

![](https://github.com/hamadkamorudeen/Alimosho-Soft-Drink-Analysis/blob/main/Consumer%20Preference-%20Package%20Types.png)

Insight: The Alimosho consumer demands portability and resealability. Cans are likely viewed as a premium luxury rather than a daily staple.


### 4. The Supply Chain Gap

Only 39% of shops are "Well Stocked." A staggering 43% are "Partially Stocked."

![](https://github.com/hamadkamorudeen/Alimosho-Soft-Drink-Analysis/blob/main/Stock%20Condition%20Overview.png)

Insight: There is a massive "Stock Gap." Brands that can optimize last-mile logistics to these small shops will capture significant market share from competitors who are out of stock.

## 🛠️ Technical Tools Used

Pandas: For data manipulation, cleaning, and aggregation.

Seaborn & Matplotlib: For generating high-quality, publication-ready visualizations.

GridSpec: For designing the composite dashboard layout.





