


# Indian Film Industry Box Office Analysis (Excel Dashboard)



## Problem Statement : 

This project analyzes Indian film industry performance across multiple industries including:

Bollywood (Hindi)
Tollywood (Telugu)
Kollywood (Tamil)
Sandalwood (Kannada)
Mollywood (Malayalam)

The goal is to understand:

Box office performance trends
Industry dominance over time
Actor impact on movie success
ROI (Return on Investment) patterns
OTT and theatrical trends

This dashboard enables stakeholders to make data-driven decisions in film production, distribution, and investment.

## Dataset Description :

The project uses three interconnected datasets to analyze box office performance and actor impact:

### Movies Dataset (~30 records)

Primary dataset containing movie-level details:

- Movie_Title – Film name (with inconsistencies/duplicates)
- Release_Date – Mixed date formats
- Industry – Bollywood, Tollywood, etc. (with variations)
- Director / Lead_Actors – Text-based fields
- Genre – Multi-genre values
- Budget_Cr – Budget in ₹ Crores (unclean formats)
- India_Net_Cr / Worldwide_Gross_Cr – Revenue metrics
- Verdict – Hit / Flop / Blockbuster
- Days_Run – Theatrical run duration
- OTT_Platform – Streaming platform

### Actor Remuneration Dataset

Contains actor-level financial details:

- Actor_Name
- Movie_Title (inconsistent naming used for merging)
- Remuneration_Cr (ranges and text values)
- Year
- Industry


### Yearly Summary Dataset

Provides aggregated yearly insights:

- Year (2015–2026)
- Industry
- Total_Budget
- Total_Collection

Data was intentionally unclean and required transformation using Power Query in Excel.


## Data Integration :
Performed a Left Join (Merge) in Power Query:
Primary Table: Movies
Secondary Table: Actor Remuneration
Join Key: Movie_Title (handled using fuzzy matching due to inconsistencies)
This enabled:
Mapping actor remuneration to each movie
- Calculating advanced metrics such as:
  - ROI (Return on Investment)
  - Actor Pay Efficiency
-Industry Dominance Index

## Key Cleaning Steps:
- Removed duplicate movie records
- Standardized date formats (DD-MM-YYYY)
- Cleaned Industry names:
e.g., "Bollywd" → "Bollywood"
- Converted currency columns:
"150Cr", "₹200 Cr" → numeric values
- Split Lead Actors into structured format
- Trimmed extra spaces and fixed casing issues
- Handled missing values using:
- Median imputation (Budget / Revenue fields)
- Standardized Verdict categories





## Excel Dashboard Structure (6 Pages)
### Page 1: Overview KPIs
- Total number of movies
- Total Revenue
- Average budget
- Average ROI 
- Movies By year
- Total gross by industry


![1](https://github.com/user-attachments/assets/fa770fdf-c89b-4767-bf66-a380b2148a95)


### Page 2: Box Office Performance
- Top 10 Movies by Revenue
- Budget vs Revenue Comparison
- Verdict Distribution
- Revenue Trend by Year


![2](https://github.com/user-attachments/assets/1c431fae-2c8c-4dfc-8cc9-7225ab06da75)

### Page 3: Industry Analysis
- Revenue by Industry
- Year vs Industry Trend
- ROI Comparison across Industries


![3](https://github.com/user-attachments/assets/f65f6998-7a1e-4d29-93e7-62f3b2a9a616)



### Page 4: Actor Insights
- Top 10 Actors by Earnings
- Actor Success Rate
- Number of Movies per Actor


![4](https://github.com/user-attachments/assets/b40be3d5-4f07-4729-8cf5-8b874c5aa7ec)


### Page 5: Trends & Time Analysis
- Genre Performance Analysis
- Language vs Year Distribution


![5](https://github.com/user-attachments/assets/523a762e-a547-4a7e-b4f3-ca0f60d1519f)

### Page 6: Deep Insights
- OTT Platform Distribution
- Days Run vs Revenue Analysis

![6](https://github.com/user-attachments/assets/4aaa924d-cfb1-4a3d-a156-381c4a530b58)

## Excel Calculations & Metrics
### ROI Calculation
ROI = India_Net_Cr / Budget_Cr
📌 Industry Dominance Index
Dominance Index = 
(ROI * (Industry_Share / 100) * (Collection / Actor_Pay))
### Actor Pay Efficiency
Efficiency = Total Collection / Actor Pay

### Forecasting

Used:

FORECAST.LINEAR()
to predict future trends beyond 2026.


![fc](https://github.com/user-attachments/assets/3982586d-4376-4717-bbc2-43d3f0350691)


## Key Insights :

### Industry Trends
Bollywood dominates overall revenue contribution
Tollywood shows strong growth in recent years

### Box Office Performance
High-budget films tend to generate higher revenue but not always higher ROI
Blockbusters significantly influence yearly trends

### Actor Impact
Certain actors consistently deliver higher returns
Actor pay does not always guarantee success

### OTT & Theatrical Trends
Increasing shift towards OTT platforms
Movies with longer theatrical runs tend to generate higher revenue


Tools Used:

- Microsoft Excel – Dashboard & analysis
- Power Query – Data cleaning & transformation
- Pivot Tables – Aggregations
- Excel Formulas – Calculations & KPIs
 
## Sources
- Sacnilk
- Box Office Mojo India
- Kaggle datasets (Bollywood box office trends)

## Conclusion : 

This dashboard provides a comprehensive analysis of the Indian film industry by combining box office performance, actor remuneration, and yearly trends into a unified analytical view.

The analysis highlights that industry type, budget, and star power play a crucial role in determining a movie’s financial success. While high-budget films often generate higher revenue, ROI varies significantly, indicating that investment alone does not guarantee profitability.

The integration of actor remuneration data reveals that actor pay does not always correlate with higher returns, emphasizing the importance of content, timing, and audience reception. Additionally, industry-level analysis shows evolving dynamics, with regional industries contributing significantly alongside Bollywood, reflecting a more diversified and competitive market landscape.

Trend analysis further indicates that factors such as genre, language, and OTT adoption are reshaping audience preferences and revenue streams, highlighting the shift toward digital platforms and changing consumption patterns.

Overall, this solution enables stakeholders to:

- Identify high-performing industries and films
- Evaluate ROI and investment effectiveness
- Analyze actor impact on box office success
- Understand market trends across genres, languages, and platforms

This project demonstrates how combining data cleaning (Power Query), data modeling, and advanced Excel analytics can transform raw movie data into actionable insights for strategic decision-making in the entertainment industry.
