# Oslo Urban Mobility Analysis

## Project Overview
This project analyzes the relationship between bike sharing usage and traffic volume in Oslo, Norway. By examining data from the Oslo City Bike system and traffic sensors at three key locations (Maridalsveien, Østre, and Bygdøy), we investigate patterns, correlations, and potential impacts of bike sharing on urban traffic flows.

## Data Sources
- **Oslo City Bike (Bysykkel) Data**: Historical trip data from Oslo's bike sharing system, collected from 2020-2024.
- **Traffic Volume Data**: Data from traffic registration points maintained by the Norwegian Public Roads Administration (Vegvesenet) at three locations:
  - Maridalsveien
  - Østre
  - Bygdøy

## Key Features
- Data collection and preprocessing from Oslo's open data sources
- Geospatial analysis of bike sharing stations and traffic sensors
- Time series analysis of traffic patterns and bike usage
- Correlation analysis between bike sharing adoption and traffic volumes
- Seasonal and temporal pattern identification
- Vehicle type classification analysis (light vs. heavy vehicles)

## Key Findings
1. **Seasonal Patterns**: Both bike sharing and traffic volume show distinct seasonal patterns, with bike usage peaking in summer months and declining in winter.
2. **Hourly Distribution**: Bike sharing peaks differ from traffic peaks, with bike usage showing both morning and evening peaks, while traffic shows a more consistent distribution.
3. **Vehicle Composition**: The percentage of light vehicles (<5.6m) versus heavy vehicles shows interesting patterns across different locations.
4. **Weekday vs. Weekend**: Both bike sharing and traffic volumes show significant differences between workdays and non-workdays.
5. **Popular Stations**: The most frequently used bike stations were identified and analyzed relative to traffic patterns.

## Repository Structure
```
├── script/
│   ├── scraping.py                   # Web scraping script for data collection
│   ├── data_analysis.py              # Main data analysis script
│   ├── bike_sharing.csv              # Combined bike sharing dataset
│   ├── cleaned_bike_sharing.csv      # Preprocessed bike sharing data
│   ├── filtered_bike_sharing_*.csv   # Location-specific bike data
│   ├── final_bike_sharing_*.csv      # Final processed bike data by location
│   ├── *_traffic.csv                 # Traffic data for each location
│   └── *_traffic_hour_2024.csv       # Hourly traffic data for 2024
└── dataset/
    └── bike_sharing/                 # Original raw bike sharing datasets by year
```

## Methodology
1. **Data Collection**: 
   - Scraped historical bike sharing data from Oslo City Bike's open data portal
   - Retrieved traffic data through the Norwegian Public Roads Administration API
   
2. **Data Preprocessing**:
   - Cleaned and standardized date/time formats
   - Filtered bike trips by proximity to traffic measurement points
   - Aggregated data at various temporal scales (hourly, daily, monthly, seasonal)
   - Calculated metrics such as trip duration, traffic volume, and vehicle classification
   
3. **Data Analysis**:
   - Correlation analysis between bike sharing usage and traffic volumes
   - Time series decomposition to identify trends and seasonality
   - Geospatial analysis of popular bike sharing stations
   - Comparative analysis across the three studied locations

## Technologies Used
- **Python**: Primary programming language
- **Pandas & NumPy**: Data manipulation and numerical analysis
- **Matplotlib & Seaborn**: Data visualization
- **Folium**: Interactive maps
- **GeoPy**: Geospatial calculations
- **Beautiful Soup**: Web scraping

## Indicators and Visualizations
1. **Bus Percentage Analysis**: Evolution of bus traffic percentage over time
2. **Workday vs. Non-workday Comparison**: Analysis of traffic and bike usage differences
3. **Seasonal Trend Analysis**: Bike sharing and traffic volume trends across seasons
4. **Station Popularity vs. Traffic Correlation**: Analysis of popular bike stations and traffic patterns
5. **Daily Usage Patterns**: Comparative analysis of daily patterns in bike sharing and traffic

## Future Work
- Expand analysis to include weather data for more nuanced seasonal analysis
- Incorporate public transit data to understand multi-modal transportation patterns
- Develop predictive models for traffic reduction based on bike sharing expansion
- Analyze the impact of bike lane infrastructure on both bike sharing usage and traffic volumes
- Investigate the economic impact of reduced traffic congestion through bike sharing
