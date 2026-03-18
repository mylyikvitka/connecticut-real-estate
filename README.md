# Connecticut Real Estate Analytics Pipeline 

## Overview
This project is an automated analytics engine for the Connecticut real estate market.  
It ingests and transforms multiple data sources into a single analytics-ready dataset, enabling insights on market opportunities, risk detection, and economic patterns.  

## Strategic Goals
1. **Market Opportunity (Investor View)**  
   - Identify "Hot" and "Cold" markets by tracking divergence between assessed value and sale price.  
   - Example Question: Which neighborhoods offer the highest price stability and potential ROI?  

2. **Risk & Anomaly Detection (Forensic View)**  
   - Flag abnormal transactions (e.g., family sales, foreclosures, or data errors).  
   - Example Question: Which sales are statistically suspicious and require review?  

3. **Economic & Geographic Insights (Analyst View)**  
   - Investigate effects of affordable housing, unemployment, and household debt on real estate activity.  
   - Example Questions:  
     - Does affordable housing affect sales ratios or transaction volume?  
     - How does unemployment impact price ratios?  
     - Which cities show consistently high or low sales ratios?

## Data Sources
- Real Estate Transactions (Connecticut)  
- Unemployment Data (Connecticut)  
- Household Debt Data (Connecticut)  
- Affordable Housing Data (Connecticut)

## Architecture & Tools
- **Data Pipeline:** Apache Airflow (orchestrated by team)  
- **Analytics Engine:** Apache Druid (flattened schema for OLAP queries) --main contribution 
- **BI & Visualization:** Upcoming dashboard layer

## My Role
- Designed the initial relational model for PostgreSQL
- Designed and implemented the Druid ingestion pipeline  
- Flattened multi-fact warehouse schema into a single analytics-ready table  
- Defined metrics and dimensions to answer key business questions  
- Prepared the dataset for downstream BI analysis

## Example Use Cases / Queries
- Average property price by town over time  
- Correlation between unemployment and sales ratios  
- Impact of household debt on number of transactions  
- Affordable housing vs. sales activity trends

## Notes
- The original data was modeled in PostgreSQL with a normalized star schema.  
- For Druid, the schema was denormalized to optimize query performance and aggregation speed.  