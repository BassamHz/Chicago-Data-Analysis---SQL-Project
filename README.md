# Chicago Data Analysis - SQL Project

SQL-based analysis of Chicago municipal datasets including crime statistics, census data, and public school metrics.

## Overview
Analyzed three Chicago datasets using SQLite and Python to extract insights on crime patterns, socioeconomic indicators, and educational performance across community areas.

## Key Features
- **Database Design**: SQLite database with normalized tables for census, crime, and school data
- **Complex Queries**: 10 analytical SQL queries including subqueries, aggregations, and joins
- **Data Insights**: Crime risk assessment, poverty analysis, and school safety metrics

## Tech Stack
- **Database**: SQLite3
- **Languages**: Python, SQL  
- **Libraries**: pandas, ipython-sql
- **Environment**: Jupyter Notebook

## Sample Queries
```sql
-- Find community areas with highest crime rates
SELECT COMMUNITY_AREA_NUMBER, COUNT(*) as CRIME_COUNT
FROM CHICAGO_CRIME_DATA 
GROUP BY COMMUNITY_AREA_NUMBER
ORDER BY CRIME_COUNT DESC;

-- Identify areas with highest hardship index
SELECT COMMUNITY_AREA_NAME FROM CENSUS_DATA
WHERE HARDSHIP_INDEX = (SELECT MAX(HARDSHIP_INDEX) FROM CENSUS_DATA);
```

## Results
- Identified high-crime community areas for resource allocation
- Mapped poverty levels across Chicago neighborhoods  
- Analyzed school safety scores by institution type
- Correlated socioeconomic factors with crime patterns

## Data Sources
Chicago Data Portal: Census data, public schools, and crime statistics (2008-2012)
